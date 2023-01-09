# Optimization

# Introduction 

This repo. is about numerical optimization algorithms 

1. Single variable gradient descent algorithm
2. Multi-variate gradient descent algorithm
3. Batch gradient descent algorithm
4. Mini-Batch gradient descent algorithm
5. Stochastic gradient descent algorithm
6. Momentum based gradient descent algorithm
7. Nesterov Accelerated Gradient algorithm (NAG) 
8. AdaGrad algorithm
9. RMSProp algorithm
10. Adam algorithm


# Optimization Algorithms
Optimization refers to a procedure for finding the input parameters or arguments to a function that result in the minimum or maximum output of the function.

The most common type of optimization problems encountered in machine learning are continuous function optimization, where the input arguments to the function are real-valued numeric values, e.g. floating point values. The output from the function is also a real-valued evaluation of the input values.


# First-Order Algorithms
First-order optimization algorithms explicitly involve using the first derivative (gradient) to choose the direction to move in the search space.

The procedures involve first calculating the gradient of the function, then following the gradient in the opposite direction (e.g. downhill to the minimum for minimization problems) using a step size (also called the learning rate).

The step size is a hyperparameter that controls how far to move in the search space, unlike “local descent algorithms” that perform a full line search for each directional move.

A step size that is too small results in a search that takes a long time and can get stuck, whereas a step size that is too large will result in zig-zagging or bouncing around the search space, missing the optima completely.

First-order algorithms are generally referred to as gradient descent, with more specific names referring to minor extensions to the procedure, e.g.:

Gradient Descent
Momentum
Adagrad
RMSProp
Adam
The gradient descent algorithm also provides the template for the popular stochastic version of the algorithm, named Stochastic Gradient Descent (SGD) that is used to train artificial neural networks (deep learning) models.

The important difference is that the gradient is appropriated rather than calculated directly, using prediction error on training data, such as one sample (stochastic), all examples (batch), or a small subset of training data (mini-batch).

The extensions designed to accelerate the gradient descent algorithm (momentum, etc.) can be and are commonly used with SGD.

Stochastic Gradient Descent
Batch Gradient Descent
Mini-Batch Gradient Descent



# Second-Order Algorithms
Second-order optimization algorithms explicitly involve using the second derivative (Hessian) to choose the direction to move in the search space.

These algorithms are only appropriate for those objective functions where the Hessian matrix can be calculated or approximated.

Examples of second-order optimization algorithms for univariate objective functions include:

Newton’s Method
Secant Method
Second-order methods for multivariate objective functions are referred to as Quasi-Newton Methods.

Quasi-Newton Method
There are many Quasi-Newton Methods, and they are typically named for the developers of the algorithm, such as:

Davidson-Fletcher-Powell
Broyden-Fletcher-Goldfarb-Shanno (BFGS)
Limited-memory BFGS (L-BFGS)
Now that we are familiar with the so-called classical optimization algorithms, let’s look at algorithms used when the objective function is not differentiable.

