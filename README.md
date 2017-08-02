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

* data -- 原始資料，支援兩種資料格式:
    * d_type = 'df' -- Pandas 資料表 (皆為類別欄位)
    * d_type = 'list' -- 交易資料集，可以是 list of list 或 array of list 
* min_support -- The minimum support of relations (float).
* min_confidence -- The minimum confidence of relations (float).
* min_lift -- The minimum lift of relations (float).
* max_length -- The maximum length of the relation (integer).
