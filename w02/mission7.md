# Mission 7 — Understand Why ML Systems Fail

The following examples illustrate common problems in machine learning, how to identify them, and what can be done to improve model reliability.

## 1. Common ML Failures and Solutions

| Situation                                                      | Possible Reason                                                 | How to Investigate                                | Recommended Solution                                                |
| -------------------------------------------------------------- | --------------------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------------------------- |
| A model predicts the wrong timing result for a new chip design | Training examples did not cover similar designs                 | Compare results from different design types       | Add representative data and evaluate the model on unseen designs    |
| Good products are incorrectly identified as defective          | Incorrect labels or unreliable measurements                     | Manually inspect selected samples                 | Fix labelling errors and improve data collection                    |
| A model performs well during testing but poorly in practice    | Information from the target or future data leaked into training | Examine input features and data-splitting methods | Remove leaked information and use an appropriate evaluation process |
| Predictions become less reliable over time                     | Operating conditions or input data have changed                 | Compare recent data with earlier records          | Monitor performance and retrain when necessary                      |

## 2. Data Bias and Human Review

**Data bias:** If a dataset mainly contains examples from one machine or operating condition, the model may perform poorly under different conditions. Testing performance across different groups can help reveal this problem.

**Human supervision:** Incorrect predictions can cause quality issues, additional costs, or faulty engineering decisions. Important results should therefore be checked by a qualified person before action is taken.

## 3. Key Takeaway

Machine learning systems can fail because of poor data, incorrect labels, data leakage, or changing real-world conditions. Regular evaluation, reliable datasets, and human oversight help reduce these risks.

## Sources

Refer to `sources.md` for Google ML Crash Course topics on data quality, fairness, generalisation, and production ML systems.
