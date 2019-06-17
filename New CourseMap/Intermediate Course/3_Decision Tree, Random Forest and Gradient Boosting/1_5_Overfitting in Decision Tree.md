# 1_5_Overfitting in Decision Tree

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video kali ini kita akan membahas terkait permasalahan klasik tentang *overfitting* pada decission tree. Dalam hal ini ketika pohon semakin dalam maka akan menyebabkan data semakin tidak ideal. Nah, maksutnya bagaimana? Pada video sebelumnya telah dijelaskan pada bagian **Regressor**. Dimana, diketahui bahwa ketika nilai *Regressor Max Depth* semakin besar maka nilai data akan semakin bagus atau semakin fit. Tapi, itu kecenderungan nya akan ke overfitting. Kenapa begitu? Di ilustrasikan, misal ketika kita mempunyai data lain yang tidak berada di area *Max Dept* maka akan langsung menghasilkan nilai akurasi yang jelek. Kira-kira seperti itu impact dari **overfitting**.

Untuk mengatasi hal diatas dapat dikombinasikan menggunakan 2 metode, yaitu **Bagging** dan **Boosting**. Lalu, persamaan dan perbedaan keduanya apa? Persamaan kedua metode diatas yaitu sama-sama menggunakan pohon yang banyak sedangkan perbedaannya ialah ketika bagging ia berjalan secara pararel sementara untuk boosting ia akan berjalan secara sekuensial atau berjalan berurutan. 