# 4-04 Logistic Regression Probability Plot

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video kali ini kita akan mempelajari bagaimana menampilkan plotting berdasarkan data pada video sebelumnya. Nah, bedanya apa sih plotting antara `linear regression` dan `logistic regression`? Bedanya yaitu, kalau di `logistic regression` kita harus menggunakan syntax **sns.regplot** dan harus menggunakan fitur tambahan berupa **logistic=True**.

```
sns.regplot(x='balance',y='default', data = data_log, logistic=True)
plt.show()
```

Nah, untuk penjelasan terkait output bisa simak video berikut ya teman-teman.
