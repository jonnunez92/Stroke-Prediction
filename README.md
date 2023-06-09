# Prediction of Stroke (Kaggle Dataset)

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

## Age by BMI
![Age by BMI](https://github.com/jonnunez92/Datasets-for-Modeling/blob/main/Age%20by%20BMI.png)
- Here we can see that as Age increases so does BMI
- Though, this does seem to plateau a bit at around 30 BMI

## Age by Hypertension with Heart Disease
![Age Hypertension](https://github.com/jonnunez92/Datasets-for-Modeling/blob/main/Age%20by%20Hypertension%20with%20Heart%20Disease.png)
- If you have Hypertension you are usually older, around 60-70
- If you have Heart Disease, you are most likely around 65 years old, but may or may not have Hypertension
- If you have no Hypertension and no Heart Disease, you are around 38 years old

## Stroke by Age
![Stroke by Age](https://github.com/jonnunez92/Stroke-Prediction/blob/main/Bargraph%20Stroke%20by%20Age.png)
- People that get strokes are, on average, older; around 65-70 years old
- People that don't get strokes are, on average, younger at around 40 years old

## Model Evaluation

- The best model overall is Tuned Under Sampling KNN
  - This dataset is very imbalanced so Under Sampling was used to account for this and balance the classes (positive and negative)
  - Then I was able to tune the KNN parameters to get the best possible results
  - This model maintained the higher `f1` and `accuracy` scores indicating that it is making correct predictions at a rate of 76% while at the same time keeping the False Negatives relatively low at a 38% rate.
    
- True Positives ('recall') is at 62%
  - Precision is at 11%, which means that there are a significant amount of False Positives, but recall is more important in this instance since falsely categorizing someone as 'not likely' to get a stroke is very harmful to the patient
- This is the model I would recommend
