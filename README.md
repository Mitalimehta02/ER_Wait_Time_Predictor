
# ER Waiting Time Prediction

This project simulates and predicts the expected waiting time for patients in an Emergency Room (ER) using machine learning and large language models (LLMs). It integrates synthetic data generation, regression modeling, and explainability tools such as SHAP.

# Overview

Hospitals often face challenges in managing patient flow in ERs. Accurately predicting wait times can improve patient satisfaction and resource allocation. This project demonstrates how to:

- Generate a synthetic ER dataset
- Model ER wait times using Random Forest and XGBoost
- Incorporate patient symptom descriptions using sentence embeddings from a pre-trained BERT model
- Visualize feature importance and interpret model decisions using SHAP

# Project Structure

 ER Waiting Time Prediction
├── er_waiting_time.py       # Complete codebase
├── synthetic_er_wait_data.csv  # Generated synthetic data 
└── README.md                # Project documentation


# Features

- Synthetic Data Generator 
  Randomly simulates patient arrivals, symptom types, staff availability, and triage levels.

- Baseline Machine Learning Models 
  Uses Random Forest and XGBoost for regression modeling of wait time.

- Text Feature Engineering 
  Leverages BERT sentence embeddings to convert symptoms into numeric features.

- Explainability with SHAP  
  Understands model predictions at both global and individual levels.


# Model Evaluation

| Model             | MAE (min) | RMSE (min) | R² Score |
|------------------|-----------|------------|----------|
| Random Forest     | ~7.1      | ~9.2       | ~0.85    |
| XGBoost (Base)    | ~6.7      | ~8.5       | ~0.88    |
| XGBoost + LLM     | ~5.9      | ~7.4       | ~0.91    |

# Visualizations

- Feature Importance
- Actual vs Predicted Wait Times
- SHAP Summary and Waterfall Plots

> These plots help stakeholders understand which features (e.g., queue length, triage level, symptom) are influencing wait time predictions the most.

# Technologies Used

- Python
- Pandas, NumPy, Scikit-learn
- XGBoost
- Sentence Transformers (BERT embeddings)
- SHAP
- Matplotlib

# Use Cases

- Hospital wait time dashboard integration
- Resource planning for emergency departments
- Scenario testing under different ER conditions

# Future Enhancements

- Deploy the model using Flask or FastAPI
- Build a front-end dashboard using Streamlit
- Use real-world datasets for improved generalizability
- Integrate alert systems for critical triage levels




