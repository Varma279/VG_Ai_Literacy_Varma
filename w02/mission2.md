# Mission 2 — Understanding Data

## 1. Basic Data Concepts

| Term                 | Explanation                                                   | Example                                   |
| -------------------- | ------------------------------------------------------------- | ----------------------------------------- |
| Dataset              | Information collected together for analysis                   | Records of several production cycles      |
| Sample / Observation | A single entry within a dataset                               | Data recorded during one production cycle |
| Feature              | A property that helps describe or analyse an observation      | Operating temperature                     |
| Label / Target       | The outcome a model is expected to determine                  | Whether a production cycle succeeds       |
| Structured Data      | Information arranged according to a defined format            | Rows of sensor readings in a spreadsheet  |
| Unstructured Data    | Information that does not follow a standard tabular structure | Photographs of electronic components      |
| Numerical Feature    | A measurable quantity represented by a number                 | Processing time = 15 minutes              |
| Categorical Feature  | Information that identifies a class or category               | Equipment category = B                    |

In this exercise, the model uses `temperature_C`, `runtime_min`, and `machine_type` as its input features. The `result` column represents the target that the model attempts to predict.

## 2. Example Dataset for Practice

The following table contains hypothetical production records created for learning purposes. It does not represent actual industrial measurements.

| Run ID | Temperature (°C) | Runtime (min) | Machine Type | Production Result |
| -----: | ---------------: | ------------: | ------------ | ----------------- |
|    101 |               24 |             9 | A            | Pass              |
|    102 |               28 |            11 | A            | Pass              |
|    103 |               36 |            19 | B            | Fail              |
|    104 |               32 |            17 | B            | Fail              |
|    105 |               26 |            10 | A            | Pass              |
|    106 |               39 |            21 | B            | Fail              |

### Understanding the table

* **Input features:** Temperature, runtime, and machine type provide information about each production run.
* **Target variable:** Production result indicates whether a run passed or failed.
* **Labelled dataset:** The outcome is available for every observation, allowing a model to learn from previous examples.
* **Unlabelled dataset:** The same records are available without their outcomes. A model could use the remaining information to make predictions, but the correct answers are not provided in advance.

For example, a machine-learning model could examine earlier production records to discover patterns associated with successful or unsuccessful runs. It could then estimate the result of a new run using its input features. However, this small dataset alone is insufficient to establish a reliable relationship between the measurements and the outcome.

## 3. Different Forms of Data

| Data Category     | Example                                                  | How It Can Be Used                                                                                 |
| ----------------- | -------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| Structured Data   | Timing reports containing delay values and clock periods | Predicting whether a circuit may satisfy timing requirements                                       |
| Unstructured Data | Photographs captured during semiconductor inspection     | Identifying potential manufacturing defects using an appropriately trained image-recognition model |

Structured data is generally easier to organise into tables and analyse using conventional data-processing methods. Unstructured data, such as images and audio, often requires specialised processing to extract useful information.

The appropriate approach depends on the problem being solved and the information available.

## 4. Why Data Quality Matters in Machine Learning

The usefulness of a machine-learning model depends heavily on the quality of the examples provided during training.

**1. Incomplete information**

Suppose a production record contains runtime information but has no temperature measurement. If many records have missing values, the model may struggle to identify useful patterns. Depending on the situation, missing information may need to be investigated, corrected, or handled using an appropriate preprocessing method.

**2. Incorrect outcomes**

Imagine that a production cycle failed, but its recorded result says “Pass.” The model may learn from this incorrect example and make less reliable predictions. Checking the accuracy of labels is therefore important.

**3. Measurement errors**

A malfunctioning sensor might record a temperature of 350°C when the actual temperature is 35°C. Such an unrealistic measurement can distort the patterns learned by the model unless the error is identified and handled appropriately.

**4. Insufficient variety**

Suppose the training dataset contains records exclusively from Machine A, but the model is later used with Machine B. Differences between the machines may cause the model to perform poorly on the new data.

**5. Biased or unrepresentative samples**

If the training examples do not reflect the conditions under which the model will actually operate, its predictions may not generalise well to real-world situations.

### Key takeaway

A large dataset is not necessarily a good dataset. Reliable machine learning requires relevant observations, accurate measurements, consistent labels, and sufficient representation of the conditions the model is expected to encounter.

Before training a model, it is important to examine where the data came from, whether its values are trustworthy, and whether it represents the intended application.
