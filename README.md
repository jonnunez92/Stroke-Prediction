# Datasets-for-Modeling

by Jonathan Nunez | jon.nunez92@gmail.com
------------------------------------------
[Link to the Data (.csv)](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset/download?datasetVersionNumber=1)\
[Source of the Data](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)

### With these graphs and models, we can predict the likelyhood of stroke for our clients.

## Data Dictionary
1. id: unique identifier
2. gender: "Male", "Female" or "Other"
3. age: age of the patient
4. hypertension: 0 if the patient doesn't have hypertension, 1 if the patient has hypertension
5. heart_disease: 0 if the patient doesn't have any heart diseases, 1 if the patient has a heart disease
6. ever_married: "No" or "Yes"
7. work_type: "children", "Govt_jov", "Never_worked", "Private" or "Self-employed"
8. Residence_type: "Rural" or "Urban"
9. avg_glucose_level: average glucose level in blood
10. bmi: body mass index
11. smoking_status: "formerly smoked", "never smoked", "smokes" or "Unknown"*
12. stroke: 1 if the patient had a stroke or 0 if not
*Note: "Unknown" in smoking_status means that the information is unavailable for this patient


## Count of Smoking Status with Stroke Count
![Count of Smoking](https://github.com/jonnunez92/Datasets-for-Modeling/blob/main/Count%20of%20Smoking.png?raw=true)
- There are much more people that *don't* have strokes
- We can see that there are a significant amount of smokers
  - That being said, their rate of stroke is about the same as non-smokers

