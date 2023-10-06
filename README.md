# EX-05-Feature-Generation


## AIM
To read the given data and perform Feature Generation process and save the data to a file. 

# Explanation
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.
 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature Generation techniques to all the feature of the data set
### STEP 4
Save the data to the file

## PROGRAM & OUTPUT:
NAME : R . JOYCEBEULAH
RED NO : 212222230058
```
import pandas as pd
from scipy import stats
import numpy as np
```
```
df=pd.read_csv("/content/bmi.csv")
```
```
from sklearn.preprocessing import StandardScaler
sc=StandardScaler()
df[['Height','Weight']]=sc.fit_transform(df[['Height','Weight']])
df.head(10)
```
![image](https://github.com/JoyceBeulah/EX-05-Feature-Generation/assets/118343698/7b655bf0-ee81-4f34-a57b-eb7e8be369bd)

```
import pandas as pd
df=pd.read_csv("/content/Encoding Data (1).csv")

from sklearn.preprocessing import LabelEncoder,OrdinalEncoder

temp=["Cold","Warm","Hot"]

enc=OrdinalEncoder(categories=[temp])

df["ord_2"]=enc.fit_transform(df[["ord_2"]])
df
```
![image](https://github.com/JoyceBeulah/EX-05-Feature-Generation/assets/118343698/ce8cf442-4ab2-448c-954a-138c28d4b076)

```
from sklearn.preprocessing import OneHotEncoder

ohe=OneHotEncoder(sparse=False)
ohe.fit_transform(df[["nom_0"]])
```
![image](https://github.com/JoyceBeulah/EX-05-Feature-Generation/assets/118343698/a4c99f23-026e-470d-9cfe-2d9b458acff3)

```
df=pd.read_csv("/content/bmi.csv")

from sklearn.preprocessing import MinMaxScaler
mms=MinMaxScaler()
df=pd.DataFrame(mms.fit_transform(df),columns=['Height','Weight','Index'])
df
```
![image](https://github.com/JoyceBeulah/EX-05-Feature-Generation/assets/118343698/53ff099b-341b-47c2-ad6b-9bfff0d297ca)

```
from sklearn.preprocessing import MaxAbsScaler
mas=MaxAbsScaler()
df=pd.DataFrame(mas.fit_transform(df),columns=['Height','Weight','Index'])
df
```
![image](https://github.com/JoyceBeulah/EX-05-Feature-Generation/assets/118343698/aa1908d6-d294-4b50-9b05-eccc7d28089a)

```
from sklearn.preprocessing import RobustScaler
rs=RobustScaler()
df=pd.DataFrame(rs.fit_transform(df),columns=['Height','Weight','Index'])
df
```
![image](https://github.com/JoyceBeulah/EX-05-Feature-Generation/assets/118343698/c7cd08ee-8c0a-434a-9587-ab67c4095ee3)

# RESULT:
Feature Generation process and Feature Scaling process is applied to the given data frames sucessfully.
