# Elections result prediction by performing sentiment analysis on tweets.

## Hypothesis: 
#### To test whether it is possible to rely on tweets posted by people on twitter during election to predict the winner in each state in the United States of America.


## How to run the code:
1. Download the data files from the below mentioned link,

   Data - https://uillinoisedu-my.sharepoint.com/:f:/g/personal/sbhing2_illinois_edu/EukRb0QIw5pFlqVJwlHkY-YBng0lsrZharURl2w8aagyeQ?e=hLiaCV

2. Create a new folder. Example: IS471_Final_Project 

3. Download and paste the python notebook i.e. 417_Final_Project.ipynb file and the data files in the IS471_Final_Project  folder.

4. Open the python notebook in Jupyter lab or Jupyter notebook and click on Kernel -> Restart kernel and run all cells.


## Overview
During elections we see a lot of people expressing their political views on the famous social media platform Twitter. The hypothesis aims to make use of these tweets to understand if there is a connection between people's sentiments for one or the other party and the outcome of the election. Since a majority of the United States population uses Twitter I thought it can be a good medium to understand people's sentiments and find whether they can be used to predict election outcomes before the actual results are declared.

## Method
I have a data source which gives me two datasets. One with tweets where "Biden" is used in almost every tweet and the other with "Trump" being the word in almost every tweet.
I started by loading each dataset in a pandas DataFrame. Since we have tweeters tweeting from all around the globe, I made sure that we use only those tweets which were posted by people residing in the United States before the actual day of election. 
Then I performed sentiment analysis on the tweets using the "vader lexicon" package of the nltk library. The vader library is able to accurately predict the sentiment of a tweet by giving a compound score, which indicates whether the tweet had a positive or a negative sentiment.
After finding the compound score of each tweet they were classified by separating them based on their sentiment which was either supportive of one or the other party. I also made sure to include the tweets which showed a negative sentiment toward one party as a positive support towards the other and vice versa.
After getting definitive counts of each tweet, I made horizontal bar chart to get the number of tweets that are in support of one or the other party. This will give a clear picture of people's sentiment towards one or the other party in each state.

## Observations
I found that in only eight states people were in favor of the Republican party and in all the other states the Democratic party was the favourite. This is not what we saw in the actual election result. We saw that Twenty Six states were won by the Democratic party and twenty five states were won by the Republican party.

## Conclusion
Based on my observations from the tweets, I can say that my hypothesis is False. I think the main reason for this may be, not all people who vote may have posted their views on Twitter. This might also be due to some biases during collecting the data.

## References
https://www.kaggle.com/manchunhui/us-election-2020-tweets?select=hashtag_joebiden.csv
https://towardsdatascience.com/sentimental-analysis-using-vader-a3415fef7664
https://www.delftstack.com/howto/python/python-dynamic-variable-name/
https://www.kite.com/python/answers/how-to-display-the-value-of-each-bar-in-a-bar-chart-using-matplotlib-in-python
https://stackoverflow.com/questions/9031783/hide-all-warnings-in-ipython