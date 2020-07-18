# Sentiment_Analysis_Using_Natural_Language_Processing
---

The following analysis uses newsapi to conduct a sentiment analysis of cryptocurrencies Bitcoin and Ethereum. A word frequency analysis, N-gram for N = 2, and word cloud were created using NLTK and Python to tokenize text for articles. Finally, a named entity recognition model was created using SpaCy to visualize tags.

---

### Sentiment Analysis

Using NewsAPI articles were called for Bitcoin and Ethereum and put into DataFrames. The text column of the DataFrame was looped through and sentiment scores were calculated for each article using NLTK's SentimentIntensityAnalyzer for a Vader approach. The resulting DataFrames are as follows:

#### Bitcoin Sentiment DataFrame
![BTC Sentiment DataFrame](SentimentDataFrameBTC.PNG)

#### Ethereum Sentiment DataFrame
![BTC Sentiment DataFrame](SentimentDataFrameETH.PNG)

The describe function was then used for a quick analysis of the sentiment scores for both cryptocurrency news DataFrames.

##### BTC.describe()
![BTC Sentiment Quick Stats](BTCDescribe.PNG)
##### ETH.describe()
![ETH Sentiment Quick Stats](DescribeETH.PNG) 

* Which coin had the highest mean positive score?
>
> Ethereum had the highest mean positive score of 10.6% compared to Bitcoin's 3.0%.
>
* Which coin had the highest compound score?
>
>A: Ethereum had the highest max compound score of 73.2% compared to Bitcoin's 59.9%. >Ethereum also has the higher mean compound score of 29.3% compared to Bitcoin's mean >compound score of -20.7%
>
* Which coin had the highest positive score?
>
>Ethereum had the highest max positive score of 22.6% compared to Bitcoin's 14.9%.
>

### NGrams and Frequency Analysis

The next step was to tokenize text of the articles. All words were converted to lower case. Punctuation was removed and stop words for english were used. The cleaned text was lemmatized into their root words. After all these steps to tokenize the words of the articles, N-grams for N = 2 and the top 10 words for each coin were counted.

##### BTC N-gram for N = 2
![BTC N-Gram](NGramBTC.PNG)
##### BTC Top 10 Words
![BTC Top 10](Top10BTC.PNG)


##### ETH N-gram for N = 2
![ETH N-Gram](NGramETH.PNG)
##### ETH Top 10 Words
![ETH Top 10](Top10ETH.PNG)

### Word Clouds

Words clouds were created for the news articles of both crytpocurrencies using WordCloud and matplotlib libraries.

##### Bitcoin Word Cloud
![BTC Word Cloud](WordCloudBTC.PNG)

##### Ethereum Word Cloud
![ETH Word Cloud](WordCloudETH.PNG)

### Named Entity Recognition

A name entity recognition model and visualization tags were created using SpaCy. Text was concatenated into a big string of text. The NER processor was then run on the big string of text creating the below visualizations.

![BTC NER](NERBTC.PNG)


![ETH NER](NERETH.PNG)

