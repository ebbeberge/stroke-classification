# :hospital: Classifying Stroke with Artifical Neural Networks
We analyze a stroke dataset and formulate neural network models for predicting whether a person has had a stroke based on measurable predictors.

| Team Members in Alphabetical Order | Email | 
|---------|-----------------|
| Eirik Berge | eirik.berge@ntnu.no |
| Camilla Idina Jensen Elvebakken| cielveba@stud.ntnu.no |
| Martin Ludvigsen | martilud@ntnu.no |

To install the needed package dependencies, simply run `pip install -r requirements.txt`

Dataset is downloaded from: https://www.kaggle.com/fedesoriano/stroke-prediction-dataset

Variables:
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
