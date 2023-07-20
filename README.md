# matplotlib-challenge

After the step of learning how to use Pandas to display our data in well organised dataframes matching with our needs.
In this project we will learn how we can use other libraries to include statistics summary and to draw charts and plots for a  better reading and better analyze: 💹

In this project, a new pharmaceutical company that specializes in anti-cancer medications. Recently, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer. In this study, 249 mice who were identified with SCC tumors received treatment with a range of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals’ drug of interest, Capomulin, against the other treatment regimens.
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

- Look for the number of unique mice  in the data, and  check for any  duplication of the identifyer (our data is identified by Mouse ID and Timepoint). Clean the DataFrame of the duplicate rows.

2. Generate Summary Statistics
   
- Create a DataFrame of summary statistics including:  mean, median, variance, standard deviation, and SEM of the tumor volume.

3. Create Bar Charts and Pie Charts
   
- Generate two bar charts showing the total number of rows (Mouse ID/Timepoints) for each drug regimen throughout the study.Use the Pandas DataFrame.plot() method and  Matplotlib's pyplot methods.

- Generate two pie chart showing the distribution of female versus male mice in the study. Use the Pandas DataFrame.plot() method and  Matplotlib's pyplot methods. 

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

- Matplotlib.pyplot:  Matplotlib has a module named pyplot which makes things easy for plotting by providing feature to control line styles, font properties, formatting axes etc. Matplotlib is a python library used to create 2D graphs and plots by using python scripts.

- scipy.stats: it is a module contains a large number of probability distributions.

- Jupyter Notebook: it is a web-based interactive computing pltaform, allows the user to compile all aspects of a data project.




Python script using Pandas:
Example with grouping by a criteria
#Calculate the total student count per school
per_school_counts =pd.DataFrame({'Total Students':school_data_complete.groupby(['school_name'])['Student ID'].count()})
per_school_counts
groupby

Example with filtring:
#Calculate the number of students per school with reading scores of 70 or higher
students_passing_reading = school_data_complete[(school_data_complete["reading_score"] >= 70)]
school_students_passing_reading =pd.DataFrame ({'reading scores of 70 or higher':students_passing_reading.groupby('school_name')['reading_score'].size()})        school_students_passing_reading
filtring

Example with Sorting:
#Sort the schools by `% Overall Passing` in ascending order and display the top 5 rows.
bottom_schools = per_school_summary.sort_values('% Overall Passing',ascending=True)
top_schools["Total students"] = top_schools["Total Students"].map("${:,.0f}".format)
bottom_schools.head(5) 
sorting

Example with benning:
#Establish the bins 
spending_bins = [0, 585, 630, 645, 680]
la = ["<$585", "$585-630", "$630-645", "$645-680"]

#Create a copy of the school summary  
school_spending_df = per_school_summary.copy()

#Categorize spending based on the bins
school_spending_df['Per Student Budget']=school_budget_capita['per school capita']
school_spending_df["Spending Ranges (Per Student)"] = pd.cut(school_spending_df['Per Student Budget'],
                                                     spending_bins, labels=la,include_lowest = True)
school_spending_df
binning

Tip:🪄
Take advantage of the first module, export dataframes to Excel and insert charts or filters to make the analyzis easier. The following is an example of a code to export a dataframe to an Excel spreadsheet:

with pd.ExcelWriter('panda.xlsx')as writer:
    type_summary.to_excel(writer,sheet_name='Sheet_1')
  image
