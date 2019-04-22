# Question

Hi there,
What's the reason that training the neural nets with the same data is not a strictly deterministic process? Loss and accuracy are slightly different in each run with the same parameters? Or is there a random selection of the 10 batches used for training each run explaining the slightly different outcomes?

# Answer
In short, we use randomness to initialize the weights at the beginning of
[stochastic gradient descent](https://en.wikipedia.org/wiki/Stochastic_gradient_descent#Iterative_method). So, each iteration of SGD will have a slightly
different answer depending on the initialization. Getting into the mechanics
of [Keras](https://www.tensorflow.org/api_docs/python/tf/keras/layers/Dense),
we can see the default setting for kernel_initializer='glorot_uniform'. This is the
method used to randomly initialize the weights. Additionally, stochastic
gradient descent sometimes will converge to a local minima rather than the
global minimum. You may get a different local min on different runs of SGD. For
these reasons, a neural network is not deterministic-resulting in the same output
each time it's run.


## Read more
- [Random weights](https://machinelearningmastery.com/why-initialize-a-neural-network-with-random-weights/)
