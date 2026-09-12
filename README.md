# Smart Home Energy Consumption Analysis

## Project Overview

This project performs an end-to-end data science and machine learning analysis on the [Smart Home Energy Consumption dataset](https://www.kaggle.com/datasets/adilshamim8/smart-home-energy-consumption). The goal is to investigate device-level energy usage across residential smart appliances, uncover key cost drivers, and build predictive models to forecast household energy costs.

## Dataset Highlights

* **Scale:** Over 50,000 device-level usage records.
* **Features:** Power consumption (W), usage duration (minutes), environmental metrics (temperature, humidity), room location, device type, time parameters, and total energy cost ($).
* **Key Findings:** High-power climate appliances (Heaters and Air Conditioners) dominate total household energy expenditure, whereas low-power electronics (Smart Plugs, Smart Bulbs) contribute marginally to overall costs.

## Key Features & Methodology

1. **Parallel Data Processing:** Utilizes [Dask](https://www.dask.org/) alongside `pandas` to process and manipulate large tabular datasets efficiently.
2. **Feature Engineering:** Extracts cyclical and temporal features (`Hour`, `DayOfWeek`, `Month`) and computes rate-based metrics (`Cost Per Min`).
3. **Exploratory Data Analysis (EDA):** Analyzes consumption distributions by device type, room location, and environmental variables.
4. **Machine Learning Pipeline:** Implements data preprocessing, unsupervised techniques (PCA and clustering), and supervised regression models (Linear Regression, Gradient Boosting, XGBoost, and Neural Networks) to forecast costs.

## Dependencies & Requirements

To run this notebook, ensure you have the following Python libraries installed:

```bash
pip install category_encoders pandasql dask pandas numpy matplotlib seaborn folium torch scikit-learn xgboost tqdm

```

## How to Run

1. Open the notebook in **Google Colab** or a local **Jupyter Notebook** environment.
2. Ensure your `kaggle.json` credentials are saved in your Google Drive or root directory to enable automatic dataset download via the Kaggle API.
3. Run all cells sequentially from **Part 1: Introduction** through the model evaluation sections.
