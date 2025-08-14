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
<a href="https://github.com/Siddharth6315/Website-Performance-Analytics/blob/main/data-export%20(1).csv"> Datasets </a>

# Datacleaning
1) df.columns = [
    'ChannelGroup', 'DateHours', 'Users', 'Sessions', 'EngagedSessions',
    'AvgEngagementTime', 'EngagedSessionsPerUser', 'EventsPerSession', 'EngagementRate', 'EventCount'
]
df=df.drop(index=0).reset_index(drop=True)
2) df['DateHours'] = pd.to_datetime(df['DateHours'], format='%Y%m%d%H', errors='coerce')
   formatted DateHours to yyyymmddhh
3) df['Hour']=df['DateHours'].dt.hour<br><br>
   This Will Give a short and meaningfull headings to the colunms and drop unnecessary columns created new colunm Hour
# Key Insights
## 1) What patterns or trends can you observe in website sessions and users over time?<br>
   The Maximum User are shown in between 16 to hours when we convert them to exact time than it state that the maximum user are between 10 to 14 hour
   as shown in the graph<br><br>
   <img width="759" height="614" alt="session over time" src="https://github.com/user-attachments/assets/21d79484-ac6f-4a05-87f8-ca423417b20b" />


## 2) Which marketing channel brought the highest number of users to the website, and how can we use this insight to improve traffic from other sources?<br>

   The Organic Social bring the most no of user and Organic Video and Email bring the least So the company has to work on organic video and email to enroll more users<br><br>
   <img width="629" height="419" alt="Channel that bring most no of users" src="https://github.com/user-attachments/assets/4b683752-5c82-4787-b796-81fece2f44e8" />


## 3) Which channel has the highest average engagement time, and what does that tell us about user behavior and content effectiveness?<br>
   Organic Video has the highest average engagement time, showing that video-driven visitors are highly interested and interact longer. Investing more in quality video content can boost engagement<br><br><br>
   <img width="610" height="459" alt="Average engagement time by channel" src="https://github.com/user-attachments/assets/bc663347-5dc1-4ecf-8208-061ba66fc2cf" />

## 4) How does engagement rate vary across different traffic channels?<br>
   Referral, Organic Search, and Organic Social show higher median engagement rates, while Direct is moderate.
Unassigned and Organic Video have very low engagement rates, and Email shows extreme variability.<br> <img width="610" height="459" alt="engagement rate distribution" src="https://github.com/user-attachments/assets/83c81f40-20a5-43db-b832-a5e5bf12fffc" />


## 5) Which channels are driving more engaged sessions compared to non-engaged ones, and what strategies can improve engagement in underperforming channels? <br>
   Organic Social, Referral, and Organic Search drive more engaged sessions than non-engaged ones, showing strong content relevance and user interest. In contrast, Direct, Organic Video, and Unassigned channels have higher non-engaged sessions, suggesting the need for better landing page optimization, more compelling video content with clear CTAs, and improved tracking for accurate source attribution. <br> <br><br><img width="630" height="659" alt="engaged vs non engaged sessions" src="https://github.com/user-attachments/assets/fe98c961-c112-4be0-a3de-9cf86b223be7" />

## 6) At what hours of the day does each channel drive the most traffic?<br>
   Direct traffic peaks late at night around 23:00, Organic Search is highest at 20:00, and Organic Social sees its largest spike at 19:00. Referral traffic performs best around midday at 11:00, while Organic Video and Unassigned traffic remain relatively low but show minor peaks at 20:00 and 15:00 respectively.<br> <br><br><img width="786" height="555" alt="Traffic by Hour and Channel" src="https://github.com/user-attachments/assets/3f3150d7-b4aa-4e3c-a852-8cc4333089b4" />

## 7) Is there any correlation between high traffic (sessions) and high engagement rate over time?<br>
   high traffic and high engagement rate — sessions (blue) fluctuate significantly over time, but the engagement rate (green) remains relatively stable and low,
   suggesting that more traffic does not necessarily lead to higher engagement.<br> <br><br>
   <img width="759" height="414" alt="session over time" src="https://github.com/user-attachments/assets/07898813-817c-4878-b658-fafd950fec08" />

   <br>
Full Code <br> (Jupyter Notebook) <br> https://github.com/Siddharth6315/Website-Performance-Analytics/blob/main/Website%20Performance.ipynb

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



