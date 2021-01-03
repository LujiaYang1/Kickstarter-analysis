# An analysis of Kickstarter Campaigns

## Overview of Project
Louise’s play Fever came close to its fundraising goal in a short amount of time, and she would like to gain more knowledge about the major factors that would alter the campaign outcomes. This report analyzes how the outcomes of Kickstarter Campaigns (in category of theator) differ in relation to Launch Date and Campaigns Goals based on the data that is given in the kickstarterBook.
### Purpose
To make Louise understand how the major two factors could affact the her potential achievement in the crowdfunding, and give her advise on determaining the optimal launch date and goal levels that would help her succeed in her campaign. 
## Analysis and Challenges
A variety of Excel functions (including sorting, filtering, Vlookup, pivoting and etc.) were adopted to perform the analysis. Pivot charts were also utilized as usualizations to help us better understand the relationships between the variables.

### Analysis of Outcomes Based on Launch Date
In order to find out how the campaign turned out based on the launch date during the year from 2010 to 2017, we would like to combine the outcomes for all years and divide them according to the month of their launch date. Firstly, I added a column on the excel sheet and use `year()`function to exact the year from the "Date Created Conversion" column which was created earlier. Once I get the "years" for all campaigns, I can create a pivot table in a new sheet named "Theater Outcome by Launch Date". When creating the pivot table, I placed the "Date Created Conversion" in the rows, "Outcomes in the rows" in columns, "Count of outcomes" in the value and chose "years" and "Parent Category" as the filters.(shown below)

<img src="Resources/Theater_Outcomes_vs_Launch_Pivot_Capture.png" width= "500">

I filtered the "parent category" to only show the outcomes for Theatre campaigns and filtered "outcomes" to only show the completed campaigns (eliminating "live"). After those steps, I get a pivot table that looks like the following: 

<img src="Resources/Theater_Outcomes_vs_Launch%20table.png" width= "500">

According to the above pivot table, I created a line chart (shown below) using the "pivot chart" function to illustrate the trend of the outcomes in different months of a year.

<img src="Resources/Theater_Outcomes_vs_Launch.png" width= "500">


### Analysis of Outcomes Based on Goals

### Challenges and Difficulties Encountered

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

- What can you conclude about the Outcomes based on Goals?

- What are some limitations of this dataset?

- What are some other possible tables and/or graphs that we could create?
