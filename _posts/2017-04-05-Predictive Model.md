---
layout: post
title: Predictive Model
author: Geraldo Braho
tags: 		
subtitle: Blood Transfusion Service Center
category: project1
visualworkflow: false
---


COMP 4353 Data Mining  
Geraldo Braho  
5/5/2017








## Project: Predictive Model

# <center> Blood Transfusion Service Center </center>

## Problem

This is a workflow for building a predictive model (classification) to determine whether the donors donated blood during the certain time.
The order of this listing corresponds to the order of numerals along the rows of
the database.

* R (Recency - months since last donation),
* F (Frequency - total number of donation),
* M (Monetary - total blood donated in c.c.),
* T (Time - months since first donation), and
* a binary variable representing whether he/she donated blood in March 2007 (1 stand for donating blood; 0 stands for not donating blood).

## Step 1 - Data Information and Descriptive Statistics


```python
#Import libraries and packages
import pandas
import numpy as np
import scipy
from pandas.tools.plotting import scatter_matrix
import matplotlib.pyplot as plt
from sklearn.preprocessing import MinMaxScaler
from sklearn import model_selection
from sklearn.metrics import classification_report
from sklearn.metrics import confusion_matrix
from sklearn.metrics import accuracy_score
from sklearn.metrics import roc_auc_score
from sklearn.linear_model import LogisticRegression
from sklearn.tree import DecisionTreeClassifier
from sklearn.neighbors import KNeighborsClassifier
from sklearn.discriminant_analysis import LinearDiscriminantAnalysis
from sklearn.naive_bayes import GaussianNB
from sklearn.svm import SVC
```


```python
dataSet = pandas.read_csv("KNN_PredictiveModel.csv");
dataSet.columns = [['recency', 'frequency', 'monetary_blood', 'time', 'class']]
```


```python
dataset = dataSet.drop(dataSet.index[0])
```


```python
dataset.shape
```




    (747, 5)




```python
dataset.head(n=10)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>recency</th>
      <th>frequency</th>
      <th>monetary_blood</th>
      <th>time</th>
      <th>class</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>0</td>
      <td>13</td>
      <td>3250</td>
      <td>28</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>16</td>
      <td>4000</td>
      <td>35</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2</td>
      <td>20</td>
      <td>5000</td>
      <td>45</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1</td>
      <td>24</td>
      <td>6000</td>
      <td>77</td>
      <td>0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>4</td>
      <td>4</td>
      <td>1000</td>
      <td>4</td>
      <td>0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>2</td>
      <td>7</td>
      <td>1750</td>
      <td>14</td>
      <td>1</td>
    </tr>
    <tr>
      <th>7</th>
      <td>1</td>
      <td>12</td>
      <td>3000</td>
      <td>35</td>
      <td>0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>2</td>
      <td>9</td>
      <td>2250</td>
      <td>22</td>
      <td>1</td>
    </tr>
    <tr>
      <th>9</th>
      <td>5</td>
      <td>46</td>
      <td>11500</td>
      <td>98</td>
      <td>1</td>
    </tr>
    <tr>
      <th>10</th>
      <td>4</td>
      <td>23</td>
      <td>5750</td>
      <td>58</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
</div>




```python
dataset.describe()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>recency</th>
      <th>frequency</th>
      <th>monetary_blood</th>
      <th>time</th>
      <th>class</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>747.000000</td>
      <td>747.000000</td>
      <td>747.000000</td>
      <td>747.000000</td>
      <td>747.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>9.516734</td>
      <td>5.455154</td>
      <td>1363.788487</td>
      <td>34.196787</td>
      <td>0.236948</td>
    </tr>
    <tr>
      <th>std</th>
      <td>8.096150</td>
      <td>5.611321</td>
      <td>1402.830334</td>
      <td>24.281086</td>
      <td>0.425495</td>
    </tr>
    <tr>
      <th>min</th>
      <td>0.000000</td>
      <td>1.000000</td>
      <td>250.000000</td>
      <td>2.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>3.000000</td>
      <td>2.000000</td>
      <td>500.000000</td>
      <td>16.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>7.000000</td>
      <td>4.000000</td>
      <td>1000.000000</td>
      <td>28.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>14.000000</td>
      <td>7.000000</td>
      <td>1750.000000</td>
      <td>50.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>74.000000</td>
      <td>46.000000</td>
      <td>11500.000000</td>
      <td>98.000000</td>
      <td>1.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python
