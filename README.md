# Mahlo Correlation Model

## Overview

The goal of this project is to correlate the results from Mahlo in-line density scanners with the manually cut in-process density, measured by the technicians in the plant.
The final notebook is designed to integrate, explore, preprocess, and model datasets extracted from SAP and Wonderware, focusing on predicting outcomes using various machine learning techniques. It is structured from data importation and cleaning to model training and evaluation. Below is a detailed walkthrough of each section of the notebook, explaining the operations performed and their significance in the overall workflow.

## Sections

### 1. **Imports**

This section loads all necessary libraries for data manipulation, visualization, and machine learning. These libraries include:

- **Pandas and NumPy**: For data manipulation and numerical operations.
- **Matplotlib and Seaborn**: For data visualization.
- **Scikit-learn**: For implementing machine learning models and performing data splitting and scaling.
and so on.

### 2. **Data Engineering**

This section begins with importing raw data from local storage, particularly an Excel file. The steps involved in this process include:

- **Data Import**: The SAP data is imported using Pandas. The data contains various metrics such as batch times, line descriptions, thickness, density, etc.
  
- **Data Cleaning**: The notebook removes irrelevant rows, handles missing data, and filters out unnecessary columns. This ensures the dataset is ready for analysis and modeling.

Programmatic connection is established with Wonderware to extract data on the inline densities.

### 3. **Exploratory Data Analysis (EDA)**

This section involves exploring the dataset to understand the underlying patterns and relationships within the data. Key activities include:

- **Descriptive Statistics**: Summary statistics provide an overview of the central tendencies, variances, and distribution shapes.
  
- **Visualizations**: Various plots (e.g., histograms, scatter plots, pair plots) are generated to visually inspect the data, identify trends, correlations, and potential outliers.

### 4. **Modeling**

This section is dedicated to building and evaluating machine learning models. It covers:

- **Data Splitting**: The dataset is divided into training, validation and testing sets to validate the models' performance.
  
- **Model Selection**: Multiple regression models are implemented, including but not limited to:
  - **Linear Regression**
  - **Ridge and Lasso Regression**
  - **Decision Tree Regression**
  - **Random Forest Regression**
  - **Gradient Boosting Regression**
  - **XGBoost Regression**

- **Hyperparameter Tuning**: GBR and RFR are chosen for further analysis; their parameters are fine-tuned to enhance performance using cross-validation techniques.

### 5. **Evaluation**

In this section, the models' performance is evaluated using appropriate metrics such as:

- **Root Mean Squared Error (MSE)**: Measures the root of the average squared difference between predicted and actual values.
- **R-squared (R²)**: Indicates the proportion of the variance in the dependent variable predictable from the independent variables.
- **Mean Absolute Percentage Error (MAPE)**: Calculates the average of the absolute percentage errors between the predicted and actual values.
  
Visual comparisons between actual and predicted values are also performed to assess the models' effectiveness.

## How to Use

1. **Prerequisites**: Ensure you have Python installed, along with all required libraries as listed in the notebook. 

2. **Run the Notebook**: Start from the top, executing each cell sequentially. It’s essential to follow the order, especially during data loading and preprocessing, to avoid errors in subsequent steps.

3. **Modify and Experiment**: Feel free to tweak parameters, try different models, or even add new datasets to test the robustness of the notebook’s approach.
