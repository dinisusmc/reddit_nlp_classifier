# Subreddit Classification Modelling Summary

## Web-Scraping data from selected Subreddits using PushShift Api to predict which subreddit the posts are from

### Problem Statement (1-2 sentences)
**Only using  posts that were web-scraped using pushshift api**, can I create a 
predictive model that accurately categorizes posts based on the words in them?
       
### Executive Summary (2-3 paragraphs)

#### Data Collection, Cleaning and Natural Language Processing

I collected a total of 705 posts from both Subreddits. I used Push Shift API to formally gather reddit data and eliminated any empty posts.
After identifying all of the text in each post including the title I created a new column which had all of the text in in.
I Lemmatized and Stemmed the data and vectorized each post. I vectorized using english stop words, 500-2500 max features, and an n gram range of 1 to 3.

#### Data Modelling

I have modeled 3 Logistic Regression Classifiers using the plain text vectorized, lemmatized text vectorized, and stemmed text vectorized.
After, I also have 2 Multinomial Naive Bayes Clssifiers using Lemmatized and Stemmed Text. 
Using a standard state of four the best model I achieved with various vectorization techniques was a Lemmatized Count Vectorized Logistic Regression Model. After fitting and predicting the validation set this model had a 97% accuracy score.

### conclusions and recommendations.
 
If monitoring and interpretting trends in a large number of company reviews or feedback forums on products is important to you, this could be deployed to gain insight on a large ammount of customer feedback to guide business decisions and product improvements.
    
### File Directory/table of contents
./project3/...
    ./data - Raw and processed data in .csv files
    ./KetoVegan.ipynb - Analysis note book
    ./presentation.odp - Presentation of findings
    ./README.md - Executive summary of the analysis
    
### Data and Data Dictionary

./project3/data/...
    ./feats.csv - Plain Text Count vectorized
    ./finaldf.csv - All posts from Subreddit DataFrame 
    ./lemfeats.csv - Lemmatized text Count Vectorized
    ./stemfeats - Porter Stemmed Text Count Vectorized
    
### Sources

Keto - https://www.reddit.com/r/keto/
Vegan - https://www.reddit.com/r/vegan/

