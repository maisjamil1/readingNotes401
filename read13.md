## How to run Linear regression in Python scikit-Learn?


Scikit-learn is a powerful Python module for machine learning. It contains function for regression, classification, clustering, model selection and dimensionality reduction. 
sklearn.linear_model module contains “methods intended for regression in which the target value is expected to be a linear combination of the input variables”.


### The first step is to import the required Python libraries into Ipython Notebook.
![img](https://bigdata-madesimple.com/wp-content/uploads/2016/04/Explore-1.png)


If you want to look inside the linear regression object, you can do so by typing LinearRegression. and the press <tab> key. This will give a list of functions available inside linear regression object.
![img](https://bigdata-madesimple.com/wp-content/uploads/2016/04/linear-regression.png)
  mportant functions to keep in mind while fitting a linear regression model are:

`lm.fit()` -> fits a linear model

`lm.predict()` -> Predict Y using the linear model with estimated coefficients

`lm.score()` -> Returns the coefficient of determination (R^2). A measure of how well observed outcomes are replicated by the model, as the proportion of total variation of outcomes explained by the model.

You can also explore the functions inside lm object by pressing `lm.<tab>`

  