dataset.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Int64Index: 747 entries, 1 to 747
    Data columns (total 5 columns):
    recency           747 non-null int64
    frequency         747 non-null int64
    monetary_blood    747 non-null int64
    time              747 non-null int64
    class             747 non-null int64
    dtypes: int64(5)
    memory usage: 35.0 KB



```python
# class distribution
print(dataset.groupby('class').size())
```

    class
    0    570
    1    177
    dtype: int64



```python
# box and whisker plots
dataset.plot(kind='box', subplots=True, layout=(2,4), sharex=False, sharey=False, figsize=(18,16))
plt.show()
```


![png](img/output_16_0.png)



```python

# histograms
dataset.hist(figsize=(18,16))
plt.show()
```


![png](img/output_17_0.png)



```python
# scatter plot matrix
scatter_matrix(dataset, figsize=(18,16))
plt.show()
```


![png](img/output_18_0.png)


## Step 2 - Train Test Split


```python
# Split-out validation dataset
array = dataset.values
X = array[:,0:4]
Y = array[:,4]
validation_size = 0.30
seed = 7
X_train, X_test, Y_train, Y_test = model_selection.train_test_split(X, Y, test_size=validation_size, random_state=seed)
```


```python
pandas.DataFrame(X_train).describe()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>522.000000</td>
      <td>522.000000</td>
      <td>522.000000</td>
      <td>522.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>9.515326</td>
      <td>5.363985</td>
      <td>1340.996169</td>
      <td>34.339080</td>
    </tr>
    <tr>
      <th>std</th>
      <td>7.885746</td>
      <td>5.529339</td>
      <td>1382.334864</td>
      <td>24.873615</td>
    </tr>
    <tr>
      <th>min</th>
      <td>0.000000</td>
      <td>1.000000</td>
      <td>250.000000</td>
      <td>2.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>2.000000</td>
      <td>2.000000</td>
      <td>500.000000</td>
      <td>16.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>8.500000</td>
      <td>4.000000</td>
      <td>1000.000000</td>
      <td>28.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>14.000000</td>
      <td>7.000000</td>
      <td>1750.000000</td>
      <td>50.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>74.000000</td>
      <td>46.000000</td>
      <td>11500.000000</td>
      <td>98.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python
pandas.DataFrame(X_test).describe()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>225.000000</td>
      <td>225.000000</td>
      <td>225.000000</td>
      <td>225.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>9.520000</td>
      <td>5.666667</td>
      <td>1416.666667</td>
      <td>33.866667</td>
    </tr>
    <tr>
      <th>std</th>
      <td>8.582624</td>
      <td>5.804093</td>
      <td>1451.023346</td>
      <td>22.897676</td>
    </tr>
    <tr>
      <th>min</th>
      <td>0.000000</td>
      <td>1.000000</td>
      <td>250.000000</td>
      <td>2.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>4.000000</td>
      <td>2.000000</td>
      <td>500.000000</td>
      <td>15.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>5.000000</td>
      <td>4.000000</td>
      <td>1000.000000</td>
      <td>28.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>14.000000</td>
      <td>7.000000</td>
      <td>1750.000000</td>
      <td>49.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>72.000000</td>
      <td>41.000000</td>
      <td>10250.000000</td>
      <td>98.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python
pandas.DataFrame(Y_train).describe()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>522.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>0.222222</td>
    </tr>
    <tr>
      <th>std</th>
      <td>0.416139</td>
    </tr>
    <tr>
      <th>min</th>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>1.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python
pandas.DataFrame(Y_test).describe()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>225.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>0.271111</td>
    </tr>
    <tr>
      <th>std</th>
      <td>0.445524</td>
    </tr>
    <tr>
      <th>min</th>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>1.000000</td>
    </tr>
  </tbody>
</table>
</div>



* Review the descriptive statistics of input output columns in Train, Test and original Full (before the splitting operation) datasets and compare them to each other.
* Are they similar or not? Do you think Train and Test dataset are representative of the Full datasets?
* Why ?

Descriptive statistics of full data set is very similar to the average of train and test data set descriptive statistics. Based on the statistics generated, I do think that the train and test data sets are good representatives of the full data set.

## Step 3 -  Analysis of the Output Column


```python
scipy.stats.iqr(Y_train)
```




    0.0




```python
scipy.stats.iqr(Y_test)
```




    1.0




```python
np.amax(Y_train) - np.amin(Y_train)
```




    1




```python
np.amax(Y_test) - np.amin(Y_test)
```




    1



* Is there a class imbalance problem?
(check if there is big difference between the number of distinct values in your categorical output column)

Yes, there is a big class imbalance problem (570 (not donated) - 177 (donated)). This can be very bad, because our model can see our data, and since majority of it is 'not donated', it can predict for the new value 'not donated' as well. There are  several possible ways to resolve this issue, we could work on collecting more data, or resampling the current set, generating artifical data based on the existing data set and some other possible approaches you can think of.

## Step 4 - Scale Training and Test dataset


```python
train_scaler = MinMaxScaler()
train_scaled = pandas.DataFrame(train_scaler.fit_transform(X_train))
```

    /anaconda/lib/python3.6/site-packages/sklearn/utils/validation.py:429: DataConversionWarning: Data with input dtype int64 was converted to float64 by MinMaxScaler.
      warnings.warn(msg, _DataConversionWarning)



```python
train_scaled.describe()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>522.000000</td>
      <td>522.000000</td>
      <td>522.000000</td>
      <td>522.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>0.128585</td>
      <td>0.096977</td>
      <td>0.096977</td>
      <td>0.336865</td>
    </tr>
    <tr>
      <th>std</th>
      <td>0.106564</td>
      <td>0.122874</td>
      <td>0.122874</td>
      <td>0.259100</td>
    </tr>
    <tr>
      <th>min</th>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>0.027027</td>
      <td>0.022222</td>
      <td>0.022222</td>
      <td>0.145833</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>0.114865</td>
      <td>0.066667</td>
      <td>0.066667</td>
      <td>0.270833</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>0.189189</td>
      <td>0.133333</td>
      <td>0.133333</td>
      <td>0.500000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python
