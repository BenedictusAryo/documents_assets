# 2-01 Linear Regression Preparation

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video sebelumnya kita telah mempelajari bagaimana konsep dari `linier regression` dan  `logistic regression`. Nah, pada video kali ini kita akan mempraktekkan langsung tentang `Simple Linear Regression`. Untuk dataset yang akan kita gunakan, bisa di download pada link berikut :

[hou_all.csv](https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Intermediate%20Course/1_Linear%20Model%20and%20Intro%20to%20Supervised%20Machine%20Learning/assets/hou_all.zip)

Hal pertama yang dilakukan untuk melakukan perhitungan `Simple Linier Regression` kita membutuhkan beberapa package, diantaranya:<br>
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```
Kemudian, kita bisa meng-import package untuk `linear regression` sebagai berikut:
```
import math
from sklearn.linear_model import LinearRegression, LogisticRegression
from sklearn.model selection import train_test_split
from sklearn.metrics import mean_squared_error, mean_absolute_error, r2_score
```
Supaya warning yang muncul tidak mengganggu, maka kita bisa ignore dengan cara :
```
import warnings
warnings.filterwarnings('ignore')
```
Kemudian, jika package telah diimport maka selanjutnya kita bisa memuat data yg telah teman-teman download sebelumnya, pada kasus ini, dataset `hou_all.csv` kita letakkan pada folder `data` sehingga script untuk membaca datanya menjadi :

```
data_lin = pd.read_csv('data/hou_all.csv')
data_lin.head()
```
Yuk kita simak penjelasan video berikut.

