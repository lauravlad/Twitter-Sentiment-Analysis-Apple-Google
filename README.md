# Twitter-Sentiment-Analysis-Apple-Google
4th Project for Flatiron School of Data Science 

## Dataset Information
The dataset used can ce found here: https://data.world/crowdflower/brands-and-product-emotions"

We use and compare various different methods for sentiment analysis on tweets.
The dataset is expected to be a csv (`list.csv`) file of type `tweet_text,emotion_in_tweet_is_directed_at,is_there_an_emotion_directed_at_a_brand_or_product` where the `tweet_text` is the tweet text, `is_there_an_emotion_directed_at_a_brand_or_product` is either  `I can't tell`, `Negative`, `No emotion toward brand or product`, or `Positive emotion` and `emotion_in_tweet_is_directed_at` is the brand or product, the respective tweet is refering to and can be
`iPad`, `Apple`, `iPad or iPhone App`,` Google `, `iPhone`, `Other Google product or service`,` Android App`, `Android`, or `Other Apple product or service`.

 

### Requirements

There are some general library requirements for the project and some which are specific to individual methods. The general requirements are as follows.  
* `numpy`
* `scikit-learn`
* `scipy`
* `nltk`

The library requirements specific to some methods are:
* `keras` with `TensorFlow` 
* `xgboost` 
* `LogisticRegression`
* `RandomForestClassifier`
* `KNeighborsClassifier`
* `Support Vector Machine`


**Note**: It is recommended to use Anaconda distribution of Python.


### Analysis and Preprocessing 

1. Run `Analysis_pre_processing.py`  This will analyse, and generate 2 preprocessed versions of the dataset. One - stored in `dataset_dichot.csv`  will have 2 dimensions for positive and negative sentiment and anothe one - stored in `dataset_multi_valued.csv` will have four dimensions for each one of the sentiments in the Sentiment column. 

Includes analysis for the various columns in the dataset and a basic overview of the dataset.

- Removes @user mentions
- Removes non-alphabetic characters + spaces + apostrophe
- Removes links
- Removes single characters
- Removes stopwords
- Lemmatizes words
- Stems words

### Modeling

2. Run `2class_modeling.py` to compare diffrent type of classifiers and find the best performing one for your 2 class dateset. 

* `keras` with `TensorFlow` 
* `xgboost` 
* `LogisticRegression`
* `RandomForestClassifier`
* `KNeighborsClassifier`
* `Support Vector Machine`


3. Run `multi_class_modeling.py` to compare diffrent type of classifiers and find the best performing one for your 4 class dateset.  

* `keras` with `TensorFlow` 
* `xgboost` 
* `LogisticRegression`
* `RandomForestClassifier`
* `KNeighborsClassifier`
* `Support Vector Machine`

### Information about other files

`: `glove.6B.50d.txt.zip` is GloVe words vectors from StanfordNLP which match our dataset for seeding word embeddings.
