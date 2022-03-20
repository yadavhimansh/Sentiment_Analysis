# Sentiment_Analysis

By using this attached dataset(review.csv), we are trying to predict the sentiment of the users based on the experience while receiving the product.

In order to understand the content of the textual data, we have used transformer based architecture called “BERT”. We have fine tune the BERT model using existing pretrained model on sentiment analysis.

There are multiple steps which required to complete this task and get the valuable insight from the text:
Step 1: Data Preprocessing:
In this steps, we selected the clothing ID = 1078 records from the whole dataset. Also, we found that some of the records are just redundant in the dataframe. Therefore we remove most of the records and try to predict the good or bad review based on the user comments.

Once we are clear with our dependent and independent variables then we apply data cleaning techniques to clean the data which includes removal of special characters, numbers etc.

Step2: Convert the text into sentences tokenizer and attention masking:
We have applied the encode_plus method to achieve this task. As we need to convert our tokens into vectors. Therefore it is most important to understand the content as well as apply attention masking technique.

Steps3: Create Dataloader for trained and tested data:
In the pytorch framework, we have the power to create a data loader for the data. So that we can use this dataloader whenever required in the whole code.

Steps 4: Creation of BERT architecture and apply freeze technique:
In this architecture, we have create the whole skeleton of the BERT model which includes input, hidden and output layers.
In the input layers, we have used the already converted tensors and adam optimizer to control the learning rate and error rate in the back propogation.

Steps 5: Model training on fine tuned data:
In this phase, we used the architecture to train the model and finally we get the 82 percent accuracy on the existing data.
In order to findout the threshold, we have used ROC AUC curve to understand the true positive and false positive rate of the trained model.

Steps 6: Prediction Method.
We have created the predict model which can directly share the result of the text whether user like the product or not.
