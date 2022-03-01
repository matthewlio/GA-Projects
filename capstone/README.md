# GA Capstone: Sentiment Analysis of Movie Reviews

## Introduction

Any business is obliged to understand their clients, like their needs, opinions, and their satisfaction with the product. The best way to obtain that understanding is via customers' feedback, through proper channels in the form of feedback and reviews. Large web-based companies in this age are putting heavy emphasis on obtaining these customers' reviews, some by incentivising customers to leave reviews and feedback on their website, after receiving the product or service. By active collection of these data, companies would be informed about their own shortcomings, as well as suggestions for improvement on their products from the end-users. This would give companies a huge advantage for change and improvement on their products and services, which would greatly improve customers' experience and satisfaction. Those, in turn, translate to increase in customer pool, revenue, and overall growth of the business. We can thus see that customers' feedback are a crucial form of data and opinion mining that should not be ignored.

Sentiment analysis is a natural language processing (NLP) technique used to determine whether the data has positive or negative sentiments. It is the task of classifying polarity of a given text, sentence or document, whether expressed opinions in the given texts or sentences are positive or negative. Sentiment analysis is often performed to help businesses monitor brand and product sentiment in customer feedback and reviews, in order to understand customer needs. In the case of web-based companies, there is a need to analyse hundreds of thousands of opinions to different products, and simply searching for pre-defined "good" or "bad" words in the comments is not enough. With the rise of machine learning, in particular, sentiment analysis and neural networks, the problem of understanding the emotional tone of a text can be solved with high accuracy. By getting to know the emotional sentiments of reviews, effective feedback can be obtained for the improvement of the business.


## Problem Statement

Companies nowadays are expanding their opinion mining and data collection beyond just reviews on their websites. They are sponsoring content creators, like YouTubers or influencers, their products for review. Some of these content creators that specializes in creating review content, are not even sponsored. They review the products simply because they have multiple fans and followers whom are eager to discuss about the products, services or content these content creators are reviewing about.

This creates an issue of ignored data. These discussions in the comments are a goldmine of crucial untapped data that companies of the reviewed products can utilize. Some popular websites with these wealth of data, even contain thousands of comments that reviews and provide insights on how products can be improved. Popular websites include media streaming ones like YouTube, social media websites like Instagram and Facebook, tech review websites like rtings.com, techradar.com, general posts websites like Reddit and Medium, and last but not least, news articles websites like The Straits Times (they do reviews on movies, books, tech, restaurants, and even concerts). Reviews in the comment sections of these websites are largely ignored, with no form of sentiment analysis done to retrieve insights by the companies. It seems that there are still so many areas where sentiment analysis can be utilized.

We want to create a model that classifies the polarities of sentiments effectively in texts. With thousands of comments in the aforementioned websites, it would be valuable if these comments are classified according to positive or negative sentiments, so that companies can easily view more useful comments that provides insights for improvement.

## Methodology

We will be examining various techniques of how sentiment analysis can be applied. By training various techniques and models, we can then do a comparison between them, and choose the best performing one out of all as our production model.

Accuracy would be the key metric to observe, as well as specificity, which places more emphasis on the correct classification of negative reviews. As such, our model will be tuned towards high accuracy and specificity. This is because reviews with negative sentiments in general tend to contain the shortcomings of the product, and are also more likely to contain suggestive feedback as compared to positive reviews.

The dataset we chose for this project is the IMDB dataset. The reason we chose this dataset is because it contains balanced data, as the number of both positive and negative sentimental reviews are almost a direct fifty percent split. With a balanced dataset, it would enable us to adequately train our models for effective classification of both polarities, which we hope would help increase the accuracy of identifying both positive and negative sentiments.

## Summary of Results

In this project, various machine learning models were used for sentiment analysis. They include lexicon-based models, machine learning models and deep learning recurrent neural network (RNN). The best performing model was the Logistic Regression with TF-IDF Vectorizer, and it performed above expectations, with scores that outperformed all other models.