# NYC Airbnb Price Prediction Pipeline

Machine learning pipeline for predicting short-term rental prices in NYC using Random Forest regression with automated data validation and experiment tracking.

## Key Features
- End-to-end MLflow orchestration
- Automated data validation with pytest
- Weights & Biases experiment tracking
- Hyperparameter optimization
- Version-controlled releases demonstrating iterative debugging

## Results
- **Model:** Random Forest (max_depth=50, n_estimators=200)
- **MAE:** 34.18
- **R²:** 0.55

## Technologies
Python • pandas • scikit-learn • MLflow • Weights & Biases • Hydra • pytest • Git

## Pipeline Components
1. **Data Download:** Retrieves sample data from remote source
2. **Data Cleaning:** Removes outliers, handles missing values, filters geographic boundaries
3. **Data Validation:** Automated tests for row count, price range, and geographic boundaries
4. **Data Splitting:** Stratified train/validation/test split
5. **Model Training:** Random Forest with hyperparameter tuning
6. **Model Testing:** Validation on held-out test set

## Project Evolution
- **v1.0.0:** Initial pipeline implementation
- **v1.0.1:** Fixed geolocation boundary validation to handle outlier data points

## Setup
Requires Python 3.10 and conda.
```bash
conda env create -f environment.yml
conda activate nyc_airbnb_dev
wandb login [your-api-key]
mlflow run .
