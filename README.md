# Predicting Functional Abdominal Pain

Chronic abdominal pain is one of the top three pain complaints in youth and often leads to significant impairment, distress, and health care use. Recent work has been done to classify pediatric abdominal pain into three subgroups, High Pain Dysfunctional (HFD), High Pain Adaptive (HPA), and Low Pain Adaptive (LPA) and assess the efficacy of two different internet-delivered treatment methods for each subgroup.

The cognitive behavioral therapy (CBT) and pain management education (EDU) treatments were both internet-delivered to a 268 patients. The study showed CBT to be much more effective in managing symptoms/challenges of High Pain Dysfunctional (HPD) patients while the easier, less intensive PM had equivalent results for the other two subgroups (HPA, LPA).

One challenge to applying these findings in a clinical setting is that in order to classify a patient into one of these subgroups requires upwards of 100 questions. For a clinical setting, this needs to be in the 20-30 range.


## Goal
Predict how a given adolescent symptoms may change as a result of treatment for each of the three outcome measures outlined below. In addition, we will be trying to reduce the overall number of questions required to make these predictions (feature selection).

To accopmish this, we will used the pre/post treatment summary measures from our outcome variables (below) in addition to all questions answered pre-treatment.

* Children’s Somataic Somatization Inventory, GI (CSI GI) - Averaged score across 7 questions
* Abdominal Pain Index (API) - Averaged score across 4 questions
* PROMIS Pain Interference (cPrinter) - Summed total across 8 questions


## About the Files
---
Each of our differnet approaches are broken out into separate Jupyter notebook files.

`00-process-data.ipynb` -- Initial data cleaning and processing (e.g. standardizing column names and null values). Creates up to 4 CSVs with combinations of rescaled or non-rescaled data inclduing or excluding records with missing values. After testing each dataset, the non-rescaled without missing values performed the best and is what was used in the other Jupyter Notebooks

`10-modeling-linear.ipynb` -- Regularized linear regression and mutual informaion gain (regression). Did not perform particularly well.

`20-modeling-rf-regression.ipynb` -- Out-of-Bootstrap Random Forest Regression. All predictions, models, and seeds have been saved to reproduce the results. Message Teddy for access.

`30-modeling-classification.ipynb` -- All classification work, including determing the clinically significant change classification. All predictions, models, and seeds have been saved to reproduce the results. Message Teddy for access.
