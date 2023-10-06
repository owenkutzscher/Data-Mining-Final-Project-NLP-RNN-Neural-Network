# Data-Mining-Final-Project-NLP-RNN-Neural-Network
Data Mining Project Proposal: Review Sentiment Analysis Model

### Team Members: 
Owen Kutzscher, owenkutzscher@gmail.com
Sebastian Vargas, seva7658@colorado.edu

## Introduction/Motivation

For our project we are going to use a neural network to create some sort of NLP model (natural language processing) that can predict a review's stars based on the language in the review. We are planning on using this data set: https://www.google.com/url?q=https://www.kaggle.com/datasets/arhamrumi/amazon-product-reviews&sa=D&source=docs&ust=1695764896933142&usg=AOvVaw1WeATDdUdlTItgNGGldkRF which includes amazon reviews, including each review's text and rating. This will fall into sentiment analysis, which involves training a computer to predict the emotional tone of a message. Our neural network will be an RNN (recurrent neural network) which will work best for our problem.
Neural networks are very impactful in today's society. From self-driving cars, to facial recognition, there are many far reaching applications of neural networks. We are interested in learning about this powerful part of modern technology.
NLPs are playing an increasingly influential role in the world. One powerful example is ChatGPT. Simple things like assistance on a website (chat bots), to complex things like writing a column in a newspaper all may be affected by the technology. In particular this has far reaching consequences for the job market as many jobs are taken away by NLP type technology.. Although we will not be making a transformer model which can generate text in LLM (large language model) style, working with similar types of data will get us closer to diving into this new emergent technology, and give us a better understanding of the topics found in NLP.
Sentiment analysis has many far reaching applications besides just product reviews. By making this model it will be able to tell us how positive or negative a statement is. One potential application of this could be scanning the internet for negative information about a product, detecting it, and informing the producer of a product. Then the producer could message the writer of the negative message and try to clear up any issues that occurred, possibly improving their product along the way.
	Another reason we are interested in this topic is it is something potentially difficult to execute. When finished we will have a solid badge to add to our resumes, and an edge over other candidates looking for similar positions to ourselves.
Lastly, we are doing this project to make learning about these topics easier. In this project we will ideally build the model from scratch and show our process of creating it. At the end of this process we will likely have a roadmap of how to get started with someone's first deep learning project.


Literature Survey	

About two years ago Arham Rumi got this data set from amazon and posted it on Kaggle. Since then many people have taken the data set and done interesting work with it related to sentiment analysis. Here are some of the latest projects people have taken on.
To start, we have Gibriel Gidley who performs sentiment analysis on the reviews using a transformer [1]. Transformer as in the T in ChatGPT. Many new LLMs are using transformers nowadays and transformers are known to deliver accurate results when it comes to text generation and classifying speech. I will now do my best to explain how their transformer works.  In their project they effectively convert each review into a scalar (with a numeric value assigned to each word), and then train the transformer model to recognize how words are related to one another, storing the associations of each word in a 300 dimensional vector [1], and then training specific instances of these combinations to be associated with different sentiment scores. When the model is complete it can be fed a sentence and it will return a predicted review rating.
Next we have Harish Neelam who uses multiple techniques to perform sentiment analysis. He generalizes the reviews into positive and negative sentiment. 1-2 is 0 (negative) and 4-5 is 1 (positive). All reviews with a score of 3 are dropped. He first uses a multinomial naive bayes algorithm to classify reviews as positive or negative, he shows the confusion matrix which demonstrates this classified reviews correctly. Next he vectorizes the data and uses logistic regression to predict the sentiment. This overall does quite poorly at predicting the sentiment, classifying almost all the reviews as positive sentiment. Lastly, he uses a LSTM model. This appears to do the best, with graphs that display it getting more accurate. But when tested against some examples like "I like this product, it's great." It rates them all as negative reviews.
Overall this data set has been used by many people to test classification methods related to sentiment analysis and interesting work has been done with it.

1. https://www.kaggle.com/code/gebrielgidey/transformer-sentiment-analyzer
2. https://www.kaggle.com/code/harishneelam/sentiment-analysis-on-amazon-reviews

Proposed Work
Below is a step by step process we will (mostly) utilize: 
Data Processing 
Tokenize
Analyze Reviews Length
Removing Outliers — Getting rid of extremely long or short reviews
Padding / Truncating the remaining data
Training, Validation, Test Dataset Split
Dataloaders and Batching
Define the LSTM Network Architecture
Define the Model Class
Training the Network
Testing (on Test data and User- generated data)
This process was one we found online, and it is designed for recurrent neural networks that are implemented using a long short term memory architecture.
Source: https://towardsdatascience.com/sentiment-analysis-using-lstm-step-by-step-50d074f09948


Evaluation
We can evaluate our model’s accuracy in a few different ways. Firstly, we can test sentiment analysis fairly easily by hand, if we were to manually enter in reviews that correlate to an obvious negative or positive sentiment, and see what our model returns. We can also compare the results of our model to results from already existing models that do sentiment analysis. 

There are a few ways we could measure success in our case. We need to do more research and we will likely figure out along the way which way will be best for us, but based on our current research we could measure success by F1-score, accuracy, or recall. As mentioned, we are both new in this field and we will research and learn as we complete our project, and tune our metrics as we go. 


Milestones
These dates signify the times that we would like to have the following tasks completed by. We realize these dates are tentative since there may be unexpected changes or hindrances to our project. 

10/1: Start exploring our data, and make sure that it is a viable source to base our model off of
10/22: Finish research on RNN models, and clean our data, including analyzing the reviews, removing outliers, etc. Start working on progress report
10/31: Progress report due
11/7: Define the LSTM network architecture, define the model class
11/15: Train the network 
11/22: Start/continue testing 
12/1: Have a tentative final report and presentation 
12/7: Final report and presentation due

