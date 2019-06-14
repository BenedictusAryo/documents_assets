# Part 9

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video sebelumnya kita telah membagi data kedalam train dan test. Pada video kali ini kita akan membuat model terkait dengan video sebelumnya. 
```
model_dt = DecisionTreeClassifier(criterion = 'entropy')
model_rf = RandomForestClassifier(criterion ='entropy')
model_gb = GradientBoostingClassifier() 
```
```
model_dt.fit(X_train,y_train)
model_rf.fit(X_train, y_train)
model_gb.fit(X_train, y_train)
```
```
model_dt.predict(X_test)
model_rf.predict(X_test)
model_gb.predict(X_test)
```
Nah, untuk penjelasannya dapat dilihat pada video berikut. 