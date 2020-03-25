# Kaggle-Sentiment-Analysis

This is the notebook for the salary prediction brackets using the Kaggle 2018 DS and ML Challenge. The dataset used for the following project was used from the Kaggle website.

Tell a Data Story about a Subset of sentiments from the Canadian 2015 Federal Elections

Through the project, I did the following:

Data Cleaning: i.Steps Involved:
All text in lowercase
Removal of URL links and twitter handles
Removal of HTML attributes such as </>
Parsing of HTML character codes into their ASCII equivalent

Cleaning the tweets (Part 2)
Steps Involved:
Tokenize the tweets
Filter out stopwords
Use SnowballStemmer to stem the remaininig words
Token: Each “entity” that is a part of whatever was split up based on rules. For examples, each word is a token when a sentence is “tokenized” into words. Each sentence can also be a token, if you tokenized the sentences out of a paragraph.
Source: https://www.geeksforgeeks.org/tokenize-text-using-nltk-python/
Stop Words: A stop word is a commonly used word (such as “the”, “a”, “an”, “in”). We would not want these words taking up space in our database, or taking up valuable processing time. For this, we can remove them easily, by storing a list of words that you consider to be stop words
Source: https://www.geeksforgeeks.org/removing-stop-words-nltk-python/
Stemming: is the process of reducing words to their core root (for instance - cooking to cook, asked to ask). As there can be understemming or overstemming of words, this process can affect the model. However, to reduce the processing time, we will perform stemming. We use SnowballStemmer instead of PorterStemmer as it is a better stemmer and universally accepted.
Source: https://towardsdatascience.com/stemming-lemmatization-what-ba782b7c0bd8

EDA Analysis:
Concept
We will look for certain keywords in a tweet to classify the tweet with a political party.
Liberal : Keywords - 'justin|trudeau|justintrudeau|liberal|lpc'
Conservative : Keywords - 'andrew|scheer|andrewscheer|conservative|cpc'
NDP : Keywords - 'thejagmeetsingh|ndp|jagmeet|singh|democratic'
Process
To look if a tweet contains keywords from two or more parties; classify the tweet as 'Mixed'
To look if the tweets contain keywords only from a particular party; classify them accordingly
If none of the keywords are found; classify it as 'None'
