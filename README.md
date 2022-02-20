# Kickstarting with Excel

## Overview of Project
This project is geared towards using a large data set for all types of Kickstarter campaigns over a set amount of time.  Captured data points are items such as type or category of campaign, amount pledged, amount donated, what the outcome of the campaign was such as success/failure/cancelled.  With this data and the tools and knowledge of excel, we are able to distill the data into trends, outcomes, and business advice for how to set up a successful Kickstarter campaign.

### Purpose
The purpose of this project is to give advice to Louise, a playwright, who is looking to achieve the highest chance of success in launching a Kickstarter campaign to fund her new idea.  The data was used to determine what a good campaign goal would be, what time of the year it should be launched, and what types of plays had the most success.  After the initial funding was complete, analysis was then conducted on campaigns in relation to their launch dates and their funding goals to further provide insight into how to maximize the chance for success compared to similar campaigns.  This latter analysis is the main focus of this report. 

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
Analysis was performed on what the outcome was of all theater based Kickstarter campaigns based on what month the Kickstarter campaign was launched.  The sheet titled "Theater Outcomes by Launch Date" in the Kickstarter_Challenge.xlsx file contains this specific analysis.  To gather this data, a pivot table was created from the master data sheet titled "Kickstarter" using the following data points:
-Date of campaign creation to show this on a per month basis
-Outcomes of the campaign to show if it was success/failure/cancelled and the count of each per month
-Filter of the category so only theater projects can be shown
-Filter of the year in which the year of the campaign launch can be used to filter the data down even further, however this filter was not utilized fot this analysis.

The final action to the table was to sort on Outcomes which ordered them as "Successful", "Failed", "Cancelled".

A pivot chart was then created to show this data graphically and provide a clear picture of what the data is showing.
![Theater Outcomes Based on Launch Date](/Resources/Theater_Outcomes_vs_Launch.png) 


### Analysis of Outcomes Based on Goals
Analysis was performed to show what the success/failure/cancelled outcomes were based at different thresholds of fundraising goals.  A table was created to show these quantities based on a dollar amounts below $1,000, and then in $5,000 increments up to $50,000.  The last threshold contained anything above $50,000 since there were only a relatively small number of campaigns above this amount, so continuing to break this down further was not warranted.  The master dataset in the sheet titled "Kickstarter" was used and the items analyzed were "goal amounts" in dollars in column D and "Outcomes" of success/failure/cancelled in column F.  Lastly, to further the specificity of our analysis to our clients goals, the outcomes were only counted if the subcategory was "plays" located in the "Subcategory" column R.

Using the "COUNTIFS" formula in excel, logic was created to count the number of "Successes", "Failures", and "Cancelled" outcomes for each dollar threshold.  These items were then summed up in a new column to calculate the total number for each dollar threshold.  The totaled amounts then allowed us to calculate the percentage of each outcome count compared to its total count at each dollar threshold.

Once this table was completed, a chart was created to show the percentage of each outcome based on the dollar range.  This chart shows the data much more intuitively and allows conclusions to be drawn much easier compared to simply looking at the numbers in the table.  A basic line chart was used as this was the most effective chart to show how the trend progresses as the dollar amount is raised.  This final chart is shown below:
[asdf](img URL)

See below the table showing the final values along with a table showing the formulas used to calculate these values.
[asdf](img URL)

### Challenges and Difficulties Encountered

- "Theater Outcomes by Launch Date" sheet:
  - I realized that after making the chart that mine still showed all the pivot table filters/items on the chart itself, while the assignment example did not. Not having these items on the chart looks much cleaner, so a quick Google search pointed me to the instructions for how to remove these items from the chart.  Knowing that I can remove/add these items will be a great skill in the future for presenting clean and professional looking charts.

- "OutcomesBbased on Goals" sheet:
  - I had to research the syntax of the "COUNTIFS" to make sure I knew how to combine multiple rules.  I then found myself frustrated with all the manual changing of each new row to change the range of the goal.  I figured there was a smarter way to reference a basic table of dollar amounts and set my COUNTIFS formula to be a simple drag and drop.  I had to then figure out how to handle the syntax of the logic operators such as ">=".  After a quick Google search, I was able to find exactly what I was looking for, and the rest of the table was just a simple drag to fill out the remaining data.  All in all, this probably took a bit more time than just manually typing in the required values for this assignment, however, I know that this knowledge/technique will come in handy with larger datasets in the future.
  - I also didn't realize that we were initially supposed to filter on "plays" so my graph looked similar to the example in the assignment but not exact.  It took re-reading the directions twice before I realized my mistake.   

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
  - Shown in the chart below, there is large spike in the number of successful campaigns that are started in May and June, and July compared to the rest of the year.  This suggests that starting a campaign in the warm summer months leads to greater success compared to the rest of the year.  Furthermore, there is a noticeable decrease in the success of a campaign towards the end of the year in November and December likely due to colder temperatures and more focus on family time and holidays.  Comparing the successes to failures over the course of a year, the failures are much more steady throughout the course of the year which can suggest that the time of the year is not a contributing factor to the success of a campaign.   

- What can you conclude about the Outcomes based on Goals?
  - The Outcomes Based on Goal chart suggests that lower goals generally yield a higher percentage chance of success.  This follows logic that it's easier to raise less money compared to higher values and this trend continues until about the $35,000 to $40,000 dollar range where there is a large increase in successes and drop-off in failures.  I would suggest that this flip in the data is a "sweet spot" of larger productions where a larger budget is required to bring in the desired talent or stage features, however, not too much to reduce the success rate as shown by the 100% failure rate of the $45,000 and roughly 90% failure rate of the $50,000+ campaigns.    

- What are some limitations of this dataset?
  - Some limitations on this dataset are we don't know specifically where this data came from and are just trusting that this contained all the data in this time period.  Since we weren't able to gather the data ourselves from the main source, its possible items were omitted that could have contributed to our analysis and conclusions.  Another data point that could have been useful is marketing budget of each campaign and/or determining if the campaign was run by an individual vs a company/group to understand the scale of resources which could have influenced the outcome of a campaign.  

- What are some other possible tables and/or graphs that we could create?
  - Outcomes vs Length of Campaign to show what the ideal length of a campaign should be.
  - Backer Count vs Length of Campaign to draw a conclusion between number of backers to outcome as opposed to just money raised.  
  - Backer Count vs Outcome at the same dollar thresholds we showed with Dollard Amount vs Outcome  - Similar to the suggestion above, there could be a correlation between the number of backers involved in a campaign to generate awareness about the campaign which could contribute to its overall success, as opposed to just looking at the dollars raised along.



