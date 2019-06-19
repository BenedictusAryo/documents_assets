# Part 6

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video kali ini, kita akan mulai melakukan praktek dalam mengimplementasikan _validation_ dan _optimization_ pada model yang akan kita buat.

Nah, untuk dataset dapat di download pada link berikut : <br>
> [diabetes.csv](https://www.dropbox.com/sh/zfpg3q89pe9hnia/AAC4umEKNsycG0ibVwQ4SQ4ga/diabetes.csv?dl=0)

Namun sebelumnya seperti biasa kita harus melakukan _import_ _packages_ yang kita butuhkan. Berikut adalah syntaxnya.

```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

import math
from sklearn.tree import DecisionTreeClassifier
from sklearn.model_selection import KFold, LeaveOneOut, GridSearchCV, RandomizedCV, train_test_split

import warnings
warnings.filterwarnings('ignore')
```


