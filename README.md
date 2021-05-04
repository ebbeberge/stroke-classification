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

## About Stroke and the Dataset

<img align="right" height="300px" src="stroke.jpg">

A stroke is a condition where the blood flow to the brain is decreased, where the lack of blood flow causes cell death in the brain. One can roughly classify strokes into two main types: ```Ischemic stroke```, which is due to lack of blood flow, and ```hemorrhagic stroke```, due to bleeding. Both of the varients causes the brain to stop functioning properly. As strokes are one of the leading causes of death, it is of vital imporantance to understand the condition, as well as being able to predict the condition in advanced so that preventory measures can be taken to decrease the change. If you suspect that someone is experiencing a stroke (due to e.g. struggling to say simple complete sentences, or struggling to smile), then call your respective immergency number (in Norway: 113) immediately. For more information about the illness (in Norwegian), see

<a href=https://www.helsenorge.no/sykdom/hjerneslag/hjerneslag-arsaker/#ring-113-umiddelbart> Helsenorge - Stroke (Hjerneslag) </a>

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

## Data Exploration

In the data, there are 201 patients where their ```bmi``` has not been reported. Due to this being a possible relevant variable, we have chosen to remove these patents since they only consitute 4% of the total amount of patients. For the variable ```gender```, there are the three options <b>Male</b>, <b>Female</b>, and <b>Other</b>. Since there is only 1 patient whom is registered with the gender <b>Other</b>, we must unfortunately discard this patient as we will not be able to use this information in a statistical significant way. The variable ```smoking_status``` has the options <b>never smoked</b>, <b>formerly smoked</b>, <b> smokes</b>, and <b>unknown</b>. Since there are a significant amount of patents registered with <b>unknown </b> as their smoking status, we have choosen to include these patents in the study.

The following histogram shows the age distribution of the patents that have experienced a stroke:

<p align="center">
  <img height="400px" src="age_distribution.png">
</p>

We see that more old people than young people have strokes, while we seem to have a good representation of all ages in the dataset. Hence it seems that ```age``` will be an important predictor for predicting ```stroke```. We end this section by showing a heatmap of the correlation between the different variables:

<p align="center">
  <img height="400px" src="corrplot.png">
</p>

We see from the heatmap above that the response ```stroke``` does not seems particularily correlated with any of the predictors. Thus the choice of non-linear models such as ensembles and neural networks is well motivated. When using methods with the assumtion that the features are independent we have to be careful though - many of the features are highly correlated with each other, for example ```age```, ```ever_married``` and ```children```.
