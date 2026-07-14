

````markdown
# Chronic Kidney Disease Prediction System using Machine Learning

## Overview

This project is a **Machine Learning-based Chronic Kidney Disease (CKD) Prediction System** that predicts whether a patient is likely to have Chronic Kidney Disease based on clinical parameters.

The system uses a **Decision Tree Classifier** trained on patient health records and deploys the trained model using a **Flask web application**.

The objective of this project is to assist in early CKD detection by analyzing important medical indicators such as:

- Blood pressure
- Blood glucose level
- Serum creatinine
- Blood urea
- Hemoglobin
- Albumin
- Specific gravity
- Red blood cell count


---

# Problem Statement

Chronic Kidney Disease is a serious health condition that requires early detection.

Traditional diagnosis requires extensive medical evaluation, which can be time-consuming.

This project aims to build a predictive system that can:

- Analyze patient medical attributes
- Predict CKD risk
- Provide quick preliminary screening support


---

# Project Architecture


```

                 Patient Input Data

                         |
                         |
                         ▼

              Flask Web Application

                         |
                         |
                         ▼

              Input Data Processing

                         |
                         |
                         ▼

             Trained ML Model (Pickle)

                         |
                         |
                         ▼

          Decision Tree Classification Model

                         |
                         |
                         ▼

             Prediction Result

          -------------------------
          |                       |
          ▼                       ▼

     CKD Detected          No CKD Detected

          |                       |
          ▼                       ▼

    Positive Page          Negative Page


```


---

# Machine Learning Workflow


## 1. Dataset Collection

Dataset:

**Chronic Kidney Disease Dataset**

The dataset contains patient medical information including:

- Age
- Blood pressure
- Blood glucose
- Albumin
- Sugar level
- Blood cell information
- Serum creatinine
- Hemoglobin
- Hypertension
- Diabetes status


---

# 2. Data Preprocessing


## Data Cleaning

Performed:

- Removed unnecessary ID column
- Renamed columns for better readability
- Converted categorical values into numerical format
- Handled missing values
- Removed irrelevant features


Example transformations:

```
Normal → 0
Abnormal → 1

Yes → 1
No → 0

Present → 1
Not Present → 0

```


---

# 3. Feature Engineering


Selected important medical features:

```
Age
Blood Pressure
Specific Gravity
Albumin
Sugar
Blood Glucose Random
Blood Urea
Serum Creatinine
Sodium
Potassium
Hemoglobin
Red Blood Cell Count
White Blood Cell Count
Hypertension
Diabetes Mellitus
Coronary Artery Disease

```


Final model features:

```
Haemoglobin
Specific Gravity
Red Blood Cell Count
Albumin
Blood Urea
Blood Pressure
Blood Glucose Random
Serum Creatinine

```


---

# 4. Handling Missing Values

Missing values were replaced using median imputation.

Example:

```
Missing Value

       |
       ▼

Feature Median Calculation

       |
       ▼

Replace Missing Data

```


---

# 5. Data Encoding


Categorical variables were converted into numerical format using:

```
Label Encoder

```


This converts medical attributes into machine-readable values.


---

# 6. Model Training


## Algorithm Used

### Decision Tree Classifier


Workflow:

```

Preprocessed Dataset

        |
        ▼

Train-Test Split

        |
        ▼

Decision Tree Training

        |
        ▼

Model Evaluation

        |
        ▼

Save Model

```


---

# 7. Model Serialization


The trained model is saved using Pickle:

```
ckd.pkl

```


This allows the Flask application to load the trained model without retraining.


---

# Flask Deployment Architecture


```

                 User

                  |
                  |
                  ▼

             HTML Form

                  |
                  |
                  ▼

            Flask Backend

                  |
                  |
                  ▼

        Load ckd.pkl Model

                  |
                  |
                  ▼

       Process Input Features

                  |
                  |
                  ▼

       Decision Tree Prediction

                  |
                  |
        ---------------------

        |                   |

        ▼                   ▼

   CKD Positive        CKD Negative

        |                   |

        ▼                   ▼

   pos.html           neg.html


```


---

# Application Workflow


## Step 1

User enters medical information through the web interface.


## Step 2

Flask receives the input values.


## Step 3

Input values are converted into numerical arrays.


## Step 4

The trained Decision Tree model predicts:

```
0 → No CKD

1 → CKD Detected

```


## Step 5

The result is displayed through HTML pages.


---

# Technology Stack


## Programming Language

- Python


## Machine Learning

- Pandas
- NumPy
- Scikit-learn
- Decision Tree Classifier


## Deployment

- Flask
- HTML Templates


## Model Storage

- Pickle


## Data Processing

- Label Encoding
- Missing Value Imputation


---

# Project Structure


```

Chronic-Kidney-Disease-Prediction

│
├── app.py
│
├── ckd.pkl
│
├── Kidney_data.csv
│
├── model_training.py
│
├── templates
│    |
│    ├── index.html
│    ├── pos.html
│    └── neg.html
│
├── requirements.txt
│
└── README.md


```


---

# Key Features


✅ Machine Learning based CKD prediction  
✅ Automated medical data preprocessing  
✅ Decision Tree classification  
✅ Flask web deployment  
✅ Real-time patient prediction  
✅ Simple user-friendly interface  


---

# Model Pipeline


```

Raw Patient Data

        |
        ▼

Data Cleaning

        |
        ▼

Feature Encoding

        |
        ▼

Missing Value Handling

        |
        ▼

Feature Selection

        |
        ▼

Decision Tree Model

        |
        ▼

CKD Prediction


```


---

# Future Improvements


- Improve accuracy using ensemble models:
  - Random Forest
  - XGBoost
  - Gradient Boosting

- Add model explainability using SHAP

- Deploy using cloud platforms

- Add patient history tracking

- Add probability-based risk scoring

- Integrate medical recommendation system


---

# Author

**SRISHHA**

````


