# ❤️ Heart Disease Prediction Hackathon

## Overview

This project was developed for a data science competition focused on privacy-preserving heart disease prediction. The challenge required creating models that accurately predict heart conditions based on anonymized clinical and demographic data, such as age, blood pressure, cholesterol, and peak heart rate, while ensuring strict adherence to privacy regulations.

### 🏥 **Objective**
The main task is to predict the likelihood of heart disease using synthetic health data. The dataset includes several clinical and demographic indicators, and the goal is to maximize prediction accuracy without compromising data privacy.

### 📊 **Dataset Features**
- **Age** (years)
- **Sex** (binary: 0/1)
- **Blood Pressure** (mm/Hg)
- **Cholesterol** (mg/dl)
- **Blood Sugar** (mg/dl)
- **Peak Heart Rate** (beats per minute)
- **Heart Condition** (binary: 0/1)

### 🚀 **Steps in the Code**

#### 1. **Neural Network Approach with Differential Privacy** 🧠
- Used **TensorFlow** with privacy-preserving techniques to train a neural network.
- The network architecture included dense layers with dropout to prevent overfitting.
- **Differential Privacy** was ensured using the `PrivateKerasModel` class from **Opacus**, which added noise during the training process to protect sensitive information.
- After training, predictions were made on the test dataset, and privacy-preserving transformations ensured no private data was leaked.

#### 2. **Logistic Regression Approach with Differential Privacy** 📈
- Applied **Logistic Regression** using the `Diffprivlib` library to model the relationship between features like blood pressure, cholesterol, and age, and the target heart condition.
- A differentially private logistic regression model was trained on the clinical data, providing a lightweight yet privacy-respecting approach.
- The trained model made predictions on the test set, which were then evaluated for accuracy and privacy compliance.

### 🔧 **Libraries Used**
- **Opacus**: For differential privacy in neural networks.
- **Diffprivlib**: For differentially private logistic regression.
- **TensorFlow Privacy**: Ensuring privacy for deep learning models.

This solution effectively balances accuracy and privacy, applying privacy-preserving techniques to two model types: neural networks and logistic regression.
