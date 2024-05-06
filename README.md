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

5.Find the accuracy of the model.
## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: pochireddy.p
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
### HEAD():
![image](https://github.com/AkilaMohan/Implementation-of-SVM-For-Spam-Mail-Detection/assets/150232043/83f05d99-6e9f-4f8d-b79b-5da8a9313e84)

### INFO():
![image](https://github.com/AkilaMohan/Implementation-of-SVM-For-Spam-Mail-Detection/assets/150232043/77af14c4-d97c-4a72-82fc-a0f3c47d16d4)

### ISNULL().SUM():
![image](https://github.com/AkilaMohan/Implementation-of-SVM-For-Spam-Mail-Detection/assets/150232043/a5c1d040-0587-4edb-a767-23133cee721d)

### PREDICTED VALUE:
![image](https://github.com/AkilaMohan/Implementation-of-SVM-For-Spam-Mail-Detection/assets/150232043/dbe28968-1e6d-4b6d-a901-a44ae3bfc100)

### ACCURACY:
![image](https://github.com/AkilaMohan/Implementation-of-SVM-For-Spam-Mail-Detection/assets/150232043/63595aa6-a777-439a-b789-b349ef380fc5)

## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
