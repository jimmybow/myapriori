# Myapriori

A simple implementation of Apriori algorithm with Python 2.7 and 3.3 - 3.6

# Installing :
```
pip install myapriori
```

# Requirements：
* pandas 
* numpy

# Usage :
```
import myapriori
import pandas as pd
```
```
df = pd.DataFrame([{'性別':'男', '身高':'低'},{'性別':'女', '身高':'低'},{'性別':'男', '身高':'高'}])
trans = myapriori.df_to_trans(df)
rules = myapriori.run(data = trans, supp = 0.3, conf = 0.8,  lift = 1.3, maxlen = 2)
rules
```
```
data = [['性別=男', '身高=低'], ['性別=女', '身高=低'], ['性別=男', '身高=高']]
rules = myapriori.run(data = data, supp = 0.06, conf = 0.75,  lift = 1.1, maxlen = 2)
rules
```

# Arguments:

* **data** -- 原始資料，支援兩種格式：pandas.DataFrame 或 list of list (交易資料集)
* **supp** -- The minimum support of rules (float)
* **conf** -- The minimum confidence of rules (float)
* **lift** -- The minimum lift of rules (float)
* **maxlen** -- The maximum length of rules (integer)
