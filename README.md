# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the necessary packages.

2.Read the given csv file and display the few contents of the data.Assign the features for x and y respectively.

3.Split the x and y sets into train and test sets.Convert the Alphabetical data to numeric using CountVectorizer.

4.Predict the number of spam in the data using SVC (C-Support Vector Classification) method of SVM (Support vector machine) in sklearn library.

5.Find the accuracy of the model.. 

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: POCHIREDDY.P
RegisterNumber:  212223240115
import chardet
file = '/content/spam.csv'
with open(file,'rb') as rawdata:
  result = chardet.detect(rawdata.read(100000))
result

import pandas as pd
data= pd.read_csv("/content/spam.csv",encoding='Windows-1252')

data.head()

data.info()

x=data["v1"].values

y=data["v2"].values

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
cv = CountVectorizer()

x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)

from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
*/
```

## Output:
## HEAD():
![image](https://github.com/pochireddyp/Implementation-of-SVM-For-Spam-Mail-Detection/assets/150232043/3cb9d7dc-5c9e-4bf5-a311-31986c33452f)

## INFO():
![image](https://github.com/pochireddyp/Implementation-of-SVM-For-Spam-Mail-Detection/assets/150232043/ed3a4c91-a3a1-4542-ac62-0b72359cf1aa)

## ISNULL().SUM():

![image](https://github.com/pochireddyp/Implementation-of-SVM-For-Spam-Mail-Detection/assets/150232043/c1df7183-2ac1-4667-8935-4a67ceb5c3eb)

## PREDICTED VALUE:

![image](https://github.com/pochireddyp/Implementation-of-SVM-For-Spam-Mail-Detection/assets/150232043/0d2ee3d5-9cbd-4101-9d28-e65d1ec4768c)

## ACCURACY:

![image](https://github.com/pochireddyp/Implementation-of-SVM-For-Spam-Mail-Detection/assets/150232043/b6a09914-66ec-4509-9d38-ee7ef9193d83)



## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
