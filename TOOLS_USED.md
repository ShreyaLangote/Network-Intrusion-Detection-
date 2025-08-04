# 🛠️ Tools & Technologies Used

This document lists the tools, platforms, and libraries used for developing the **Network Intrusion Detection System (NIDS)** using IBM Cloud services.

---

## ☁️ IBM Cloud Services

### 1. IBM Watson Studio
- Used to create the project workspace
- Hosts AutoAI experiments and Jupyter notebooks

### 2. IBM Cloud Object Storage
- Stores the dataset files (`Train_data.csv`, `Test_data.csv`)
- Connected to the Watson Studio project for AutoAI access

### 3. IBM Watson Machine Learning
- Used to deploy the trained model as an **online REST API**
- Allows live testing and integration of the model

---

## 🤖 AutoML Platform

### IBM Watson AutoAI
- Automatically handled:
  - Data preprocessing (encoding, scaling)
  - Model training and selection
  - Cross-validation and optimization
- Final selected algorithm: **Snap Random Forest Classifier**

---

## 📊 Dataset

- Source: Kaggle Network Intrusion Detection Dataset  
  [https://www.kaggle.com/datasets/sampadab17/networkintrusion-detection](https://www.kaggle.com/datasets/sampadab17/network-intrusion-detection)

---

## 🧰 ML Libraries (used internally by AutoAI)

> Although manual coding was not required, the following libraries are used by AutoAI in the backend:

- `scikit-learn` – ML algorithms and pipeline
- `xgboost` – Gradient boosting (used in some pipelines)
- `pandas` – Tabular data handling
- `joblib` – Model serialization
- `NumPy` – Array manipulation

---

## 💻 Development Environment

- Platform: IBM Cloud Lite (Free Tier)
- Interface: IBM Watsonx.ai Studio (GUI-based AutoAI, Notebooks, Deployment tools)
- Browser: Google Chrome

---

## ✅ Summary

| Category              | Tool/Service                    |
|-----------------------|----------------------------------|
| Cloud Platform        | IBM Cloud Lite                   |
| ML Development        | Watson Studio + AutoAI           |
| Storage               | IBM Cloud Object Storage         |
| Model Deployment      | Watson Machine Learning          |
| Dataset Source        | Kaggle                           |
| Primary Algorithm     | Snap Random Forest Classifier    |
