# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import required libraries.
2. Detect the CSV file encoding.
3. Load the spam dataset.
4. Display dataset details and check missing values.
5. Extract input and output columns.
6. Split data into training and testing sets.
7. Convert text data into numerical vectors.
8. Create the SVM classifier model.
9. Train the SVM model.
10. Predict labels for test data.
11. Calculate and display model accuracy.
## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: Cholimgapuram Sai Likitha
RegisterNumber:  212224230046
import chardet
file = '/content/spam.csv'
with open(file, 'rb') as rawdata:
    result = chardet.detect(rawdata.read(100000))
print(result)
import pandas as pd
data = pd.read_csv("/content/spam.csv", encoding='Windows-1252')
print(data.head())
print(data.info())
print(data.isnull().sum())
x = data["v1"].values
y = data["v2"].values
from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test = train_test_split(
    x, y, test_size=0.2, random_state=0
)
from sklearn.feature_extraction.text import CountVectorizer
cv = CountVectorizer()
x_train = cv.fit_transform(x_train)
x_test = cv.transform(x_test)
from sklearn.svm import SVC
svc = SVC()
svc.fit(x_train, y_train)
y_pred = svc.predict(x_test)
print(y_pred)
from sklearn import metrics
accuracy = metrics.accuracy_score(y_test, y_pred)
print("Accuracy:", accuracy)
*/
```

## Output:
<img width="571" height="481" alt="image" src="https://github.com/user-attachments/assets/367d1366-b5ab-4723-bb76-2fc19f58c177" />



## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
