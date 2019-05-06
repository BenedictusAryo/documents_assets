# 04 Dataframe Filtering

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Nah, pada video sebelumnya, kta telah berhasil menjawab pertanyaan tentang jumlah total dari tiap-tiap nilai tertentu, pada kasus ini ialah pengelompokan jumlah pada tiap benua. Selanjutnya kita mendapat pertanyaan kedua terhadap data kita, yakni: 

>**How many countries in Asia who doesn't consume beer?**

Untuk menjawab pertanyaan tersebut, kita membutuhkan teknik filtering dataframe, **pertama** kita filter terlebih dahulu datanya agar hanya memuat negara-negara di benua Asia. **Kedua**, kita filter kembali dari negara-negara Asia tersebut yang jumlah konsumsi beernya adalah **0**. **Ketiga**, kita dapat menghitung jumlah baris yang ada masuk kedalam filter pertama dan kedua.

```
df[(df['continent'] == 'Asia') & (df['beer_servings'] == 0)]
```
*Output :*

| country      | beer_servings | spirit_servings | wine_servings | total_litres_of_pure_alcohol | continent |
|--------------|---------------|-----------------|---------------|------------------------------|-----------|
| Afghanistan  | 0             | 0               | 0             | 0                            | Asia      |
| Bangladesh   | 0             | 0               | 0             | 0                            | Asia      |
| North Korea  | 0             | 0               | 0             | 0                            | Asia      |
| Iran         | 0             | 0               | 0             | 0                            | Asia      |
| Kuwait       | 0             | 0               | 0             | 0                            | Asia      |
| Maldives     | 0             | 0               | 0             | 0                            | Asia      |
| Pakistan     | 0             | 0               | 0             | 0                            | Asia      |
| Saudi Arabia | 0             | 5               | 0             | 0.1                          | Asia      |

Nah, untuk menghitung jumlah negaranya, kita tinggal menambahkan fungsi ```len()``` di luar dari table filtering yang telah kita buat di atas.

```
len(df[(df['continent'] == 'Asia') & (df['beer_servings'] == 0)])
```
*Output :*
```
8
```
