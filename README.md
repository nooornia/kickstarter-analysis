# Kickstarting with Excel 
##  Overview of Project
The purpose of this project is to analyze the data of Kickstarter campaigns to determine what factors influence the success of a Kickstarter campaign. My client is a playwright who needs to break down what results in a successful Kickstarter campaign, so the data I analyzed focused specifically on theater campaigns, as well as the potential to narrow the data down further to the subcategory of plays. I analyzed the outcomes of theater campaigns based on two separate criteria: their launch date and their goal amount. By analyzing the results of this data, I can paint a picture of what a successful theater campaign looks like and assist my client in setting up her own Kickstarter campaign. 
## Analysis of Outcomes Based on Launch Date 
In order to analyze the outcome data of Kickstarter campaigns based on their launch dates, I created a pivot table filtered by the category of “theater” which contained data for successful, failed, and canceled Kickstarter campaigns. I sorted each outcome into categories based on the month they were launched in. Out of a total of 1369 theater campaigns, 839 were successful, 493 failed, and 37 were canceled. Using the pivot table, I then created a line chart to visually analyze the trends of the data. 

![Resources/Theater_Outcomes_vs_Launch.png] (/assets/images/Theater_Outcomes_vs_Launch.png)

The line chart shows us the trends in the data based on the launch date of the campaigns, broken down into the three outcome categories. From this chart, we can see successful campaigns at a peak of 111 in May, failed campaigns at a peak of 52 in May, and canceled campaigns at a peak of 7 in January. Failed campaigns have a secondary peak of 50 in October.
## Analysis of Outcomes Based on Goals 
To analyze the outcome data of Kickstarter campaigns based on their goals, I created a table to categorize the goal amounts into ranges of about $5,000, starting with goals that were less than $1,000 and progressing to goals greater than $50,000. I broke down each range into successful, failed, and canceled projects by using the COUNTIFS formula to calculate the number of campaigns from the original data that fit both the outcome category and the goal range. For example, for the range of $1,000 to $4,999, my code looked like: 
```
=COUNTIFS(Kickstarter!F:F,"=Failed",Kickstarter!D:D,"<=9999",Kickstarter!D:D,">=5000", Kickstarter!R:R,"plays").
```
Finally, I used a formula to calculate the percentage of each outcome category within each range. Then I created a pivot table from the data that organized the percentages of each outcome based on rows of goal ranges. I generated a line chart to showcase the data. 

![https://github.com/noorsami12/kickstarter-analysis/blob/43427358cb638d5567f157963a7775834e7b1a38/Resources/Outcomes_vs_Goals.png] (https://github.com/noorsami12/kickstarter-analysis/blob/43427358cb638d5567f157963a7775834e7b1a38/Resources/Outcomes_vs_Goals.png)

The line chart shows us several trends in the data of outcomes based on the Kickstarter campaign goals. We can see failed campaigns have a peak percentage of 100% when they had a goal within the range of $45,000 to $49,999. Successful campaigns had a peak of 80% successful when they were less than $1,000. 
## Challenges and Difficulties Encountered 
Most of the challenges I encountered while analyzing this data happened during the creation of the Outcomes based on Goals table and chart. Ensuring that the formulas were calculating correctly, as well as pulling from the correct range of data, was essential. I had to recheck each set of formulas multiple times to account for small mistakes, like an incorrect value, before I could generate the appropriate results. Formatting the pivot tables to filter and arrange and rows and columns in a visually-appropriate way also took a lot of time and experimentation.
## Results ##
### Conclusions: Outcomes Based on Launch Date 
Based on the chart generated for Kickstarter campaign outcomes based on their launch dates, we can conclude that most successful projects occurred in May, June, and July. Late spring and summer are the best time to launch a theater Kickstarter campaign. We can also conclude that Kickstarter campaigns are more likely to fail when they are launched at the end of the year, from October to December. 
### Conclusions: Outcomes Based on Goals 
Based on the chart generated for Kickstarter campaign outcomes based on their goal amounts, we can conclude that projects are more likely to fail when the goal amount is above $45,000. Projects have a much higher success rate at lower goal amounts, namely $5,000 and less. 
### Limitations of the Dataset 
There are a few limitations to the dataset and the conclusions drawn based on it. One major limitation is the Outcomes Based on Launch Date table uses number amounts instead of percentages, meaning the amounts shown on the chart are relative. The highest number of successful campaigns are in May, but the highest number of failed campaigns are also in May; this is only because the most campaigns launched were in May. Percentages would have accounted for this issue. 
Another limitation to the dataset is that it only covers the years 2014-2017. A larger dataset might reveal more trends. Additionally, in the Outcomes Based on Goal chart, there are some conflicting trends. There is a high failure rate above $45,000, but there is also a high failure rate around $25,000 and a very low failure rate in between those ranges, around $35,000 to $40,000. This makes it difficult to truly analyze what that data might mean. There may be other confounding factors affecting that data, such as the content of the campaigns during those ranges or the level of promotion done by the campaign managers.  
### Additional Tables/Graphs 
There are a few possible tables we could create from this dataset that might reveal additional useful trends. One graph we could create is outcomes based on subcategory in order to narrow down the most successful types of theater campaigns. We could also create a graph showing the outcomes based on staff pick to learn whether having a campaign be a staff pick really influences the outcome or not. We could also create a table and chart showcasing outcomes based on the overall length of the campaign; does having the campaign open longer help or harm the outcomes? 
 


