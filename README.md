# Rain Prediction Model

## Project Overview

This project aims to predict rainfall using historical and current weather data. The model integrates three datasets:

1. **Daily Rainfall Data** from January 2024.
2. **District-Wise Rainfall Normals** for various districts.
3. **Historical Rainfall Data** from 1901 to 2015.

The goal is to develop a predictive model using Linear Regression to forecast average rainfall based on various features.

## Why It's a Test Project

This project is primarily a proof of concept and test model. The predictions from this model may not be practically accurate due to:
- Limited and possibly inaccurate data.
- Simplistic approach using linear regression without more advanced techniques.
- Preliminary preprocessing and feature engineering.

The results obtained are:
- **Mean Absolute Error (MAE):** 0.0704
- **Root Mean Squared Error (RMSE):** 0.2222
- **R^2 Score:** 0.0147

These results suggest that the model may not perform well in real-world scenarios.

## Tools and Technologies

- **Python**: Programming language used for data processing and modeling.
- **Pandas**: Library for data manipulation and analysis.
- **Scikit-Learn**: Library for machine learning, used for creating and evaluating the Linear Regression model.
- **Jupyter Notebook**: Development environment used for running the code and visualizing results.

## Steps and Methodology

1. **Data Loading and Inspection**:
   - Loaded datasets from CSV files.
   - Inspected the datasets to understand their structure and contents.

2. **Data Transformation**:
   - Converted datasets to long format using `pd.melt()` to facilitate merging.
   - Processed the daily rainfall data to extract relevant features.

3. **Data Merging**:
   - Merged daily rainfall data with monthly norms and historical rainfall data based on geographical and temporal features.

4. **Data Preprocessing**:
   - Handled missing values by filling them with zeros.
   - Defined features (`Day`, `Monthly_Rainfall`, `Historical_Rainfall`) and target variable (`Avg_rainfall`).

5. **Model Training and Evaluation**:
   - Split the data into training and testing sets.
   - Trained a Linear Regression model on the training data.
   - Evaluated the model's performance using MAE, RMSE, and R^2 Score.

## Future Improvements

- **Advanced Modeling**: Explore other machine learning models such as Decision Trees, Random Forests, or Gradient Boosting.
- **Feature Engineering**: Improve feature selection and engineering to enhance model performance.
- **Data Quality**: Use more accurate and comprehensive datasets for better predictions.
- **Hyperparameter Tuning**: Optimize model parameters for better results.

## How to Contribute

If you'd like to contribute to this project:
1. **Fork** the repository.
2. **Clone** your fork to your local machine.
3. **Create** a new branch for your changes.
4. **Commit** your changes and **push** them to your fork.
5. **Create** a pull request describing your changes and improvements.

## Installation and Usage

To use this project, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/rain-prediction-model.git
   ```

2. **Navigate to the Project Directory**:
   ```bash
   cd rain-prediction-model
   ```

3. **Set Up a Virtual Environment**:
   ```bash
   python -m venv env
   source env/bin/activate  # On Windows, use `env\Scripts\activate`
   ```

4. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

5. **Run the Jupyter Notebook**:
   ```bash
   jupyter notebook
   ```

