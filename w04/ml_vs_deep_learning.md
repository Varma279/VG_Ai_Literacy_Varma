# Mission 2: What Makes Deep Learning Different?

## 1. Introduction

Artificial Intelligence (AI) is the broad field of creating systems that perform tasks requiring intelligent behaviour. Machine Learning (ML) is a branch of AI in which systems learn patterns from data. Deep Learning (DL) is a branch of ML that uses neural networks with multiple layers to learn complex patterns.

Neural networks are computational models made up of interconnected units called neurons. They learn by adjusting their parameters based on training data.

## 2. Comparison of Different Approaches

| Approach                     | How It Works                                                                         | Example                                                                           | Limitation                                                  |
| ---------------------------- | ------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| Rule-Based System            | Follows predefined rules written by humans.                                          | Flag a semiconductor image if a measured dark region exceeds a threshold.         | May fail when conditions differ from the programmed rules.  |
| Traditional Machine Learning | Learns patterns from data using an algorithm, often with manually selected features. | Predict chip failure using temperature, voltage, and current measurements.        | Performance depends on data quality and feature selection.  |
| Deep Learning                | Uses multilayer neural networks to learn complex patterns from data.                 | Detect scratches and other defects directly from semiconductor inspection images. | May require more training data and computational resources. |

## 3. How Neural Networks Learn

A neural network typically consists of three types of layers:

* **Input layer:** Receives numerical data.
* **Hidden layers:** Process information and learn useful patterns.
* **Output layer:** Produces a prediction.

During training, the network makes predictions and compares them with the correct answers. An optimisation process adjusts its learnable parameters to reduce prediction errors.

For example, when trained on labelled semiconductor inspection images, a neural network can learn patterns that help distinguish defective images from non-defective ones.

## 4. Why Deep Learning Is Useful

Deep learning is useful for complex data such as images, audio, and text because it can learn useful representations from the data rather than relying entirely on manually designed features.

Examples include:

* **Images:** Detecting defects in semiconductor inspection images.
* **Audio:** Recognising spoken words.
* **Text:** Classifying messages as spam or non-spam.

However, deep learning is not always the best choice. Adding more layers does not automatically improve accuracy. A deeper network may require more resources, take longer to train, or overfit the training data.

## 5. When Are Simpler Approaches Better?

Rule-based systems or traditional ML models may be preferable when:

* The problem can be solved using clear, reliable rules.
* The available dataset is small.
* The input consists of structured numerical data.
* Computing resources are limited.
* A simpler model already meets the required performance.

For example, a predefined temperature threshold may be sufficient to flag an overheating device. A deep neural network would be unnecessary if a simple rule solves the problem reliably.

## 6. Example Outside Semiconductors

**Email Spam Detection**

A rule-based system may flag emails containing predefined suspicious phrases. A traditional ML model can learn from features such as word frequencies and sender information. A deep-learning model can learn more complex patterns in email text.

The best approach depends on the available data, performance requirements, and computational resources.

## 7. Conclusion

Rule-based systems follow predefined instructions, traditional ML models learn from data, and deep learning uses multilayer neural networks to learn complex patterns.

Deep learning can be valuable for semiconductor defect detection, but greater model complexity does not guarantee better results. The most suitable approach is the one that meets the engineering requirements reliably and efficiently.
