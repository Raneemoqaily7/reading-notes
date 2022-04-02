# Linear Regressions

##  What is simple linear regression?
Simple linear regression is a regression model that estimates the relationship between one independent variable and one dependent variable using a straight line. 
- Regression searches for relationships among variables.


## **When Do You Need Regression?**
Typically, you need regression to answer whether and how some phenomenon influences the other or how several variables are related. For example, you can use it to determine if and to what extent the experience or gender impact salaries.


## **Linear Regression**
Linear regression is probably one of the most important and widely used regression techniques. It’s among the simplest regression methods. One of its main advantages is the ease of interpreting results.
Regression is also useful when you want to forecast a response using a new set of predictors. For example, you could try to predict electricity consumption of a household for the next hour given the outdoor temperature, time of day, and number of residents in that household.

Regression is used in many different fields: economy, computer science, social sciences, and so on. Its importance rises every day with the availability of large amounts of data and increased awareness of the practical value of data.


## **Python Packages for Linear Regression**


The package NumPy is a fundamental Python scientific package that allows many high-performance operations on single- and multi-dimensional arrays

The package scikit-learn is a widely used Python library for machine learning, built on top of NumPy and some other packages. It provides the means for preprocessing data, reducing dimensionality, implementing regression, classification, clustering, and more. Like NumPy, scikit-learn is also open source.

Beyond Linear Regression
Linear regression is sometimes not appropriate, especially for non-linear models of high complexity.

Fortunately, there are other regression techniques suitable for the cases where linear regression doesn’t work well. Some of them are support vector machines, decision trees, random forest, and neural networks.

There are numerous Python libraries for regression using these techniques. Most of them are free and open-source. That’s one of the reasons why Python is among the main programming languages for machine learning.

The package scikit-learn provides the means for using other regression techniques in a very similar way to what you’ve seen. It contains the classes for support vector machines, decision trees, random forest, and more, with the methods .fit(), .predict(), .score() and so on.

- How to implement a linear regression in Python ?
 
 There are several ways in which you can do that, you can do linear regression using numpy, scipy, stats model and sckit learn. But in this post I am going to use scikit learn to perform linear regression.


 - **Scikit-learn** is a powerful Python module for machine learning. It contains function for regression, classification, clustering, model selection and dimensionality reduction.

 - **sklearn.linear_model ** module  contains “methods intended for regression in which the target value is expected to be a linear combination of the input variables”.

 -  import linear regression from sci-kit learn module
 - If you want to look inside the linear regression object, you can do so by typing LinearRegression. and the press <tab> key. This will give a list of functions available inside linear regression object.

     [linear regression object](https://bigdata-madesimple.com/wp-content/uploads/2016/04/linear-regression.png)


- Important functions to keep in mind while fitting a linear regression model are:

lm.fit() -> fits a linear model

lm.predict() -> Predict Y using the linear model with estimated coefficients

lm.score() -> Returns the coefficient of determination (R^2). A measure of how well observed outcomes are replicated by the model, as the proportion of total variation of outcomes explained by the model.

- You can also explore the functions inside lm object by pressing lm.<tab>

- .coef_ gives the coefficients and .intercept_ gives the estimated intercepts.

# Conclusion
***Linear regression is implemented with the following packages and tools: NumPy, scikit-learn, and statsmodels. If you don't need detailed results, or want to explore more advanced statistical parameters of a model, you can explore further by exploring the links below.***

