# An Analysis of Kickstarter Campaigns
# Kickstarting with Excel

## Overview of Project
An up-an-coming play write named Louise, has started a crowdfunding campaign to help fund her new play, Fever. Louise had an initial goal of $10,000 and almost reached this goal in a very short period of time through her crowdfunding campaign. She has reached out to learn more information about the outcomes of other campaigns when looking at their start date and funding goals. 
### Purpose

## Analysis and Challenges
### Analysis of Outcomes Based on Launch Date
Louise is interested in learning about the outcomes of other campaigns based on the starting date. The best way to look at this data is using a pivot table and then creating a chart from there. The pivot table needs to show a count of the successful, failed, and canceled outcomes for each month of the year. When the table is first created, the data is filtered by year instead of showing the outcomes filtered by month. The first challenge is to determine how to correctly filter the data. The best way to fix this is to highlight the years in the first column, right click, and select ‘Group’. From the new pop-up window, different filtering options are available. The best option for this analysis is months. This should now show the data filtered by months in the first column instead of years. From here, a quick line graph can be created from the pivot table that will show the months along the x-axis and the count along the y-axis. This graph is labeled Theater_Outcomes_vs_Launch.png and is attached in the resources folder along with this file. 
### Analysis of Outcomes Based on Goals
Louise is not only interested in the time of year that similar projects originated, but also the outcomes of these projects based on the size of the goal they are trying to reach. To find, simplify, and view this information, a count of the campaigns filtered in $5000 increments is pulled into a new sheet in excel. The Countifs function in excel is used to filter on the outcomes column, the goals column using the $5000 increments created in the new sheet, and the subcategory column filtered by ‘plays’. An example of the code is listed below. 
=COUNTIFS(Kickstarter!$D:$D, "<1000", Kickstarter!$F:$F, "Canceled", Kickstarter!$R:$R, "plays")
To make the data easier to understand, new columns were created at the end of this new sheet to show the percent completed, the percent failed, and the percent cancelled. Percentages are an easy way to get an idea of the changes in the data versus looking at the raw figures. 
With the creation of these percentage columns, a line graph can be created that shows the outcomes based on the goal with percentages on the y-axis and the dollar increments on the x-axis. This graph is  titles Outcomes_vs_Goals.png and is also located in the attached resources folder 
### Challenges and Difficulties Encountered

## Results
- What are two conclusions you can draw about the Outcomes based on Launch Date?
The graph labeled Theater_Outcomes_vs_Launch makes it easy to see that campaigns that began in the spring and summer months had a higher chance of succeeding than those campaigns that were initiated in the winter months, with May being the most successful month of the year. The worst month to start a crowdfunding campaign would be in December where nearly the same number of campaigns failed as were successful. The canceled field was added for more information, but with so few campaigns being canceled, this information could have been left off to help simplify the graph. 
- What can you conclude about the Outcomes based on Goals?
A quick conclusion about the Outcomes_vs_Goals graph is that none of the play campaigns were canceled. If they were started, they saw it through to either success or failure. For Louise’s case, she has about a 50/50 chance of success or failure. For campaigns around $10,000 almost as many campaigns fail as succeed. Outside of the price range from $35,000-$45,000, the higher the goal value, the smaller chance of success. 
- What are some limitations of this dataset?
You don’t know how quickly a campaign was funded. Was a large amount pledged on the final day of the campaign? It is also hard to determine if one large donor pledged all the money and if that was a corporate sponsor or not. 
- What are some other possible tables and/or graphs that we could create?
Other information from the dataset could be helpful for Louise as she looks to complete her campaign. 
-	Look at the average donation given by dividing the pledged value by the number of backers. 4You can find out if a play was successful with a $10,000 budget because 3 people funded the entire campaign or if 500 people helped fund the campaign. An example is TREKKAYAK was a successful campaign that raised over $82,000 from just 33 backers. Each backer pledging on average, $2500. Very high amount of money pledged per backer. 
-	It might also be helpful to look at the number of days the campaign was open. This can be done by subtracting the created date from the end date in excel to get the number of days the campaign was open. Then the campaigns can be compared to the campaign that Louise is running since she is almost fully funded in a short amount of time. The average amount pledged per day can also be determined by dividing the pledged amount by the number of days. 

