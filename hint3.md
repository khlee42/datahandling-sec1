# Better sentiment index

The Reddit API returns diverse information about posts and comments in subreddits, which might contain useful information about the market sentiment that is difficult to capture with conventional numeric data. For instance, we could utilize sentiment and subjectivity scores from TextBlob in combination with other data points in API response, such as:

- `score`
- `ups`
- `downs`
- `upvote_ratio`
- `num_comments`

For instance, you could use the average sentiment score of all posts in a subreddit, or you could use the sentiment score of the most popular post in a subreddit. You could also use the sentiment score of the most popular post in a subreddit that has more than a certain number of comments. The possibilities are endless, and you can experiment with different combinations to see which one works best.

You may also want to consider different subreddits for data sources. For instance, you could use a subreddit that is more focused on news and announcements, such as r/Bitcoin, or you could use a subreddit that is more focused on memes, such as r/CryptoCurrency. You could also use a combination of subreddits to see if the results are different.