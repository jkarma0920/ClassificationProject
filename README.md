# Classification Modeling: NYC Poverty Status
Jay Kim

## Task:
Aim: To identify classifier models to predict whether an individual is or is not officially in poverty
(according to NYC government terms).
* Citywide poverty rate fell to 19% in 2017 from 20.6% in 2014...(but)
* 839,705 city students (74% of total student population) qualify for free or reduced-priced lunches, a common poverty marker and the highest percentage in over five years.
* One reason: new classification practices that have improved the ability to identify low-income kids.
* One of a growing class of city-wide datasets (via NYC OpenData)

## Data Sources & Data Science Tools
__Sources__
* NYC Open Data ("NYCgov_PovertyStatus_2017")
* Future Development: will join additional external tables- demographic, income, time data

__Classifier Models__
* Logistic Classifier
* KNN
* Decision Tree
* Random Forest
* Adaboost & XGBoost

__Additional Tools__
* SMOTE
* PCA
* GridSearchCV


__Baseline Data = 68,094 total samples__
<p align='center'>
<img src="Images/Pov1.png" width="600" height="350">
<img src="Images/PovZZ.png" width="700" height="600">
</p>

* _12,109 (~17%) qualified for Poverty Status_

__Calculating Poverty Status: Income vs. Poverty Threshold__
* _If Income < Poverty Threshold, individual qualifies for Poverty Status_
* _If Income > Poverty Threshold, individual does *not* qualify for Poverty Status_
* _Sample scales up to entire NYC Population (multiplied by specific weights for individual or household)_


<img src="Images/Pov3.png" width="800" height="600">
<img src="Images/Pov4.png" width="800" height="600">

## Challenges
Data:
* Inconsistent
* Multi-Indexed variables
Models:

## Modeling Overview
Logistic Regression
* Under- / Over-Fit
* Confounding Variables, Multicollinearity
* Class Imbalance
K-Nearest Neighbors (KNN)
<img src="Images/Pov56.jpg" width="900" height="250">

Decision Tree
<img src="Images/Pov7thruA.png" width="900" height="600">

Feature Importances (Decision Tree vs. Random Forest)
<img src="Images/PovAABB.png" width="800" height="400">


## Final Metrics
Currently, Inconclusive Results
* Cross Validation metrics were okay, but not much better than Dummy Classifier
* To be continued:
_(even) deeper dive into data_
_Many more iterations of tuning hyper-parameters_

<img src="Images/PovCC.png" width="1100" height="175">

![issues](Images/PovDD.png "DD Plot")

## Conclusions and Recommendations: Much Room for Improvement
__For me: more to come!__
_- Maximize Precision or Recall?_
   _(which is more tolerable- FP or FN?)_

__For NYC’s system:__
_- Slim down + Optimize bureaucracy-laden data structure
- Potential as Keystone / Connector Data
- Predictive Power, Systemic “Nudges”
