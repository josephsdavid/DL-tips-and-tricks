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

big batches take less time per epoch, but converge more slowly, and are also more likely to overfit. However, tuning this first is a good idea, as your learning rate is somewhat related. Note for RNNs: tuning batch size may be tricky! Too big or too small and gradients will explode! I typically start big and work my way down, as if you are converging quickly without overfitting with big, fast, batches, you dont need to worry about the slower small batches.

### Network size/complexity

After tuning batch size, you make your network as big/complex as you can until you again run into overfitting issues. How to expand the layers and the depth of the model is TBD

### Learning rate

Once you have decided on a general architecture, make a very small version of it and use that to tune learning rate, the optimal learning rate is independent of model size, so it will make your life (and your computer's life) much easier.

## Very helpful resources:
https://yashuseth.blog/2018/11/26/hyper-parameter-tuning-best-practices-learning-rate-batch-size-momentum-weight-decay/

## Other considerations:

When designing networks, try and think about how easy it is for errors to backpropogate! Combine RNNs by adding them!
