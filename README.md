# Sobrix: AI-Powered Substance Recovery Time Predictor

Sobrix is a Python-based web application driven by machine learning that estimates the recovery timeline for individuals undergoing substance rehabilitation. Because actual hospital and rehabilitation data are highly confidential and legally protected, this project utilizes a structurally realistic dummy dataset to simulate real-world clinical parameters safely.

## 📌 Project Overview
Sobrix uses a dual-model approach to provide comprehensive predictions based on a patient's historical, physical, and substance-use parameters:
*   **Classification Task:** Predicts the category or phase of recovery progression (`classifier.pkl`).
*   **Regression Task:** Estimates the exact recovery time in days or weeks (`regressor.pkl`).

## 📊 Core Features & Parameters
The machine learning models process various user inputs to generate an accurate recovery profile:
*   **Substance Variables:** Type of substance used, frequency of use, and duration of dependency.
*   **Patient Demographics:** Age, physical health metrics, and genetic predisposition indicators.
*   **Support Factors:** Therapy attendance, presence of a social support system, and treatment type.

## ⚙️ Model Artifacts
The application relies on four pre-trained serialization files located in the model directory to process data and serve predictions:
1.  `scaler.pkl`: Normalizes continuous numerical inputs (e.g., age, dosage levels).
2.  `encoders.pkl`: Transforms categorical inputs (e.g., substance type, gender) into numerical formats.
3.  `classifier.pkl`: Categorizes the recovery tracking stream or success probability class.
4.  `regressor.pkl`: Outputs the final numerical prediction for the expected recovery duration.

## 🚀 Installation & Local Setup

### Prerequisite
Ensure you have **Python 3.8+** installed on your system.

### 1. Clone the Repository
```bash
git clone https://github.com
cd sobrix
```

### 2. Install Required Packages
Install all the necessary Python packages using pip:
```bash
pip install Django pandas numpy scikit-learn joblib
```

### 3. Run the Development Server
Apply database migrations and start the Django web server:
```bash
python manage.py migrate
python manage.py runserver
```
Open your browser and navigate to `http://127.0.0` to view the application interface.

## 🛠️ Tech Stack
*   **Backend & Web Framework:** Django
*   **Data Processing:** Pandas, NumPy
*   **Machine Learning:** Scikit-Learn
*   **Model Serialization:** Joblib
*   **Primary Language:** Python
