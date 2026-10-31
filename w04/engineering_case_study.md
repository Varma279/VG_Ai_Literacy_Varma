# Engineering Case Study: Deep Learning for Routing Congestion Prediction in VLSI Physical Design

## 1. Engineering Problem

Routing congestion is a major challenge in VLSI physical design. During placement, standard cells and macros are positioned on the chip. If too many connections need to pass through a limited routing region, congestion can occur.

This may lead to routing difficulties, longer wirelength, timing degradation and additional design iterations.

The proposed solution is to use a deep learning model to predict possible routing congestion hotspots at an early stage of physical design, before detailed routing.

## 2. Input Data Required

The model could use the following physical design information:

* Placement information of standard cells.
* Macro locations and dimensions.
* Cell and pin density maps.
* Net connectivity information.
* Estimated wirelength.
* Routing resource availability.
* Global routing congestion information.

These inputs describe the physical and connectivity characteristics of the design.

## 3. Data Preparation and Labels

The collected placement and routing information would be converted into numerical features.

For example:

* Placement data can be represented as two-dimensional feature maps.
* Cell density and routing demand can be represented as numerical grids.
* Net connectivity can be represented as graph information.

Historical routing results can provide labels for training:

* Congested region.
* Non-congested region.

The dataset should be checked for incorrect labels, duplicate designs and missing information. It should also be divided into training, validation and test datasets.

## 4. Proposed Model and Prediction

A Convolutional Neural Network (CNN) could process placement and congestion feature maps to identify spatial patterns.

The model would predict a congestion map highlighting regions where routing problems may occur.

For example, it could identify a particular region of the chip as having a high probability of routing congestion.

The prediction could help physical design engineers investigate the floorplan, macro placement, cell density and placement strategy before detailed routing.

## 5. Why Deep Learning?

Deep learning may be useful because routing congestion depends on several interacting factors, including cell density, connectivity and available routing resources.

A CNN can learn spatial patterns from placement feature maps.

However, a traditional machine learning model or rule-based congestion estimation method should also be considered. These approaches may be sufficient for simpler designs and can be easier to interpret.

## 6. Evaluation on Unseen Data

The model should be evaluated using designs that were not included during training.

Possible evaluation measures include:

* Precision: How many predicted congestion regions were actually congested?
* Recall: How many actual congestion regions did the model identify?
* F1-score: A combined measure of precision and recall.
* False-positive rate: How often does the model incorrectly predict congestion?

Predictions should also be compared against actual routing results from established EDA tools.

## 7. Incorrect Predictions and Their Consequences

**False positive:** The model predicts congestion in a region where routing would actually be successful. This may cause unnecessary placement changes and additional design iterations.

**False negative:** The model fails to identify a region that later becomes congested. This may lead to routing failures, timing problems and additional engineering effort.

## 8. Human Review and Engineering Judgement

The model should support engineers rather than independently make final physical design decisions.

Physical design engineers must review predicted congestion hotspots, inspect routing reports, evaluate timing and analyse design constraints.

Final decisions should be based on actual implementation results and sign-off verification.

## 9. Research Evidence and Application Status

Published research has investigated machine learning and neural networks for predicting routing congestion during VLSI physical design.

A 2025 paper in the *Proceedings of the Institute for System Programming of the RAS* investigates neural-network-based routing congestion prediction using initial layout parameters.

An IEEE conference paper published in 2025 investigates graph neural networks for pre-routing congestion prediction.

These publications demonstrate research into this application. They do not establish that every commercial EDA tool uses the same model or workflow.

**My proposal:** A deep learning congestion prediction model could be developed using placement and routing data from suitable benchmark designs. Its predictions could be used as an additional guide during physical design, while conventional routing and sign-off tools remain necessary.

## Conclusion

This case study helped me understand how deep learning could support VLSI physical design. By learning patterns from previous placement and routing results, a model could help identify possible congestion problems earlier. However, its predictions must be verified using actual EDA implementation and routing results. Deep learning should assist engineering judgement rather than replace it.
