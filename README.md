# Depth Series Forecasting

This repository contains a deep learning framework for forecasting multi-modal well logs from geological depth series. The project focuses on robust evaluation and modeling of well log signals, addressing common issues in data imbalance across lithofacies.

## 📘 Overview

Subsurface formations, characterized by well logs, offer vital insights into the lithological structure of the Earth's subsurface. This project implements a depth-wise sequence prediction model to forecast well log responses using multimodal inputs, mitigating the bias often introduced by dominant lithofacies in traditional evaluation metrics.

## 📂 Dataset

- **Well Logs**: Five wells are used — four for training and one held out for testing.
- **Formats**: `.xlsx` and `.csv`
- **Features**: Depth, CGR, SGR, Facies, among others

## ⚙️ Methodology

- Data preprocessing includes:
  - Interpolation and normalization (StandardScaler, MinMaxScaler)
  - Stratified balancing techniques for lithofacies
- Model architecture:
  - Deep Learning (Keras/TensorFlow)
  - Custom loss and evaluation functions
- Post-processing and smoothing

## 📈 Evaluation Metrics

To ensure fairness across all lithofacies, especially rare ones, the project adopts **weighted** evaluation metrics:

- **Weighted MAPE (MAPEW)**: Enhances fairness by assigning more importance to rare lithofacies in the error calculation.
- **Weighted R²**: Adjusts traditional R² to fairly represent prediction quality for underrepresented lithofacies.

These adjustments make the performance assessment more robust and reliable for geoscientific tasks.

## 🛠 Dependencies

- `Python 3.8+`
- `numpy`
- `pandas`
- `matplotlib`, `seaborn`
- `tensorflow`, `keras`
- `scikit-learn`
- `scipy`

To install dependencies:

```bash
pip install -r requirements.txt
```

## ▶️ Running the Notebook

The main analysis is in the Jupyter notebook:  
`Depth series forecasting.ipynb`

Simply open the notebook and run cells sequentially to preprocess data, train models, and evaluate performance.

## 🔬 Academic Relevance

This project was developed as part of an academic research effort focused on geostatistical modeling and deep learning in subsurface interpretation. The weighted metrics were designed to improve reliability in the prediction of rare lithofacies critical to geological decision-making.
