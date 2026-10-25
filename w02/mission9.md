# Mission 9 — Semiconductor Case Study: Predicting Chip Power Consumption

## 1. Engineering Problem

During chip design, engineers estimate power consumption to ensure the design operates within its power budget. Machine learning could help estimate power consumption from previous design runs and identify configurations that may require further investigation.

This is a proposed educational example, not a claim that a particular company uses this exact system.

## 2. Data Required

| Input Feature      | Description                               |
| ------------------ | ----------------------------------------- |
| Cell count         | Number of cells used in the design        |
| Switching activity | How frequently signals change state       |
| Clock frequency    | Operating clock speed                     |
| Supply voltage     | Voltage supplied to the circuit           |
| Design utilization | Percentage of core area occupied by cells |
| Target value       | Measured power consumption of the design  |

Only permitted data should be used. Confidential company designs and proprietary reports must not be uploaded to public repositories.

## 3. Proposed ML Approach

| Component       | Description                                                                      |
| --------------- | -------------------------------------------------------------------------------- |
| Objective       | Estimate power consumption before further design investigation                   |
| Task type       | Regression                                                                       |
| Learning method | Supervised learning using historical runs with measured power values             |
| Model output    | Estimated power consumption                                                      |
| Evaluation      | Compare predicted power against actual measurements using suitable error metrics |
| Baseline        | Compare against a simple estimate or existing prediction method                  |
| Human review    | Engineers verify the estimates before making design decisions                    |

## 4. Basic Workflow

```mermaid
flowchart LR
    A[Historical Design Data] --> B[Clean and Prepare Data]
    B --> C[Train Regression Model]
    C --> D[Test with Unseen Designs]
    D --> E[Estimate Power Consumption]
    E --> F[Engineer Reviews Results]
```

## 5. Limitations and Verification

* **Inaccurate measurements:** Incorrect training values may lead to unreliable estimates.
* **Limited data:** A model trained on a narrow range of designs may not work well on different circuits.
* **Changing conditions:** Different libraries, operating voltages, or design configurations may affect predictions.
* **Prediction error:** Estimated power may differ significantly from actual power.
* **Engineering review:** The model should assist engineers, not replace power analysis or design sign-off.

## 6. Evidence and Source Distinction

This case study illustrates a possible application of regression in semiconductor design. Its workflow is a proposed example and should not be interpreted as evidence of a deployed industrial system.

To support the study, consult technical publications on machine-learning-based power estimation in VLSI design and Google's ML resources on regression and model evaluation. Any specific claim about a real implementation should be verified against the relevant publication.

## Sources

Refer to `sources.md` for supporting references on machine learning, regression, and semiconductor power estimation.
