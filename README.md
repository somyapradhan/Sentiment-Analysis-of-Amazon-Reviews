# Sentiment-Analysis-of-Amazon-Reviews
Implemented various algorithms to classify sentiments into 3 classes:Positive,Negative and Neutral

# Introduction
There are thousands of products of similar category. So it will be tedious for the customer to make selection. So what would make customers’ life easier in selecting right product for them??? Yes , It’s the ‘reviews’ and ‘ratings’ of the product given by customers who have already used that product customers who have already got that and brief their experience by giving reviews. Ratings can be easily sorted and judged whether a product is good or bad. But when it comes to reviews which consists of sentences or may be paragraphs, we need to read through every line to make sure the review conveys a positive or negative sense. So we use NLP Technique for this.

# Dataset
The dataset was downloaded from Kaggle. It consists of reviews and ratings of around 10000 musical instruments.We have to categorize the revies. This can be utilized for feedback management system. We Classification of individual reviews.and we also determining overall rating based on individual reviews. So that company can get a complete idea on feedback's provided by customers and can take care on those particular fields.

# Prepocessing
We are fiiling the NaN values in review with 'Missing' and usinf Tfidf vectorizer to convert the text into vectors.
And we are converting the target variable into 0, 1 and 2 (label encoding). And since we got highly imbalance dataset , we are using SMOTE technique to oversample the low rating dataset as these are less in number( around 10%).We are removing the english stopwords and applying stemming ( for this we are using Porter Stemmer).

# Model Training
We have used the following alogorithms:
1. Logistic Regression
2. K-nearest neighbors
3. Support Vector Classifier
4. Naive Bayes
5. Decision Tree Classifier
6. Random Forest Classifier

# Results 
After training and hyperparameter tuning, the following conclusions were drawn:
1. Logistic Regression worked well and we got accuracy of 98% on test set and the f1 score  was also quite good And the best part was eventhough the accuracy is a bit less than KNN and SVC, the all of the negative sentiments were classified correctly.
2. KNN seemed to work best with test accuracy 99.69% and f1-score=1.
3. SVC also worked well and similar to KNN but it took lot of time in training. This may be due to large number of features.
4. Decision Tree performed poorly . We got overfitting and high variance problem.
5. Randdom Forest Classifier( Ensembling Technique) seemed to work well than Decision Tree with accuracy of around 98% and f1-score 0.9 .


