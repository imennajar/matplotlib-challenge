# matplotlib-challenge
in this project













pandas-challenge
After the step of lerning how to use Pandas to display our data in dataframes well organised with our needs, in this project we will learn how we can use other libraries to include statistics summary and to drow charts and plots for a  better reading and better analyze: 💿
In this project we will analyze a city's future school budgets and priorities. This we will start by analyzing the district-wide standardized test results, and then we will aggregate the data to showcase obvious trends in school performance using available information on the school.

What we will learn from this project:

- How to create Summary Statistics: Mean,	Median, Variance, Standard deviation and Standard error.

- How to perform the necessary calculations and create a high-level snapshot of the key metrics

- How to filter, merge, sort, group and bin to enable more vigorous dataset customization

- How to analyze the output Data to make the right decisions
Instructions:
District Summary: Performing the necessary calculations and creating a high-level snapshot of the district's key metrics:

- Total number of schools

- Total students

- Total budget

- Average test scores (Math and Reading)

- Passing rates (Math, Reading and both)
All this information will be used for a subsequent deeper analysis

School Summary: Performing the necessary calculations and summarizing key metrics about each school:

 - Total student count per school

 - Total school budget and per capita spending per school

 - Average test scores per school (Math and Reading)

 - Passing rates (Math, Reading and both)

 - Associate all this information with the name and the type of each school
Sorting the information to organize and analyze data in a more efficient and meaningful way:

- Sort the schools by the percentage of Overall Passing to analyze the Highest-Performing Schools and the Lowest-Performing Schools 
Placing values into groups to enable more vigorous dataset customization:

 - Scores by Grade: for students of each grade level (9th, 10th, 11th, 12th) at each school

 - Scores by School Spending: average spending ranges (per student)

 - Scores by School Size:  school performance based on school size (small, medium, or large)

 - Scores by School Type: school performance based on the type of the school
Analyzing and make conclusions for batter decisions

Program:
Tools:
Pandas, which is a Python library for data manipulation and analysis

Jupyter Notebook, a web-based interactive computing pltaform, allows the user to compile all aspects of a data project.

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
