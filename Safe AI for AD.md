___
# SAFE AI FOR AD
Links: [[Artificial Intelligence]]
Status: #🌳 
Tags: [[Automated Driving]]

<!--- Created on: 2023.10.26, 14:46 --->

 - Model the probability of an **action** conditioned on the realization of the **environment**.
 - Use ML to model the relation between both variables via knowledge representation and reasoning 
 - ML decisions are based on correlation, not causality --> safety challenge
___
# Taxonomy

| Term                         | Definition                                                                                                                                                                        |
| ---------------------------- |:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Intelligence                 | Ability to gain information from a potentially changing environment, store it as knowledge and use it to generate optimal behavior.                                               |
| [[Artificial Intelligence]]  | Study of creating machines, which can perform tasks that when performed by humans require intelligence, for the purpose of supporting or even replacing the humans at such tasks. |
| [[Perception]]               | Data processing to gain information and relevant cues.                                                                                                                            |
| [[Learning]]                 | Acquire new knowledge or modify existing the one.                                                                                                                                 |
| [[Knowledge Representation]] | Store what you know and what information you gain.                                                                                                                                |
| Deduction and Reasoning      | Infer over stores information.                                                                                                                                                    |
| [[Action]]                   | Generate and output based on the inference results.                                                                                                                               |
| Problem Space                | Logical framework of the problem that is solved by the ML solution                                                                                                                |
| [[Generalization]]           | Ability correctly classify previously unseen.                                                                                                                                     |
| Capacity / Model Capability  | Richness of the function space to which the ML solution belongs to.                                                                                                               |
| Empirical Risk               | Error in the Training Samples                                                                                                                                                     |
# Safety
## ML Failure Causes
- **Inappropriate Samples:**
	- Cannot approximate the probability density function of the problem space.
- **Distribution Shift:**
	- Data during inference is consistently different to the one seen during training. (e.g. image not sharp).
- **Corner Cases:**
	- Rare occurrences that were not in the data set.
- **Brittleness:**
	- Small input change equals large output changes. (e.g. dog becomes panda due to invisible image manipulation during classification)
- **Label Quality:**
	- Worse model performance due to wrong labels.
- **Wrong Metrics:**
	- Different behaviour depending on metrics. (e.g. FP, accuracy, ...)
- **Train/Test Data Split**
	- Independent and identically distributed samples are required in both sets
- **Unreliable Confidence**
	- Large confidence for false decisions. (calibration, watch dog, ...required)
- **Incomprehensible Behavior**
	- Exploitation of features that were not foreseen (correlation vs. causality)
## Safety via Generalization Capability
>[!info] Optimizing generalization capability leads to better performance and safety!
 
 - **ML works correlation-based**
	 - safety argumentation has to consist of data, development infrastructure and algorithm design
	 - follow sound ML design strategies
	 - do not ignore corner cases (long-tail of the distribution)
	 - address safety at inference time via calibration and watch dogs
 - **Generalization error can be theoretically upper-bounded**
	- e.g. via Vapnik-Chervonenkis (VC) Learning Theory, which covers the failure causes above:
		- bad data (size and quality)
		- poor development environment (i.i.d assumption)
		- empirical risk and capacity (design)
		![[Pasted image 20231026163600.png]]
# References
- [ISO-8800: Road Vehicles, Safety and Artificial Intelligence](https://www.iso.org/standard/83303.html)