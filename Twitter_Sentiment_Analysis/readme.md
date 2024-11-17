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


## Analysis

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


## Cleaning

Now, applying the above mentioned, we are going to proceed to the cleaning of the text. To do this we will do the following:

- Use the “nltk” library to import the “stopwords” module which eliminates irrelevant words such as articles, pronouns...
- All non-alphabetic characters will be removed and then the text will be normalized to lower case.
- All hashtags, mentions (including their content) and URLs will be removed from the text. 
- Common words in negative and positive tweets that have no relevant meaning will be removed. For example “today”. These words were obtained in a later analysis of the most common words in negative and positive tweets, but are not shown in this notebook to make it more readable.

![image](https://github.com/user-attachments/assets/8e25bf2c-e881-4ae7-8a52-5622bd5b22d6)

After cleaning, we visualize how the data of the dataset is now:

![image](https://github.com/user-attachments/assets/df59d5e6-4722-4db5-92b6-a8fd955c25bc)

Now let's visualize the most common words in positive tweets and negative tweets. You can see how the words are related to these feelings

### Negative tweets

![image](https://github.com/user-attachments/assets/fc0d629e-a83b-4973-a801-cdbc051c3aa1)

Result:

![image](https://github.com/user-attachments/assets/c61f66a6-5a85-48ae-8a72-1155abd0fa53)

### Positive tweets

In this histogram the same code is used as in the one for the negative words.

![image](https://github.com/user-attachments/assets/c50ab6dc-2dee-4683-8b77-4d41bfd159d1)



After the cleaning we check if there is any empty or null value. There are 687.

![image](https://github.com/user-attachments/assets/423fb0d2-fecd-4017-840f-0dd9475e5012)

These empty rows are removed.

![image](https://github.com/user-attachments/assets/60731af9-4a3e-49d7-ab12-38a129d7ee83)


## Training 

Now let's create the bag of words that will be used to train the model.

![image](https://github.com/user-attachments/assets/c2331f92-6a77-4a33-8c75-b9ab71b7b864)

The model is now going to be trained using Random Forest. 20 percent of the data will be used for the test.

![image](https://github.com/user-attachments/assets/5b97dd0a-aa17-414e-ae98-9b9a078da01a)

Once the prediction has been made, we will paint a confusion matrix to evaluate the result. We can see that there are 231120 hits in a set of 315585 data, therefore the success percentage is 73.23%

![image](https://github.com/user-attachments/assets/f6fadc37-b1c7-4401-aa43-f74aaeb52061)

![image](https://github.com/user-attachments/assets/3fde7889-ff7e-431e-86bc-5325ebcf6d16)
