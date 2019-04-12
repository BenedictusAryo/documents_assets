# 05 Deal with Missing Value

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Ketika data yang diinputkan kosong maka akan ditampilkan oleh python dengan ```NaN``` seperti pada variabel 'Medal'. Pada penjelasan kali ini ```NaN``` pada variabel 'Medal' akan diisi dengan ```None``` atau tidak mendapatkan mendali. 

Pada pembelajaran kali ini kita hanya ingin menggunakan data pada tahun 2016 dengan perintah berikut
```
df = df[df['Year']==2016]
df.shape
```
*Output :*
```
(13688,15)
```

Nilai yang kosong pada variabel 'Medal' akan diisi dengan 'None' menggunakan fungsi ```fillna``` seperti perintah berikut
```
df = df.fillna({'Medal' : 'None'})
df.head()
```
*Output :*

| ID | Name              | Sex | Age  | Height | Weight | Team    | NOC | Games       | Year | Season | City           | Sport         | Event                                   | Medal |
|----|-------------------|-----|------|--------|--------|---------|-----|-------------|------|--------|----------------|---------------|-----------------------------------------|-------|
| 22 | Andreea Aanei     | F   | 22.0 | 170.0  | 125.0  | Romania | ROU | 2016 Summer | 2016 | Summer | Rio de Janeiro | Weightlifting | Weightlifting Women's Super-Heavyweight | None  |
| 51 | Nstor Abad Sanjun | M   | 23.0 | 167.0  | 64.0   | Spain   | ESP | 2016 Summer | 2016 | Summer | Rio de Janeiro | Gymnastics    | Gymnastics Men's Individual All-Around  | None  |
| 51 | Nstor Abad Sanjun | M   | 23.0 | 167.0  | 64.0   | Spain   | ESP | 2016 Summer | 2016 | Summer | Rio de Janeiro | Gymnastics    | Gymnastics Men's Floor Exercise         | None  |
| 51 | Nstor Abad Sanjun | M   | 23.0 | 167.0  | 64.0   | Spain   | ESP | 2016 Summer | 2016 | Summer | Rio de Janeiro | Gymnastics    | Gymnastics Men's Parallel Bars          | None  |
| 51 | Nstor Abad Sanjun | M   | 23.0 | 167.0  | 64.0   | Spain   | ESP | 2016 Summer | 2016 | Summer | Rio de Janeiro | Gymnastics    | Gymnastics Men's Horizontal Bar         | None  |

Dapat dilihat dari tabel diatas bahwa pada variabel Medal yang sebelumnya kosong atau ```NaN``` telah beruabh menjadi None.