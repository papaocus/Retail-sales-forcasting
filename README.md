# Retail-sales-forcasting

Importing Required Libraries:

pandas is imported as pd for data manipulation and analysis.
numpy is imported as np for numerical operations.
matplotlib.pyplot is imported as plt for data visualization.
Loading Data:

Three CSV files, namely 'Features data set.csv', 'stores data-set.csv', and 'sales data-set.csv', are loaded into DataFrames named features, stores, and sales, respectively.
Date Parsing:

The 'Date' columns in both the features and sales DataFrames are converted to datetime format using pd.to_datetime() function. However, there are UserWarnings indicating that the dates might not be consistently parsed.
Printing DataFrame Shapes:

The shapes of the three DataFrames (features, sales, and stores) are printed using the shape attribute.
Printing Date Range:

The first and last dates in the 'Date' column of the sales and features DataFrames are printed.
Merging DataFrames:

The sales, features, and stores DataFrames are merged using the pd.merge() function, first on the columns ['Store', 'Date', 'IsHoliday'], and then on the 'Store' column.
Handling Missing Values:

The merged DataFrame (df) is filled with 0 for any missing values using df.fillna(0).
Data Preprocessing:

The 'Temperature' column in the DataFrame is converted from Fahrenheit to Celsius.
The 'Type' column is encoded using factorize() function to convert categorical values to numerical labels.
Displaying DataFrame:

The first few rows of the DataFrame are displayed using df.head().
Checking for Duplicates:

The number of duplicated rows in the DataFrame is calculated using df.duplicated().sum().
Descriptive Statistics:

Summary statistics of the numerical columns in the DataFrame are displayed using df.describe().
Creating Tabular Information:

A DataFrame named tab_info is created to store column information, including column type, number of null values, and percentage of null values.
Data Visualization:

Several visualizations are created using the plot() function from matplotlib.pyplot to show trends in specific columns of the DataFrame.
Analyzing Average Sales:

A new DataFrame (df_average_sales_week) is created by grouping the data by 'Date' and summing the 'Weekly_Sales' column.
The DataFrame is sorted in descending order of 'Weekly_Sales'.
A line plot is created to visualize the weekly sales trend over time.
Analyzing Top Sales:

The DataFrame (df_average_sales) is reversed to display the top sales dates.
The top sales dates are printed using df_average_sales[::-1].head().
Time Series Analysis:

The 'Date' column is set as the index for the df_average_sales_week DataFrame.
Autocorrelation and partial autocorrelation plots are created using plot_acf() and plot_pacf() from statsmodels.graphics.tsaplots.
Analyzing Top Stores:

Two DataFrames (df_top_stores) are created to group the data by 'Type' and 'Store' and sum the 'Weekly_Sales' column.
The DataFrames are sorted in descending order of 'Weekly_Sales'.
