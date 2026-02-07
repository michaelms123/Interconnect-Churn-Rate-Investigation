# Interconnect Telecom — Customer Churn Prediction

## Project Overview
Interconnect, a telecom operator, wants to predict customer churn. If the company can identify users who are likely to leave, they can proactively offer promotional codes and better plan options to retain them.

This project builds a machine learning model to forecast churn using customer contract details, personal information, and subscribed services.

## Objective
Predict whether a customer is likely to churn.

### Target Definition
A customer is considered **churned** if the `EndDate` column is **not** equal to `"No"`.

## Evaluation Metrics
- **Primary metric:** AUC-ROC  
- **Additional metric:** Accuracy  

##  Dataset Description
The dataset is split across four files, each containing customer data from different sources.

## Files and Descriptions:
| `contract.csv` | Contract information |
| `personal.csv` | Customer personal data |
| `internet.csv` | Internet services |
| `phone.csv` | Phone services |

Each file includes a `customerID` column that uniquely identifies each customer.

Contract data is valid as of **February 1, 2020**.

## Interconnect Services
Interconnect provides:

### Core Services
- **Landline communication** (multiple lines possible)
- **Internet** (DSL or fiber optic)

### Additional Services
- Online security (malicious website blocker)
- Device protection (antivirus)
- Tech support line
- Cloud backup / file storage
- TV streaming
- Movie streaming

Customers may pay monthly or sign a **1-year** or **2-year** contract, use different payment methods, and receive electronic invoices.

## Project Workflow
1. **Load and inspect datasets**
2. **Merge all files into one master dataset**
3. **Data preprocessing**
   - Handle missing values
   - Fix data types (especially date fields)
   - Encode categorical features
4. **Feature engineering**
   - Convert contract dates into duration-based features
   - Create churn target from `EndDate`
5. **Model training**
   - Train multiple models
   - Use cross-validation
6. **Model evaluation**
   - Compare AUC-ROC and Accuracy
7. **Final model selection**
8. **Conclusions and recommendations**

## Model Output (Fill After Training)
| Model | AUC-ROC | Accuracy |
|------|---------|----------|
| Baseline | 0.87 | 0.76 |
| Final Model | 0.90 | 0.80 |
