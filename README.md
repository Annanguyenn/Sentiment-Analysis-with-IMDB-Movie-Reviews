# Sentiment Analysis on IMDB Movie Reviews

Perform Sentiment Analysis on IMDB Movie Reviews using Unigram and Bigram setting, compared model performances with and without stemming and lemmatizing methods.

Tools: Python, Sci-kit Learn, Random Forest Classifier, Stemming, Lemmatizing.


## Data:


**Data set**

The labeled training data set consists of 25,000 IMDB movie reviews. There is also an unlabeled test set with 25,000 IMDB movie reviews. The sentiment of the reviews are binary, meaning an IMDB rating < 5 results in a sentiment score of 0, and a rating >=7 have a sentiment score of 1 (no reviews with score 5 or 6 are included in the analysis). No individual movie has more than 30 reviews.

**File description**

* **labeledTrainData** - The labeled training set. The file is tab-delimited and has a header row followed by 25,000 rows containing an id, sentiment, and text for each review. 

* **testData** - The unlabeled test set. 25,000 rows containing an id, and text for each review. 

** Data columns
* **id** - Unique ID of each review
* **sentiment** - Sentiment of the review; 1 for positive reviews and 0 for negative reviews
* **review** - Text of the review

## Summary: 

Main steps in the code: 
1. Use the labeledTrainData.tsv from data folder in a dataframe `train`.
2. Build a function to clean the reviews in the input file: review_cleaner(train['review'],lemmatize,stem).
3. Build a function to train the sentiment prediction models: train_predict_sentiment(cleaned_reviews, y=train["sentiment"],ngram=1,max_features=1000
4. Train models on unigrams of the reviews without lemmatizing and stemming.
5. Train models on unigrams and bigrams setting of the reviews with lemmatizing and stemming.
6. Compare the performance of original cleaned reviews in Sentiment anlysis to
lemmatized reviews, stemmed reviews for Unigram and Bigram settings, with different max_features (from 100 to 1000).