test_scaler = MinMaxScaler()
test_scaled = pandas.DataFrame(test_scaler.fit_transform(X_test))
```

    /anaconda/lib/python3.6/site-packages/sklearn/utils/validation.py:429: DataConversionWarning: Data with input dtype int64 was converted to float64 by MinMaxScaler.
      warnings.warn(msg, _DataConversionWarning)



```python
test_scaled.describe()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>225.000000</td>
      <td>225.000000</td>
      <td>225.000000</td>
      <td>225.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>0.132222</td>
      <td>0.116667</td>
      <td>0.116667</td>
      <td>0.331944</td>
    </tr>
    <tr>
      <th>std</th>
      <td>0.119203</td>
      <td>0.145102</td>
      <td>0.145102</td>
      <td>0.238517</td>
    </tr>
    <tr>
      <th>min</th>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>0.055556</td>
      <td>0.025000</td>
      <td>0.025000</td>
      <td>0.135417</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>0.069444</td>
      <td>0.075000</td>
      <td>0.075000</td>
      <td>0.270833</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>0.194444</td>
      <td>0.150000</td>
      <td>0.150000</td>
      <td>0.489583</td>
    </tr>
    <tr>
      <th>max</th>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
    </tr>
  </tbody>
</table>
</div>



## Step 5 - Build Predictive Model


```python
# Test options and evaluation metric
seed = 7
scoring = 'accuracy'
```


