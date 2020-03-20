## Lab 8 Recurrent Neural Networks in Pytorch

In this lab we are going to look at how we can train a neural network with LSTM layer for sentiment analysis. A sort of continuation of your Naive Bayes Sentiment Analysis. The content of the lab is based on [this tutorial](https://github.com/bentrevett/pytorch-sentiment-analysis/blob/master/2%20-%20Upgraded%20Sentiment%20Analysis.ipynb) from Ben Trevet. 

During this exercise pay attention to the of parameterized NN initialization with parameters computed at run time based on the size of the vocabulary from the text base. 
```python
    def __init__(self, vocab_size, embedding_dim, hidden_dim, output_dim, n_layers, 
                 bidirectional, dropout, pad_idx):
```
As the input dimension and embedding dimensions will depends on how the training set vocabulary which is determined at run time instead of predetermined dimensions such as in MNIST 28x28.

And usage of pretrained word embeddings. Instead of randomly assigning words to random vector values, using pretrained embedding places the words with similar semantic meanings closer together in the vector space. e.g words such as bad and terrible shold be placed closer in the vector space.
```python
TEXT.build_vocab(train_data, 
                 max_size = MAX_VOCAB_SIZE, 
                 vectors = "glove.6B.100d", 
                 unk_init = torch.Tensor.normal_)
```

The user of dropout should be considered as well. It is a common approach to tackle overfitting in NNs. Some randomly selected weights are set to 0 during a forward pass. ALso note that this rather simple network has millions of parameters as you can see in 
```python
def count_parameters(model):
    return sum(p.numel() for p in model.parameters() if p.requires_grad)

print(f'The model has {count_parameters(model):,} trainable parameters')
```

There is another example of simple NN with RNN from the same author resources which does train at all. You can have a look at it [here](simple_sentiment_analysis_rnn.ipynb) to see the challenges involved in training NN. That simple example is perform quite badly it covers encoding and embedding steps that are necessary in NLP with Neural Networks. It uses one-hot vector approach to encode words into vector and then simply using a dense embedding vector instead of more sophisticated approaches like word2vec. 





## Tasks
1. Open the tutorial in google collab and read the steps thoroughly. A slightly modified version of the notebook is [here](sentiment_analysis_lstm.ipynb). After that train your model and compute the accuracy. Click the files icon on the left and then create a folder called assets if you want to see the images.
2. You can also use scikitlearn in google collab. Throw in a Naive Bayes Classifier from SK learn and train a Naive Bayes model for the same task. 
3. Compare the performances.
