# matplotlib-challenge

In the previous project, we learned how to use Pandas to display our data in well organized dataframes matching our needs.
In this project we will learn how we can use other libraries to include a statistics summary and to draw charts and plots for better reading and analysis: 📊

In this project, we will study a new pharmaceutical company that specializes in anti-cancer medications. Recently, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer. In this study, 249 mice that were identified with SCC tumors received treatment with a range of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals’ drug of interest, Capomulin, with the other treatment regimens.
What we will learn from this project:

- How to generate a Summary Statistics: Mean,	Median, Variance, Standard deviation and Standard error.

- How to generate Bar and Pie Charts using Pandas and pyplot
  
- How to calculate Quartiles, Find Outliers, and Create a Box Plot

- How to generate a line plot

- How to generate a scatter plot

- How to calculate the correlation coefficient and a linear regression model 

Instructions:

Prepare the data.

Generate summary statistics.

Create bar charts and pie charts.

Calculate quartiles, find outliers, and create a box plot.

Create a line plot and a scatter plot.

Calculate correlation and regression.

All this information will be used for a subsequent deeper analysis

1. Prepare the Data
   
- Merge our datasets into a single DataFrame.

- Look for the number of unique mice in the data, and check for any duplication of the identifyer (our data is identified by Mouse ID and Timepoint). Clear the DataFrame of the duplicate rows.

2. Generate Summary Statistics
   
- Create a DataFrame of summary statistics including:  mean, median, variance, standard deviation, and SEM of the tumor volume.

3. Create Bar Charts and Pie Charts
   
- Generate two bar charts showing the total number of rows (Mouse ID/Timepoints) for each drug regimen throughout the study.Use the Pandas DataFrame.plot() method and Matplotlib's pyplot methods.

- Generate two pie charts showing the distribution of female versus male mice in the study. Use the Pandas DataFrame.plot() method and  Matplotlib's pyplot methods. 

4. Calculate Quartiles, Find Outliers, and Create a Box Plot
   
- Calculate the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Then, calculate the quartiles and IQR, and determine if there are any potential outliers across all four treatment regimens. 

- Using Matplotlib, generate a box plot that shows the distribution of the final tumor volume for all the mice in each treatment group. Highlight any potential outliers in the plot.

5. Create a Line Plot and a Scatter Plot
   
- Select a single mouse that was treated with Capomulin, and generate a line plot of tumor volume versus time point for that mouse.

- Generate a scatter plot of mouse weight versus average observed tumor volume for the entire Capomulin treatment regimen.

6. Calculate Correlation and Regression
   
- Calculate the correlation coefficient and linear regression model between mouse weight and average observed tumor volume for the entire Capomulin treatment regimen.

- Plot the linear regression model on top of the previous scatter plot.

Program:

Tools:

- Pandas: it is a Python library for data manipulation and analysis

- Matplotlib.pyplot:  Matplotlib has a module named pyplot which makes things easy for plotting by providing features to control line styles, font properties, formatting axes etc. Matplotlib is a python library used to create 2D graphs and plots by using python scripts.

- scipy.stats: it is a module that contains a large number of probability distributions.

- Jupyter Notebook: it is a web-based interactive computing platform that allows the user to compile all aspects of a data project.

Code to generate charts using pyplot methods
## Bar Charts
## Pie Chart
## Boxplots
## Line Plot
## Scatter Plots

Tip:🪄
For a better analysis, generate lines plot of tumor volume vs. time point for more than one mouse treated with Capomulin
