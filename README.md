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

## Project Continuation  

The following steps will be implemented in the continuation of this project:  

- Feature Engineering    
- Segmentation and Clustering  
- Machine Learning Models  
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
