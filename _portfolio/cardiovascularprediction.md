---
title: "Cardiovascular Prediction"
excerpt: "Used Kaggle dataset to predict risk of cardiovascular disease using machine learning tools <br/><img src='/aboutme/images/cardiovascularpic'>"
collection: portfolio
---

My team's objective is to be able to predict if an indicidual has cardiovascular disease based on serveral factors. We used a Cardiovascular Disease dataset from [kaggle](https://www.kaggle.com/datasets/sulianova/cardiovascular-disease-dataset).

The various data figures that they have is:

1. Age | Objective Feature | age | int (days) |
2. Height | Objective Feature | height | int (cm) |
3. Weight | Objective Feature | weight | float (kg) |
4. Gender | Objective Feature | gender | categorical code |
5. Systolic blood pressure | Examination Feature | ap_hi | int |
6. Diastolic blood pressure | Examination Feature | ap_lo | int |
7. Cholesterol | Examination Feature | cholesterol | 1: normal, 2: above normal, 3: well above normal |
8. Glucose | Examination Feature | gluc | 1: normal, 2: above normal, 3: well above normal |
9. Smoking | Subjective Feature | smoke | binary |
10. Alcohol intake | Subjective Feature | alco | binary |
11. Physical activity | Subjective Feature | active | binary |
12. Presence or absence of cardiovascular disease | Target Variable | cardio | binary |

**Data Preparation**

To ensure that the data we use is the most relevant to helping us achieve our objective, we cleaned the dataset by removing outliers for various features such as blood pressure and weights, also creating a BMI column from weight and height. In total, we dropped 5689 rows of data.
![Cleandataset]({{ site.baseurl }}/images/cleandataset.png)

**Exploratory Data Analysis**

From this, we are able to gain more insights about the dataset, identify patterns and observe if there is any biasness of dataset. We used box plot, histogram and violin plot for age and BMI values. For categorical and discrete variables, we decided to use count plot.

We also plotted each discrete variable against cardio (column of data that shows if someone has cardiovascular disease) and coded a heatmap to identify which features have the highest correlation with cardio.


This is an item in your portfolio. It can be have images or nice text. If you name the file .md, it will be parsed as markdown. If you name the file .html, it will be parsed as HTML. 
