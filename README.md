# NYC Housing Price Prediction: Geospatial ML [Work in Progress]

Predicting NYC residential prices using spatial features and machine learning.

**Current Best Model**: RandomForestRegressor (R²=0.622, baseline R²=0.216)

## 🚀 Project Workflow (v2.0 - Refactored)

This project is split into **3 modular notebooks** with explicit data pipeline:

1. **`01_data_cleaning_eda.ipynb`** 
   - Load raw housing data
   - Data quality assessment and cleaning
   - Exploratory Data Analysis (EDA)
   - Output: `data/processed/housing_cleaned.csv`

2. **`02_spatial_analysis_features.ipynb`**
   - Spatial autocorrelation analysis (Moran's I)
   - Hotspot/coldspot detection
   - Feature engineering (neighborhood effects, broker analysis)
   - Output: `data/processed/housing_with_features.gpkg`

3. **`03_modeling.ipynb`**
   - Baseline and advanced model development
   - Hyperparameter tuning
   - Model evaluation and comparison
   - Output: Model predictions and performance metrics

## Project Overview

### Goal
Predict housing prices with geospatial features (proximity, neighborhood effects) and understand key price drivers in NYC market.

### Data
- **Primary**: [New York Housing Market (dataset from Kaggle)](https://www.kaggle.com/datasets/nelgiriyewithana/new-york-housing-market)
- **Secondary**: Borough boundary shapefiles
- **Size**: ~4,500 properties across NYC boroughs

### Project Status

- ✅ Exploratory Data Analysis (Completed)
- ✅ Baseline Model Development (Completed)
- 🔄 Spatial Feature Optimization (In Progress)
- ⬜ K-fold Target Encoding (Planned)
- ⬜ Model Selection and Optimization (Planned)

**Experiment Tracker**
[![Experiment History](https://img.shields.io/badge/View-Experiment_Log-blue)](outputs/experiment_log.csv)

### Version History

- **v2.0** (Current): Modular notebook structure with explicit data pipeline
- **v1.0**: [Original monolithic notebook](link-to-archive-branch) - See `archive/v1-monolithic-notebook` branch