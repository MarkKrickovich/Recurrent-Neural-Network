# **Recurrent-Neural-Network**
## Sentiment Analysis of Film Reviews<br> [Recurrent Neural Network using Python, TensorFlow & Keras]
<p float="left">
  <img src="Images/TFlow.png" width="200" />
  <img src="Images/keras.png" width="125" /> 
 </p>
 
I trained an Recurrent Neural Network to classify if a written movie review was positive or negative.
I achieved an accuracy score of ~80% using only the first 80 lines of each movie review.  For this project, I viewed a beginners TensorFlow lesson from SimpliLearn.  

**Recurrent Nueral Networks:** RNN's are very powerful tools for wide variety of problems, used for sequences of data, including languages (which are sequences of words).  As it turns out, **Deep Learning** is especially suitable to predicting sequences of events, like which videos you're likely to watch next.  So this has applications and recommender systems that deal with situations where the order of events matters.  

## Overview
### Dataset
**IMDB PreFormatted Movie Data** I used a movide data set from IMDB, which is an embedded Keras dataset.  The data set we're using consists of user-generated movie reviews and classification of whether the user liked the movie or not based on its associated rating.
https://keras.io/datasets/#imdb-movie-reviews-sentiment-classification 

### The Magic 
I am using an Recurrent Neural Network, which will be trained how to "read" movie reviews and guess whether the author liked the movie or not. And this was completed by creating a sentiment classification from the first 80 words of a movie review.<br>


## Contents
Notebook 00: Install Surprise<br>
Notebook 01: Load MovieLens Data<br>
Notebook 01: 
