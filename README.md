# DocAssist: AI-Powered Medical Decision Support System
## Overview

DocAssist is an AI-powered medical decision support system designed to assist doctors in making informed treatment decisions by analyzing patient data, including medical history, symptoms, and lab results. The system leverages machine learning to provide personalized treatment recommendations, reducing variability in medical decision-making and improving patient outcomes.

## Features
- Upload blood test reports in **PDF** format.
- AI-powered analysis of blood test parameters.
- Intuitive and user-friendly interface.
- Visual representation of test results.
- Secure and efficient processing.

## UI Snapshots
UI repo link: https://github.com/Neo28A/DocAssist_AI-UI.git
### Main Page
![Main page](https://github.com/user-attachments/assets/2c9c1f29-cff0-42d2-8c4e-abb4a4640fe0)

### Upload PDF Section
![Upload pdf section](https://github.com/user-attachments/assets/7f2676ce-8104-4316-ab48-2b30ce6fa402)

### Enter Values Section
![Enter values Section](https://github.com/user-attachments/assets/e0cfe564-5b14-4f53-81c5-c711ca356d03)

### Deploy Link: https://docassist-ai.netlify.app/

## Problem Statement

In the current medical landscape, doctors often face challenges in processing vast amounts of patient data to make treatment decisions. This can result in delays, inconsistencies, and suboptimal treatment recommendations. DocAssist aims to bridge this gap by providing a data-driven decision support tool.

## Objectives

- Develop an intelligent medical decision support system.
- Analyze patient data to assist doctors in choosing the best treatment options.
- Leverage machine learning for personalized treatment recommendations.

## Dataset Information

The dataset is collected from a private hospital in Indonesia and contains patient laboratory test results to determine treatment recommendations.

### Features:

| Name         | Data Type        | Description                               |
| ------------ | ---------------- | ----------------------------------------- |
| HAEMATOCRIT  | Continuous       | Haematocrit test result                   |
| HAEMOGLOBINS | Continuous       | Haemoglobin test result                   |
| ERYTHROCYTE  | Continuous       | Erythrocyte test result                   |
| LEUCOCYTE    | Continuous       | Leucocyte test result                     |
| THROMBOCYTE  | Continuous       | Thrombocyte test result                   |
| MCH          | Continuous       | MCH test result                           |
| MCHC         | Continuous       | MCHC test result                          |
| MCV          | Continuous       | MCV test result                           |
| AGE          | Continuous       | Patient age                               |
| SEX          | Nominal (Binary) | Patient gender (M/F)                      |
| SOURCE       | Nominal          | 1 = In-care patient, 0 = Out-care patient |

## Data Preprocessing

- Handling missing and duplicate values.
- Feature engineering (e.g., creating a thrombocyte-leucocyte ratio).
- Encoding categorical variables.
- Scaling numerical features using RobustScaler.

## Exploratory Data Analysis (EDA)

- Distribution analysis of class labels, gender, and age.
- Feature correlations using heatmaps.
- Histogram and density plots for numerical features.

## Model Selection & Evaluation

Several machine learning models were trained and evaluated:

- **Logistic Regression**
- **Support Vector Machine (SVM)**
- **K-Nearest Neighbors (KNN)**
- **Random Forest**
- **AdaBoost**
- **Gradient Boosting**
- **XGBoost**

### Performance Before Hyperparameter Tuning:

| Model               | Train Accuracy | Test Accuracy |
| ------------------- | -------------- | ------------- |
| Random Forest       | 1.000000       | 0.761042      |
| XGBoost             | 0.993199       | 0.751982      |
| Gradient Boosting   | 0.800227       | 0.738392      |
| SVM                 | 0.770757       | 0.736127      |
| KNN                 | 0.801360       | 0.725934      |
| AdaBoost            | 0.735903       | 0.723669      |
| Logistic Regression | 0.724568       | 0.718007      |



### XGBoost Before Hyperparameter Tuning

- **Train Accuracy: 0.9931**
- **Test Accuracy: 0.7519**

### XGBoost After Hyperparameter Tuning

Top-performing models were fine-tuned using **Hyperopt** to optimize parameters. After hyperparameter tuning, XGBoost achieved the best performance:

- **Train Accuracy**: 0.9354
- **Test Accuracy**: 0.7780

### Deployment Plan

- Convert the trained model into a deployable format (e.g., Joblib or Pickle).
- Use the trained model for predictions.

## Future Improvements

- Expand dataset diversity for better generalization.
- Incorporate deep learning techniques for improved accuracy.
- Build an API (Flask/FastAPI) for model inference.
- Develop a user-friendly interface for doctors to input patient data and receive recommendations.

## How to Use

- Load the dataset into the script.
- Run the preprocessing and model training steps.
- Use the trained model for predictions.

## Conclusion

DocAssist provides a data-driven approach to medical decision-making, helping doctors make informed treatment choices with the power of AI.

For further details, refer to the project repository or documentation.

