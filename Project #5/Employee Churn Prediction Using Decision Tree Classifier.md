# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm

~~~
1.import pandas module and import the required data set.
2.Find the null values and count them.
3.Count number of left values.
4.From sklearn import LabelEncoder to convert string values to numerical values.
5.From sklearn.model_selection import train_test_split.
6.Assign the train dataset and test dataset.
7.From sklearn.tree import DecisionTreeClassifier.
8.Use criteria as entropy.
9.From sklearn import metrics.
10.Find the accuracy of our model and predict the require values.
~~~
## Program:
```

/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: Bharath Kumar V
RegisterNumber:  212220040025
*/
import pandas as pd
data = pd.read_csv("Employee.csv")
data.head()
data.info()

data.isnull().sum()

data["left"].value_counts

from sklearn.preprocessing import LabelEncoder
le= LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()

x= data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]

x.head()
y=data["left"]

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.2,random_state = 100)

from sklearn.tree import DecisionTreeClassifier
dt = DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)

y_pred = dt.predict(x_test)
from sklearn import metrics

accuracy = metrics.accuracy_score(y_test,y_pred)
accuracy

dt.predict([[0.5,0.8,9,260,6,0,1,2]])

*/
```


## Output:

![5 1](https://user-images.githubusercontent.com/93427201/169464199-48c6ec39-a17a-497a-a019-eacf1d407504.png)


![5 2](https://user-images.githubusercontent.com/93427201/169464214-50ba4c35-d595-4f52-9fc7-fb1261aa0863.png)


![5 3](https://user-images.githubusercontent.com/93427201/169464218-70fef879-cf2c-4b5a-91b3-2093027bad61.png)

![5 888](https://user-images.githubusercontent.com/93427201/169465155-3072f216-95c4-424f-9e02-839ba0a58649.png)


![5 4](https://user-images.githubusercontent.com/93427201/169464229-b8355e16-5fcc-4b29-9f82-0ad3722c7d32.png)


![5 5](https://user-images.githubusercontent.com/93427201/169464240-bedddfb9-3e16-43d0-959b-85c2de57c60d.png)


![5 6](https://user-images.githubusercontent.com/93427201/169464249-db5864fc-9fb0-49f3-82be-26661f4b30a4.png)

![5 7](https://user-images.githubusercontent.com/93427201/169464949-8e0cad92-493c-4980-b5fb-14da96824345.png)






## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
