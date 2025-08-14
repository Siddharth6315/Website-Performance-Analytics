# Website-Performance-Analytics
Web analytics project using Python(Numpy, Pandas, Seaborn &amp; Matplotlib)
# Project Overview
This repository contains an exploratory data analysis (EDA) and visualization project on website performance. The goals are to clean and prepare the exported session data, answer a set of business questions about traffic and engagement, and produce visualizations and short, actionable insights.

# Key business questions this project answers:
1) What patterns or trends can you observe in website sessions and users over time?
2) Which marketing channel brought the highest number of users to the website, and how can we use this insight to improve traffic from other sources?(https://github.com/Siddharth6315/Website-Performance-Analytics/blob/main/session%20over%20time.png)
3) Which channel has the highest average engagement time, and what does that tell us about user behavior and content effectiveness?
4) How does engagement rate vary across different traffic channels?
5) Which channels are driving more engaged sessions compared to non-engaged ones, and what strategies can improve engagement in underperforming channels?
6) At what hours of the day does each channel drive the most traffic?
7) Is there any correlation between high traffic (sessions) and high engagement rate over time?

# Datasets
https://github.com/Siddharth6315/Website-Performance-Analytics/blob/main/data-export%20(1).csv

# Datacleaning
1) df.columns = [
    'ChannelGroup', 'DateHours', 'Users', 'Sessions', 'EngagedSessions',
    'AvgEngagementTime', 'EngagedSessionsPerUser', 'EventsPerSession', 'EngagementRate', 'EventCount'
]
df=df.drop(index=0).reset_index(drop=True)
Give a short and meaningfull headings to the colunms and drop unnecessary columns
2) df['DateHours'] = pd.to_datetime(df['DateHours'], format='%Y%m%d%H', errors='coerce')
   formatted DateHours to yyyymmddhh
3) df['Hour']=df['DateHours'].dt.hour
   created new colunm Hour
# Key Insights
1) What patterns or trends can you observe in website sessions and users over time?

The Maximum User are shown in between 16 to hours when we convert them to exact time than it state that the maximum user are between 10 to 14 hour
as shown in the graph https://github.com/Siddharth6315/Website-Performance-Analytics/blob/main/session%20over%20time.png

2) Which marketing channel brought the highest number of users to the website, and how can we use this insight to improve traffic from other sources?

The Organic Social bring the most no of user and Organic Video and Email bring the least So the company has to work on organic video and email to enroll more users
https://github.com/Siddharth6315/Website-Performance-Analytics/blob/main/Channel%20that%20bring%20most%20no%20of%20users.png

3) Which channel has the highest average engagement time, and what does that tell us about user behavior and content effectiveness?



