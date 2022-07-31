# Heart-Failure-Prediction-Using-ANN
## Highlights
1. We observed the data attributes with plots for selecting the mains factors that truly increased the
probability of Heart failure.
2. By visualizing 4 features which have more correlation with Death_event.
3. We used 8 different models to see the accuracy and confusion matrix.
4. According to accuracy we select catboost, xgboost and Decision Tree are more optimized models to
predict more effectively.

## Introduction
1. Cardiovascular diseases kill approximately 17 million people globally every year, and they mainly
exhibit as myocardial infarctions and heart failures.
2. Heart failure (HF) occurs when the heart cannot pump enough blood to meet the needs of the body.
3. Available electronic medical records of patients quantify symptoms, body features, and clinical
laboratory test values, which can be used to perform biostatistics analysis aimed at highlighting
patterns and correlations otherwise undetectable by medical doctors.
4. Machine learning, in particular, can predict patients’ survival from their data and can individuate the
most important features among those included in their medical records.

## Data
### Columns description:
1. Anaemia: Decrease of red blood cells or hemoglobin (boolean)
2. Creatinine_phosphokinase: Level of the CPK enzyme in the blood (mcg/L)
3. Diabetes: If the patient has diabetes (boolean)
4. Ejection_fraction: Ejection fraction (EF) is a measurement, expressed as a percentage, of how much
blood the left ventricle pumps out with each contraction
5. High_blood_pressure: blood hypertension
6. Platelets: are a component of blood whose function (along with the coagulation factors)
7. Serum_creatinine: Serum creatinine is widely interpreted as a measure only of renal function
8. Serum_sodium: to see how much sodium is in your blood it is particularly important for nerve and muscle
function.

## Data Information
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 299 entries, 0 to 298
Data columns (total 13 columns):
 # Column Non-Null Count Dtype
--- ------ -------------- -----
 0 age 299 non-null float64
 1 anaemia 299 non-null int64
 2 creatinine_phosphokinase 299 non-null int64
 3 diabetes 299 non-null int64
 4 ejection_fraction 299 non-null int64
 5 high_blood_pressure 299 non-null int64
 6 platelets 299 non-null float64
 7 serum_creatinine 299 non-null float64
 8 serum_sodium 299 non-null int64
 9 sex 299 non-null int64
 10 smoking 299 non-null int64
 11 time 299 non-null int64
 12 DEATH_EVENT 299 non-null int64
dtypes: float64(3), int64(10)
memory usage: 30.5 KB

## Data Pre-Processing
Handling the missing values, We can see all the attributes have no null Values.

## Data Visualization
All the attributes are visualized to observe the distribution and relations.
1. Age
2. Distribution of AGE Vs DEATH_EVENT
3. Gender
4. Distribution of Gender Vs DEATH_EVENT
5. Distribution of Diabetes
6. Distribution of Ejection_factor
## Feature Selection
For selection of better attributes which helps to predict the Death_event, we
considering below key points,
1.  Before dealing with outliers we require knowledge about the outlier of the every features of the
dataset and possibly some domain knowledge that figure out the ranges of values.
2. Removing outliers with a good logic will always increase accuracy of the model.
3. With a deep understanding of what are the possible ranges that exist within each feature, removing
outliers becomes reasonable.
4. We observed the feature distribution and found that all the values in serum_creatinine, time,
ejection_fraction, serum_sodium are falls in possible range of values.So they are not outliers.
5. They are actual data points that helps in predicting DEATH_EVENT.

## Removing Outliers
1. Ejection_factor:
A. We can observed from the graph that there are two outliers.
B. The two outliers(70 and 80) removed from the dataset.

2. Serum_creatinine:
  We can see that there are more outliers, so we drop the feature.
## Correlation with Death_event

From graph of correlation we can observed that some of our features have correlation almost
equal to 0. We dropped all that feature in below:
1. Anaemia
2. Creatinine_phosphokinase
3. Diabetes
4. High_blood_pressure
5. Platelets
6. Sex
7. Smoking

We will select only 3 features : time, ejection_fraction, serum_creatinine.

## Models
We select only for most effective features that can predict the death_event. For predicting,
we train and test different types of machine learning models.They are listed below,

1. Logistic Regression.
2. K-Near Neighbour.
3. Support Vector Machine.
4. Decision Tree Classifier.
5. Random Forest Classification.
6. Artificial Neural Network.
7. Xgboost.

## Optimizing ANN model
The ANN model layer are shown below,
Input Layer, Hidden Layer-1, Hidden Layer-3, Hidden Layer-2, Hidden Layer-4, Output Layer
## We optimized the model with,
1. Creating more hidden layers.
2. Train the model with more dataset.
3. Increase the batch size to get more efficient output.
4. Using more epochs.
We can get upto 86% accuracy from the model.

## Model and Score
The accuracy of different models are tabulate
descending order in the right side table.
From table by compare score we can select the
particular model which is best for the data set.

## Model Score
1. xgboost 0.855556
2. catboost 0.855556
3. Decision Tree 0.844444
4. Logistic Regression 0.822222
5. Random Forest 0.822222
6. Support Vector Machines 0.811111
7. ANN 0.811111
8. KNN 0.800000

## Conclusion
We collect the data and went through steps that reach out our desired prediction. From data information
we saw the attributes of table with value ranges then we pre-processed the data to get good data set.
After observing the data distribution and outliers we select more effective feature and evaluate the
correlation with death_event feature. To predict the desire feature we tested eight different machine
learning models.
By comparing accuracy score and confusion matrix,We visualizing different models.The best accurate
models are KNN, Catboost, RandomForestClassifier that can be used to determine the Heart failure
prediction.
We predict the heart failure with more accurately by using and standardizing the models that helps to early
predict the patient by input selective medical test results.

## References
1. Improving risk prediction in heart failure using machine learning.
2. Machine learning can predict survival of patients with heart failure from serum creatinine and ejection fraction alone.
3. Predicting heart failure using deep neural network.
4. Artificial intelligence algorithm for predicting mortality of patients with acute heart failure.
5. Feature selection and transformation by machine learning reduce variable numbers and improve prediction for heart failure readmission or death.

