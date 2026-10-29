# Mission 4: How Does a Neural Network Learn?

## 1. Introduction

A neural network learns by adjusting its internal parameters to reduce prediction errors. During training, it makes predictions, compares them with the correct answers, and updates its parameters to improve future predictions.

This process involves a forward pass, loss calculation, backpropagation, and optimisation.

## 2. The Neural Network Learning Process

### 2.1 Forward Pass

During a forward pass, input data travels through the neural network's layers. The network uses its current weights, biases, and activation functions to produce a prediction.

**Example:** A semiconductor inspection image enters the network, which predicts whether the image contains a defect.

### 2.2 Loss Function

A loss function measures how different a model's prediction is from the target answer.

For example, if the correct label is `Defect` but the model predicts `No Defect`, the loss function measures the prediction error according to the chosen loss calculation.

A lower loss generally indicates better agreement between predictions and target values for the examples being evaluated.

### 2.3 Backpropagation

Backpropagation calculates how the model's parameters contributed to the loss by computing gradients. These gradients provide information about how changes to the parameters may affect the loss.

### 2.4 Optimisation

An optimisation algorithm, such as gradient descent, uses the gradients to update the model's parameters in an attempt to reduce the loss.

The forward pass, loss calculation, backpropagation, and parameter updates are repeated during training.

### 2.5 Epoch

An epoch is one complete pass through the training dataset.

A model is commonly trained for multiple epochs so that its parameters can be updated repeatedly using the training examples.

However, more epochs do not always improve performance on new data. Excessive training can cause overfitting.

## 3. Training vs. Inference

| Training                                       | Inference                                                   |
| ---------------------------------------------- | ----------------------------------------------------------- |
| The model learns from training examples.       | The trained model makes predictions on new inputs.          |
| Parameters are updated during training.        | Parameters are normally kept fixed during prediction.       |
| Loss and optimisation guide learning.          | The model uses its learned parameters to produce an output. |
| Requires training data and a learning process. | Requires an input and a trained model.                      |

For example, training teaches a model to recognise patterns associated with semiconductor defects. Inference uses the trained model to predict whether a new inspection image may contain a defect.

## 4. Complete Learning Flowchart

```text
Input and Target Examples
          |
          v
     Forward Pass
          |
          v
      Prediction
          |
          v
    Loss Calculation
          |
          v
    Backpropagation
          |
          v
 Parameter Updates
   (Optimisation)
          |
          v
  Repeat Training
          |
          v
 Evaluate on Unseen Data
```

The training steps are repeated to improve the model. Evaluation on unseen data helps determine whether the learned patterns generalise beyond the training examples.

## 5. Applying the Process to Semiconductor Inspection

Imagine that a neural network initially misclassifies several semiconductor inspection images.

During training, the network processes each image and produces a prediction. The loss function compares that prediction with the correct label. Backpropagation calculates gradients, and the optimisation algorithm uses them to update the model's parameters.

By repeating this process, the model may learn patterns that help it classify images more accurately.

After training, the model should be evaluated on suitable unseen images to assess its performance.

### Problem 1: Incorrect Training Labels

If an image containing a defect is labelled `No Defect`, the model receives incorrect information. Repeated exposure to incorrectly labelled examples can negatively affect learning.

**Lesson:** Reliable training data and correct labels are important for effective learning.

### Problem 2: Good Training Performance but Poor Performance on New Images

This situation may indicate **overfitting**. The model may have learned patterns specific to its training data instead of patterns that generalise well to unseen images.

**Possible improvements:**

* Use representative training data.
* Apply suitable regularisation techniques.
* Monitor performance on validation data.
* Evaluate the final model using an independent test dataset.

## 6. Generalisation and Evaluation

Generalisation is the ability of a model to perform well on previously unseen data.

A model should not be considered reliable simply because it achieves high accuracy on its training dataset.

For semiconductor defect detection, evaluation should use suitable images that were not used to train or select the model. Metrics such as precision, recall, and a confusion matrix can help reveal different types of classification errors.

Human review may still be necessary, particularly when missing a real defect could have serious consequences.

## 7. Conclusion

A neural network learns through repeated prediction, loss calculation, backpropagation, and parameter updates. An epoch represents one complete pass through the training dataset.

Training adjusts the model's parameters, while inference uses the trained model to make predictions. Evaluating performance on unseen data helps determine whether the model has learned useful patterns rather than simply memorising its training examples.
