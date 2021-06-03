### Let's regress

https://bigdata-madesimple.com/how-to-run-linear-regression-in-python-scikit-learn/

Helpful link alert

https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html

The first step is to import the required Python libraries into Ipython Notebook.

```
import numpy as np
import pandas as pd
import scipy.stats as stats
import matplotlib.pyploy as plt
import sklearn
```

**NOTE**: Since this demo was published scikit-learn has been updated. The train_test_split function is now imported from sklearn.model_selection

Set the thing you are looking into as the target:
In the example:
```bos['PRICE'] = boston.target```

import linear regression:
```
from sklearn.linear_model import LinearRegression
X = bos.drop('PRICE', axis = 1)

# this creates a LinearRegression object
lm = LinearRegression()
lm
```

Important functions to keep in mind while fitting a linear regression model are:

**lm.fit()** -> fits a linear model

**lm.predict()** -> Predict Y using the linear model with estimated coefficients

fit a LG model:
```
In [20]: lm.fit(X, bos.PRICE)

Out[20]: LinearRegression(copy_X=True, fit_intercept=True, normalize=False)
```

calulate mean squared error:
```
mseFull = np.mean((bos.PRICE - lm.predict((x)) **2)

**lm.score()** -> Returns the coefficient of determination (R^2). A measure of how well observed outcomes are replicated by the model, as the proportion of total variation of outcomes explained by the model.

**How to do train-test split**:

You have to divide your data sets randomly. Scikit learn provides a function called train_test_split to do this.

```
x_train, X_test, Y_train, Y_test = sklearn.cross_validation.train_test_split(X, bos.Price, test_size=0.33, randoms_state = 5)
print X_train.shape
print X_test.shape
print Y_train.shape
prting Y_Test.shape
```

Build a linear regression model using my train-test data sets:

```
lm = LinearRegression()
lm.fit(X_train, Y_train)
pred_train = lm.predict(X_train)
pred_test = lm.predict(X_test)
```

Then calculate the mean squared error for training and test data.

**Input:**
print “Fit a model X_train, and calculate MSE with Y_train:”, np.mean((Y_train – lm.predict(X_train)) ** 2)

print “Fit a model X_train, and calculate MSE with X_test, Y_test:”, np.mean((Y_test – lm.predict(X_test)) ** 2)

**Output:**
Fit a model X_train, and calculate MSE with Y_train: 19.5467584735 Fit a model X_train, and calculate MSE with X_test, Y_test: 28.5413672756

