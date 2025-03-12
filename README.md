# DSAI
DSAI assignment
# Titanic Dataset Exploration and Preprocessing

This project explores the Titanic dataset and performs preprocessing steps to prepare it for machine learning.

## Description

The code in this notebook performs the following tasks:

1. **Data Loading and Initial Exploration:** Loads the Titanic dataset and displays its shape, data types, and missing values.
2. **Exploratory Data Analysis (EDA):**
   - Analyzes the 'Age', 'Cabin', and 'Embarked' columns for missing values and patterns.
   - Creates visualizations to understand the distribution of numerical and categorical features.
   - Investigates the relationship between survival and other features.
3. **Data Preprocessing:**
   - Imputes missing values in the 'Age', 'Cabin', and 'Embarked' columns.
   - Verifies the imputation by checking for missing values and visually inspecting the data.

## Usage

1. **Install necessary libraries:** Make sure you have the following libraries installed:2. **Download the dataset:** Download the Titanic dataset (titanic.csv) and place it in the same directory as the notebook.
3. **Run the notebook:** Execute the code cells in the notebook sequentially.

## Insights

- **Missing Values:** The 'Age', 'Cabin', and 'Embarked' columns contain missing values.
- **Age:** Age is an important factor in survival, with younger passengers having a higher survival rate.
- **Cabin:** The 'Cabin' column has a high percentage of missing values and may not be very useful for prediction.
- **Embarked:** The port of embarkation may have some influence on survival.
- **Pclass:** Passengers in higher classes (1st and 2nd) had a better chance of survival.
- **Sex:** Female passengers had a significantly higher survival rate than male passengers.

## Further Exploration

- **Feature Engineering:** Create new features from existing ones to potentially improve model performance.
- **Model Building:** Use the preprocessed data to build machine learning models for predicting survival.
- **Model Evaluation:** Evaluate the performance of different models and select the best one.
1. Data Loading and Initial Exploration

The code starts by importing the necessary libraries: pandas, matplotlib, and seaborn.
It then loads the Titanic dataset from a CSV file named 'titanic.csv' using pd.read_csv().
It checks the shape of the DataFrame using df.shape to see the number of rows and columns.
It displays the first few rows of the DataFrame using df.head() to get an initial look at the data.
It identifies the data types of each column using df.dtypes.
It calculates and prints the number of missing values for each column using df.isnull().sum().
2. Exploratory Data Analysis (EDA)

It calculates and prints the percentage of missing values for each column to understand the extent of missing data.
It analyzes the 'Age' column by creating box plots to visualize its distribution across different categories like 'Survived', 'Pclass', and 'Sex'.
It analyzes the 'Cabin' column by creating box plots to see its relationship with 'Fare' and 'Survived'.
It analyzes the 'Embarked' column by creating count plots and box plots to see its relationship with 'Pclass', 'Fare', and 'Sex'.
3. Data Preprocessing

It imputes missing 'Age' values using the median age for each passenger class using df.groupby() and transform().
It imputes missing 'Cabin' values with "Unknown" using fillna().
It imputes missing 'Embarked' values with the mode (most frequent value) using fillna() and mode().
It verifies the imputation by checking for missing values again using isnull().sum() and printing the results.
It prints the first 10 rows of the DataFrame using df.head(10) to visually inspect the imputed values.
4. Further Data Visualization and Correlation Analysis

It visualizes the distribution of numerical features using histograms and box plots.
It visualizes the counts of categorical features using count plots and bar plots.
It calculates and visualizes the correlation matrix for numerical features using corr() and a heatmap.
It explores the relationship between survival and other features using bar plots and survival rate calculations.
It performs age analysis by creating age bands and visualizing survival rates across these bands.
It combines categorical features to analyze survival rates based on multiple factors using groupby and a heatmap.
In summary, the code loads the Titanic dataset, performs exploratory data analysis to understand the data, preprocesses the data by imputing missing values, and further visualizes the data and explores correlations between features, particularly focusing on factors affecting surviv
