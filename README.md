# Develop a Twitter Data Crawler and Perform Sentiment Analysis

**Background:**  
An article by New York Times wrote:
["The U.S. is falling to the lowest vaccination rates of the world's wealthiest democracies."](https://www.nytimes.com/2021/09/11/world/asia/us-vaccination-rate-low.html)

## Table of Contents

- Project Overview
- Code and Resources Used
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

![Schema](minions/Charts and images/schema.jpg?raw=true)  
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

### Common words found in tweets

### Sentiment analysis - Word cloud

### Sentiment analysis - Polarity

## Contributors
