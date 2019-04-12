# 07 How to Change Categorical into Numerical (part2)

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Melanjutkan video sebelumnya, total mendali belum tersusun secara rapi. Akan dilanjutkan dengan penyusunan data Negara berdasarkan total atlet, total Gold, total Silver dan total Bronze. 
```
all_go['None'] = np .where(all_go['Medal'] == 'None', all_go['Total'],0)
all_go['G'] = np .where(all_go['Medal'] == 'Gold', all_go['Total'],0)
all_go['S'] = np .where(all_go['Medal'] == 'Silver', all_go['Total'],0)
all_go['B'] = np .where(all_go['Medal'] == 'Bronze', all_go['Total'],0)
all_go.head()
```
*Output :*
| NOC | Medal  | Total | None | G | S | B |
|-----|--------|-------|------|---|---|---|
| AFG | None   | 3     | 3    | 0 | 0 | 0 |
| ALB | None   | 6     | 6    | 0 | 0 | 0 |
| ALG | None   | 72    | 72   | 0 | 0 | 0 |
| ALG | Silver | 2     | 0    | 0 | 2 | 0 |
| AND | None   | 4     | 4    | 0 | 0 | 0 |

Dari output diatas agar lebih mudah dipahami lebih baiknya kita menggunakan ```groupby ``` untuk menggabungkan negara yang sama, total atlet, total Gold, total Silver dan total Bronze dengan perintah

```
all_go = all_go.groupby('NOC').sum().reset_index().sort_values(by=['G','S','B'], ascending = False)
all_go.head()
```
*Output :*
| NOC | Total | None | G   | S  | B  |
|-----|-------|------|-----|----|----|
| USA | 719   | 455  | 139 | 54 | 71 |
| GBR | 478   | 333  | 64  | 55 | 26 |
| RUS | 406   | 291  | 52  | 28 | 35 |
| GER | 536   | 377  | 49  | 43 | 67 |
| CHN | 499   | 386  | 46  | 30 | 37 |

Untuk menambahkan total mendali dengan nama variabel 'Total_Medals' yang didapat bisa menggunakan perintah berikut
```
all_go ['Total_Medals'] = all_go['Total'] - all_go['None']
all_go.head()
```
*Output :*
| NOC | Total | None | G   | S  | B  | Total_Medals |
|-----|-------|------|-----|----|----|--------------|
| USA | 719   | 455  | 139 | 54 | 71 | 264          |
| GBR | 478   | 333  | 64  | 55 | 26 | 145          |
| RUS | 406   | 291  | 52  | 28 | 35 | 115          |
| GER | 536   | 377  | 49  | 43 | 67 | 159          |
| CHN | 499   | 386  | 46  | 30 | 37 | 113          |

Total Mendali dapat dicari dengan Total atlet dikurangi dengan kolom None (tidak mendapatkan mendali) hasilnya dapat dilihat pada variabel 'Total_Medals'.
