# Analyses-Youtube-Trending-videos-python-Data-Analysis

1. Project Overview
The project analyzes YouTube's trending video data in India to uncover trends in views, likes, dislikes, comments, and categories. It uses data science techniques such as data cleaning, transformation, and visualization to identify which types of videos and channels receive the most engagement.

2. Data Used
a. Datasets
- Your project uses two key datasets:

- Trending Video Data (IN_youtube_trending_data.csv)
  Csv File link:**https://drive.google.com/file/d/1Tji3Q62Ta0SbxXzMdhcN6I67WgzB6rCu/view?usp=sharing**

- Contains trending YouTube videos in India.
Includes details like video title, channel name, category, views, likes, dislikes, comments, and trending dates.
Category Data (IN_category_id.json)

- Provides mappings between category ID and category name.
b. Key Columns in IN_youtube_trending_data.csv
- video_id → Unique identifier for each video.
- title → Title of the video.
- channelTitle → Name of the YouTube channel.
- categoryId → Numeric ID representing the video category.
- view_count → Number of views.
- likes → Number of likes.
- dislikes → Number of dislikes.
- comment_count → Number of comments.
- publishedAt → Date and time when the video was published.
  
trending_date → Date when the video appeared on the trending list.

3. Data Processing Steps
a. Loading the Data
- Reads IN_youtube_trending_data.csv using pandas.
- Reads IN_category_id.json to map category IDs to names.
  
b. Cleaning the Data
- Missing Values → Fills missing values in channelTitle and description columns.
- Dropping Unnecessary Columns → Removes columns like channelId and thumbnail_link.
- Handling Duplicate Titles → Keeps only the latest entry for videos with duplicate titles.
  
c. Feature Engineering
- Converts publishedAt and trending_date to datetime format.
- Maps categoryId to actual category names.
- 
4. Exploratory Data Analysis (EDA)
a. Basic Statistics
- Counts unique videos and channels.
- Identifies top trending videos with the most views.
  
b. Most and Least Viewed Videos
- Finds most-viewed and least-viewed videos using sorting.
- Uses groupby to analyze views across different categories.
  
c. Public Engagement Analysis
- Groups data by video category to analyze:
 - Total views
 - Total likes
 - Total dislikes
 - Total comments
   
Computes engagement metrics like:
Like Percentage → (likes / views) * 100
Dislike Percentage → (dislikes / views) * 100
Comment Percentage → (comments / views) * 100

5. Data Visualization
The project uses matplotlib, seaborn, and plotly to create insights through graphs and charts.

a. Top Trending Video Categories
- Bar chart showing which categories have the most trending videos.

b. Public Response Analysis
- Bar chart comparing:

Like Percentage vs Dislike Percentage across video categories.
Comment Percentage for different types of videos.
c. Top Performing Channels
- Bar chart of the 5 most viewed and 5 least viewed channels.

d. Engagement Comparison
- Stacked bar charts for:

Most liked, disliked, and commented categories.
Categories with the highest public interaction.
6. Insights from Analysis
a. Popular Video Categories
- Some categories attract higher views than others.
- Categories with high engagement (likes, dislikes, comments) indicate strong audience interaction.
  
b. Channel Performance
- Identifies the top-performing channels with the highest views and engagement.
  
c. Public Response to Content
- Finds which categories receive positive (likes) vs negative (dislikes) feedback.
- Identifies categories where audiences engage through comments.
  
7. Conclusion
This project provides valuable insights into YouTube trends in India, helping:
- Content creators understand which video types perform best.
- Businesses/advertisers decide where to place ads.
- Data scientists explore public engagement trends.
