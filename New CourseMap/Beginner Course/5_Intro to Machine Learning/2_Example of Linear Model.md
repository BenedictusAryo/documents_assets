# 02 Example of Linear Model

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Pada video kali ini kita akan kita akan menganalisis data uang kita miliki dengan menggunakan linier model. Sebelumnya, kita perlu untuk menginstal package berikut

```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

Misalnya, kita mempunyai data data berat badan dan tinggi badan. Kita dapat membentuk garis regresi linier hubungan antara berat badan dan tinggi badan pada data yang akan kita inputkan berikut 

```
dt = pd.DataFrame({'Height':[150,160,170,175,165,155],
                   'Weight':[40,50,60,65,55,45]})
sns.lmplot(x='Height', y='Weight', data=dt, ci=False)
plt.show()
```

*Output :*

<img src ="https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Beginner%20Course/5_Intro%20to%20Machine%20Learning/Assets/Figure_1.png" width="360" height="360" align="center"/>

Dari gambar diatas didapatkan garis regresi linier yang artinya ketika tinggi badan 150 maka berat badan 40, ketika tinggi 155 maka berat badan 45, dst. 