# 10 Line Chart 

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
_Dataset untuk Latihan pada Bab ini bisa di download di : 
[athlete_events.csv](https://drive.google.com/file/d/1M5KLfA9DpVWiKqVQ9bwjFJWcl0yl-9TX/view?usp=sharing)_

Pada pembelajaran ini kita ingin melihat total perolehan mendali dari tahun ke tahun untuk negara Yunani (pelopor olimpiade). Kita perlukan pemanggilan data kembali karena biasanya cukup bagus ketika ingin melihat perkembangan dari tahun ketahun.
```
df1 = pd.read_csv('data/athlete_events.csv')
```
Kemudian kita lanjutkan dengan menggabungkan jumlah mendali  sesuai dengan Year, NOC dan Mendali.
```
all_new = pd.DataFrame(df1.groupby(['Year','NOC','Medal'])['Medal'].size())
```
*Output :*

| Year | NOC | Medal  | Medal |
|------|-----|--------|-------|
| 1896 | AUS | Bronze | 3     |
|      |     | Gold   | 6     |
|      | AUT | Bronze | 72    |
|      |     | Gold   | 2     |
|      |     | Silver | 4     |

Pada tabel diatas mempunyai 2 nama variabel 'Medal'. Kita harus mengubah salah satu nama variabel tersebut karena ketika proses selanjutnya ketika memanggil kolom Medal akan error karena kolom Medal ada 2 dan dilanjutkan untuk me-reset index. 

```
all_new.columns = ['Total']
all_new = all_new.reset_index()
```
*Output :*

| Year | NOC | Medal  | Total |
|------|-----|--------|-------|
| 1896 | AUS | Bronze | 1     |
| 1896 | AUS | Gold   | 2     |
| 1896 | AUT | Bronze | 2     |
| 1896 | AUT | Gold   | 2     |
| 1896 | AUT | Silver | 1     |

Setelah variabel terlah berubah dan index telah di-reset menjadi seperti output diatas. Maka, dilanjutkan untuk penyusunan data Negara berdasarkan total atlet, total Gold, total Silver dan total Bronze dilanjutkan dengan ```.grupby``` berdasarkan tahun.

```
all_new['None'] = np.where(all_new['Medal'] == 'None', all_new['Total'],0)
all_new['G'] = np.where(all_new['Medal'] == 'Gold', all_new['Total'],0)
all_new['S'] = np.where(all_new['Medal'] == 'Silver', all_new['Total'],0)
all_new['B'] = np.where(all_new['Medal'] == 'Bronze', all_new['Total'],0)

all_new = all_new.groupby(['Year','NOC']).sum().reset_index().sort_values(by=['G','S','B'], ascending = False)
```
*Output :*

| Year | NOC | Total | None | G   | S   | B   |
|------|-----|-------|------|-----|-----|-----|
| 1980 | URS | 496   | 0    | 205 | 158 | 133 |
| 1984 | USA | 361   | 0    | 190 | 121 | 50  |
| 1988 | URS | 366   | 0    | 174 | 81  | 111 |
| 1996 | USA | 259   | 0    | 159 | 48  | 52  |
| 1976 | URS | 342   | 0    | 152 | 102 | 88  |

Nah, kemudian kita akan pilih negara yang akan kita lihat total mendalinya dalam hal ini kita memilih Yunani (GRE) sebagai pelopor Olympiade. 
```
gre = all_new[all_new['NOC']=='GRE']
sns.lineplot(x='Year', y='Total', data=gre)
```
*Output :*


<img src ="https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Basic%20Course/3_Basic%20Visualization/Assets/Figure_6.png" width="460" height="360" align="center"/>

Didapatkan bahwa pada tahun 1906 mendapatkan mendali paling tinggi dan turun secara signifikan pada tahun selanjutnya, dst.