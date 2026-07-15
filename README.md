# NYC Taxi Fare Prediction

## End-to-End Machine Learning Project

### Overview

This project develops a complete end-to-end machine learning pipeline for predicting taxi fare amounts in New York City using historical NYC Yellow Taxi trip data.

The workflow follows industry-standard machine learning practices including:

- Data Cleaning
- Feature Engineering
- Exploratory Data Analysis (EDA)
- Model Development
- Hyperparameter Tuning
- Model Evaluation
- Model Interpretation

The primary objective is to predict the **fare amount** of a taxi trip based on trip-related information such as travel distance, pickup time, and passenger count.

---

## Problem Statement

Accurate taxi fare estimation is an important component of modern transportation systems. Predicting fares helps improve pricing transparency, customer experience, and operational efficiency.

**Goal:** Build a machine learning model capable of predicting NYC taxi fares using historical trip data.

**Target Variable:** `fare_amount`

---

## Dataset

This project uses the **NYC Yellow Taxi Trip Dataset**, which contains real-world taxi trip records from New York City.

Key features include:

- Pickup Date & Time
- Pickup Coordinates
- Drop-off Coordinates
- Passenger Count
- Fare Amount

---

## Project Workflow

### 1. Data Loading & Initial Exploration

- Load dataset
- Examine structure and data types
- Generate statistical summaries

### 2. Data Cleaning

- Handle missing values
- Remove invalid fare amounts
- Filter unrealistic passenger counts
- Validate geographic coordinates
- Convert datetime features

### 3. Feature Engineering

- Calculate Haversine distance
- Extract hour, day, month, year
- Create weekday features

### 4. Exploratory Data Analysis (EDA)

Visualizations performed:

- Trip Distance vs Fare Amount
- Passenger Count vs Fare Amount
- Pickup Hour vs Fare Amount

### 5. Time-Aware Train-Test Split

To avoid data leakage:

- Earlier trips used for training
- Later trips used for testing

### 6. Machine Learning Models

#### Linear Regression

Baseline regression model.

#### Random Forest Regressor

Main machine learning model used for prediction.

### 7. Hyperparameter Tuning

Model optimization using:

- RandomizedSearchCV
- GridSearchCV

### 8. Model Evaluation

Evaluation metrics:

- RMSE (Root Mean Squared Error)
- RMSLE (Root Mean Squared Logarithmic Error)

### 9. Model Interpretation

- Feature Importance Analysis
- Business Insights
- Model Limitations

---

## Technologies Used

### Programming Language

- Python

### Data Analysis

- Pandas
- NumPy

### Visualization

- Matplotlib
- Seaborn

### Machine Learning

- Scikit-Learn

---

## Repository Structure

```text
end-to-end-nyc-taxi-fare-prediction/
│
├── README.md
├── requirements.txt
├── End_to_End_NYC_Taxi_Fare_Prediction.ipynb
│
├── data/
│   └── sample_dataset.csv
│
└── images/
    ├── distance_vs_fare.png
    ├── passenger_vs_fare.png
    ├── pickup_hour_vs_fare.png
    └── feature_importance.png
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/end-to-end-nyc-taxi-fare-prediction.git
```

Navigate to the project directory:

```bash
cd end-to-end-nyc-taxi-fare-prediction
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Running the Project

Open the notebook using:

- Google Colab
- Jupyter Notebook
- JupyterLab

Run all notebook cells sequentially to reproduce the complete workflow.

---

## Results

The Random Forest Regressor achieved better performance than Linear Regression and was selected as the final model.

Key findings:

- Trip distance is the strongest predictor of fare amount.
- Time-based features improve predictive performance.
- Passenger count has relatively low impact on fare estimation.

---

## Future Improvements

Potential enhancements include:

- Traffic data integration
- Weather information
- Airport proximity features
- XGBoost, LightGBM, and CatBoost models
- Real-time fare prediction application

---

## Author

**Haider Ali**  
BS Data Science  
University of Engineering and Technology (UET) Peshawar

---

## License

This project was developed for educational and academic purposes.
