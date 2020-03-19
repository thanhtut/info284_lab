## Lab 8 Recurrent Neural Networks in Pytorch

In this lab we are going to look at how we can train a RNN for sentiment analysis. A sort of continuation of your Naive Bayes Sentiment Analysis. The content of the lab is based on [this tutorial](https://github.com/bentrevett/pytorch-sentiment-analysis/blob/master/1%20-%20Simple%20Sentiment%20Analysis.ipynb) credited to Ben Trevet. Though it is simple and perform quite badly it covers encoding and embedding steps that are necessary in NLP with Neural Networks.

It uses one-hot vector approach to encode words into vector and then simply using a dense embedding vector instead of more sophisticated approaches like word2vec. 

Please note that the constructor of the NN is parameterized     
    def __init__(self, input_dim, embedding_dim, hidden_dim, output_dim):
As the input dimension and embedding dimensions will depends on how the training set vocabulary which is determined at run time instead of predetermined dimensions such as in MNIST 28x28.

## Tasks
1. Open the tutorial in google collab and read the steps thoroughly. A slightly modified version of the notebook is [here](simple_sentiment_analysis_rnn.ipynb). After that train your model and compute the accuracy. Click the files icon on the left and then create a folder called assets if you want to see the images.
2. You can also use scikitlearn in google collab. Throw in a Naive Bayes Classifier from SK learn and train a Naive Bayes model for the same task. 
3. Compare the performances.

## More into sentiment analysis with RNN
Performing sentiment analysis with RNN is more involved. 