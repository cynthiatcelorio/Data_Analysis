# Twitter Sentiment Analysis

## Introduction

In this project we are going to do a sentiment analysis of a collection of tweets. The objective is to find out if the text of the tweets is of negative or positive nature.

### Dataset

The dataset used in this project is called "sentiment140" and contains 1578612 tweets. 
This dataset is composed of 4 columns, which are "ItemID", "Sentiment", "SentimentSource" and "SentimentText". The columns "ItemID" and "SentimentSource" are not relevant so they will be deleted.

The sentiment column can take two possible values: 
- 0 for negative tweets
- 1 for positive tweets

![image](https://github.com/user-attachments/assets/8c8a15a0-d438-4f37-a058-a9e4662bc58f)


## Análisis y limpieza

First of all, the two columns mentioned above ("ItemID" and "SentimentSource") will be eliminated because they are not very relevant.

![image](https://github.com/user-attachments/assets/0604b1f1-22b2-4d17-a83e-46d6f5b7039d)

Now let's paint a histogram showing the number of negative and positive tweets to see how the data is distributed. As we can see, the numbers are quite similar.

![image](https://github.com/user-attachments/assets/acf816a7-1407-4e7c-a73b-9c32062dee74)

![image](https://github.com/user-attachments/assets/3185017c-5d0d-416a-8716-8c45dc1fe58a)


An important thing to keep in mind when analyzing tweets is the elements they may contain in addition to text. A tweet may contain hashtags, mentions (@) or URLs. These elements must be identified in order to eliminate them, as they contaminate the information. An example of each case is shown below.

![image](https://github.com/user-attachments/assets/40529eda-6591-4659-8fb7-d196c42c5592)

Now let's draw a histogram to see the most frequent words in tweets. As we can see there are no relevant words, there are only articles, pronouns, etc. After cleaning up the text, another revision of this graph will be made.

![image](https://github.com/user-attachments/assets/7b31d742-c9c8-45ec-aa96-b6aa41803b00)

![image](https://github.com/user-attachments/assets/1c893854-678f-4e71-955a-68e3cdab3142)
















# Entrenamiento
## Entrenamiento 1
Tipo, features, resultados
Matriz de confusion

# Conclusion final
