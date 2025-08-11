![Axiom Banner](banner.png)

Axiom: AI-Powered Indonesian Stock Predictor
A predictive engine that leverages NeuralProphet, a PyTorch-based time-series forecasting model, to predict the future performance of stocks listed on the Indonesia Stock Exchange (IDX). The project is designed not just to provide a single prediction, but to find the most accurate forecasting model through rigorous hyperparameter tuning. By systematically testing various model configurations, axiom identifies the optimal parameters to minimize prediction errors (RMSE), ensuring the insights are as reliable as possible. It serves as a powerful analytical tool for investors seeking a data-driven edge in the Indonesian market.

Key Features:
- Time-Series Forecasting: Utilizes the NeuralProphet library to model trends, seasonality, and predict future stock prices.
- Hyperparameter Optimization: Automatically performs a grid search to find the best model parameters (lags, learning rate, epochs, etc.) for the highest accuracy.
- Technical Indicator Analysis: Calculates and visualizes key indicators like Simple Moving Average (SMA) and Relative Strength Index (RSI) alongside predictions.
- IDX Focused: Specifically tailored and trained on historical data from companies in the IDX30 index.
- Interactive Visualization: Uses Plotly to generate interactive charts for in-depth analysis of forecasts versus actuals.

Methodology:

The project follows a systematic data science workflow:
1. Data Loading & Preprocessing: Historical stock data for various IDX30 companies are loaded from .xlsx files. The data is cleaned, and the 'Close' prices are prepared for time-series analysis.
2. Model Training & Hyperparameter Tuning: The data is split into training and validation sets. A grid search is performed on the training data, iterating through numerous combinations of NeuralProphet parameters to build and train different models.
3. Model Evaluation: Each trained model makes predictions on the validation set. The Root Mean Squared Error (RMSE) is calculated to measure the accuracy of each model configuration.
4. Prediction & Visualization: The best-performing model is used to make future forecasts. The results, including historical data, predictions, and technical indicators, are visualized using interactive Plotly charts.

Technology Stack:

This project is built with a specific set of powerful data science libraries:
Core Libraries: pandas, numpy
Machine Learning & Forecasting: neuralprophet, scikit-learn, torch
Data Visualization: plotly

Getting Started:
To get a local copy up and running, follow these simple steps.

  Prerequisites:
  - Make sure you have Python 3.8+ installed.

  Installation:
  1. Clone the repository (replace your-username with your actual GitHub username): git clone https://github.com/daemon-10k/axiom.git
  2. Navigate to the project directory: cd axiom
  3. Create a data directory and place your .xlsx stock files inside, following the structure in the script.
  4. Install the required packages: pip install pandas numpy neuralprophet scikit-learn torch plotly

Usage:

- The primary script is designed to be run in a Jupyter-like environment to see the plots and dataframes.
- Open the .ipynb file in a Jupyter Notebook, JupyterLab, or VS Code with a Python extension.
- Adjust the file_paths dictionary to match the location of your data files.
- Run the cells sequentially to perform the data loading, model tuning, and visualization. The results of the hyperparameter search and the final forecast plots will be displayed as output.

  
