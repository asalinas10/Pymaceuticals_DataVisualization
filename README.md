# Pymaceuticals DataVisualization

I've been given access to the complete data from a pharmaceutical company's most recent animal study. In this study, 249 mice who were identified with SCC tumors received treatment with a range of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals’ drug of interest, Capomulin, against the other treatment regimens.

I've been tasked with generating all of the tables and figures needed using Python and Matplotlib for the technical report of the clinical study and a summary of the study results.

# Summary

This assignment is broken down into the following tasks:

    - Prepare the data.

    - Generate summary statistics.

    - Create bar charts and pie charts.

    - Calculate quartiles, find outliers, and create a box plot.

    - Create a line plot and a scatter plot.

    - Calculate correlation and regression.

    - Submit your final analysis.

1. Prepare the Data

    - Run the provided package dependency and data imports, and then merge the mouse_metadata and study_results DataFrames into a single DataFrame.

    - Display the number of unique mice IDs in the data, and then check for any mouse ID with duplicate time points. Display the data associated with that mouse ID, and then create a new DataFrame where this data is removed. Use this cleaned DataFrame for the remaining steps.

    - Display the updated number of unique mice IDs.

![Alt text](<Screen Shot 2024-01-03 at 9.27.36 PM.png>)

2. Generate Summary Statistics

    - Create a DataFrame of summary statistics. Remember, there is more than one method to produce the results you're after, so the method you use is less important than the result.

    - Your summary statistics should include:

        - A row for each drug regimen. These regimen names should be contained in the index column.

        - A column for each of the following statistics: mean, median, variance, standard deviation, and SEM of the tumor volume.

![Alt text](<Screen Shot 2024-01-03 at 9.57.39 PM.png>)

3. Create Bar Charts and Pie Charts

    - Generate two bar charts. Both charts should be identical and show the total total number of rows (Mouse ID/Timepoints) for each drug regimen throughout the study.

        - Create the first bar chart with the Pandas DataFrame.plot() method.

        - Create the second bar chart with Matplotlib's pyplot methods.

    - Generate two pie charts. Both charts should be identical and show the distribution of female versus male mice in the study.

        - Create the first pie chart with the Pandas DataFrame.plot() method.

        - Create the second pie chart with Matplotlib's pyplot methods.

![Alt text](<Screen Shot 2024-01-03 at 9.31.55 PM.png>)

![Alt text](<Screen Shot 2024-01-03 at 9.32.22 PM.png>)

4. Calculate Quartiles, Find Outliers, and Create a Box Plot

    - Calculate the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Then, calculate the quartiles and IQR, and determine if there are any potential outliers across all four treatment regimens. Use the following substeps:

        - Create a grouped DataFrame that shows the last (greatest) time point for each mouse. Merge this grouped DataFrame with the original cleaned DataFrame.

        - Create a list that holds the treatment names as well as a second, empty list to hold the tumor volume data.

        - Loop through each drug in the treatment list, locating the rows in the merged DataFrame that correspond to each treatment. Append the resulting final tumor volumes for each drug to the empty list.

        - Determine outliers by using the upper and lower bounds, and then print the results.

    - Using Matplotlib, generate a box plot that shows the distribution of the final tumor volume for all the mice in each treatment group. Highlight any potential outliers in the plot by changing their color and style.

![Alt text](<Screen Shot 2024-01-03 at 9.34.38 PM.png>)

5. Create a Line Plot and a Scatter Plot

    - Select a single mouse that was treated with Capomulin, and generate a line plot of tumor volume versus time point for that mouse.

    - Generate a scatter plot of mouse weight versus average observed tumor volume for the entire Capomulin treatment regimen.

![Alt text](<Screen Shot 2024-01-03 at 9.35.39 PM.png>)

![Alt text](<Screen Shot 2024-01-03 at 9.49.25 PM.png>)

6. Calculate Correlation and Regression

    - Calculate the correlation coefficient and linear regression model between mouse weight and average observed tumor volume for the entire Capomulin treatment regimen.

    - Plot the linear regression model on top of the previous scatter plot.

![Alt text](<Screen Shot 2024-01-03 at 9.55.08 PM.png>)





