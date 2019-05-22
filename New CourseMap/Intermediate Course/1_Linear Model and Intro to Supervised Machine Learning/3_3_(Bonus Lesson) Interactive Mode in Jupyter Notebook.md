# 3-03 (Bonus Lesson) Interactive Mode in Jupyter Notebook

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Video kali ini merupakan video bonus interactive. Sebelumnya kita membutuhkan beberapa perintah diantaranya:

```
from IPython.display import SVG
from IPython.display import display
from ipywidgets import interactive
```
Tujuan dari perintah diatas sebenarnya simple. Ketiga syntax diatas bertujuan untuk mengubah gambar menjadi `interactive` sesuai dengan keinginan kita. Pada dasarnya untuk membuat `interactive` sama seperti video sebelumnya namun yang membedakan disini ialah pada `interactive` kita menggunakan perintah **subplot**. Untuk lebih jelasnya perhatikan syntax berikut yuk.

```
lm = LinearRegression()

def plot_reg(feature, target, test_size):
    # feature matrix
    X = data_lin [[feature]]
    y = data_lin [target]
    X_train,X_test, y_train, y_test = train_test_split(X, y,
    test_size = 0.2, random_state=45)
    lm.fit(X_train, y_train)

    f = plt.figure(figsize = (15,15))

    plt.subplot(221)
    sns.regplot(x = X_train, y = y_train, data = data_lin, ci 
    = None);
    plt.xlabel(feature)
    tl = lm.score(X_train, y_train)
    plt.title ('Training - R2 score:%f' %t1)
    
    lm.predict(X_test)

    plt.subplot(222)
    sns.regplot(x = X_test, y = y_test, data = data_lin,
    ci=None);
    plt.xlabel(feature)
    t2 = lm.score(X_test, y_test)
    plt.title('Testing - r2 score:%f' %t2)

inter = interactive(plot_reg, feature = list(data_lin.columns), target = ["MEDV"],test_size = [.05, .10, .15, .20, .25, .30, .35, .40, .45, .50])
display (inter)
```

Nah, nanti akan menghasilkan ouput sebagai berikut:

![assets](https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Intermediate%20Course/1_Linear%20Model%20and%20Intro%20to%20Supervised%20Machine%20Learning/assets/2019-05-17_11-31-30.png)

Penasaran sama penjelasan output diatas? Yuk simak video berikut.