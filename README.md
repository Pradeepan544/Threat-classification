# Threat Classification

## Overview
This project focuses on detecting various types of cyber attacks using the CICIDS 2017 dataset. The dataset was preprocessed, and machine learning models were trained to classify network traffic into multiple attack categories.

## Dataset
- **Name**: CICIDS 2017
- **Source**: [Canadian Institute for Cybersecurity](https://www.unb.ca/cic/datasets/ids-2017.html)
- **Description**: The dataset contains normal and attack network traffic, including various intrusion types such as DoS, DDoS, Brute Force, and Web Attacks.

## Workflow
1. **Data Collection**
   - Combined all CSV files from the CICIDS 2017 dataset.
   
2. **Data Preprocessing**
   - Handled missing values and cleaned anomalies.
   - Encoded the target column labels.
   
3. **Feature Selection**
   - Used feature selection techniques to retain the most relevant features.
   
4. **Model Training**
   - **XGBoost One-vs-Rest Classifier**: Trained an ensemble model for multi-class classification.
   - **CatBoost MultiOutput Classifier**: Used for handling multiple attack types efficiently.
   
5. **Evaluation**
   - Confusion matrices and accuracy scores were analyzed for model performance.

## Attack Labels
The models were trained to classify network traffic into the following categories:
- **BENIGN**
- **PortScan**
- **Web Attack – Brute Force**
- **Web Attack – XSS**
- **Web Attack – SQL Injection**
- **FTP-Patator**
- **SSH-Patator**
- **DDoS**
- **Bot**
- **Infiltration**
- **DoS Slowloris**
- **DoS Slowhttptest**
- **DoS Hulk**
- **DoS GoldenEye**
- **Heartbleed**

## Future Improvements
- Train a **Neural Network** for better multi-class classification.
- Optimize hyperparameters for improved model performance.
- Implement real-time detection using streaming data.

## How to Run
1. Install dependencies:
   ```bash
   pip install xgboost catboost pandas numpy scikit-learn
   ```
2. Run the preprocessing and training script:
   ```bash
   python train_model.py
   ```
3. Evaluate model predictions and analyze results.

## Contributors
- **Shanmuga Pradeepan R**

---
Feel free to modify and expand based on your needs! 🚀
