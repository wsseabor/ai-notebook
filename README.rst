MNIST dataset can be found at http://yann.lecun.com/exdb/mnist/

Given code will work downloading from source and stashing it in a local folder


Conceptually:
-------------

The convolution neural network is an ideal candidate for general image recognition tasks.
Commonly used for images where each pixel of a given grid (for our purposes, a 28x28 image
of handwritten numbers, with 784 total inputs, each with its own numerical value between 0 and 1
which represents the grayscale value of the input, 0 for black, 1 for white).



Error:
    Error value = (target value - output value)
    Correcting for error: (target + delta(target))x

Learning Rate:
    - Modifiable value to parse the signal / noise ratio in numerous
    iterative refinements

Activation Function:
    -

Weight:
    -Each input signal has its associated weight which diminishes or amplifies
    the given inputs signal that travels to the other nodes
    - Multiply each given weight by the output signal from the previous node,
    sum them, and use that value as the x value in the sigmoid function

Matrices:
    - In constrast to singular (scalar) values, matrix values (vectors) described
    in this context form a 2d array between link weights and input / output values
    - Having two input nodes...

          Matrix 1          Matrix 2
        W 1,1 ; W 2,1        Input 1
        W 1,2 ; W 2,2        Input 2

        Through matrix multiplication:
        (Weight1,1 * Input 1) + (Weight 2,1 * Input 1)
        (Weight1,2 * Input 2) + (Weight 2,2 * Input 2)

        Will give us our x value for the sigmoid activation function for
        each node

Hidden Layer:
    - Any layer of nodes that is between the initial input and final output
    layer of nodes, used to further tune and moderate link weights and 
    the final signal

Backpropogation:
    - In order to modify link weights succefully in a way that does not
    overfit the error, proportional weight tuning via backpropogation is used
    - Our earlier error function is used here, as we have the target (expected) data
    and the output signal 
