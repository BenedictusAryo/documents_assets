# 4_2_Random Search

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video sebelumnya, kita telah mencoba menggunakan _grid search_. Pada video kali ini kita akan menerapkan _optimization_ menggunakan _random search_ untuk meningkatkan performa dari model yang kita miliki.

Berikut adalah syntaxnya.

```
from scipy.stats import randint as sp_randint
dt_tuned_params = {   "max_depth": sp_randint(1, 4),
                      "min_samples_leaf"  : sp_randint(2, 11),
                      'min_samples_split' : sp_randint(2, 11)}
# you can change it
n_iter_search = 20
random_search = RandomizedSearchCV(model_dt, dt_tuned_params,
                                   n_iter = n_iter_search, cv=5)

random_search.fit(X, y)
print("Best Params : ",random_search.best_params_)
print()
means = random_search.cv_results_['mean_test_score']
stds = random_search.cv_results_['std_test_score']

for mean, std, params in zip(means, stds, random_search.cv_results_['params']):
        print("%0.3f (+/-%0.03f) for %r"
              % (mean, std * 2, params))
```
