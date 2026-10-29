# Mission 5: Experiment and Observe

## Objective

To understand how input features, hidden layers, and neurons affect a neural network's ability to classify data using the TensorFlow Neural Network Playground.

**Tool:** [TensorFlow Neural Network Playground](https://playground.tensorflow.org/)

## Experiment 1: Basic Neural Network

### Configuration

| Parameter               | Value  |
| ----------------------- | ------ |
| Dataset                 | Circle |
| Noise                   | 0%     |
| Training data           | 50%    |
| Testing data            | 50%    |
| Input features          | X1, X2 |
| Hidden layers           | 1      |
| Neurons in hidden layer | 4      |
| Activation function     | Tanh   |
| Learning rate           | 0.03   |
| Regularization          | None   |
| Training iterations     | 1,000  |

### Observations

* The input features X1 and X2 represent the two coordinates of each data point.
* The dots represent the actual training examples and their classes.
* The background colours show the classes predicted by the neural network.
* The boundary between background colours is the decision boundary.
* With one hidden layer and four neurons, the network has limited flexibility to learn complicated patterns.

**Conclusion:** A simple network can learn basic patterns, but its performance depends on whether its structure is sufficient for the selected dataset.

## Experiment 2: Increasing the Network Size

### Configuration

| Parameter                    | Value  |
| ---------------------------- | ------ |
| Dataset                      | Circle |
| Input features               | X1, X2 |
| Hidden layers                | 2      |
| Neurons in each hidden layer | 8      |
| Activation function          | Tanh   |
| Learning rate                | 0.03   |
| Regularization               | None   |
| Training iterations          | 2,000  |

### Observations

* The first hidden layer processes the input features.
* The second hidden layer processes the information produced by the first hidden layer.
* Increasing the number of neurons gives the network more flexibility to learn complex patterns.
* For a circular dataset, a sufficiently trained network can learn a curved decision boundary that separates the classes.
* Adding more neurons does not guarantee better results; the outcome also depends on the data, learning rate, and training process.

**Conclusion:** A larger network can learn more complex decision boundaries, but network size should match the problem.

## Experiment 3: Changing Input Features

### Configuration

| Parameter                    | Value                                       |
| ---------------------------- | ------------------------------------------- |
| Dataset                      | Circle                                      |
| Input features               | X1, X2, X1², X2², X1 × X2, sin(X1), sin(X2) |
| Hidden layers                | 2                                           |
| Neurons in each hidden layer | 8                                           |
| Activation function          | Tanh                                        |
| Learning rate                | 0.03                                        |
| Training iterations          | 2,000                                       |

### Example Input Values

Suppose a data point has:

* X1 = 0.6
* X2 = -0.4

The derived input features are:

| Feature | Calculation    |  Value |
| ------- | -------------- | -----: |
| X1      | Original input |  0.600 |
| X2      | Original input | -0.400 |
| X1²     | 0.6 × 0.6      |  0.360 |
| X2²     | -0.4 × -0.4    |  0.160 |
| X1 × X2 | 0.6 × -0.4     | -0.240 |
| sin(X1) | sin(0.6)       |  0.565 |
| sin(X2) | sin(-0.4)      | -0.389 |

*The trigonometric values are rounded to three decimal places.*

These values describe the same data point. They are additional features, not seven different training examples.

### Observations

* X1 and X2 provide the original coordinates.
* X1² and X2² provide information about the squared coordinates, which can help represent curved patterns.
* X1 × X2 represents an interaction between the two coordinates.
* The sine features provide additional nonlinear information.
* Changing the input features changes the information available to the network.
* The network must still learn suitable weights from the training data.

**Conclusion:** Input features influence what patterns a neural network can learn. More features are not automatically better; unnecessary features can make learning more difficult.

## Comparison of Experiments

| Experiment | Configuration                                          | Main observation                                            |
| ---------- | ------------------------------------------------------ | ----------------------------------------------------------- |
| 1          | 2 inputs, 1 hidden layer, 4 neurons                    | Simple network with limited flexibility                     |
| 2          | 2 inputs, 2 hidden layers, 8 neurons per layer         | Greater capacity to learn complex patterns                  |
| 3          | 7 input features, 2 hidden layers, 8 neurons per layer | Additional features provide more information about the data |

## What I Learned

1. Input features determine what information the neural network receives.
2. Hidden layers and neurons process the inputs to learn patterns.
3. The decision boundary shows how the trained network separates predicted classes.
4. Training adjusts weights and biases to reduce prediction errors.
5. A more complex network does not necessarily produce better predictions.
6. The network should be evaluated on unseen data to check whether it generalises beyond its training examples.

## Final Conclusion

This experiment helped me understand how input features and network architecture affect classification. By changing the number of hidden layers, neurons, and input features, I could observe changes in the predicted decision boundary. I learned that successful neural network training depends not only on network size but also on the quality of the data, suitable features, and evaluation on unseen examples.

## Screenshots

Add screenshots of the following from your actual Playground experiment:

1. Experiment 1 — one hidden layer with four neurons.
2. Experiment 2 — two hidden layers with eight neurons each.
3. Experiment 3 — the additional input features enabled.

Each screenshot should show the selected configuration and the resulting decision boundary.
