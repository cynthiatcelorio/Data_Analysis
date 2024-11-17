# Spam Detection

## Introduction

In this project we are going to analyze a dataset with data about e-mails. The objective is to detect if the email is spam or not according to its content.

## Dataset

The dataset named “telegram-spam-ham” comes from https://huggingface.co/datasets/thehamkercat/telegram-spam-ham . 
This dataset is composed of 20'3 K rows and two columns: “text” which contains the text of the email and “text_type” which can take two values:
- Spam: if the email is spam
- Ham: if the email is NOT spam

![image](https://github.com/user-attachments/assets/5b3ca59f-a1fd-4a86-9981-f128129ca4a0)

## Analysis and Cleaning

There are no columns to delete so we proceed to see how many 'Spam' or 'Ham' values exist.

![image](https://github.com/user-attachments/assets/b0a95e2c-678b-4594-aab6-876ac1c57877)

![image](https://github.com/user-attachments/assets/042b7ee6-fda4-48ff-8182-587a016b6d86)

Now we are going to proceed to the cleaning of the text. To do this we will do the following:

- Use the “nltk” library to import the “stopwords” module which eliminates irrelevant words such as articles, pronouns...
- All non-alphabetic characters will be removed and then the text will be normalized to lower case.
- All URLs will be removed from the text. 

![image](https://github.com/user-attachments/assets/ff470f5a-8ef8-40c0-b3f3-a23f242a85d4)

After the cleaning we check if there is any empty or null value. There are 257. The empty rows are removed.

![image](https://github.com/user-attachments/assets/68563ed8-e5c8-49c3-b0a7-4d37f9f94751)

Now let's create the bag of words that will be used to train the model.

![image](https://github.com/user-attachments/assets/ee40367b-3746-45a3-ae2a-9ebd6a0b1f50)


## Training 


The model is now going to be trained using Random Forest. 25 percent of the data will be used for the test.

![image](https://github.com/user-attachments/assets/0bf57e27-b23b-4698-9dc9-5048f33af68a)

Once the prediction has been made, we will paint a confusion matrix to evaluate the result. We can see that there are 4644 hits in a set of 4973 data, therefore the success percentage is 93.38%

![image](https://github.com/user-attachments/assets/afcd0fad-ca63-42a7-a90f-738293cade8c)

![image](https://github.com/user-attachments/assets/6e14cf10-9292-42cb-af4e-5c3b4a09b381)



