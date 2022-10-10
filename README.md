# Kickstarting with Excel

## Overview of Project

### Purpose

The purpose of this analysis is using Excel to organize, sort, and analyze data for each project to help Louise to have a better understanding of each project from start to finish and determine whether there are specific factors that make a project's campaign successful. Specifically, in this Challenge, perform data visualization to help Louise to know how different campaigns fared in relation to their launch dates and their funding goals by visualizing campaign outcomes based on the launch dates and funding goals.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

* Select all data listed in the spreadsheet to create a pivot table by choosing "Outcomes" in "Columns", "Date Created Conversion" grouping by "Month" in "Rows" to show the months of the year, "Count of outcomes in "Values" to show the total number in each outcomes, then filtering the column labels to show only "successful", "failed" and "canceled". Filter the pivot table based on "Parent Category" and "Years".Then filter the "Parent Category" to show only the data for "Theater" so we can perform a data analysis and find the result located in "Theater" Category. Sort the campaign outcomes in descending order so "successful" is first.

* Click anywhere on the pivot table to bring up the PivotTable Analyze tab, and then click the PivotChart button in it. Click on the chart and then click the Design tab on the toolbar to change chart type and choose a line chart to visualize the relationship between outcomes and launch month, which may show the result clearer and more straightforward. Click Add Chart Element on the left side of the toolbar on Design tab to the add chart title as "Theater Outcomes Based on Launch Date" to make the chart easily understand.

* Select the chart by clicking anywhere on it and then right-click and select "Save as Picture" to save the line chart as an image named as Theater_Outcomes_vs_Launch.png.


### Analysis of Outcomes Based on Goals

* Create a new sheet named as "Outcomes Based on Goals" with the following statistics:
  * Goal
  * Number Successful
  * Number Failed
  * Number Canceled
  * Total Projects
  * Percentage Successful
  * Percentage Failed
  * Percentage Canceled

* In the "Goal" column to create the dollar-amount ranges so projects can be grouped based on their goal amount.

* Use `COUNTIFS()` function to populate the "Number Successful," "Number Failed," and "Number Canceled" columns by filtering on the Kickstarter "outcome" column, on the "goal" amount column using the ranges created in above, and on the "Subcategory" column using "plays" as the criteria so that we can perform a data analysis and find the result located in "plays" Subcategory.

* Use `SUM()` function to populate the "Total projects" and calculate the percentage of successful, failed and canceled projects for each "goal"amount range.

* Select "Goal" , "Percentage Successful", " Percentage Failed" and " Percentage Canceled" column as the dataset to create a line chart titled "Outcomes Based on Goal" to visualize the relationship between the goal-amount ranges on the x-axis and the percentage of successful, failed, or canceled projects on the y-axis.

* Select the chart by clicking anywhere on it and then right-click and select "Save as Picture" to save the line chart as an image.

### Challenges and Difficulties Encountered

The Challenge I met is how to use `COUNTIFS()` function to calculate the correct number. So I chose to use the hint to watch the video for a detailed overview of how to use `COUNTIFS()` function to have a better understanding of the syntax of this function, which can be listed as bellow:

  * criteria_range1 which is required. The first range in which to evaluate the associated criteria.

  * criteria1 which is required. The criteria in the form of a number, expression, cell reference, or text that define which cells will be counted.

  * criteria_range2, criteria2, which are optional. Up to 127 range/criteria pairs are allowed.

## Results

### What are two conclusions you can draw about the Outcomes based on Launch Date?

* According to the pivot table and line chart created, we can find that:

  1. For "Theater" category, the number of successful projects is the highest and the number of canceled projects is the lowest in every single month. Based on the line chart created, the number of canceled projects in each month is relatively low and the trend is relatively smooth compared to the trend of successful and failed projects. There is even no canceled project when the Launch date is in October.

  2. There are 166 projects in theater category launched in May, of which 111 projects are successful. The successful rate is around 67% which is also the highest compared to other 11 months. The total number of projects launched and succeeded are the highest in May during the whole year. There are only 75 projects launched in December with 37 projects successful. The total number of projects launched and succeeded are lowest in December during the whole year. The successful rate is around 49% which is also lowest compared to other 11 months.

### What can you conclude about the Outcomes based on Goals?

* According to the new sheet and line chart created, we can find that for "Play" subcategory, there are 534 projects having the goal of 1000 to 4999, which means that each of these 543 projects will need 1000 to 4999 to succeed. The amount range (1000 to 4999) of the goal has highest total number of projects compared to others. The successful rate is 76% with the goal less than 1000, which is the highest successful rate compared to other goals. When the goal is 45000 to 49999, the failed rate is 100%, which is the highest one. There are no trends for the successful rate and failed rate based on goals for "Play" subcategory.

### What are some limitations of this dataset?

* The dataset appears to be too concentrated in some specific years as around 78% projects were launched in 2014, 2015 and 2016, and only 22% were launched in other years, which may have a better analysis and more accurate result if the data would be distributed more evenly in different years.

* The dataset appears to have too small number of total projects in specific categories such as journalism which only includes 24 projects so that the analysis may not evaluate the outcomes accurately based on such small database.

### What are some other possible tables and/or graphs that we could create?

* We can create a table and/or graph for projects in general ( all categories) or specific categories such as theater based on different country to find in which country the projects are most likely to be successful.

* We can also create the tables and/or graphs for projects in general ( all categories) or specific categories such as theater based on different deadline.
