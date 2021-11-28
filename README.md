# **Kickstarting with Excel**
	
## **Overview of Project** 
* Louise wants to start a crowdfunding campaign to fund her play “Fever”. Her estimated budget is over $10,000. By analyzing, organizing, and visualizing the crowdfunding data, we will be able to help her plan her campaign and determine whether there are specific factors that make the campaign successful.
 
### Purpose 
 
* Analyze and visualize campaign outcomes (successful, failed and cancelled) based on their lunch dates and their funding goals.As well to creat a summay report based on the analysis and visualizations.

## **Analysis and Challenges** 
 
### Analysis of Outcomes Based on Launch Date 
![Theater Outcomes Based on Launch](C:/Users/Ruth/OneDrive/Desktop/HW1_Submission_Excel/HW1_Submission_Excel/Resources/Theater_Outcomes_vs_Launch.png) 
 
* We can see from the chart (blue line) that the total number of Successful campaigns are high in the month of May, June and July. 

* The total number of successful campaigns is declining from October to December. 
 
### Analysis of Outcomes Based on Goals 

![Outcomes_vs_Goals](C:/Users/Ruth/OneDrive/Desktop/HW1_Submission_Excel/HW1_Submission_Excel/Resources/Outcomes_vs_Goals.png) 
 
* We can see from the chart that percentage successful is highest (76%) when Goals are <1000, followed by (73%) When Goals are between 1000 and 5000. This percentage successful is relative to number failed for each row. We can see from the table on `Outcomes Based on Goals` worksheet that total number of successful campaigns are highest(388) when goals are between 1000 and 5000.

* Also the higher the Goal the lower the percentage Successful and the higher the percentage Fail. 

### Challenges and Difficulties Encountered 

* For the Analysis of Outcomes based on Goals, useed COUNTIFS()function to populate the Number Successful, Number Failed and Number Canceled columns on Outcomes Based on Goals worksheet. If you set filter on Subcategory to plays on the Kickstarter data and then do COUNTIFS()formula like this `=COUNTIFS(Kickstarter!D:D,"<1000",Kickstarter!F:F,"=successful")` with out putting criteria for the Subcategory plays, the total number of successful Outcomes for < 1000 goal is 322 different from total number of outcomes populated when plays filter on Subcategory is in the formula `=COUNTIFS(Kickstarter!R:R,"=plays",Kickstarter!D:D,"<1000",Kickstarter!F:F,"=successful")`. So to get the correct total number of outcomes for Successful, Fail and Cancel Columns, all filters must be part of the COUNTIFS() formula on the Outcomes Based on Goals worksheet. Do not set filters on Kickstarter worksheet.


## **Results** 

- What are two conclusions you can draw about the Outcomes based on Launch Date? 

* The Month of May has most success rate in theater category Pick periods for successful campaigns in theater category are in the summer season (MAY, JUNE and JULY) correlating with school closures and family vacations
* Campaigns are less successful towards the end of the year October to December in Theater Category 

- What can you conclude about the Outcomes based on Goals?

* We can conclude that the most successful campaigns have Goals less than $5000, Louise has a goal of over $10000 which is twice of the successful goals. Louse should revise her goal.

- What are some limitations of this dataset?

* There is no data for the backers. This will would have helped with targeting the population 
* We do not have data for location of specific cities where the campains are performed. This would have helped to identify specific cities where the campaigns are successful.

- What are some other possible tables and/or graphs that we could create? 

* Can create a pie chart for Analysis of Outcomes based on Launch dates. Chart is on Kickstarter_Challenge file on Outcomes based on Goals worksheet

* Can create a bar chart for Analysis of Outcomes based on Goals.Chart is on Kickstarter_Challenge file on Outcomes based on Goals worksheet

* For Analysis of Outcomes based on Goals, we can create table for the for Successful, Fail and Cancel columns using statistical calculations. On Kickstarter sheet, set filter to Plays on the Subcategory column and to successful on the Outcome column. Copy the data and paste into a different sheet1. Then Create four columns on separate sheet as in `Descriptive Statistics` sheet. Then calculate the mean, median, Standard deviation, Lower Quartile, Upper Quartile and IQR based on goal column of sheet1 and populate `Successful` column. Repeat steps for `Fail` and `Cancel` columns. We can see the spread of the data from the mean and standard deviation. We can also identify outliers using mean and IQR data `(Upper Quartile+(1.5 X IQR) and Lower Quartile-(1.5 X IQR))`. 
* Can also create statistical chart for the analysis of the Outcomes based on Goals which can help identify the spread of data and outliers. Clear all filters on Kickstarter worksheet and set filter for Subcategory to plays and for outcomes column to Successful. Then Select Goal column and create the Box and Whisker chart. We can see from the graph mean, median, Upper quartile, lower quartile and highest data points within the upper quartile plus `(1.5 X IQR)`. All the data points above the top line `(Upper quartile plus (1.5 X IQR))` in the chart are outliers that is goals > $9500.Chart is on Kickstarter_Challenge file on Box and Whisker plot worksheet.



