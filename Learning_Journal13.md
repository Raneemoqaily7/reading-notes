# What I Learned 
## Linear regression

- Important points in the process
1. Determain the Final  Goal
2. Select  What Variables (Features)effect process(Independent Features)
3. finde a realation  between the features(variables) and the decession that we made .
 - Aquire a big set of data 
 - Classify the data 
 - Load the data into ML model 
 - Train the model == >Usually(80% of data take randomly for train data ) 
 - Test the model == >(20 % of data take for test  ) 
 - Approve on the accuracy of the predections .
 - Use the modul to predict

 4. Result will provide based in the relarion 


- **Scikit-learn** is a powerful Python module for machine learning. It contains function for regression, classification, clustering, model selection and dimensionality reduction.

- `from sklearn.model_selection import train_test_split`
- train_test_split: this function will return for me four values  (x_train ,x_test,y_train,y_test)
- x_train, x_test, y_train, y_test = train_test_split(X,Y, train_size = 0.8, test_size=0.2, random_state = 21)
-  train_size = 0.8 ==> 80% of data for train 
- test_size=0.2  ==> 20% of data for test 
- random_state ==> if a fixed value is assigned like random_state = 0 or 1 or 42 or any other integer then no matter how many times you execute your code the result would be the same .i.e, same values in train and test datasets.

**What is Train/Test**
Train/Test is a method to measure the accuracy of your model.

It is called Train/Test because you split the the data set into two sets: a training set and a testing set.

80% for training, and 20% for testing.

You train the model using the training set.

You test the model using the testing set.



- **scatter diagram**

A scatter diagram is used to examine the relationship between both the axes (X and Y) with one variable. In the graph, if the variables are correlated, then the point drops along a curve or line. A scatter diagram or scatter plot gives an idea of the nature of relationship.

In a scatter correlation diagram, if all the points stretch in one line, then the correlation is perfect and is in unity. However, if the scatter points are widely scattered throughout the line, then the correlation is said to be low. If the scatter points rest near a line or on a line, then the correlation is said to be linear.


- to predict ==> predict

`model.predict(x_test reshape(-1,1))`

- to accuracy ==> score

`model.score(x_test , y_test)`







Train the model means create the model.

Test the model means test the accuracy of the model.


