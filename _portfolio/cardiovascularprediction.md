---
title: "Cardiovascular Prediction"
excerpt: "Used Kaggle dataset to predict risk of cardiovascular disease using machine learning tools <br/><img src='/aboutme/images/cardiovascularpic.jpg'>"
collection: portfolio
---

My team's objective is to be able to predict if an individual has cardiovascular disease based on serveral factors. We used a Cardiovascular Disease dataset from [kaggle](https://www.kaggle.com/datasets/sulianova/cardiovascular-disease-dataset).

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

To ensure that the data we use is the most relevant to helping us achieve our objective, we cleaned the dataset by removing outliers for various features such as blood pressure and weights, also creating a BMI column from weight and height. In total, we dropped 5689 rows of data.
![Cleandataset]({{ site.baseurl }}/images/cleandataset.png)

**Exploratory Data Analysis**

From this, we are able to gain more insights about the dataset, identify patterns and observe if there is any biasness of dataset. We used box plot, histogram and violin plot for age and BMI values. 
![Cleandataset]({{ site.baseurl }}/images/histplot.png)
For categorical and discrete variables, we decided to use count plot.
![Cleandataset]({{ site.baseurl }}/images/countplot.png)


We also plotted each discrete variable against cardio (column of data that shows if someone has cardiovascular disease) and coded a heatmap to identify which features have the highest correlation with cardio.


This is an item in your portfolio. It can be have images or nice text. If you name the file .md, it will be parsed as markdown. If you name the file .html, it will be parsed as HTML. 