```python
# Introduce Algorithms
models = []
# models.append(('LR', LogisticRegression()))
# models.append(('LDA', LinearDiscriminantAnalysis()))
models.append(('KNN', KNeighborsClassifier()))
# models.append(('CART', DecisionTreeClassifier()))
# models.append(('NB', GaussianNB()))
# models.append(('SVM', SVC()))
# evaluate each model in turn
results = []
names = []
for name, model in models:
    kfold = model_selection.KFold(n_splits=10, random_state=seed)
    cv_results = model_selection.cross_val_score(model, train_scaled, Y_train, cv=kfold, scoring=scoring)
    results.append(cv_results)
    names.append(name)
    msg = "%s: %f (%f)" % (name, cv_results.mean(), cv_results.std())
    print(msg)
```

    KNN: 0.779790 (0.044200)



```python
# Compare Algorithms
# fig = plt.figure()
# fig.suptitle('Algorithm Comparison')
# ax = fig.add_subplot(111)
# plt.boxplot(results)
# ax.set_xticklabels(names)
# plt.show()
```

## Step 6 - Model Predictions on Training Dataset


```python
# Make predictions on train dataset
knn = KNeighborsClassifier()
knn.fit(X_train, Y_train)
predictions = knn.predict(train_scaled)
# print(accuracy_score(Y_train, predictions))
print(confusion_matrix(Y_train, predictions))
```

    [[406   0]
     [116   0]]


## Step 7 - Model Predictions on Test Dataset


```python
# Make predictions on test dataset
knn = KNeighborsClassifier()
knn.fit(X_train, Y_train)
predictions = knn.predict(X_test)
# print(accuracy_score(Y_test, predictions))
print(confusion_matrix(Y_test, predictions))
```

    [[154  10]
     [ 43  18]]


## Step 8 - Model Performance


```python
# Training Performance
# Make predictions on train dataset
knn = KNeighborsClassifier()
knn.fit(X_train, Y_train)
predictions = knn.predict(train_scaled)
print(accuracy_score(Y_train, predictions))
# print(classification_report(Y_train, predictions))
```

    0.777777777778



```python
# Testing Performance
# Make predictions on test dataset
knn = KNeighborsClassifier()
knn.fit(X_train, Y_train)
predictions = knn.predict(X_test)
print(accuracy_score(Y_test, predictions))
# print(classification_report(Y_test, predictions))
```

    0.764444444444


* Which one (Training or Testing performance) is better, is there an overfitting case, why ?.
* Would you deploy (Productionize) this model for using in actual usage in your business system? Why?

Currently, Training performance is better. I wouldn't say that there is overfitting case, because overfitting usually occurs when there is complex model deployed (with various and multiple parameters). The reason behind low performance of our model might be insuficcient number of data instances, and imbalanced classes.

In order to determined if I would productionize this model, I would have to scale it on the biger data set. And to understand the real behavior and real execution of the performance, I would have to tweek existing parameters and maybe introduce the new ones for a closer statistical fit. With the current output, on this data set I would not productionize this model.

## Step 9 - Update the Model


```python
###### STEP 5 ##############
# Update the model         #
# parameters and re-train  #
# the model.               #
###########################

# Introduce Algorithms
models = []
# models.append(('LR', LogisticRegression()))
# models.append(('LDA', LinearDiscriminantAnalysis()))
models.append(('KNN', KNeighborsClassifier(n_neighbors=40, algorithm='ball_tree', leaf_size=50)))
# models.append(('CART', DecisionTreeClassifier()))
# models.append(('NB', GaussianNB()))
# models.append(('SVM', SVC()))
# evaluate each model in turn
results = []
names = []
for name, model in models:
    kfold = model_selection.KFold(n_splits=10, random_state=seed)
    cv_results = model_selection.cross_val_score(model, train_scaled, Y_train, cv=kfold, scoring=scoring)
    results.append(cv_results)
    names.append(name)
    msg = "%s: %f (%f)" % (name, cv_results.mean(), cv_results.std())
    print(msg)
```

    KNN: 0.789405 (0.049755)



