
# Meteorological Data Analysis

## Overview

This project aims to analyze meteorological data using Python and the pandas library. The dataset used for analysis is stored in the file `weatherHistory.csv`.

## Dataset

The dataset was loaded using the pandas library with the following code:

```python
import pandas as pd
```
# Load the dataset
```
dataset = pd.read_csv("F:/d/weatherHistory.csv")
```
Analysis Steps
Data Exploration:
Investigate the structure of the dataset.
Check for missing values and handle them if necessary.
```
# Explore the dataset
print(dataset.head())
print(dataset.info())
print(dataset.describe())
```
Data Cleaning:
Handle missing values or outliers.
Convert data types if needed.
```
# Handle missing values
dataset.dropna(inplace=True
```
# Convert data types
# Example: dataset['Date'] = pd.to_datetime(dataset['Date'])
Exploratory Data Analysis (EDA):
Visualize key metrics.
Explore relationships between different variables.

# Example EDA
```
import matplotlib.pyplot as plt
import seaborn as sns
```
# Visualize temperature distribution
```
sns.histplot(dataset['Temperature (C)'], bins=20, kde=True)
plt.title('Temperature Distribution')
plt.show()
```
Statistical Analysis:
Perform statistical tests or calculations.
```
# Example statistical analysis
mean_temperature = dataset['Temperature (C)'].mean()
print(f"Mean Temperature: {mean_temperature}")
```

Dependencies
pandas
matplotlib
seaborn
How to Run the Analysis
Install the required dependencies:
```
pip install pandas matplotlib seaborn
```
Run the analysis script:
```
python meteorological_analysis.py
```
