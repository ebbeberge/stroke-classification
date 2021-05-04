# :hospital: Predicting Stroke 
## with Artifical Neural Networks, Ensamble-Methods, and Explainable Artificial Intellegence

| Team Members in Alphabetical Order | Email | 
|---------|-----------------|
| Eirik Berge | eirik.berge@ntnu.no |
| Camilla Idina Jensen Elvebakken| cielveba@stud.ntnu.no |
| Martin Ludvigsen | martilud@ntnu.no |

To install the needed package dependencies, simply run `pip install -r requirements.txt`

## Table of Contents
1. [TL;DR: Predicting Stroke with Advanced Statistical Methods](https://github.com/ebbeberge/stroke-classification#tldr-predicting-stroke-with-advanced-statistical-methods)
2. [About the Dataset](https://github.com/ebbeberge/stroke-classification#about-the-dataset)

## TL;DR: Predicting Stroke with Advanced Statistical Methods

We analyze a stroke dataset and formulate various statistical models for predicting whether a patient has had a stroke based on measurable predictors. The goal is to, with the help of several easily measuable predictors such as ```smoking```,  ```hyptertension```, ```age```, to predict whether a person will suffer from a stroke. Since the data is heavily skewed (about 96% of the patients has never suffered a stroke), then we are forced to consider other measures that simply the accuracy of the model. As such, we develop various methods where we report both the accuracy, the recall, and the precision of the methods. 

The various methods with their properties are listed below. As can be seen from the diagram, some of the methods perform better than others with respect to different metrics. If a model should be used, it should carefully be considered whether high accuracy, precision, or recall is the most attractive property to have.

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

Unfortunately, the origin of the data is confidential, so we do not have any context regarding the data other than the variables listed above. In particular, we do not know the origin of the patients, nor do we know why the patients filled out the information we have been presented with. If the patients already had a sufficient medical history so that a e.g. a physician asked them to fill out the details presented, then this can heavily influence the data we have been given. With such little information about the data collected, the models we develop can only be used for illustrative/educational purposes. For furter development of the project, the focus should be on better data quality rather  than more advanced models.
