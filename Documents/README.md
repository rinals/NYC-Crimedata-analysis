# New York Crime Data Analysis (2024)

## Project Overview

This project involves the analysis of New York City crime data for the year 2024. The goal is to gain insights into crime patterns, identify hotspots, and build machine learning models to predict the severity of crimes (Felony, Misdemeanor, Violation) based on various features such as location, time, and demographics.

## Key Objectives

- **Data Exploration**: Explore and visualize the crime data to uncover trends and patterns.
- **Data Preprocessing**: Handle missing values, encode categorical variables, and scale numeric features.
- **Machine Learning**: Build and evaluate models to classify the severity of crimes.
- **Visualization**: Use interactive and static visualizations to show crime patterns across New York City.

## Steps Performed

### 1. Data Exploration and Visualization

- **Visualizations**: Created visualizations to analyze crime distribution across different boroughs, time periods, and demographic groups.
- **Key Visualizations**:
  - Crime types and frequency
  - Crime rates by borough
  - Demographic analysis of victims and suspects
  - Heatmaps showing crime hotspots

### 2. Data Preprocessing

- **Missing Values**: Identified and handled missing values in the dataset.
- **Encoding**: Applied one-hot encoding and label encoding for categorical variables.
- **Scaling**: Standardized numeric columns like latitude and longitude.

### 3. Machine Learning Models

- **Random Forest**:
  - Built a Random Forest classifier to predict the severity of crimes.
  - Achieved an accuracy of **0.71** with strong performance in predicting Felony, Misdemeanor, and Violation.
- **Neural Network**:
  - Constructed a Multilayer Perceptron (MLP) using Keras.
  - Achieved an accuracy of **0.44**, indicating room for improvement.
- **Model Optimization**: Tuned hyperparameters for both models to improve performance and handled class imbalance using SMOTE.

### 4. Saving Models and Results

- **Model Caching**: Saved trained models and predictions using `joblib` and Keras to avoid re-training.
- **Model Files**: The trained models are saved in the `saved_models` folder for future use.

## Results

- The **Random Forest** model performed better, achieving higher accuracy and F1-scores in predicting crime severity.
- The **Neural Network** model struggled with imbalanced data, despite optimization efforts.

## How to Run the Project

1. Install required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

2. Run the notebook to explore the visualizations and machine learning models:
    - Make sure to load the saved models from the `saved_models` folder to avoid re-training.
  
3. Models and predictions are saved for quicker future evaluations.

## Conclusion

This project offers insights into crime patterns in New York City and demonstrates the use of machine learning to predict crime severity. The **Random Forest** model outperformed the Neural Network, showing that ensemble methods work better in this context. Future improvements can include fine-tuning models and exploring additional features for more accurate crime predictions.
