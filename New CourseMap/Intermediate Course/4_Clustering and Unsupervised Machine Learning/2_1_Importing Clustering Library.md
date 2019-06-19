# 2_1_Importing Clustering Library

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video sebelumnya kita telah mempelajari terkait teori dari **clustering**. Pada video kali ini waktunya untuk mempraktikkan teori yang telah dijelaskan pada video sebelumnya.<br> 
Untuk data yang digunakan dapat di download pada link berikut :<br>

> [data_1024.csv](https://www.dropbox.com/sh/ew6mjmoq0illzml/AAB0kjCLYYBNerjqLPpKL05ya/data_1024.csv?dl=0)

Seperti biasa, langkah awal sebelum mengimport data yang akan digunakan kita perlu mengimport beberapa packages yang digunakan, diantaranya:
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

import math
from sklearn.cluster import KMeans, DBSCAN
from scipy.cluster.hierarchy import dendogram, linkage
from scipy.spatial.distance import cdist
from sklearn.model_selection import train_test_split

import warnings
warnings.filterwarnings('ignore')
```
```
data_clue = pd.read_csv('data/data_1024.csv', delimiter=';')
data_clue.head()
 ```

Nah, jika biasanya kita selalu menggunakan library dari `sklearn` untuk pengolahan machine learning, pada praktek kali ini, kita juga akan mencoba library dari `scipy` terutama untuk melakukan komputasi _hierarhial clustering_.