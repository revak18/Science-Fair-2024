# Post-Wildfire Tree Mortality Prediction Using Machine Learning

## Overview
This project uses machine learning to predict tree mortality following wildfires by combining historical drought conditions and satellite-derived burn severity measurements.

The goal is to identify trees at risk of delayed mortality and support forest recovery and restoration planning.

## Methodology
- Uses the USDA Forest Service Fire and Tree Mortality (FTM) dataset.
- Collects Palmer Drought Severity Index (PDSI) data from GRIDMET using Google Earth Engine.
- Extracts Normalized Burn Ratio (NBR) measurements from Landsat satellite imagery.
- Calculates burn severity indicators, including dNBR and RdNBR.
- Analyzes environmental conditions before, during, and after wildfires.
- Combines drought and burn severity data with observed tree mortality records.
- Evaluates different combinations of long-term and short-term environmental features.
- Trains and compares four classifiers: Support Vector Machine, Random Forest, K-Nearest Neighbors, and Decision Tree.
- Uses an 80:20 training/testing split and evaluates accuracy, precision, recall, F1 score, and confusion matrices.
- Applies the Random Forest model to a case study of California's 2021 Dixie Fire.

## Code

**`PDSI_NBR_Data.ipynb`**
- Collects and processes historical PDSI and Landsat NBR data.
- Calculates annual and six-month environmental indicators.
- Combines satellite measurements with USDA tree mortality records.
- Generates datasets for model training and evaluation.

**`TreeMortality_Prediction.ipynb`**
- Performs exploratory data analysis and feature selection.
- Trains and evaluates machine learning classifiers.
- Compares different environmental predictor combinations.
- Analyzes feature importance.
- Generates tree mortality predictions and geographic visualizations for the Dixie Fire.

## Requirements
Python, Google Earth Engine API, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, GeoPandas, Folium, and Altair.

The notebooks are designed for Google Colab and require Google Earth Engine authentication, access to the USDA FTM dataset, and configured Google Drive paths for intermediate CSV files.

## Outputs
The analysis generates:
- Historical drought and burn severity datasets
- Machine learning model performance comparisons
- Feature importance rankings
- Confusion matrices and environmental trend visualizations
- Geographic predictions of post-wildfire tree mortality
- Dixie Fire case study maps

Model predictions depend on the available satellite observations, environmental features, and training data.
