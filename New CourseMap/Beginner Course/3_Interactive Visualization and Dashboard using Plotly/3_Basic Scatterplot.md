# 03 Basic Scatterplot

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Pada video kali ini, kita akan belajar bagaimana membuat sebuah Scatterplot dengan plotly.
Sebelumnya, kita perlu mengetahui bahwa untuk membuat plot visualisasi dengan plotly, **kita perlu mengimpor library plotly terlebih dahulu**. Kita akan menggunakan plotly versi offline dengan ```plotly.ofline``` sehingga kita tidak perlu membuat akun di situsnya terlebih dahulu dan nanti hasilnya akan muncul di browser kita sendiri.
kemudian kita dapat menggunakan *graph object* untuk membuat berbagai jenis plot seperti yang akan kita pelajari pada video kali ini yakni **scatterplot**.

```
import plotly.offline as pyo
import plotly.graph_objs as go
```
Untuk membuat Scatterplot, kita dapat menggunakan function ```go.Scatter()``` Namun terlebih dahulu kita harus membuat sample datanya menggunakan **Numpy** 

```
import numpy as np

# Create Sample data
np.random.seed(20)
random_x = np.random.randint(0, 51, 100)
random_y = np.random.randint(0, 51, 100)
```

Kemudian untuk melakukan plottingnya, kita gunakan function ```go.Scatter()``` dengan perintah seperti ini :

```
data = [go.Scatter(x=random_x,
                   y=random_y,
                   mode='markers)]

pyo.plot(data)
```

Maka kemudian akan muncul pop up di browser kita. Perlu diperhatikan bahwa ```data``` harus berupa **list** kemudian dalam list itu kita menggunakan ```go.Scatter``` dengan data *x* dan *y* yang telah dibuat sebelumnya.
