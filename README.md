# ❤️ Heart Disease Prediction Using Logistic Regression

## 📌 Project Overview

This project uses **Machine Learning (Logistic Regression)** to predict whether a patient is likely to have heart disease based on clinical and medical attributes. The model is trained using the Heart Disease dataset and deployed through an interactive **Streamlit web application**, allowing users to enter patient information and receive instant predictions. Logistic Regression is a commonly used baseline model for heart disease classification tasks and is widely used in healthcare prediction projects.

---

## 🎯 Objectives

- Perform data exploration and preprocessing.
- Build a binary classification model using Logistic Regression.
- Evaluate model performance using standard classification metrics.
- Save the trained model for reuse.
- Deploy the model using Streamlit.
- Create an easy-to-use interface for heart disease prediction.

---

## 📊 Dataset

The dataset contains patient medical information used to determine the likelihood of heart disease.

### Features

| Feature | Description |
|----------|------------|
| age | Age of patient |
| sex | Gender (0 = Female, 1 = Male) |
| cp | Chest Pain Type |
| trestbps | Resting Blood Pressure |
| chol | Serum Cholesterol (mg/dl) |
| fbs | Fasting Blood Sugar > 120 mg/dl |
| restecg | Resting Electrocardiographic Results |
| thalach | Maximum Heart Rate Achieved |
| exang | Exercise Induced Angina |
| oldpeak | ST Depression Induced by Exercise |
| slope | Slope of Peak Exercise ST Segment |
| ca | Number of Major Vessels Colored by Fluoroscopy |
| thal | Thalassemia Type |
| target | Heart Disease (0 = No, 1 = Yes) |

The dataset uses 13 clinical features that are commonly found in the Cleveland/UCI Heart Disease dataset. :contentReference[oaicite:1]{index=1}

---

## 🛠️ Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Streamlit
- Pickle
- Ngrok (for temporary public deployment)

---

## 📂 Project Structure

```text
Heart-Disease-Prediction-Logistic-Regression/
│
├── heart_disease.csv
├── Heart_Disease_Prediction.ipynb
├── heart_model.pkl
├── app.py
├── requirements.txt
└── README.md
```

---

## 🔍 Exploratory Data Analysis (EDA)

The following analyses were performed:

- Dataset inspection
- Missing value checks
- Feature distribution analysis
- Correlation analysis
- Target class distribution visualization
- Statistical summary of features

### Sample Visualizations

- Count Plot of Target Variable
- Correlation Heatmap
- Feature Distributions
- Confusion Matrix

---

## ⚙️ Data Preprocessing

The following preprocessing steps were applied:

1. Loaded dataset using Pandas.
2. Checked for missing values.
3. Separated features and target variable.
4. Split dataset into training and testing sets.
5. Prepared data for Logistic Regression training.

---

## 🤖 Model Development

### Algorithm Used

**Logistic Regression**

Why Logistic Regression?

- Simple and interpretable.
- Efficient for binary classification.
- Fast training and prediction.
- Strong baseline model for healthcare classification problems. :contentReference[oaicite:2]{index=2}

### Train-Test Split

```python
test_size = 0.2
random_state = 42
```

### Model Training

```python
from sklearn.linear_model import LogisticRegression

model = LogisticRegression(max_iter=1000)
model.fit(X_train, y_train)
```

---

## 📈 Model Evaluation

The model was evaluated using:

- Accuracy Score
- Confusion Matrix
- Precision
- Recall
- F1-Score
- Classification Report

### Example

```python
accuracy_score(y_test, y_pred)
classification_report(y_test, y_pred)
```

---

## 💾 Saving the Model

The trained model was saved using Pickle.

```python
import pickle

pickle.dump(model, open("heart_model.pkl", "wb"))
```

---

## 🌐 Streamlit Deployment

The trained model was deployed as a Streamlit web application where users can enter:

- Age
- Sex
- Chest Pain Type
- Blood Pressure
- Cholesterol
- Heart Rate
- ECG Results
- Exercise Induced Angina
- Thalassemia Information

and instantly receive a prediction.

Interactive Streamlit applications are commonly used for machine learning demonstration and deployment projects. :contentReference[oaicite:3]{index=3}

---

## 🚀 Running the Project Locally

### Clone Repository

```bash
git clone https://github.com/yourusername/Heart-Disease-Prediction-Logistic-Regression.git
cd Heart-Disease-Prediction-Logistic-Regression
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Run Streamlit App

```bash
streamlit run app.py
```

---

## 🌍 Deploying with Ngrok (Google Colab)

### Install Dependencies

```python
!pip install streamlit pyngrok
```

### Run Streamlit

```python
!streamlit run app.py &
```

### Generate Public URL

```python
from pyngrok import ngrok

ngrok.set_auth_token("YOUR_NGROK_TOKEN")

public_url = ngrok.connect(8501)

print(public_url)
```

---


```

---

## 📋 Requirements

```text
pandas
numpy
matplotlib
seaborn
scikit-learn
streamlit
pyngrok
pickle-mixin
```

---

## ⭐ Acknowledgements

- UCI Heart Disease Dataset
- Scikit-Learn Documentation
- Streamlit Documentation
- Google Colab
