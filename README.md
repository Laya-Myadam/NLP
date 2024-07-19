# NLP

1. 2 different feature-extraction that is text representation techniques have been performed , one is bag-of-words(BOW) and the other one is Frequency-inverse-document-frequency technique(Tf-IDF) and applied them to extract the features.
2. Performed all the pre-processing techniques like tokenizing all the TweetContents into individual words on the twitter dataset.
3. we have all the words into lower-case for better analysis of the content and help us to standardize the text and make sure it has consistent representation.
4. Removed all the stop-words from the tweetContent that is we removed all the common-words which are frequently used like “the”,”an”,”and” and many more which are used frequently but are of not much use and they don’t contribute much to the meaning of text as well. Then we have removed unnecessary punctuations , symbols and also  non-alphanumeric characters. Next, we performed stemming to reduce or bring back the words to their root form. This is mostly useful for the analysis of model.
5. Loaded  pre-processed dataset which is the csv file into the pandas data-frame. And I have split the dataset into two sub-sets of equal size such that one is used for bag-of-words technique and the other is used for Term Frequency-Inverse-Document-Frequency technique.
6. In bag-of-words technique I have used countVectorizer to convert each and every tweet into a matrix of the word-counts and the result extracted features of bow are stored in a csv file.
Now in Tf-IDF technique, I have used tf-idfVectorizer to convert our teweetContent into the tf-idf features by considering the importance of words in the whole dataset and then stored the extracted features of tf-idf in a dataframe and then saved them into a csv file.
The target-variable of tf-idf is assumed to be df_tfidf and for bow it is assumed to be df_bow and now a multinomial naive-bayes classifier is trained separately on both bow and tf-idf features and then we calculate the accuracies of both the techniques and print them. 
3&4) 
7. Performed model-building and evaluation by implementing the model using logistic-regression. 
8. Divided the dataset into both training and testing datasets, by considers 80 percent of it for training and then 20% of it for testing.
9 Used tf-idf vectorization method to convert the tweetContent into numerical-features and using this step we have transformed the text-data into a format which is suitable for machine learning. 
10. Built a regression-model and trained it using the tf-idf transformed training-data. Next, we have made predictions like sentiment labels for testing set using the training model. Next we created a result_df data-frame containing all the columns like tweetId, TweetContent, original sentiment and the predicted sentiment for the testing data-set. 
11. At the end, we have computed and printed the evaluation metrices like accuracy, precision, f1 score and recall values to check and evaluate how well our model’s performance is on the testing dataset. In the end, we have evaluated and predicted the sentiment of tweets.
12. Finally, Under the comparative-analysis we have performed both bag-of-words technique and tf-idf technique and then found the values of accuracy,precision, f1 score and recall value which will tell us about the overall performance of our model. Then we have created a visual representation of our model’s performance by showing the number of true-positive, true-neagtive,false-positive and false-negative predictions with the help of confusion matrix and printed them.  

