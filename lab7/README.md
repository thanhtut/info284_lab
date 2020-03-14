## Neural Networks Part 2 

### Goals 
1. Understanding PyTorch neural network data preparation, network definition, training and evaluation. 
2. Saving a NN weights.

### Submission
Copy and paste the answers in each text cells at the end of the notebook [MNIST_with_GPU.ipynb](MNIST_with_GPU.ipynb) with code changes. Submit it to the TAs responsible for the lab attendance to get the grade.



### Exercise 1
Read the code from [MNIST_with_GPU.ipynb](MNIST_with_GPU.ipynb) and answer the following questions and paste the answers in the notebook you are submitting.
Hint: You can use print(model) on the model to see the layers as well as the statements from the init() and forward() methods.

1. What batch size is used for training the neural network?
2. How many epochs the network is trained?
3. How many layers are there in the network?
4. Describe each layers by the type of the layer, dimensions of neurons in that layer and the type of activation function usd. If it is a Convolutional Layer also describe its filter size and stride length.
5. What method is used for optimization and describe the prameters of the algorithm.
6. Will the network improve with epoch for training why or why not?
7. Note the accuracy after each epoch and save it.

### Exercise 2
Improve the performance of the the NN accuracy slightly by adjusting parameters such as number of epoches and different learning rates. Note that there wont be any drastic improvements as there is not much room to improve after 98.9% accuracy.

### Exercise 3
Now use SGD for training the NN and compare the performance with the numbers saved in Exercise 1.7 for each epoch. For the documentation on the optimizer read it here [Optimizer](https://pytorch.org/docs/stable/optim.html#torch.optim.ASGD). Note that it all optimizier in PyTorch are subclasses of the same base torch.optim.Optimizer so changing optimizers can be done by just using a different constructor.

Note: zeroing out the gradients is necessary [zero_grad](https://pytorch.org/docs/stable/optim.html#torch.optim.Optimizer.zero_grad) after every optimization step as PyTorch accumulates gradients on every backward pass step loss.backward(). This is necessary unless you are tranining RNN where the accumulation of gradients is part of the process.

### Exercise 4
Training a NN is expensive, time consuming and in larger datasets it is hard to converge. Therefore after you have trained your network find a way to save the model. After the the model is saved, you can reload the model anytime from the file. Load the model form the fle and use it to classify some sample from the training set.
For this execise saving the weight can be done using a method provided by [save](https://pytorch.org/tutorials/beginner/saving_loading_models.html#save-load-entire-model) 