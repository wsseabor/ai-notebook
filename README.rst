MNIST dataset can be found at http://yann.lecun.com/exdb/mnist/

Given code will work downloading from source and stashing it in a local folder in the same
master directory the code is in


Conceptually:
=============
With increasing amounts of buzz and ink spilled over the concept and practice of neural networks,
deep learning, machine learning and artificial intelligence, this project aimed to try and demystify the "black box"
nature of these concepts. At its' base, it breaks away from traditional ideas of programming strict rules for a 
program to execute its' functional purpose, instead of providing rules, we prodive data and rules for interpolating
that data, while the program fine tunes a probabilistic model for selecting an output.


The convolution neural network is an ideal candidate for general image recognition tasks.
Commonly used for pixelated images in greyscale (for our purposes, a 28x28 image
of handwritten numbers, with 784 total inputs, each with its own numerical value between 0 and 1
which represents the grayscale value of the input, 0 for black, 1 for white). From here on the parts of 
what makes these models work will be discussed and investigated into how and why they work the way they do.
Through this we can (hopefully) peel back the curtain and "look into" the black box of machine learning and gain 
a clearer picture of the way these models do what they do.

Starting out:
=============
Our basic model is concerned with one of the ten different handwritten digits that can be used as possible candidate
values for our output. Since each image is a 28 x 28 grid of greyscale pixels, our inputs will be exanded to that
28 x 28 = 784, and our outputs will number ten, again for each possible digit chosen by the model. We'll then use 
these nodes and connect each and every one via a link with a given weight assigned to it. 

Error is one of the core functionalities in ML models. Given target data (output we desire) and model output value
(selected by the model), we can calculate the difference or distance between the current output and expected output. 
This measurement is used as feedback which can adjust the way the model works on future runs. 

Error:
    Error value = (target value - output value)
    Correcting for error: (target + delta(target))x

Activation Function:
    

Weight:
    Each input signal has its associated weight which diminishes or amplifies
    the given inputs signal that travels to the other nodes

    Multiply each given weight by the output signal from the previous node,
    sum them, and use that value as the x value in the sigmoid function

Learning rate determines the step size of the gradient descent in the loss function. 
Gradient descent is an iterative process that finds local function minima. What is of interest here
is analyzing the local function minima through the dependent variable (the error that is output) stacked against
the independent variable (the link weights that will change over time).

Learning Rate:
    Modifiable value to parse the signal / noise ratio in numerous
    iterative refinements

Matrices:
    In constrast to singular (scalar) values, matrix values (vectors) described
    in this context form a 2d array between link weights and input / output values

    Having two input nodes...

          Matrix 1          Matrix 2
        W 1,1 ; W 2,1        Input 1
        W 1,2 ; W 2,2        Input 2

        Through matrix multiplication:
        (Weight1,1 * Input 1) + (Weight 2,1 * Input 1)
        (Weight1,2 * Input 2) + (Weight 2,2 * Input 2)

        Will give us our x value for the sigmoid activation function for
        each node

Hidden Layer:
    Where the "deep" of deep learning introduces itself. With hidden layers
    we have successive layers of representation that can further prune model output.


    Any layer of nodes that is between the initial input and final output
    layer of nodes, used to further tune and moderate link weights and 
    the final signal

Backpropogation:
    In order to modify link weights succefully in a way that does not
    overfit the error, proportional weight tuning via backpropogation is used

    Our earlier error function is used here, as we have the target (expected) data
    and the output signal 
