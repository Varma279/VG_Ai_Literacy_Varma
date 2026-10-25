# Mission 4 — Understand ML Task Types

A **learning approach** explains how a model learns, while a **task type** describes what the model needs to do.

## 1. Examples of Machine Learning Tasks

| Problem                                | Task Type                | Input                   | Output                |
| -------------------------------------- | ------------------------ | ----------------------- | --------------------- |
| Detect unwanted messages               | Classification           | Email details           | Spam / Not Spam       |
| Predict house prices                   | Regression               | House size and location | Estimated price       |
| Group customers with similar interests | Clustering               | Customer preferences    | Customer groups       |
| Detect unusual electricity usage       | Anomaly Detection        | Electricity readings    | Unusual reading alert |
| Reduce many data columns               | Dimensionality Reduction | Large dataset           | Simplified data       |
| Suggest suitable movies                | Recommendation           | Viewing history         | Suggested movies      |
| Check whether a chip passes timing     | Classification           | Timing measurements     | Pass / Fail           |
| Estimate circuit delay                 | Regression               | Circuit design data     | Delay value           |

## 2. Learning Approach vs Task Type

These terms describe different things:

* **Classification:** Predicts a category, such as Pass or Fail.
* **Regression:** Predicts a numerical value, such as circuit delay.
* **Clustering:** Groups similar data points without predefined labels.
* **Supervised Learning:** Learns from examples that already have correct answers.

For example, a model can use supervised learning to classify a chip's timing result as Pass or Fail.

**Key takeaway:** The task type depends on the problem we want to solve, while the learning approach depends on how the model learns from data.

## Sources

Refer to `sources.md` for Google ML Crash Course materials on classification and regression.
