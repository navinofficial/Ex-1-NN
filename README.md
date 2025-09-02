# Introduction to Kaggle and Data preprocessing

### Name : Navinkumar V
### Reg  : 212223230141
### Date : 30/8/2025 

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:

Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
### STEP 1:Importing the libraries<BR>
### STEP 2:Importing the dataset<BR>
### STEP 3:Taking care of missing data<BR>
### STEP 4:Encoding categorical data<BR>
### STEP 5:Normalizing the data<BR>
### STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:

```
import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split
```
```
df = pd.read_csv("Churn_Modelling.csv")
print(df)
```
```
print(df.isnull().sum())
```
```
df.duplicated().sum
```
```
df.describe()
```
```
df= df.drop(['Surname', 'Geography','Gender'], axis=1)
print(df)
```
```
scaler = MinMaxScaler()
df1 = pd.DataFrame(scaler.fit_transform(df), columns=df.columns)
print(df1)
```
```
X = df1.drop('Exited', axis=1)
y = df1['Exited']
print(X,y)
```
```
X_train ,X_test ,y_train,y_test=train_test_split(X,y,test_size=0.2)
```
```
print("X_train:\n", X_train)
print("X_test:\n", X_test)
print("y_train:\n", y_train)
print("y_test:\n", y_test)
```
## OUTPUT:

### Reading Dataset:
<img width="862" height="328" alt="image" src="https://github.com/user-attachments/assets/db428143-8a8c-4e78-b79c-d246c302ef5d" />

### Missing values:
<img width="292" height="410" alt="image" src="https://github.com/user-attachments/assets/68f9d267-4c43-43dc-a90a-38f7fe268213" />

### Duplicate values:
<img width="457" height="326" alt="image" src="https://github.com/user-attachments/assets/1686c8af-bb92-4ab4-8eaa-1e6384523315" />


### Outlier Detection:
<img width="913" height="332" alt="image" src="https://github.com/user-attachments/assets/e7ce1f22-b025-4b42-b3e9-341287f84919" />

### Remove UUnnecessary Columns:
<img width="746" height="324" alt="image" src="https://github.com/user-attachments/assets/7faa860e-1c7f-4d58-9d11-de7909523f34" />

### Normalize:
<img width="761" height="317" alt="image" src="https://github.com/user-attachments/assets/b4288146-98fe-4646-b0a7-008a6ceac361" />

### X and Y Columns:
<img width="799" height="312" alt="image" src="https://github.com/user-attachments/assets/db9bd701-4b32-4907-b7e7-d5470453da0f" />

### Xtrain and ytrain:
<img width="700" height="712" alt="image" src="https://github.com/user-attachments/assets/e8f8f6d2-cd9b-480b-9440-f7972938a953" />

## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


