# Mission 1: Data Behind Deep Learning

## 1. Introduction

Deep learning models learn patterns from data. For image-based applications, such as semiconductor defect detection, the model uses images to identify whether a chip or wafer contains defects.

However, a neural network cannot directly understand an image in the same way a human does. The image must first be converted into numerical data and prepared for training.

This mission explains how raw images become a dataset that can be used to train, test, and evaluate a deep learning model.

## 2. How Images Become Numerical Data

A digital image consists of small units called **pixels**. Each pixel represents information about a particular location in the image.

In a grayscale image, pixel values commonly range from 0 to 255:

* `0` represents black.
* `255` represents white.
* Values between 0 and 255 represent different shades of gray.

For example, a small grayscale image can be represented as a matrix:

```text
[
  [  0,  50, 100],
  [150, 200, 255],
  [ 30,  80, 120]
]
```

A deep learning model processes these numerical values to identify patterns in the image.

For a colour image, each pixel commonly contains three values representing the red, green, and blue colour channels (RGB).

Therefore, an image is not just a picture. It is a collection of numerical values that a computer can process.

## 3. Data Preparation

Raw images may have different sizes, formats, quality levels, or unwanted information. Before training a model, the data must be prepared.

Common data preparation steps include:

| Step           | Purpose                                                                           |
| -------------- | --------------------------------------------------------------------------------- |
| Resizing       | Makes images consistent in dimensions when the model requires a fixed input size. |
| Cleaning       | Identifies corrupted, unusable, or irrelevant images.                             |
| Formatting     | Converts images into a format suitable for the model.                             |
| Normalisation  | Scales numerical values to a suitable range, often between 0 and 1.               |
| Label checking | Ensures that images have correct labels.                                          |

For example, pixel values ranging from 0 to 255 can be normalised by dividing each value by 255.

**Example:**

```text
Original pixel value = 128

Normalised value = 128 / 255

Normalised value ≈ 0.502
```

Normalisation can help make numerical inputs easier for a neural network to process.

Not every dataset requires exactly the same preparation steps. The process depends on the type of images and the model being used.

## 4. Labels and Examples

A labelled dataset contains examples paired with the correct answers, also called labels.

For semiconductor defect detection, the labels might be:

* `Defect`
* `No Defect`

Example dataset:

| Image         | Label     |
| ------------- | --------- |
| image_001.png | No Defect |
| image_002.png | Defect    |
| image_003.png | No Defect |
| image_004.png | Defect    |

During supervised learning, the model learns patterns from the images and their corresponding labels.

For example, if an image contains a visible scratch and is correctly labelled `Defect`, the model can use that example to learn patterns associated with defects.

The quality of the labels matters. Incorrect labels can teach the model incorrect patterns and reduce its performance.

## 5. Why Data Quality Matters

A deep learning model depends heavily on the quality and representativeness of its training data.

Two important data-related problems are incorrect labels and imbalanced datasets.

### Problem 1: Incorrect Labels

Suppose an image contains a semiconductor defect but is labelled `No Defect`.

The model receives incorrect information during training. If many examples have incorrect labels, the model may learn misleading patterns.

**Possible solution:**

Review the dataset and verify labels using reliable inspection results or expert review.

### Problem 2: Imbalanced Dataset

Suppose a dataset contains 1,000 semiconductor inspection images:

| Category  | Number of Images |
| --------- | ---------------: |
| No Defect |              900 |
| Defect    |              100 |
| **Total** |        **1,000** |

This dataset is imbalanced because images without defects greatly outnumber images containing defects.

A model may become biased towards predicting `No Defect` because that category appears much more frequently.

For example, a model that predicts `No Defect` for every image would achieve 90% accuracy on this dataset, but it would fail to detect any actual defects.

Therefore, accuracy alone may not provide a complete picture of model performance.

**Possible solutions:**

* Collect more representative defect images.
* Use suitable sampling or class-weighting techniques.
* Evaluate performance separately for each category.
* Examine metrics such as precision, recall, and the confusion matrix.

The appropriate solution depends on the dataset and the engineering requirements.

## 6. Training, Validation, and Test Datasets

A dataset is commonly divided into three parts.

| Dataset            | Purpose                                                                                     |
| ------------------ | ------------------------------------------------------------------------------------------- |
| Training dataset   | Used by the model to learn patterns from examples.                                          |
| Validation dataset | Used during development to evaluate the model and help select settings.                     |
| Test dataset       | Used to evaluate the final model on data that was not used for training or model selection. |

One possible split is:

* 70% for training
* 15% for validation
* 15% for testing

These percentages are examples, not fixed requirements. The appropriate split depends on the size and characteristics of the dataset.

The test dataset should remain separate from the training process. If test images influence model training or repeated model selection, the evaluation may no longer provide an independent estimate of performance.

For semiconductor inspection, images from the same wafer, inspection run, or production batch may be closely related. Where appropriate, data should be split in a way that prevents highly related images from appearing in both training and test datasets. Otherwise, the model's test performance may appear better than its performance on genuinely new data.

## 7. Complete Data Flow

The following flow illustrates how raw images become predictions that can be evaluated.

```text
Raw Images
    |
    v
Data Preparation
(Resize, Clean, Format, Normalise)
    |
    v
Labelled Dataset
(Defect / No Defect)
    |
    v
Dataset Splitting
(Training / Validation / Test)
    |
    v
Model Training
(Learn Patterns from Training Data)
    |
    v
Trained Model
    |
    v
Prediction on New Images
    |
    v
Evaluation
(Compare Predictions with Verified Labels)
```

### Explanation of Each Stage

1. **Raw Images:** Images are collected from semiconductor inspection systems.
2. **Data Preparation:** Images are cleaned, resized when necessary, formatted, and normalised.
3. **Labelled Dataset:** Each image is associated with an appropriate label.
4. **Dataset Splitting:** The data is divided into training, validation, and test sets.
5. **Model Training:** The model learns patterns from the training images and their labels.
6. **Trained Model:** The training process produces a model that can make predictions.
7. **Prediction:** The model processes new inspection images and predicts whether defects are present.
8. **Evaluation:** Predictions are compared with verified labels to measure model performance.

## 8. Key Learnings

From this mission, I learned that:

1. Digital images are represented as numerical pixel values.
2. Image data often needs preparation before it can be used for deep learning.
3. Labels provide the correct categories for supervised learning.
4. Incorrect labels can negatively affect the learning process.
5. Imbalanced datasets can cause a model to favour the more common category.
6. Training, validation, and test datasets serve different purposes.
7. A reliable evaluation requires test data that has not influenced model training or selection.
8. Data quality is an important factor in building a reliable deep learning model.

## 9. Conclusion

Data is the foundation of deep learning. Even a sophisticated neural network may perform poorly when trained on incorrect, unrepresentative, or imbalanced data.

In semiconductor defect detection, preparing reliable images, checking labels, creating appropriate dataset splits, and evaluating predictions are important steps towards developing a useful model.

Understanding the data pipeline provides a foundation for learning how neural networks are trained and how their performance can be improved.
