# Coronavirus-Tweet-Sentiment-Analysis
 Classification model to predict the sentiment of COVID-19 tweets

# Index
1. Introduction
2. Exploratory Data Analysis./Reviwing Our Dataset
3. Data Preprocessing.
4. Model Training- MULTICLASS AND BINARY.
5. Evaluation.
6. Conclusion

# 1. Introduction
Our objective is to build a classification model to predict the sentiment of COVID-19 tweets.The tweets have been pulled from Twitter and manual tagging has been done then. The names and usernames have been given codes to avoid any privacy concerns.

![image](https://user-images.githubusercontent.com/84126197/133555061-d39d739f-ae0a-42ea-9389-72acadcb4397.png)

We are given the following information:
Username: Unique user-IDs of the users
Location: Location of the user
Tweet At: Date at which the tweet was made
Original Tweet: The exact tweet
Sentiment: Sentiment of the tweet

# Workflow in this Project

![image](https://user-images.githubusercontent.com/84126197/133555175-1476781e-cf97-472d-a815-ef75edc57b88.png)

# 2. Exploratory Data Analysis
The original dataset has 6 columns and 41157 rows.

There are five types of sentiments- Extremely Negative, Negative, Neutral, Positive and Extremely Positive.

![download](https://user-images.githubusercontent.com/60484501/162560081-ef067fb8-b7bf-4063-bdfb-f3a683543ac1.png)


All tweets data collected from the months of March and April 2020. Bar plot shows us the number of unique values in each column.
![image](https://user-images.githubusercontent.com/84126197/133555271-9eed4b85-7a21-44b9-a4fc-0a904120e97f.png)


The columns such as “UserName” and “ScreenName” does not give any meaningful insights for our analysis.

There are 20.87%(8567) null values in various places of location column.

Most of the tweets came from London followed by U.S. 

![download](https://user-images.githubusercontent.com/60484501/162560140-339cef4d-62d4-48ac-920d-1e6edaf5a241.png)

## Number of tweets as per days of the month
<img width="900" alt="image" src="https://user-images.githubusercontent.com/82973819/207886958-9c12ce32-b68f-424f-8806-c342460d10cf.png">


## Tweet sentiment count
<img width="700" alt="image" src="https://user-images.githubusercontent.com/82973819/207887661-186726d0-813b-4bb5-a136-6a1722f0b20b.png">


## 3. Data Preprocessing
The preprocessing of the text data is an essential step as it makes the raw text ready for mining.

The objective of this step is to clean noise those are less relevant to find the sentiment of tweets such as punctuation, special characters, numbers, and terms which don’t carry much weightage in context to the text.

Stop words are those words in natural language that have a very little meaning, such as "is", "an", "the", etc.To remove stop words from a sentence, you can divide your text into words and then remove the word if it exits in the list of stop words provided by NLTK.

Stemming is a rule-based process of stripping the suffixes (“ing”, “ly”, “es”, “ed”, “s” etc) from a word. For example – “play”, “player”, “played”, “plays” and “playing” are the different variations of the word – “play”.

Lemmatization is a more powerful operation, and it takes into consideration morphological analysis of the words. It returns the lemma which is the base form of all its inflectional forms.

In tokenization we convert group of sentence into token . It is also called text segmentation or lexical analysis. It is basically splitting data into small chunk of words. Tokenization in python can be done by python NLTK library’s word_tokenize() function

After cleaning text we also create wordblog

![download](https://user-images.githubusercontent.com/60484501/162560110-b1234f1c-4f48-4ff5-be67-d6b91d3e9d60.png)

4. Model Training- MULTICLASS AND BINARY.
Trained 7 different algorithms for each Multiclass and Binary classification. In Multiclass we have 5 different classes but in binary we have only two class i.e. Positive and Negative. The algorithms that were used -

1. Logistic Regression
2. Support Vector Machine
3. Random Forest
4. Naive Bayes


