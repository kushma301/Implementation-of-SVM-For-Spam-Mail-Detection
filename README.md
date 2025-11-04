# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1.Import the necessary python packages using import statements. 
2.Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head(). 
3.Split the dataset using train_test_split. 
4.Calculate Y_Pred and accuracy. 
5.Print all the outputs. 
6.End the Program.

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: KUSHMA S
RegisterNumber:  212224040168

import pandas as pd
data=pd.read_csv("spam.csv",encoding='latin-1')

import chardet 
file='/content/spam.csv'
with open(file,'rb') as rawdata:
  result = chardet.detect(rawdata.read(100000))
result

data.head()

data.info()

data.isnull().sum()

x=data["v1"].values
y=data["v2"].values

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
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

*/
```

## Output:

## Data head:
<img width="824" height="378" alt="505373976-cdab7479-c1f3-4674-845b-29a1a2324b9c" src="https://github.com/user-attachments/assets/f2fa261d-6416-4886-92a6-8f61792dfbe2" />

## Data info:
<img width="939" height="286" alt="505374086-9d4e7f52-0dfa-4ab6-ac7a-6ecc80e7d007" src="https://github.com/user-attachments/assets/889cefe8-568b-4ad0-b062-2582a448c95f" />

## Checking null:
<img width="686" height="306" alt="505374174-9129b891-860b-478f-bff1-f5413d552e13" src="https://github.com/user-attachments/assets/1506294c-6150-4b8b-8a1c-b917cdde02e3" />

## SVC:
<img width="900" height="406" alt="505374268-0241eed5-67df-4062-b691-1fa93d8ffe5f" src="https://github.com/user-attachments/assets/f4050985-e903-48b3-ac4b-373c37e1c8c1" />

## Y_prediction values:
<img width="791" height="148" alt="505374352-4837361c-232c-409c-8428-152e17e5b490" src="https://github.com/user-attachments/assets/55975850-9824-40dc-b29a-a694bb41812d" />

## Accuracy value:
<img width="707" height="133" alt="505374470-a6212612-248f-44cf-8922-a1af72f28d6b" src="https://github.com/user-attachments/assets/5312b9b4-80f5-4d65-948f-171afcada818" />

## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
