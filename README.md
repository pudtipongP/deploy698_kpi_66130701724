https://deploy698kpi66130701724-czve68sr74tdtdhwaywvyd.streamlit.app/

# Employee KPIs Prediction and Visualization App

## Overview
This Streamlit application is designed to predict and visualize employee Key Performance Indicators (KPIs) using a pre-trained machine learning model. The app provides three main functionalities:
1. Predicting KPIs for individual employees
2. Visualizing data distributions
3. Bulk prediction from CSV files

## Prerequisites
- Python 3.7+
- Required Libraries:
  - Streamlit
  - Pandas
  - NumPy
  - Matplotlib
  - Seaborn
  - Scikit-learn
  - XGBoost
  - Pickle

## Application Tabs

### 1. Predict KPIs
- Allows manual input of employee characteristics
- Input features include:
  - Department
  - Region
  - Education
  - Gender
  - Recruitment Channel
  - Number of Trainings
  - Age
  - Previous Year Rating
  - Length of Service
  - Awards Won
  - Average Training Score

- Predicts whether the employee will meet KPIs (more than 80%)
- Uses pre-trained XGBoost classifier with label encoders for categorical features

### 2. Visualize Data
- Enables interactive data visualization
- Features:
  - Select a condition feature from the dataset
  - Filter data by specific values
  - Generates a count plot showing the distribution of KPIs
  - Uses Seaborn for visualization with a viridis color palette

### 3. Predict from CSV
- Bulk prediction functionality
- Steps:
  1. Upload a CSV file
  2. Automatically preprocess and encode data
  3. Predict KPIs for all employees in the file
  4. Display results with a new column 'KPIs_met_more_than_80'
  5. Visualize predictions based on a selected feature

## Key Technical Components
- Machine Learning Model: XGBoost Classifier
- Preprocessing: 
  - Label Encoding for categorical features
  - StandardScaler for numerical features
- Model and Encoders loaded from a pickle file
- Streamlit for interactive web application

## Limitations and Considerations
- Requires a pre-trained model file (`model_kpi_66130701724.pkl`)
- Needs a specific dataset structure
- Assumes clean input data
- Predictions based on historical training data

## Possible Improvements
- Add data cleaning options
- Implement more detailed error handling
- Create more advanced visualizations
- Add model performance metrics
- Support for more machine learning algorithms

## Usage Notes
1. Ensure all required libraries are installed
2. Place the model pickle file in the same directory
3. Prepare input data according to the expected format
4. Run the Streamlit app using `streamlit run app.py`

## Sample Use Cases
- HR Analytics
- Performance Prediction
- Employee Potential Assessment
- Training Effectiveness Evaluation
