# Develop a Twitter Data Crawler and Perform Sentiment Analysis

**Background:**  
An article by New York Times wrote:
["The U.S. is falling to the lowest vaccination rates of the world's wealthiest democracies."](https://www.nytimes.com/2021/09/11/world/asia/us-vaccination-rate-low.html)

## Table of Contents

- [Project Overview](## Project Overview)
- [Code and Resources Used](## Code and Resources Used)
- Data Crawled
- Data Cleaning
- Analysis Results
- Contributors

## Project Overview

**Problem statement:**
1. US is experiencing significant decrease in COVID-19 vaccination rate.
2. Evaluate President Joe Biden's sentiments towards COVID-19 vaccinations on Twitter and its impact on US vaccination rate.

## Code and Resources Used

**Python Version:** 3.9  
**Packages:** Tweepy, Pandas, Time, RE, Sqlalchemy, Matplotlib, NLTK, Wordcloud, Numpy, Pillow, Itertools, Collections, Textblob, Datetime, Decimal

## Database Schema  

![Schema](https://github.com/olliechan92/minions/blob/main/Charts_and_images/schema.jpg?raw=true)  
The data crawled will be loaded into 3 tables and stored in a PostGreSQL database namely:

user_info:  
- Twitter user id
- User's name
- User's profile description
- User's location

tweets:
- Tweet ID
- Tweet
- Tweet's like counts
- Tweet's retweet counts
- User's tweet
- User's name

user_social_network:
- User's followers count
- User's follow count
- User's name

## Data Cleaning

- Crawled tweets are filtered based on keywords "vaccinated" and "covid-19"
- Tweets are stored in a list
- Tweets are changed to lowercase and split into individual elements
- Unwanted characters and URLs are removed using Regular Expressions library
- Stop words are removed using NLTK library
- Words are then sent for analysis

## Analysis Results

### 1. Common words found in tweets
![Schema](https://github.com/olliechan92/minions/blob/main/Charts_and_images/counter.jpg?raw=true)  


### 2. Sentiment analysis - Word cloud
![Schema](https://github.com/olliechan92/minions/blob/main/Charts_and_images/wordcloud.jpg?raw=true)  
- After pre-processing Joe Biden’s tweets by removing stop words and url links, word cloud (on the right) was created using python in Jupyter notebook.
- The size of each word indicates its frequency in his tweets. The bigger the word, the higher the frequency count. Other than the two search keywords “vaccinated” and “covid-19”, the most frequently appearing words are “get”, and “vaccine”.

### 3. Sentiment analysis - Polarity
![Schema](https://github.com/olliechan92/minions/blob/main/Charts_and_images/polarity.jpg?raw=true)  
- Using the python module “Textblob”, we calculated the polarity score of his tweets with a range of -1 to 1. Values closer to 1 indicate more positivity, while values closer to -1 indicate more negativity.
- We then categorized all polarity scores into 3 buckets with a positive tweet having a polarity score > 0, neutral tweet having a score of 0 and negative tweet having a score of < 0
- From the pie chart on the left, we can observe that Joe Biden’s tweets are largely positive at 58%, hence, we can conclude his sentiments about vaccination for covid-19 are more positive.

## Contributors
