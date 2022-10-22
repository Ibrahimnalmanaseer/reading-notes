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

First, you need to call .fit() on model:

```
>>> model.fit(x, y)
LinearRegression()
```
With ```.fit()```, we calculate the optimal values of the weights 𝑏₀ and 𝑏₁, using the existing input and output, x and y, as the arguments.


- **Step 4: Get results** :

Once we have our model fitted, we can get the results to check whether the model works satisfactorily and to interpret it.

we can obtain the coefficient of determination, 𝑅², with .score() called on model:

```
>>> r_sq = model.score(x, y)
>>> print(f"coefficient of determination: {r_sq}")
coefficient of determination: 0.7158756137479542
```

The attributes of model are .intercept_, which represents the coefficient 𝑏₀, and .coef_, which represents 𝑏₁:
```
>>> print(f"intercept: {model.intercept_}")
intercept: 5.633333333333329

>>> print(f"slope: {model.coef_}")
slope: [0.54]
```

The code above illustrates how to get 𝑏₀ and 𝑏₁. You can notice that .intercept_ is a scalar, while .coef_ is an array.

The value of 𝑏₀ is approximately 5.63. This illustrates that your model predicts the response 5.63 when 𝑥 is zero. The value 𝑏₁ = 0.54 means that the predicted response rises by 0.54 when 𝑥 is increased by one.

- **Step 5: Predict response** :

Once we have a satisfactory model, then you can use it for predictions with either existing or new data. To obtain the predicted response, use .predict():

```
>>> y_pred = model.predict(x)
>>> print(f"predicted response:\n{y_pred}")
predicted response:
[ 8.33333333 13.73333333 19.13333333 24.53333333 29.93333333 35.33333333]
```

When applying .predict(), you pass the regressor as the argument and get the corresponding predicted response. This is a nearly identical way to predict the response:

```
>>> y_pred = model.intercept_ + model.coef_ * x
>>> print(f"predicted response:\n{y_pred}")
predicted response:
[[ 8.33333333]
 [13.73333333]
 [19.13333333]
 [24.53333333]
 [29.93333333]
 [35.33333333]]
```

