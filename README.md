# Sentiment_analysis_of_reviews

We'll go over 8 different ways to analyze reviews. In this case, we will work with a dataset from Kaggle. This dataset contains reviews about a capuccino cup, with a five star feature rating - 1 (negative) to 5 (positive). We'll start preprocessing our reviews by creating a new feature called name "sentiment", with a "positive" label, if the review has 4 or 5 stars, and "negative" label, if the review has 1 or 2 stars. Reviews with 3 stars will be dropped. Finally, this sentiment feature will be our target.

With our preprocessed text, we'll create two word count vector: the first with unigram and values will be word counts, and the second with unigram and bigram and values will be binary counts. Also, we'll create two tf-idf vector in the same way as the previous.

We'll use Logistic Regressor for count and binary vector, Bernoulli Naives Bayes for binary vector, and Multinomial Naives Bayes for count vector. You can go over the link for more information about this decision.

https://scikit-learn.org/stable/modules/naive_bayes.html


Finally, we will show the confusion matrix, we'll get accuracy, precision, recall and F1 parameters from each modelation, and we'll show them in a dataframe.

## Conclusion
it seems if we use TF-IDF vector, we improve the "recall", but lose "accuracy" and "precision". Whereas, the Multinomial NB model, with counts and unigrams, had a better performance classifying between positive and negatives reviews, in our case. We should try the same model (MNB), with counts and bigrams, and counts with unigrams an bigrams but that is for another time.
