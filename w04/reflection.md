# Week 04 — Learning Reflection

## 1. What I Learned

This week helped me understand the fundamentals of deep learning and how neural networks learn patterns from data. I learned how raw data is prepared, labelled, and used for training a model. I also understood the differences between traditional machine learning and deep learning, and how neural networks use input layers, hidden layers, neurons, weights, biases, and activation functions to process information.

I learned the training process, including forward propagation, loss calculation, backpropagation, and parameter updates. Through the TensorFlow Playground experiment, I observed how changing input features, hidden layers, and neurons affects the decision boundary and the network's ability to classify data.

## 2. What Was Difficult?

Initially, I found it difficult to understand the coloured regions, data points, and decision boundaries in TensorFlow Playground. I was also confused about how additional input features such as X1², X2², and X1 × X2 influence the network.

After experimenting with different network configurations, I understood that these features provide additional information about the same data point and help the network learn different patterns.

## 3. What Surprised Me?

I was surprised that increasing the number of hidden layers and neurons does not automatically guarantee better results. The quality of the dataset, selected features, and training process also influence model performance.

I also learned that a model can perform well on training data but still fail to generalise to unseen data.

## 4. Connection to VLSI Physical Design

The engineering case study helped me understand how deep learning could be applied to routing congestion prediction in VLSI Physical Design.

A neural network could learn patterns from placement information, cell density, and routing data to identify potential congestion hotspots before detailed routing.

This made me realise that deep learning could become a useful supporting technology for EDA tools and physical design engineers.

## 5. What I Still Need to Understand

* How neural networks calculate weights and biases mathematically.
* How different activation and loss functions affect training.
* How to select an appropriate network architecture.
* How to implement neural networks using Python and TensorFlow.
* How machine learning and reinforcement learning can be applied to automate physical design tasks.

## 6. What I Will Do Differently Next Time

I will focus more on understanding the data and experiment settings before increasing network complexity. I will also record actual training results, compare configurations, and evaluate predictions using unseen data rather than relying only on visual observations.

## 7. Final Reflection

Week 04 gave me a foundation in deep learning and helped me connect theoretical concepts with practical experimentation. I now understand the basic working process of a neural network and how it learns from data. Most importantly, I started seeing how these concepts could be applied to real engineering problems, especially VLSI Physical Design. I want to continue learning Python, machine learning, and reinforcement learning to eventually explore intelligent automation of EDA tools and physical design workflows.
