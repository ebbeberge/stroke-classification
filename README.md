# :hospital: Predicting Stroke 
## with Artifical Neural Networks, Ensamble-Methods, and Explainable Artificial Intellegence

## Table of Contents
1. [TL;DR: Modeling Water Flow in Eggafossen](https://github.com/ebbeberge/water-flow-modeling#tldr-modeling-water-flow-in-eggafossen)
2. [Files and Dependencies](https://github.com/ebbeberge/water-flow-modeling#files-and-dependencies)
3. [Water Flow & Water Level in Norwegian Rivers](https://github.com/ebbeberge/water-flow-modeling#water-flow--water-level-in-norwegian-rivers)
   - [General About Water Flow and Water Level](https://github.com/ebbeberge/water-flow-modeling#general-about-water-flow-and-water-level)
   - [Eggafossen](https://github.com/ebbeberge/water-flow-modeling#eggafossen)
   - [The HBV model](https://github.com/ebbeberge/water-flow-modeling#the-hbv-model)
4. [A Brief View of the Eggafoss Data](https://github.com/ebbeberge/water-flow-modeling#a-brief-view-of-the-eggafoss-data)
5. [Models Developed](https://github.com/ebbeberge/water-flow-modeling#models-developed)
6. [Conclusions](https://github.com/ebbeberge/water-flow-modeling#conclusions)


## TL;DR: Predicting Stroke with Advanced Statistical Methods

We analyze a stroke dataset and formulate various statistical models for predicting whether a person has had a stroke based on measurable predictors.

| Team Members in Alphabetical Order | Email | 
|---------|-----------------|
| Eirik Berge | eirik.berge@ntnu.no |
| Camilla Idina Jensen Elvebakken| cielveba@stud.ntnu.no |
| Martin Ludvigsen | martilud@ntnu.no |

To install the needed package dependencies, simply run `pip install -r requirements.txt`

## Abot the Dataset

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
