# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.Import the required packages.

2.Import the dataset to operate on.

3.Split the dataset.

4.Predict the required output.

5.End the program. 

## Program:
```
Program to implement the SVM For Spam Mail Detection..
Developed by: Bharath Kumar V
RegisterNumber: 212220040025

import pandas as pd
data=pd.read_csv("spam.csv",encoding='latin-1')
data.head()
data.info()
data.isnull().sum()
x=data["v1"].values
y=data["v2"].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.feature_extractiaon.text import CountVectorizer
cv=CountVectorizer()
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
```

## Output:
### Data Head:
![image](https://user-images.githubusercontent.com/93427201/173607454-7cd13092-5f36-430d-ab16-bb9a566a63d6.png)

### Data Info:
![image](https://user-images.githubusercontent.com/93427201/173607604-905180f5-96c1-4f4f-aef4-1b6af4d13a3a.png)

### Data isnull():
![image](https://user-images.githubusercontent.com/93427201/173607749-93b839a9-a7c0-455f-bd06-8808c3f19939.png)

### y_pred:
![image](https://user-images.githubusercontent.com/93427201/173607839-47466fd3-cee9-45e6-9d81-2098688a3f16.png)

### Accuracy:
![image](https://user-images.githubusercontent.com/93427201/173608031-788d7fbf-fbb3-4c04-a4fb-1161e5b93d96.png)



## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