```python
# Make predictions on train dataset
knn = KNeighborsClassifier(n_neighbors=40, algorithm='ball_tree', leaf_size=50)
knn.fit(X_train, Y_train)
predictions = knn.predict(train_scaled)
# print(accuracy_score(Y_train, predictions))
print(confusion_matrix(Y_train, predictions))
# print(classification_report(Y_train, predictions))
```

    [[406   0]
     [116   0]]



```python
# Make predictions on test dataset
knn = KNeighborsClassifier(n_neighbors=40, algorithm='ball_tree', leaf_size=50)
knn.fit(X_train, Y_train)
predictions = knn.predict(X_test)
# print(accuracy_score(Y_test, predictions))
print(confusion_matrix(Y_test, predictions))
# print(classification_report(Y_test, predictions))
```

    [[164   0]
     [ 61   0]]



```python
# Training Performance
# Make predictions on train dataset
knn = KNeighborsClassifier(n_neighbors=40, algorithm='ball_tree', leaf_size=50)
knn.fit(X_train, Y_train)
predictions = knn.predict(train_scaled)
print(accuracy_score(Y_train, predictions))
# print(confusion_matrix(Y_train, predictions))
# print(classification_report(Y_train, predictions))
```

    0.777777777778



```python
# Testing Performance
# Make predictions on test dataset
knn = KNeighborsClassifier(n_neighbors=40, algorithm='ball_tree', leaf_size=50)
knn.fit(X_train, Y_train)
predictions = knn.predict(X_test)
print(accuracy_score(Y_test, predictions))
# print(confusion_matrix(Y_test, predictions))
# print(classification_report(Y_test, predictions))
```

    0.728888888889


* Did you get a better performance on Training or Test set?
* Explain why the new model performs better or worse than the former model.

Again, we got the better performance on the Training set.

And we go the same performance as previously. The reason for so could be that we didn't change the right parameters, or that we didn't change them enough to effect the performance of the model on the current data set.

## Step 10 - Change the Error Metric


```python
# Training Performance
# Make predictions on train dataset
knn = KNeighborsClassifier(n_neighbors=40, algorithm='ball_tree', leaf_size=50)
knn.fit(X_train, Y_train)
predictions = knn.predict(train_scaled)
print(accuracy_score(Y_train, predictions))
# print(confusion_matrix(Y_train, predictions))
print(roc_auc_score(Y_train, predictions))
print(classification_report(Y_train, predictions))
```

    0.777777777778
    0.5
                 precision    recall  f1-score   support

              0       0.78      1.00      0.88       406
              1       0.00      0.00      0.00       116

    avg / total       0.60      0.78      0.68       522



    /anaconda/lib/python3.6/site-packages/sklearn/metrics/classification.py:1113: UndefinedMetricWarning: Precision and F-score are ill-defined and being set to 0.0 in labels with no predicted samples.
      'precision', 'predicted', average, warn_for)



```python
# Testing Performance
# Make predictions on test dataset
knn = KNeighborsClassifier(n_neighbors=40, algorithm='ball_tree', leaf_size=50)
knn.fit(X_train, Y_train)
predictions = knn.predict(X_test)
print(accuracy_score(Y_test, predictions))
print(roc_auc_score(Y_test, predictions))
# print(confusion_matrix(Y_test, predictions))
print(classification_report(Y_test, predictions))
```

    0.728888888889
    0.5
                 precision    recall  f1-score   support

              0       0.73      1.00      0.84       164
              1       0.00      0.00      0.00        61

    avg / total       0.53      0.73      0.61       225



    /anaconda/lib/python3.6/site-packages/sklearn/metrics/classification.py:1113: UndefinedMetricWarning: Precision and F-score are ill-defined and being set to 0.0 in labels with no predicted samples.
      'precision', 'predicted', average, warn_for)


* Compare the results and explain which error metric is better for your modeling and why?

Neglecting the fact that we have a big class imbalance within our data set, the "AUC" error metric would the best one for our modeling. Because Area Under the ROC Curve is known as an error metric for binary classification. And since in our problem we have two classes, it is considered as binary classification as well.

If we deploy one of the above mentioned methods for resolving the class imbalance issue, we could maybe see the better performance of our model.
