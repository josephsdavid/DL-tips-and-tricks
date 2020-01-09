# Practical Deep Learning Tips, Tricks, and Pitfalls

Here we will go through some deep learning practicalities which catch people (or at least me!) by surprise, and are good to know in general

## Loss functions, tasks, and output activation functions are related!

We will list the task, the loss functions you may want to use, and what activation function you use on the output layer

### Numerical Prediction

### Binary Classification

### Multiclass Classification

## Relu and dropout...

dropout after relu activation = bad! (talk about probabilities)

## Model tuning procedure
This is currently my understanding of how to build a good deep learning model in general. Steps in order. For all steps it is assumed that you are taking standard measures against overfitting

### Batch size

Tune this first. Bigger batch sizes mean your model will learn less, while if they are too small, your model will take forever to train AND you will run into either A) overfitting or B) weird things happening to your loss, for example loss and validation loss steadily decreasing when suddenly validation loss explodes. This is because your model is too dependent on the training data! To tune batch size, a good rule of thumb is to start big, and make it smaller and smaller until you run into these issues. Then you make it a little bigger than the threshhold for weird data issues. 

### Network size/complexity

After tuning batch size, you make your network as big/complex as you can until you again run into overfitting issues. How to expand the layers and the depth of the model is TBD

### Learning rate

After this is done, you can adjust the loss curve with the learning rate

## How many hidden nodes should I put in a layer
tbd

## How big should I make my network
tbd
