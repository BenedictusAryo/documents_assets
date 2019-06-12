# Part 6

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video sebelumnya telah dijelaskan konsep dari **SVM** itu sendiri. Nah, pada video kali ini kita akan membahas terkait implementasinya pada program python.

Hal pertama yang perlu dilakukan ialah meng-import package yang digunakan. Secara general package ataupun perintah yang digunakan untuk membuat **SVM** hampir sama seperti **Linear Regression*** atau **Logistic Regression** dan bedanya hanya di beberapa bagian saja.<br>
Sebelum melakukan import package jangan lupa kita perlu menginstall salah satu package mengunakan perintah **_pip install mixtend_**

```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```
```
import math
from sklearn.svm import SVC, SVR
from sklearn.model_selection import trainn_test_split
from sklearn.metrics import mean_squared_error, mean_absolute_error, r2_score
from sklearn.preprocessing import LabelEncoder
from mlxtend.plotting import plot_decision_regions
```

```
import warnings
warnings.filterwarnings('ignore')
```
Untuk datanya dapat di download pada link berikut:<br>
[Reference](https://www.dropbox.com/sh/3escqhuxix16hj2/AACymsRstz7Cd6nxfPKeuZ04a?dl=0&preview=iris.csv)

Nah, untuk lebih jelasnya yuk simak video berikut.