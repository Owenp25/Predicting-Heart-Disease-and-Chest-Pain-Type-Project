# Predicting-Heart-Disease-and-Chest-Pain-Type-Project
Final Project completed in a group by me, Atticus Patrick, and Cameron Lunn. This was a collaborative effort where we split up the work equally between the three of us. We used R to analyze a public heart disease data set from kaggle where each row is an individual patient. Our aim was to look into the key factors that determine heart disease and predict the occurrence of heart disease in individuals based on a number of heart-health related predictor variables. A secondary goal was to look at chest pain type and to try and predict this in patients as well. The data used in this study consists of 5 independent sub-datasets of heart health related data. The main response variables looked at in the study were heart disease status and chest pain type. We found that the data are well suited to make predictions for heart disease status when using a decision tree. Additionally, we discovered that predicting chest pain type was very difficult and could not fit an accurate model using KNN, QDA, or a decision tree. For full report access "HeartDiseasePredictionReport.pdf".

## Introduction
Introduction
Every year, 25% of all deaths in the US are attributed to heart disease. There are many different types,
which respectively can have different root causes. Malfunctions of the valves, arteries, and other physiological
components can lead to a patient developing heart disease. On the other hand, lack of exercise, diet, and
other environmental and even genetic factors can play a role in this outcome as well. To be succinct: heart
disease is one of the biggest health-related killer the United States faces. If we can better understand the
variables that comprise the complex system of developing heart disease, we have a better shot at preventing
it from happening. The main goal for this study is to determine what factors are associated with heart
disease, and if they can be used to predict a patient’s outcome for it, as well as what factors are associated
with chest pain, and which of these factors can be used to predict types of chest pain.
Our goals / hypotheses:
1) Exploratory analysis: look at descriptive statistics, and group means. See if there are any relationships
between variables, and look at a correlation matrix of the numeric variables.
2) Use PCA to see which variables are most important and related to each other.
3) See if heart disease and chest pain type can be classified:
a) LDA/QDA
b) KNN
c) Decision Tree
4) See if factor analysis is applicable.

## EDA

![corr](https://github.com/Owenp25/Predicting-Heart-Disease-and-Chest-Pain-Type-Project/blob/master/corr%20plot.png)

Variances of the numeric variables: RestingBP - 342.7739 Cholesterol - 11964.89 MaxHR - 648.2286 Oldpeak 1.137572 
As shown by the correlation plot above of the numeric variables in our data set, there does not appear to be any high correlations between variables.

![box](https://github.com/Owenp25/Predicting-Heart-Disease-and-Chest-Pain-Type-Project/blob/master/Chest%20Pain%20boxplots.png)

Above is a set of box plots showing the distribution of the four chest pain types in each of the 5 numeric
variables in our data set. The chest pain types appear relatively equal across Cholesterol and RestingBP,
5 while MaxHR is noticeably lower for those with ASY, and both ASY and TA are noticeably higher in Oldpeak.

![density](https://github.com/Owenp25/Predicting-Heart-Disease-and-Chest-Pain-Type-Project/blob/master/Heart%20Disease%20Density%20plots.png)

Also shown above is a set of density plots showing the distribution of those affected or unaffected by heart
disease in each of the 5 numeric variables in our data set. It appears that MaxHR has a higher median
for those without heart disease when compared to those with heart disease. It appears that Oldpeak and
RestingBP have slightly higher medians for those with heart disease when compared to those without heart
disease. Cholesterol level appears to be relatively equal between the two.

![biplot](https://github.com/Owenp25/Predicting-Heart-Disease-and-Chest-Pain-Type-Project/blob/master/PCA%20biplot.png)

We used PCA to check variable dependencies, as well as significance of the variables. To no surprise, PCA
wasn’t super useful because there wasn’t much collinearity between the numeric variables (as shown in the
correlation matrix). This is shown in the screeplot, because the first two PC’s only account for around 55%,
and ff of the PC’s would get us to ~88% of the proportion covered. The biplot also shows this because the
direction of the vector’s do not overlap - they point in mostly different directions.

Predictive Modeling, Limitations, and Conclusions are in the full report included in the repository: "HeartDiseasePredictionReport.pdf".
