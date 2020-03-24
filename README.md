# Project 3 - NLP on Subreddits

This project compares subreddits for two podcasting networks, Gimlet and Maximum Fun. Gimlet was founded in 2014 by former NPR host Alex Blumberg, and hosts a variety of shows, including true crime and narrative storytelling. Maximum Fun was founded in 2004 by another NPR host, Jesse Thorn, and leans more towards comedy and culture. I chose these two subreddits because there are similarities since they are both podcast networks, but the content is different enough for a machine learning algorithm to learn to distinguish between them. 

## Problem Statement:

Over the past few decades, machine learning for Natural Language Processing has come so far. We have so many different tools and machine learning algorithms to choose from. As someone who is interested in improving Human Language Technology as a future career, I wanted to see which models (of what we have learned so far) work best for analyzing a text in English. I tested Naive Bayes, Logistic Regression, K Nearest Neighbors, Decision Trees, Random Forest, Support Vector Machine, Bagging Classifier, AdaBoost Classifier, Gradient Boost Classifier, and Extra Trees with Count Vectorizer and TFIDF Vectorizor. 

## Executive Summary:

In the 1940s, when an Italian Jesuit Priest named Roberto Busa set out to analyze the works of Saint Thomas Aquinas, he had very little computing power and had to use more than 11 million punch cards to complete his decades-long project. These days we have so many different machine learning models at our fingertips, and it can be hard to narrow down the best one to use. As someone deeply interested in human language, I am fascinated by the different models that can classify text and voice and how they work.

In this project, I gathered 28,000 submissions and comments from two subreddits for the podcast networks Maximum Fun and Gimlet. I chose these because the language would be similar enough for the models to be challenged, but different enough to be able to teach the machine to distinguish between them. I tried ten different classification models combined with two different word vectorizers to see which combination got the best result. Within those models, I set many different parameters in pipelines and grid searching to see which models performed the best, adding up to over 200 different models.

## Data Dictionary

|Feature|Type|Description|
|---|---|---|
|subreddit|object|Which subreddit an item is from| 
|type|object|Whether the item is a submission or comment|
|author|object|Author of item|
|title|object|Title, only found on submissions|
|body|oject|Content of comment, not found on submissions|
|self_text|object|Content of a submission|
|created_utc|integer|Time in Coordinated Universal Time| 

## Questions for Future Research

- How do these models compare to Neural Networks?
- What is the effect of different stemming/lemmatization methods on each model?

## Conclusion

Of the ten classification models I tried, the two that worked the best were Multinomial Naive Bayes and Support Vector Machine. While both got similar results in accuracy, the Multinomial Naive Bayes is quicker and more efficient. Of the two word vectorizors, in most models the TFIDF word vectorizer worked better than the count vectorizer, because the former gives words that are more unique to one category a higher rating, whereas the latter just uses word counts.

Overall, the Multinomial Naive Bayes model with the TFIDF Vectorizer was about 90% accurate in identifying whether a reddit post was from Gimlet or Maximum Fun.
