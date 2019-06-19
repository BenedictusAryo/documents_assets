# 4_1_Grid Search

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Setelah kita memperoleh performa model kita yang divalidasi menggunakan _K-Fold CV_ atau _LOOCV_, kita dapat melakukan _optimization_ untuk meningkatkan performa dari model yang kita miliki. Pada video kali ini kita akan melakukan _optimization_ dengan menggunakan _grid search_.

Berikut adalah syntaxnya.

```
dt_tuned_params = {'min_samples_leaf': [1, 5, 10],
                   'min_samples_split' : [2, 3, 5, 7],
                   'max_depth' : [3,5,7,10]}
GridDT = GridSearchCV(model_dt, dt_tuned_params, cv=5)
GridDT.fit(X,y)

print("Best Params : ",GridDT.best_params_)
print()
means = GridDT.cv_results_['mean_test_score']
stds = GridDT.cv_results_['std_test_score']

for mean, std, params in zip(means, stds, GridDT.cv_results_['params']):
        print("%0.3f (+/-%0.03f) for %r"
              % (mean, std * 2, params))
```
