# Earthquake PGA Forecasting using Machine Learning

This repository contains two separate but related studies using machine learning models to forecast **Peak Ground Acceleration (PGA)** values from seismic event features. The models are trained separately for:

- **PGA_H**: Horizontal component  
- **PGA_UD**: Up-Down (vertical) component

These studies use artificial neural networks (ANNs) and other models to learn nonlinear relationships between input features and ground motion intensity.

---

## 📁 Files

- `PGA_H_ForecastingML.ipynb`: Forecasts horizontal PGA from earthquake data.
- `PGA_UD_ForecastingML.ipynb`: Forecasts vertical/up-down PGA from the same/similar dataset.

---

## 🔍 Objective

The goal is to provide a predictive framework for estimating PGA based on basic earthquake event parameters such as:

- Latitude, Longitude
- Depth
- Moment Magnitude (Mw)
- Station Count (NST)
- Event Gap
- Time of event (Month, Day)

This is useful in rapid damage estimation and earthquake early warning systems.

---

## 📊 Features

- Data cleaning and normalization  
- Feature selection and correlation analysis  
- ANN model architecture with Keras  
- Evaluation metrics:
  - R² (coefficient of determination)
  - RMSE
  - Error distributions  
- Comparative performance of multiple models

---

## 🧠 Model Architecture

- Input Layer: Earthquake features (e.g., Mw, Depth, Lat/Lon, Time)  
- Hidden Layers: Dense layers with ReLU activation  
- Output Layer: Single node predicting PGA (regression task)  
- Optimizer: Adam  
- Loss Function: Mean Squared Error (MSE)  
- Training Method: 80/20 split, early stopping

---

## 📈 Sample Results

| Metric        | PGA_H Model | PGA_UD Model |
|---------------|-------------|--------------|
| R² Score      | ~0.85       | ~0.80        |
| RMSE          | varies      | varies       |
| Visualizations| Scatter, Histogram, Parity plots |

*Note: These values vary depending on exact random seed, training cycles, and dataset splits.*

---

## 🚀 How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/CaglarTemiz/ML-ANN_Study_to_Estimate_Earthquake_Intensity.git
   cd ML-ANN_Study_to_Estimate_Earthquake_Intensity

2. Set up the requirements and run:

   ```bash 
   pip install -r requirements.txt

   jupyter notebook PGA_H_ForecastingML.ipynb
   jupyter notebook PGA_UD_ForecastingML.ipynb


---

This study was conducted as a term project for the course CENG 562: Machine Learning at Middle East Technical University (METU). The project involved the application of machine learning techniques—specifically artificial neural networks—to real-world earthquake engineering problems. Thanks the course instructors and peers for their feedback and support throughout the semester
