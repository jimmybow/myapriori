# Myapriori

*Myapriori* is a simple implementation of
Apriori algorithm with Python 2.7 and 3.3 - 3.6.

# Installing :
```
pip install mydcc
```

# Usage :
```
import myapriori
import pandas as pd
data = pd.DataFrame([{'性別':'男', '身高':'低'},{'性別':'女', '身高':'低'},{'性別':'男', '身高':'高'}])
rule = myapriori.run(data = data, supp = 0.3, conf = 0.8,  lift = 1.3, maxlen = 2)
rule
```

# Arguments:

* **data** -- 原始資料
* **d_type** -- 資料格式，支援以下兩種:
    * d_type = **"df"**  -- Pandas 資料表 (皆為類別欄位) (**Default**)
    * d_type = **"list"** -- 交易資料集，可以是 list of list 或 array of list 
* **supp** -- The minimum support of rules (float).
* **conf** -- The minimum confidence of rules (float).
* **lift** -- The minimum lift of rules (float).
* **maxlen** -- The maximum length of rules (integer).
