# Online Retail Data Analysis and Preprocessing 

## Table of Contents  
- [Overview](#overview)
- [Features](#features) 
- [Source](#source)
- [Installation Guide](#installation-guide) 
- [Completed Steps](#completed-steps)  
- [Project Continuation](#project-continuation) 
- [How to Use](#how-to-use)  

## Overview  

This repository contains the ongoing work for a data analysis and preprocessing project focused on an online retail dataset. The dataset includes 541,909 observations and features such as InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, and Country. The goal of this project is to gain insights into customer behavior, sales performance, and product trends through various data analysis techniques.  

### Project Status  

This project is a work in progress, and I will be adding additional steps and improvements over time. The current steps completed are outlined below, and future enhancements will include advanced analyses and modeling.  

## Features  

The dataset comprises the following features:  

- **InvoiceNo**: A unique identifier for each transaction. This helps in tracking individual purchases.  
- **StockCode**: A unique identifier for each product. This is used to differentiate between different items sold.  
- **Description**: A textual description of the product. This helps in understanding what each item is.  
- **Quantity**: The number of units purchased during the transaction. This is crucial for analyzing sales volume.  
- **InvoiceDate**: The date and time when the transaction occurred. This feature is vital for time-series analysis and seasonal trends.  
- **UnitPrice**: The price per unit of the product. This is important for revenue calculations and price analysis.  
- **CustomerID**: A unique identifier for each customer. This allows for customer segmentation and analysis of purchasing behavior.  
- **Country**: The country where the customer is located, which can help in understanding geographical trends in sales.

## Source

Here's a stable link to download the "Online Retail" dataset (in xlsx format) directly from the UCI Machine Learning Repository: [Online Retail Dataset](https://archive.ics.uci.edu/dataset/352/online+retail)

### Steps to Use the Downloaded Dataset
1. **Download the dataset**: Click the link above and save the file (named Online Retail.xlsx) to a directory of your choice.
2. **Load it in your project**: You can then load it in your Jupyter Notebook or Python script using the local path like this:

- import pandas as pd  
- Replace 'path/to/your/file.xlsx' with the actual path where you saved the file  
df = pd.read_excel('path/to/your/file.xlsx')

## Installation Guide 

To run this project locally, ensure you have Python and Jupyter Notebook installed along with the necessary libraries. You can install the required libraries using pip:  

```bash  
pip install pandas numpy scipy
```

## Completed Steps

1. **Imported Libraries**:   
   - Pandas  
   - NumPy  
   - SciPy 

2. **Imported the dataset**
   - Imported the dataset using `pandas` library.

3. **Data Preprocessing**:  
   - **Convert Data Types**: Ensured that data types are appropriate for analysis.  
   - **Duplicate Tuples**: Identified and removed duplicate entries in the dataset.  
   - **Handling Missing Values**: Addressed missing data to maintain data integrity.  
   - **Filter Out Unnecessary Data**: Removed irrelevant data points to streamline analysis.  
   - **Detecting Outliers (Noise)**: Identified and dealt with outliers in the dataset.  

4. **Exploratory Data Analysis (EDA)**:

Initial EDA steps have been completed, focusing on understanding the data structure and uncovering early insights. The following tasks were performed:
   - **Visualized Data Distributions**: Analyzed numerical and categorical features using histograms, boxplots, and barplots.
   - **Explored Relationships Between Variables**: Used scatter plots, correlation matrices, and grouped bar charts, boxplots and heatmaps to explore inter-variable relationships.
   - **Performed Trend Analysis**: Created time series plots to examine trends over time based on key metrics such as quantity and sales (grouped by month and week).

These visualizations provide a foundation for deeper analysis and pattern recognition in future phases.

### complete EDA

This part of the update, called "complete EDA" focuses on time-based and seasonal exploratory data analysis to understand customer behavior, sales performance, and the effect of calendar dynamics on sales trends. The completed steps are:

   - **Cohort Analysis**:    
      1. Identified customer behaviors over time by grouping them into cohorts based on their first purchase month.
      2. Generated a retention heatmap to visualize customer engagement across different times.
   - **Time-Based Heatmap**:
      1. Interaction heatmap: When customers engaged most often.
      2. Sales heatmap: When the highest sales amounts occurred.
      3. Quantity heatmap: When the most products were sold.
   - **Seasonal & Holiday Trends Analysis**:
      1. Tracked seasonal sales patterns to identify high-performing periods.
      2. Evaluated customer activity trends across different seasons.
      3. Compared sales between weekdays and weekends.
      4. Visualized sales distribution differences between weekdays and weekends using boxplots.
      5. Assessed the effect of holidays on sales (including Black Friday, etc.).

5. **Feature Engineering Phase**:

This recent update contains the **Feature Engineering** phase for the Retail Online Dataset. It focuses on transforming raw data into meaningful features that can improve model performance and support further analysis. The following steps are performed in this phase:

   - New Feature Creation:
      1. Total Price Calculation
      2. Customer Behavior Analysis
      3. Product Popularity Analysis
      4. Time-Based Analysis
      5. Location-Based Features
      6. Lag Features
   - Feature Encoding:
      1. One-hot Encoding:
      #### It is a technique used to convert categorical variables into a numerical format that can be provided to machine learning algorithms. This method creates binary (0 or 1) columns for each category in the original variable.

      #### How It Works:
      - For each unique category in a categorical feature, a new binary column is created.
      - A value of `1` is assigned to the column corresponding to the category for a given observation, while `0` is assigned to all other columns.

   - Feature Scaling:
      1. Standard Scaling 

This phase prepared a clean, enriched, and machine-learning-ready dataset to be used in the next modeling steps.  

6. **Segmentation & Clustering**:

This part of the project focuses on segmenting customers based on their purchasing behavior using RFM (Recency, Frequency, Monetary) metrics. Here's a summary of the main steps:

   - **RFM Feature Engineering**  
      - Calculated `Recency`, `Frequency`, and `Monetary` values for each customer.

   - **Rule-Based Segmentation**  
      - Customers labeled using simple logic rules based on RFM thresholds.
      
   - **Exploratory Segment Analysis**
      - Performed exploratory segment analysis for customer segmentation and created various plots to visualize the distinct segments identified.

   - **K-Means Clustering**  
      - Applied `K-Means` clustering algorithm and determined the optimal number of clusters using **WCSS**.
      - The **Elbow Method** and **Silhouette Score** was used to choose the *optimal k*.
      - Segmented customers into *2 groups*.
      - Performed Cluster Analysis & Visualization

7. **Machine Learning Models**:

In this section, the `Linear Regression Model` was used to predict the *Monetary* value of customers based on encoded behavioral features.

#### These steps were performed:

- **Regression Assumption Checks:**
   - *Normality* Test: Checked with *Anderson-Darling*.
   - *Multicollinearity* Check: Verified with *VIF*.
   - Feature Relationship.
- **Data Preparation for Linear Regression Modeling:**
   - *Box-Cox Transformation*.
   - Outlier Detection.
   - One-Hot Encode.
   - Final Dataset Construction.
   - Split the Dataset.
- **Building and Evaluating the Linear Regression Model:**
   - Used Linear Regression.
   - Evaluated with metrics: `R²`, `MAE`, `MSE`, `Max Error`.
- **Feature Importance via Coefficients:**
   - Extracted top predictors influencing the model output.
- **Model Adequacy Checks:**
   - Normality of residuals: Histogram, *Q-Q plot*, Anderson-Darling Test.
   - Linearity Check: Scatter plot.
   - *Homoscedasticity*: Residuals vs Fitted plot.
   - Independence of Residuals: *Durbin-Watson test* + *ACF plot*.
   - *Model Generalization Check* (Overfitting / Underfitting): Compared training vs test scores and residual patterns.
   - *Overall Model Significance*: Assessed via `F-test` (*ANOVA-style summary*).

### OLS Regression Summary

#### Model Overview

- **R-squared:** 0.675  
  → The model explains approximately 67.5% of the variance in the target variable `Monetary_BoxCox`.

- **Adjusted R-squared:** 0.674  
  → Indicates a good balance between model complexity and performance.

- **F-statistic:** 2367 | **Prob (F-statistic):** 0.000  
  → The overall model is statistically significant.

#### Coefficients Interpretation

| Feature            | Coefficient | P-value | Interpretation                            |
|--------------------|-------------|---------|--------------------------------------------|
| `const`            | 4.5617      | 0.000   | Intercept; base value of the prediction.   |
| `Recency_BoxCox`   | 0.0018      | 0.611   | Not statistically significant             |
| `Frequency_BoxCox` | 0.7867      | 0.000   | Strong positive effect on `Monetary`      |
| `cluster_1`        | 0.4600      | 0.000   | Belonging to cluster 1 increases spending  |


#### Assumption Checks

| Test               | Value     | Interpretation                                      |
|--------------------|-----------|------------------------------------------------------|
| **Durbin-Watson**  | 2.026     | Residuals are independent (ideal: ~2.0)             |
| **Omnibus**        | 65.555    | Some deviation from normality, but acceptable        |
| **Jarque-Bera**    | 122.668   | Skewness: 0.111 | Kurtosis: 3.900 – Nearly normal          |
| **Condition No.**  | 28.3      | No signs of multicollinearity (well below 30)      |


#### Final Summary

> The linear regression model is statistically significant and well-behaved.  
> `Frequency_BoxCox` and `Cluster_1` are the key drivers of the target variable.  
> Residuals show independence and approximate normality.  
> The model is stable and interpretable.


## Project Continuation  

The following steps will be implemented in the continuation of this project:  
  
- Improving the Model    
- Visualization and Reporting  

## How to Use

Clone this repository and navigate to the project directory:

1. Clone the repository:
   ```bash
   git clone https://github.com/Ehsan-Behzadi/Online-Retail-Data-Analysis-and-Preprocessing.git  
   cd Online-Retail-Data-Analysis-and-Preprocessing
   ```
Next, open the Jupyter Notebook file (usually with a .ipynb extension) using Jupyter Notebook.   

2. To start Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
