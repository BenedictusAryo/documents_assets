# 2_1_Decision Tree Library Importing

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video sebelumnya telah dijelaskan mengenai konsep dari decission tree itu sendiri. Nah, pada video kali ini kita akan mulai mempraktekkan nya pada Jupyter Notebook.

Nah, untuk data yang akan kita gunakan pada video pembelajaran dapat di download pada link berikut : <br>
> [diabetes.csv](https://www.dropbox.com/sh/zfpg3q89pe9hnia/AAC4umEKNsycG0ibVwQ4SQ4ga/diabetes.csv?dl=0)


Hal pertama yang kita perlu lakukan ialah mengimport packages yang dibutuhkan. Untuk syntax nya sebagai berikut. 

```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

import math
from sklearn.tree import DecisionTreeClassifier
from sklearn.ensemble import RandomForestClassifier, GradientBoostingClassifier
from sklearn.model_selection import train_test_split
from sklearn.metrics import mean_squared_error, mean_absolute_error,r2_scored
from mlxtend.plotting import plot_decision_regions

import warnings
warnings.filterwarnings('ignore')
```

Teman-teman mungkin perlu memperhatikkan bahwa kita import Library **_DecisionTree_** yang berada pada `sklearn.tree` namun untuk **_Random Forest_** dan **_Gradient Boosting_** berada pada `sklearn.ensemble`.