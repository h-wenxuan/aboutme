---
title: "Cardiovascular Prediction"
excerpt: "Used Kaggle dataset to predict risk of cardiovascular disease using machine learning tools <br/><img src='/aboutme/images/cardiovascularpic.jpg' style='width:300px; height:auto;'>"
collection: portfolio
---

With this machine learning project, my team's objective is to be able to predict if an individual has cardiovascular disease based on serveral factors. We used a Cardiovascular Disease dataset from [kaggle](https://www.kaggle.com/datasets/sulianova/cardiovascular-disease-dataset).

The various data figures that they have is:
1. Age (age), int (days)
2. Height (height), int (cm)
3. Weight (weight), float (kg)
4. Gender (gender), categorical code (1: women, 2: men)
5. Systolic blood pressure (ap_hi), int
6. Diastolic blood pressure (ap_lo), int
7. Cholesterol (cholesterol), categorical code (1: normal, 2: above normal, 3: well above normal)
8. Glucose (gluc), categorical code (1: normal, 2: above normal, 3: well above normal)
9. Smoking (smoke), binary (0: non-smoker, 1: smoker)
10. Alcohol intake (alco), binary (0: non-drinker, 1: drinker)
11. Physical activity (active), binary (0: not active, 1: active)
12. Presence or absence of cardiovascular disease (cardio), binary (0: absence of cardiovascular disease, 1: presence of cardiovascular disease)

**Data Preparation**

To ensure the relevance of our data for achieving our objectives, we cleaned the dataset by removing outliers in features such as blood pressure and weight. Additionally, we created a BMI column from weight and height. In total, we dropped 5,689 rows of data.
![Cleandataset]({{ site.baseurl }}/images/cleandataset.png)

**Exploratory Data Analysis**

We conducted exploratory data analysis to gain insights, identify patterns, and check for biases in the dataset. For continuous variables like age and BMI, we used box plots, histograms, and violin plots. 
![Histplot]({{ site.baseurl }}/images/histplot.png)

For categorical and discrete variables, we decided to go with count plot.
![Countplot]({{ site.baseurl }}/images/countplot.png)

We also plotted each discrete variable against presence of cardiovascular disease and generated a heatmap to identify which features had the highest correlation with cardiovascular disease.
![Heatmap]({{ site.baseurl }}/images/heatmapplot.png)

**Machine Learning Tools**

We applied various machine learning models, such as feature importance analysis and decision trees, to confirm the correlation between features and the presence of cardiovascular disease. Each model was trained with 70% of random data points and tested with the remaining 30%, achieving an accuracy of around 71%.
After identifying the top four factors influencing cardiovascular disease: age, bp_cat (Systolic & Diastolic blood pressure), BMI, and cholesterol, we dropped the rest of the features. We then prompted users to input their age, blood pressure category, BMI, and cholesterol level to predict the presence of cardiovascular disease using a logistic regression model. If you are interested to test it out, can click on our code below. 😁
![Prediction]({{ site.baseurl }}/images/prediction.png)

To evaluate our model's accuracy, we used logistic regression model to plot a confusion matrix and for True Positive Rate (TPR) and False Positive Rate (FPR) values, we used a threshold of 0.5 (standard value).

![ConfusionMatrix]({{ site.baseurl }}/images/Matrixgraph.png){:width="400px" height="auto"}

To explain True Positive Rate (TPR) and False Positive Rate (FPR), imagine a scenario with data from 10 people, where 5 have the disease and 5 do not. With a threshold of 0.45, we might correctly classify 4 out of 5 diseased individuals, giving us a TPR of 0.8. Conversely, we have misclassify 2 out of 5 healthy individuals as diseased, getting an FPR of 0.4.
![TPR&FPRexample]({{ site.baseurl }}/images/TPRvalue.png){:width="500px" height="auto"}

We also plotted an ROC (Receiver Operating Characteristic) Curve, which is plotted with TPR against FPR. When threshold is small, TPR and FPR will be 1 and we get first point on graph. By increasing the treshold and continue plotting the graph, our model achieved an AUC (Area Under Curve) value of 0.77. Thr higher the AUC value, the better the machine learning model.
![ROCgraph]({{ site.baseurl }}/images/rocgraph.png)

**Future Improvements**

Although this AUC value is too low for real-life application, there are ways to improve our model, such as separating BMI by gender or using anomaly detection. Nevertheless, this project was meaningful and interesting as it demonstrated the practical application of machine learning models, providing an eye-opening experience for me.

[View our complete code here.](https://github.com/h-wenxuan/cardiovascular-prediction/blob/main/CardiovascularPrediction.ipynb)
