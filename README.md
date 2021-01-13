# Regression Analysis: Red Wine Quality

![Red_wine](https://user-images.githubusercontent.com/67468718/104449221-20733600-5553-11eb-9449-20c930dc57cb.jpg)

## Introduction

The objective of this project is to use exploratory data analysis (EDA) and regression to predict alcohol levels in wine with a model that's as accurate as possible.

We'll try a univariate analysis (one involving a single explanatory variable) as well as a multivariate one (involving multiple explanatory variables), and we'll iterate together towards a decent model by the end of this project..

For this notebook, we're going to use the red wine dataset, wineQualityReds.csv. This is a very common dataset for practicing regression analysis and is actually freely available on Kaggle, [here](https://www.kaggle.com/piyushgoyal443/red-wine-dataset)

## Content:

**1. Sourcing and loading** 
* Import relevant libraries
* Load the data 
* Exploring the data
* Choosing a dependent variable
 
**2. Cleaning, transforming, and visualizing**
* Visualizing correlations
  
  
**3. Modeling** 
* Train/Test split
* Making a Linear regression model: First model
* Making a Linear regression model: Second model: **Ordinary Least Squares (OLS)**
* Making a Linear regression model: Third model: **Multiple Linear Regression**
* Making a Linear regression model: Fourth model: **Avoiding Redundancy**

**4. Evaluating and concluding** 
* Reflection 
* Which model was best?
* Other regression algorithms

## Description of Wine Dataset Features:

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

## Feature Engineering: 

![pairplot](https://user-images.githubusercontent.com/67468718/104464724-1d367500-5568-11eb-9796-1809d6bc5e4a.jpg)


