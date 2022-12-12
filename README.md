# Twitter Sentiment Analysis

## Process Followed:

* Extracting twitter data using tweepy API
* Data processing
* Data labelling using polarity
* Model training using Logisitic Regression, Grid Regression, Support Vector Classifier, Naive bayes Classifier on top of TF-IDF, Count Vectorizers
* Creating pickle of the best model. 
* Used the pickle in flask application to use it for live twitter sentiment anlysis.

## Technologies Used:
* Flask Framework
* HTML
* Python
* Google Colab

## Extracting tweets:

Created twitter developer account and used tweepy API to extract 1000 tweets and saved it as a dataframe. 

## Data Processing:
* Removed unnecessary, unwanted characters and tokenized the words
* Used Porter Stemming to stem the words to their root forms. 
* Labelled the tweets as per their sentiment using polarity

### Bag-of-Words:
The bag-of-words model converts text into fixed-length vectors by counting how many times each word appears.

### Term Frequency Inverse Document Frequency (TFIDF) :
TFIDF works by proportionally increasing the number of times a word appears in the document but is counterbalanced by the number of documents in which it is present

TF-IDF is better than Count Vectorizers because it not only focuses on the frequency of words present in the corpus but also provides the importance of the words. We can then remove the words that are less important for analysis, hence making the model building less complex by reducing the input dimensions.


### Labelling Data
Labelled the tweets as per their sentiment using polarity


## Modelling the Data:
Model training was done using Logisitic Regression, Grid Regression, Support Vector Classifier, Naive bayes Classifier on top of TF-IDF, Count Vectorizers. 
SVC with TFIDF performed the best. 

<img width="1366" alt="image" src="https://user-images.githubusercontent.com/12370049/207133982-6bef8e90-c2c9-4136-9489-9bfa62b2a9f4.png">

## All the training and saving model as been done in https://colab.research.google.com/drive/1xh6HrG3ATqngNVK1_zdHfLM2JVh9ccVd?usp=sharing








