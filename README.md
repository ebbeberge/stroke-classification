# :hospital: Predicting Stroke 
## with Artifical Neural Networks, Ensamble-Methods, and Explainable Artificial Intellegence

## Table of Contents
1. [TL;DR: Predicting Stroke with Advanced Statistical Methods](https://github.com/ebbeberge/stroke-classification#tldr-predicting-stroke-with-advanced-statistical-methods)
2. [About the Dataset](https://github.com/ebbeberge/stroke-classification#about-the-dataset)



## TL;DR: Predicting Stroke with Advanced Statistical Methods

We analyze a stroke dataset and formulate various statistical models for predicting whether a person has had a stroke based on measurable predictors.

| Team Members in Alphabetical Order | Email | 
|---------|-----------------|
| Eirik Berge | eirik.berge@ntnu.no |
| Camilla Idina Jensen Elvebakken| cielveba@stud.ntnu.no |
| Martin Ludvigsen | martilud@ntnu.no |

To install the needed package dependencies, simply run `pip install -r requirements.txt`

## About the Dataset

The dataset stems from <a href=https://www.kaggle.com/fedesoriano/stroke-prediction-dataset> Kaggle - Stroke Prediction </a> and records several details about over 5000 patients along with whether they have experienced a stroke. The complete list of recorded variables of the patients are:

* **id**: unique identifyer
* **gender**: gender of the patient (*Male*, *Female*, *Other*)
* **age**: age of the patient
* **hypertension**: if the patient has hypertension or not (1,0)
* **heart_disease**: if the patient has a heart disease or not (1, 0)
* **ever_married**: if the patient was ever married (*No*, *Yes*)
* **work_type**: what kind of work the patient has (*Children*, *Govt_job*, *Never_worked*, *Private*, *Self-employed*)
* **residence_type**: what type of place the patient lives in (*Rural*, *Urban*)
* **avg_glucose_level**: average glucose level in blood
* **bmi**: body mass index
* **smoking_status**: smoking status of patient (*formerly smoked*, *never smoked*, *smokes*, *Unknown*)
* **stroke**: if the patient has had a stroke or not (1, 0)
