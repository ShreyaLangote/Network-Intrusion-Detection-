# 🛡️ Network Intrusion Detection System (NIDS) using IBM Cloud & AutoAI

## 📌 Project Overview

This project aims to develop a Machine Learning–based **Network Intrusion Detection System (NIDS)** that can classify network traffic as either **normal** or **anomalous**. Built entirely using **IBM Cloud Lite services**, this solution uses **Watson Studio AutoAI** to automate model training, and **Watson Machine Learning** to deploy the model as an online REST API.

---

## 🚨 Problem Statement

Modern communication networks are vulnerable to cyberattacks like DoS, Probe, R2L, and U2R. Traditional rule-based systems struggle to adapt to evolving threats. The goal is to develop an intelligent system that can automatically analyze network traffic and detect malicious activities in real time.

---

## 🧠 Solution Approach

The solution uses a publicly available dataset to train and deploy a classification model that distinguishes between normal and anomalous network behavior. IBM’s **AutoAI** automates the ML workflow — from preprocessing to model selection and optimization.

---

## 🛠️ Tech Stack

- **IBM Watson Studio**
- **IBM Cloud Object Storage**
- **IBM Watson Machine Learning**
- **IBM AutoAI**
- Dataset: [Kaggle - Network Intrusion Detection Dataset](https://www.kaggle.com/datasets/sampadab17/network-intrusion-detection)

---

## 📁 Dataset Details

- **Train_data.csv**: 25,192 rows × 42 columns (with labels)
- **Test_data.csv**: 22,544 rows × 41 columns (no labels)
- Features include:
  - `protocol_type`, `service`, `flag`, `src_bytes`, `dst_bytes`, etc.
- Target column: `class` (`normal`, `anomaly`)

---

## 🔄 System Workflow

1. **Upload dataset** to IBM Cloud Object Storage
2. **Create a Watson Studio project**
3. **Launch AutoAI** and configure:
   - Prediction column: `class`
   - Prediction type: Binary Classification
   - Positive class: `anomaly`
4. **Run AutoAI experiment** to train and rank models
5. **Save the best pipeline** (Snap Random Forest Classifier)
6. **Promote the model** to a deployment space
7. **Deploy model as online REST API**
8. **Test predictions** using the Watson interface

---

## ✅ Results

- Best Model: **Snap Random Forest Classifier**
- Accuracy: *~96% (AutoAI cross-validation)*
- Precision (anomaly): High
- Model deployed as a REST API and tested with JSON input:
  ```json
  "prediction": ["anomaly"]
