# Kickstarting with Excel: Analysis

## Overview of Project
    This is a detailed analysis of a large data set gathered from thousands of crowdfunding campaigns hosted on the platform Kickstarter. The data set represents information from multiple theater productions who hosted crowdfunding campaigns. There is great diversity in the types of theater productions in this data set, from the topic of the production, to where and when it was produced, to the dollar amount needed to fully fund the campaign, and whether or not the campaigns met their goals. The following analysis has been produced by an expert team of Data Analysts (who should be compensated accordingly). 

### Purpose
    The purpose of our analysis was to find and examine patterns in the data set that could provide helpful information for our client (who will remain confidential) in planning and executing their own theater production Kickstarter campaign. 

## Analysis and Challenges
    We analyzed the data based on two parameters: success in relation to the launch date of the Kickstarter and success in relation to the goal dollar amount needed to fully fund the campaign. 


### Analysis of Outcomes Based on Launch Date
     When assessing success based on launch date, the team ran into an issue of the launch and completion dates being presented in Unix Timestamps rather than something more readable. However we were able to use this formula `=(((J2/60)/60)/24)+DATE(1970,1,1)` to convert these time stamps into a day-month-year format. After converting the dates in the data into a readable format, we generated a Pivot Table in order to visualize our data. The Pivot Table illustrated the number of Successful, Failed, Canceled, and Live Kickstarter campaigns based on the month the campaign was launched. Ge then generated a Pivot Chart in the form of a line graph based on this data. 
    
    ![See the graph!](https://github.com/Jace-Loo/Advanced-Excel-Analysis-of-Kickstarter-Success/blob/48d2f483cdd43e84d90c10bacef17868565ff7eb/Theater_Outcomes_vs_Launch.png)

    We found the number of campaigns launched trended higher in the summer months. We also found that the highest number of successful campaigns were launched in the late spring and summer months, with May being the most successful and September being the least successful. Out of all months, October had the highest ratio of failed to successful campaigns. May saw the same number of failed campaigns as October, however, as mentioned above, also had the most successful campaigns. 

### Analysis of Outcomes Based on Goals
    In our analysis of the campaign goals, we found that most campaigns had goals between $1,000 and $4,999. However the bracket with the highest number of successfully funded campaigns was the bracket between $0 and $1,000 with a 71% success rate, compared to a 66% success rate for campaigns between $1,000 and $4,000. The bracket with the highest rate of failure was for campaigns with goals $50,000 and above, boasting a 58% failure rate. In between $0 and $50,000 most amount brackets had at least a 50% success rate.
    
    When assessing success based on goal amount, we used the formula `=COUNTIFS(Kickstarter!$D:D, "<1000", Kickstarter!$F:F, "=successful")` in order to count the number of successful campaigns with a goal amount under $1000. We adapted the formula for failed andcanceled campaigns, as well as other dollar maount brackets. When copying the formula to other columns, we found that the relative columns were changing in the formula, and adding `$` to lock the columns in the formula solved that issue. 


## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
    1) It would be best to launch during May.
    2) Launching in October would be the worst decision

- What can you conclude about the Outcomes based on Goals?
    1) Having a goal of less than $1,000 leads to the highest success rate.

- What are some limitations of this dataset?
    1) We are only able to make conclusions based on campaigns hosted on Kickstarter. We are not accounting for data on platforms such as IndieGoGo or GoFundMe.

- What are some other possible tables and/or graphs that we could create?
    1) Success based on location of the Kickstarter
    2) Success based on the Parent of Subcategory of the production
    3) Success based on the duration of the campaign