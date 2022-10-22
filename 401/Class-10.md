# Linear Regressions

## Linear Regressions :

Is a linear approach for modelling the relationship between a scalar response and one or more explanatory variables .

## What used for 

Linear regression is a basic and commonly used type of predictive analysis,The overall idea of regression is to examine two things: (1) does a set of predictor variables do a good job in predicting an outcome (dependent) variable.

## Python Packages for Linear Regression


- The package scikit-learn is a widely used Python library for machine learning, built on top of NumPy and some other packages
- NumPy is a fundamental Python scientific package that allows many high-performance operations on single-dimensional and multidimensional arrays

## Linear Regression With scikit-learn

- **Step 1: Import packages and classes** :
```
>>> import numpy as np
>>> from sklearn.linear_model import LinearRegression
```

- **Step 2: Provide data** :

defining data to work with. The inputs (regressors, 𝑥) and output (response, 𝑦) should be arrays or similar objects.
```
>>> x = np.array([5, 15, 25, 35, 45, 55]).reshape((-1, 1))
>>> y = np.array([5, 20, 14, 32, 22, 38])
```

- **Step 3: Create a model and fit it** :

create a linear regression model and fit , and Create an instance of the class LinearRegression
```
>>> model = LinearRegression()
```
This statement creates the variable model as an instance of LinearRegression. we can provide several optional parameters to LinearRegression:

  1. ```fit_intercept``` is a Boolean that, if True, decides to calculate the intercept 𝑏₀ or, if False, considers it equal to zero. It defaults to True.
  2. ```normalize``` is a Boolean that, if True, decides to normalize the input variables. It defaults to False, in which case it doesn’t normalize the input variables.
  3. ```copy_X``` is a Boolean that decides whether to copy (True) or overwrite the input variables (False). It’s True by default.
  4. ```n_jobs``` is either an integer or None. It represents the number of jobs used in parallel computation. It defaults to None, which usually means one job. -1 means to use all available processors.

- **Step 3: Create a model and fit it** :

create a linear regression model and fit , and Create an instance of the class LinearRegression
```
>>> model = LinearRegression()
```

