# ✰ Regression Analysis: Red Wine Quality

![Red_wine](https://user-images.githubusercontent.com/67468718/104449221-20733600-5553-11eb-9449-20c930dc57cb.jpg)

## 1. Introduction

The objective of this project is to use exploratory data analysis (EDA) and regression to predict alcohol levels in wine with a model that's as accurate as possible.

We'll try a univariate analysis (one involving a single explanatory variable) as well as a multivariate one (involving multiple explanatory variables), and we'll iterate together towards a decent model by the end of this project..

For this notebook, we're going to use the red wine dataset, wineQualityReds.csv. This is a very common dataset for practicing regression analysis and is actually freely available on Kaggle, [here](https://www.kaggle.com/piyushgoyal443/red-wine-dataset)


**✰ Evaluating and concluding** 
* Reflection 
* Which model was best?
* Other regression algorithms

## 2. Description of Wine Dataset Features:

* <code>fixed acidity</code>: most acids involved with wine or fixed or nonvolatile (do not evaporate readily)
* <code>volatile acidity</code>: the amount of acetic acid in wine, which at too high of levels can lead to an unpleasant, vinegar taste
* <code>citric acid</code>: found in small quantities, citric acid can add 'freshness' and flavor to wines
* <code>residual sugar</code>: the amount of sugar remaining after fermentation stops, it's rare to find wines with less than 1 gram/liter and wines with greater than 45 grams/liter are considered sweet
* <code>chlorides</code>: the amount of salt in the wine
* <code>free sulfur dioxide</code>: the free form of SO2 exists in equilibrium between molecular SO2 (as a dissolved gas) and bisulfite ion; it prevents microbial growth and the oxidation of wine
* <code>total sulfur dioxide</code>: amount of free and bound forms of S02; in low concentrations, SO2 is mostly undetectable in wine, but at free SO2 concentrations over 50 ppm, SO2 becomes evident in the nose and taste of wine
* <code>density</code>: the density of water is close to that of water depending on the percent alcohol and sugar content
* <code>pH</code>: describes how acidic or basic a wine is on a scale from 0 (very acidic) to 14 (very basic); most wines are between 3-4 on the pH scale
* <code>sulphates</code>: a wine additive which can contribute to sulfur dioxide gas (S02) levels, wich acts as an antimicrobial and antioxidant
* <code>alcohol</code>: the percent alcohol content of the wine
* <code>quality</code> (score between 0 and 10)

## 3. Feature Engineering: 

#### Visualizing correlations using: seaborn pairplot & heatmap as shown below:
1. Seaborn pairplot:
![pairplot](https://user-images.githubusercontent.com/67468718/104464724-1d367500-5568-11eb-9796-1809d6bc5e4a.jpg)

2. Seaborn Heatmap:
![heatmap](https://user-images.githubusercontent.com/67468718/104465194-9fbf3480-5568-11eb-8057-d20bdaac3048.JPG)

## 4. Feature Selection:

After Analyzing the correlation from the visualizations above we noticed the following:

* A given cell value represents the correlation that exists between two variables 
* On the diagonal, you can see a bunch of histograms. This is because pairplotting the variables with themselves would be pointless, so the pairplot() method instead makes histograms to show the distributions of those variables' values. This allows us to quickly see the shape of each variable's values.  
* The plots for the quality variable form horizontal bands, due to the fact that it's a discrete variable. We were certainly right in not pursuing a regression analysis of this variable.
* Notice that some of the nice plots invite a line of best fit, such as alcohol vs density. Others, such as citric acid vs alcohol, are more inscrutable.
* There is a relatively strong correlation between the density and fixed acidity variables respectively, let's explore this correlation further using scatterplot and regplot with 1st and 2nd order regressions:

![density](https://user-images.githubusercontent.com/67468718/104465548-004e7180-5569-11eb-906f-275ec5380264.JPG)

## 5. Modeling:

* Train/Test split
* Making a Linear regression model: First model
* Making a Linear regression model: Second model: **Ordinary Least Squares (OLS)**
* Making a Linear regression model: Third model: **Multiple Linear Regression**
* Making a Linear regression model: Fourth model: **Avoiding Redundancy**

## 6. Conclusions & next steps:

#### Conclusions:
  1. While our most predictively powerful model was **Third Model: 'multiple linear regression'**, this model had explanatory variables that were correlated with one another, which made some redundancy. 
  2. Our most elegant and economical model was **Fourth Model: 'Avoiding Redundancy'** - it used just a few predictors to get a good result. 
  
  ![Model4](https://user-images.githubusercontent.com/67468718/104470453-93d67100-556e-11eb-91ff-56d3463e7d39.JPG)




