# Mission 6 — Understand Evaluation and Generalisation

## 1. Understanding Data Splits and Model Performance

| Concept         | What It Means                                                          | Example                                                 |
| --------------- | ---------------------------------------------------------------------- | ------------------------------------------------------- |
| Training Data   | Examples from which a model learns                                     | Previous machine inspection records                     |
| Validation Data | Data used to compare models and adjust settings                        | Checking which model works better                       |
| Test Data       | Independent data used to check the final model                         | Evaluating the model on new inspection records          |
| Generalisation  | How well a model handles unfamiliar data                               | Detecting defects in newly manufactured chips           |
| Overfitting     | When a model performs well on training data but poorly on new examples | Recognising familiar defects but missing new ones       |
| Underfitting    | When a model fails to learn important relationships                    | Using a simple rule that misses complex defect patterns |

A model should not be judged only by its training results. Separate validation and test data help reveal whether it has learned useful patterns or simply adapted too closely to its training examples.

## 2. Example: Evaluating a Machine Failure Model

Consider a factory dataset containing **100 machine operations**:

* 92 operations completed successfully.
* 8 operations experienced failures.

Suppose a model labels every operation as successful.

| Evaluation Measure  |     Result |
| ------------------- | ---------: |
| Total operations    |        100 |
| Correct predictions |         92 |
| Wrong predictions   |          8 |
| Overall accuracy    |        92% |
| Failures detected   | 0 out of 8 |
| Recall for failures |         0% |

The model appears effective because its accuracy is 92%. However, it cannot identify a single failed operation, making it unsuitable for detecting machine failures.

### Metrics Used to Evaluate a Model

* **Accuracy:** Measures the proportion of predictions that are correct.
* **Precision:** Indicates how often a predicted failure is actually a failure.
* **Recall:** Measures the proportion of actual failures successfully identified.
* **Confusion Matrix:** Displays the correct and incorrect predictions for each category.

For industrial applications, choosing an appropriate metric is important. Missing a machine failure could have a greater impact than raising an unnecessary warning.

## 3. Establishing a Baseline

A baseline is a simple prediction method used to judge whether a more advanced model provides real improvement.

For example, a system that always predicts the most common outcome can serve as a starting point. A trained model should outperform this simple approach on independent test data to demonstrate its practical value.

## Sources

Refer to `sources.md` for Google ML Crash Course topics covering model evaluation, classification metrics, and generalisation.
