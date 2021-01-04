# An analysis of Kickstarter Campaigns

## Overview of Project
Louise’s play Fever came close to its fundraising goal in a short amount of time, and she would like to gain more knowledge about the major factors that would alter the campaign outcomes. This report analyzes how the outcomes of Kickstarter Campaigns (in category of theator) differ in relation to Launch Date and Campaigns Goals based on the data that is given in the kickstarterBook.
### Purpose
To make Louise understand how the major two factors could affact the her potential achievement in the crowdfunding, and give her advise on determaining the optimal launch date and goal levels that would help her succeed in her campaign. 
## Analysis and Challenges
A variety of Excel functions (including sorting, filtering, Vlookup, pivoting and etc.) were adopted to perform the analysis. Pivot charts were also utilized as usualizations to help us better understand the relationships between the variables. All the procedure related to the analysis are performed in the Excel file: [kickstarter_challenge,xlsx](Kickstarter_Challenge.xlsx)

### Analysis of Outcomes Based on Launch Date
To find out how the campaign turned out based on the launch date during the year from 2009 to 2017, we would like to combine the outcomes for all years and divide them according to the month of their launch date. Firstly, I added a column on the excel sheet and use `year()`function to exact the year from the "Date Created Conversion" column which was created earlier. Once I get the "years" for all campaigns, I can create a pivot table in a new sheet named "Theater Outcome by Launch Date". When creating the pivot table, I placed the "Date Created Conversion" in the rows, "Outcomes in the rows" in columns, "Count of outcomes" in the value and chose "years" and "Parent Category" as the filters.(shown below)

<img src="Resources/Theater_Outcomes_vs_Launch_Pivot_Capture.png" width= "500">

I filtered the "parent category" to only show the outcomes for Theatre campaigns and filtered "outcomes" to only show the completed campaigns (eliminating "live"). After those steps, I get a pivot table that looks like the following: 

<img src="Resources/Theater_Outcomes_vs_Launch%20table.png" width= "500">

According to the above pivot table, I created a line chart (shown below) using the "pivot chart" function to illustrate the trend of the outcomes with launch dates in different months of a year.

<img src="Resources/Theater_Outcomes_vs_Launch.png" width= "500">


### Analysis of Outcomes Based on Goals
To find out the relationship between the outcomes and the goals, we need to divide the goals into different ranges according to its dollar value. When we take a look at the data, we see that most of the goals were between $1000 to $50,000. Therefore, we use $1000 as the lower bond and $50000 as the higher bond, and all the values in the middle are equally divided into 10 range groups, with $5000 for each interval. Then I use the `countif()`function to collect the numbers of different outcomes (successful, failed and canceled) for different goal ranges in the subacategory of "plays". I also calculated the percentages of different outcomes for each goal range, After that, we get a new table shown below:

<img src="Resources/Outcomes_vs_Goals_table.PNG" width= "800">

After I have all the relevant data put together in one table, I created a Pivot table. I selected goals in the rows and average percentages different outcomes (succesful, failed and canceled) in the columns.(Because we only get one value for each outcome in each goal range, it doesn't matter if we select "sum" or "average", it will just show the original percentage.) Finally, I created the pivot chart (shown below) to demonstrate the trend of the outcomes within different goal ranges.

<img src="Resources/Outcomes_vs_Goals.png" width= "500">

### Challenges and Difficulties Encountered
One challenge I encountered when working with the data was that sometimes I forget to clear the filters before I go on to a new data search. This might lead to data missing and will alter the result for my analysis. When I got confused or unsure about my data sets, I tried to cross check my results with the previous work I have done. For example, I double checked my total numbers of successful, failed and canceled cases within the subcategory of "plays" on the previous pivot table called "Subcategory Statistics" I created during the module study (shown below). I filtered the the subcategory to diplay "plays" only and compared the total numbers I got in the two tables to make sure my numbers are consistent.

<img src="Resources/Subcategory_Statistics.png" width= "500">


## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
1.May seemed to be the best month for the launch time as it gives the biggest number of successful cases (the peak) which exceeds the number of failed cases by the most(almost twice as failed cases) throughout the year.
2.December seemed to be the worst month for the launch time as it gives the lowest number of successful cases which became equal to the number of failed cases, meaning that the percentage of being successful is as low as 50%.
(Both conclusions are made given that the numbers of canceled cases stay relatively minimal and consistant throughout the year, so that we don't take consideration of it when camparing the numbers of successful and failed cases.)

- What can you conclude about the Outcomes based on Goals?
Goals fall in the two ranges seemed to give a higher percentage (greater than 50%) of success: 1) lower than $5000; with 72-75% of being successful. 2)between $35,000 and $45,000; with 67% of being successful. 

- What are some limitations of this dataset?
1) The dataset only contains 9 years of data (from 2009 to 2017). It might not be enough for us to come up with meaningful conclusion.
2) More explanatory variables should be included for people to better understand how the campaign succeeded. For example 1)who are the initiators of the campaign? Any celebraty or special people envolved? 2) What are the demogaphics of the donors? Different people donate for different purposes? 3) What are the channels for people to donate? Does the use of different on-line platforms affact the result?

- What are some other possible tables and/or graphs that we could create?
We can also create a new variable called "time span", which is a measure of how many months each campaign lasted,and creat a line chart filtered with successful cases in the category of "plays" to show among the successful campaigns, how long did they usually take. This way, we can help Louis to better plan her campaign for the time span.
