# 2_2_SVM Library Importing

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video sebelumnya telah dijelaskan konsep dari **SVM** itu sendiri. Nah, pada video kali ini kita akan membahas terkait implementasinya pada Dataset iris yang bisa teman-teman download pada link di bawah ini :

[iris.csv](https://www.dropbox.com/sh/3escqhuxix16hj2/AACymsRstz7Cd6nxfPKeuZ04a?dl=0&preview=iris.csv)

Hal pertama yang perlu dilakukan ialah meng-import package yang digunakan. Secara general package ataupun perintah yang digunakan untuk membuat **SVM** hampir sama seperti **Linear Regression*** atau **Logistic Regression** dan bedanya hanya di beberapa bagian saja.

Sebelum melakukan import package jangan lupa kita perlu menginstall salah satu package mengunakan perintah **_pip install mixtend_** seperti yang telah teman-teman lihat pada video sebelumnya

```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```
Kemudian kita juga memerlukan SVM yang terdapat pada `sklearn` sekaligus juga data preprocessing seperti `LabelEncoder` dan `train_test_split` maupun untuk Scoring yang terdapat pada `sklearn.metrics`.
<br>
Selain itu, kita juga akan menggunakan `plot_decision_regions` yang telah kita install pada package `mlxtend` sebelumnya yang berfungsi untuk memperlihatkan plotting terhadap hasil dari SVM yang kita buat.
```
import math
from sklearn.svm import SVC, SVR
from sklearn.model_selection import train_test_split
from sklearn.metrics import mean_squared_error, mean_absolute_error, r2_score
from sklearn.preprocessing import LabelEncoder
from mlxtend.plotting import plot_decision_regions
```
Sesekali Jupyter notebook menampilkan Warning seperti _Future Deprecation_ dan lainnya yang sebenarnya bukan merupakan error, sehingga terkadang kita membutuhkan ignore warning berikut.
```
import warnings
warnings.filterwarnings('ignore')
```
