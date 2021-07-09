# **Recurrent-Neural-Network**
## Sentiment Analysis of Film Reviews<br> [Recurrent Neural Network using Python, TensorFlow & Keras]
<p float="left">
  <img src="Images/TFlow.png" width="200" />
  <img src="Images/keras.png" width="120" /> 
 </p>
 
I trained an Recurrent Neural Network to classify if a written movie review was positive or negative.
I achieved an accuracy score of ~80% using only the first 80 lines of each movie review.  For this project, I viewed a beginners TensorFlow lesson from SimpliLearn.  

**Recurrent Nueral Networks:** RNN's are very powerful tools for wide variety of problems, used for sequences of data, including languages (which are sequences of words).  As it turns out, **Deep Learning** is especially suitable to predicting sequences of events, like which videos you're likely to watch next.  So this has applications and recommender systems that deal with situations where the order of events matters.  

## Overview
### Dataset
**IMDB PreFormatted Movie Data** I used a movide data set from IMDB, which is an embedded Keras dataset.  The data set we're using consists of user-generated movie reviews and classification of whether the user liked the movie or not based on its associated rating. I imported the data directly into training and testing data arrays.  I limited data load to the 20,000 most popular words in the dataset, which precludes obscure words from entering the dataset.  (x_train, y_train), (x_test, y_test) = imdb.load_data(num_words=20000)
https://keras.io/datasets/#imdb-movie-reviews-sentiment-classification 

### The Magic 
I am using an Recurrent Neural Network, which will be trained how to "read" movie reviews and guess whether the author liked the movie or not. And this was completed by creating a sentiment classification from the first 80 words of a movie review.<br>

### Model
The RNN was trained how to "read" movie reviews and guess whether the author liked the movie or not from them. The model was trained on the first 80 words from each movie review, to limit the computing expense; while only the 20,000 most populart words were selected from the IMDB dataset. This is an example of a "Sequence to Vector" RNN Problem, where I take a sequence of words, that is a movie review, and output vector that is a single binary value of like and dislike. 
The RNN Model has Three Layers:
1. **Embedding Layer** - converts the input data into dense vectors of fixed size that's better suited for a neural network. 
2. **LSTM Layer** is created for the RNN itself. I specify 128 to match the output size of the Embedding layer, and dropout terms of 0.2 to avoid overfitting, which RNN's are particularly prone to.
3. **Sigmoid Activation Function** to choose our binary sentiment classification of 0 or 1.<br>
Finally, as this is a binary classification problem, I used the binary_crossentropy loss function. And the Adam optimizer.  

