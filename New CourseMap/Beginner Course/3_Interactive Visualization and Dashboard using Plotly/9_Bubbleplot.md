# 09 Bubble Plot

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video kali ini kita akan membahas bagaimana caranya membuat sebuah **Bubble Plot**.

Nah, kan sebelumnya telah dijelaskan mengenai **scatterplot**. Dimana scatterplot merupakan sekumpulan data yang kita plot dan peta-kan dalam dua axis, yakni x dan y. 

Lalu, bagaimana jika data yang dimiliki memiliki kolom yang cukup banyak dan kita ingin menambahkan kolom dan dimensi yang dapat ditampilkan dalam sebuah plot?

Dataset untuk kita gunakan pada video kali ini dapat didownload di link berikut : [mpg.csv](https://www.dropbox.com/s/bdmy0iaqustpck7/mpg.csv?dl=0) <br>
Atau bisa juga menggunakan shortlink berikut pada pandas :

```
import pandas as pd
df = pd.read_csv('http://bit.ly/datasetmpg')
```

Untuk membuat **Bubble Plot** pada dasarnya sama seperti membuat scatterplot dan hanya menambahkan `marker size` pada kolom ketiga sebagai berikut:

 ```
 data = [go.Scatter(x=df['weight'],
                    y=df['mpg'],
                    text=df['name'],
                    mode='markers',
                    marker=dict(size=df['cylinders']))]
 ```

Jadi hasilnya akan sebagai berikut :

![assets](https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Beginner%20Course/3_Interactive%20Visualization%20and%20Dashboard%20using%20Plotly/assets/11_Bubble_plot.gif)

 Untuk lebih jelasnya, yuk simak video berikut.
