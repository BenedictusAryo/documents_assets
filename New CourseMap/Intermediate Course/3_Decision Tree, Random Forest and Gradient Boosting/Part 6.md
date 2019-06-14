# Part 6

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video sebelumnya telah dijelaskan mengenai konsep dari decission tree itu sendiri. Nah, pada video kali ini kita akan mulai mem-praktekkan nya pada software.

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
Nah, untuk data dapat di download pada link berikut ya <br>
[Reference](https://www.dropbox.com/sh/zfpg3q89pe9hnia/AAC4umEKNsycG0ibVwQ4SQ4ga/diabetes.csv?dl=0)

