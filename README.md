# Website-Performance-Analytics
Web analytics project using Python(Numpy, Pandas, Seaborn &amp; Matplotlib)
# Project Overview
This repository contains an exploratory data analysis (EDA) and visualization project on website performance. The goals are to clean and prepare the exported session data, answer a set of business questions about traffic and engagement, and produce visualizations and short, actionable insights.

# Key business questions this project answers:
1) What patterns or trends can you observe in website sessions and users over time?
2) Which marketing channel brought the highest number of users to the website, and how can we use this insight to improve traffic from other sources?
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
1) What patterns or trends can you observe in website sessions and users over time?<br>
   The Maximum User are shown in between 16 to hours when we convert them to exact time than it state that the maximum user are between 10 to 14 hour
   as shown in the graph https://github.com/Siddharth6315/Website-Performance-Analytics/blob/main/session%20over%20time.png

2) Which marketing channel brought the highest number of users to the website, and how can we use this insight to improve traffic from other sources?<br>

   The Organic Social bring the most no of user and Organic Video and Email bring the least So the company has to work on organic video and email to enroll more users
   https://github.com/Siddharth6315/Website-Performance-Analytics/blob/main/Channel%20that%20bring%20most%20no%20of%20users.png

3) Which channel has the highest average engagement time, and what does that tell us about user behavior and content effectiveness?<br>
   Organic Video has the highest average engagement time, showing that video-driven visitors are highly interested and interact longer. Investing more in quality video content can boost engagement<br>https://github.com/Siddharth6315/Website-Performance-Analytics/blob/main/Average%20engagement%20time%20by%20channel.png

4) How does engagement rate vary across different traffic channels?<br>
   Referral, Organic Search, and Organic Social show higher median engagement rates, while Direct is moderate.
Unassigned and Organic Video have very low engagement rates, and Email shows extreme variability.<br> https://github.com/Siddharth6315/Website-Performance-Analytics/blob/main/engagement%20rate%20distribution.png

5) Which channels are driving more engaged sessions compared to non-engaged ones, and what strategies can improve engagement in underperforming channels?<br>
   Organic Social, Referral, and Organic Search drive more engaged sessions than non-engaged ones, showing strong content relevance and user interest. In contrast, Direct, Organic Video, and Unassigned channels have higher non-engaged sessions, suggesting the need for better landing page optimization, more compelling video content with clear CTAs, and improved tracking for accurate source attribution. <br> https://github.com/Siddharth6315/Website-Performance-Analytics/blob/main/engaged%20vs%20non%20engaged%20sessions.png

6) At what hours of the day does each channel drive the most traffic?<br>
   Direct traffic peaks late at night around 23:00, Organic Search is highest at 20:00, and Organic Social sees its largest spike at 19:00. Referral traffic performs best around midday at 11:00, while Organic Video and Unassigned traffic remain relatively low but show minor peaks at 20:00 and 15:00 respectively.<br> https://github.com/Siddharth6315/Website-Performance-Analytics/blob/main/Traffic%20by%20Hour%20and%20Channel.png


7) Is there any correlation between high traffic (sessions) and high engagement rate over time?<br>
   high traffic and high engagement rate — sessions (blue) fluctuate significantly over time, but the engagement rate (green) remains relatively stable and low,
   suggesting that more traffic does not necessarily lead to higher engagement.<br>https://github.com/Siddharth6315/Website-Performance-Analytics/blob/main/Engage%20rate%20vs%20Session%20over%20time.png
   <br>
## Full Code (Jupyter Notebook) <br> https://github.com/Siddharth6315/Website-Performance-Analytics/blob/main/Website%20Performance.ipynb

## Conclusion
This project helped in understanding which channels bring the most traffic, when users are most active, and how engagement varies.  
The insights can be used to improve marketing strategies and create better content for higher user interaction.

## Next Steps
- Add more data like location and device for deeper analysis.  
- Create automated scripts to refresh the analysis.  
- Make an interactive dashboard for quick tracking.

---

**Author:** Siddharth Singh  
📧 Contact: [siddharth77th@gmail.com]  



