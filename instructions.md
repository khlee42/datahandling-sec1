# Social Speculation: Harnessing Reddit to Forecast Bitcoin Fluctuations

This exercise is designed to blend data analytics and machine learning concepts with real-world applications in cryptocurrency markets. We will use Reddit posts from cryptocurrency-related subreddits and financial data to create an sentiment index that predicts Bitcoin price movements. The exercise involves fetching data using APIs, performing sentiment analysis, and correlating the results with Bitcoin price changes.

**Objectives**

- To understand the relationship between public sentiment on social media and cryptocurrency market movements.
- To develop practical skills in data extraction, transformation, and loading (ETL) using APIs and Python.
- To apply text analysis techniques to social media data.
- To create visualizations that communicate the results effectively.

## Checkpoints

### 1. ETL Reddit Data
This step involves fetching data from **Reddit API** and storing it in a database. While the overall process will follows a typical ETL pipeline, there are two challenges involved in this step: 
- **Extracting more than its default limit through pagination (See "Extracting new posts")**
- **Run sentiment analysis on the posts (See "Sentiment analysis")**

### 2. ETL Crypto Data
This step involves fetching data from **Alpha Vantage API** and storing it in a databases and will be similar to the previous class exercises. Use the **"Weekly"** crypto price endpoint to fetch Bitcoin price data.

### 3. Data Analysis and Visualization
This step involves analyzing the data and creating visualizations to communicate the results effectively. Most importantly, this is where **you will develop an sentiment index that predicts Bitcoin price movements using the information from the Reddit posts (See "Better sentiment index").**

## Getting Started

1. Decide on the subreddits you want to use. You can use the list of subreddits in the **Best Crypto Subreddits in 2023** page.
2. Read the [Reddit API documentation](https://www.reddit.com/dev/api/), [Alpha Vantage API documentation](https://www.alphavantage.co/documentation/), and [TextBlob documentation](https://textblob.readthedocs.io/en/dev/) to understand how to fetch data from the APIs and perform sentiment analysis.
3. Plan your project, including pseudocode, database schema, and analysis and visualization ideas.
    - In each checkpoint, there is a list of template functions that you need to complete. Each function has a description, requirements, and estimated difficulty level.