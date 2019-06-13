# Part 10

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Pada video sebelumnya kita telah mendapatkan score untuk SVM. Nah, pada video kali ini kita akan melakukan visualiasi hasil dari SVM yang telah kita latih menggunakan `plot_decision_regions` pada _mlxtend_ yang telah kita import sebelumnya 
```
plt.figure(figsize = (10,5))
plt.subplot(121)
plt.title('Training data score = %1.2f'%model.score(X_train, y_train))
plot_decision_regions(X= X_train.values, y= y_train.values, clf = model, legend = 2)

plt.subplot(122)
plt.title('Testing data score = %1.2f'%model.score(X_test, y_test))
plot_decision_regions(X= X_test.values, y= y_test.values, clf = model, legend = 2)

plt.show()
```
Dimana, perintah diatas akan menghasilkan output seperti di bawah.

![Assets](https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Intermediate%20Course/2_Support%20Vector%20Machine/assets/4.png)


