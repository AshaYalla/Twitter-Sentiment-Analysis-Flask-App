# Twitter Sentiment Analysis

## Process Followed:

* Extracting twitter data using tweepy API
* Data processing
* Data labelling using polarity
* Model training using Tensorflow, Logisitic Regression, Grid Regression, Support Vector Classifier, Naive bayes Classifier on top of TF-IDF, Count Vectorizers
* Creating pickle of the best model. 
* Used the pickle in flask application to utilize it for live twitter sentiment anlysis.

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
Model training was done using Tensorflow, Logisitic Regression, Grid Regression, Support Vector Classifier, Naive bayes Classifier on top of TF-IDF, Count Vectorizers. 

SVC with TFIDF performed the best. 

<img width="1366" alt="image" src="https://user-images.githubusercontent.com/12370049/207133982-6bef8e90-c2c9-4136-9489-9bfa62b2a9f4.png">



Confusion matrix of SVC with TFIDF model: 

<img width="438" alt="image" src="https://user-images.githubusercontent.com/12370049/207134850-ce323e3e-6c91-4e53-9d71-fc7ecb39708e.png">


## All the training and saving model has been done in https://colab.research.google.com/drive/1xh6HrG3ATqngNVK1_zdHfLM2JVh9ccVd?usp=sharing


### Distribution of tweets:

![image](https://user-images.githubusercontent.com/12370049/207135197-8ffb7165-0beb-4f73-9851-fd9cd51d4495.png)

### Most frequent words in positive tweets

![image](https://user-images.githubusercontent.com/12370049/207135279-de5e64c5-2060-4868-9287-973938b6b742.png)


### Most frequent words in negative tweets
![image](https://user-images.githubusercontent.com/12370049/207135328-9c9be02e-affb-4244-b2b2-875c222bd24e.png)


### Most frequent words in neutral tweets
![image](https://user-images.githubusercontent.com/12370049/207135402-6cf55316-9cdc-4bbf-9724-99b50a77cd92.png)

### Used the saved best model in flask application to utilize it for live twitter sentiment anlysis.

<img width="1440" alt="image" src="https://user-images.githubusercontent.com/12370049/207135817-766ca265-0741-4b9c-886a-d8c14f82cfb5.png">
















