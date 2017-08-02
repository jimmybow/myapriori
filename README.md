# Myapriori

*Myapriori* is a simple implementation of
Apriori algorithm with Python 2.7 and 3.3 - 3.5,

# Installing :
```
pip install mydcc
```

Usage :
```
import myapriori
import pandas as pd
data = pd.DataFrame([{'性別':'男', '身高':'低'},{'性別':'女', '身高':'低'},{'性別':'男', '身高':'高'}])
rule = myapriori.run(data = data, supp = 0.3, conf = 0.8,  lift = 1.3, maxlen = 2)
rule
```
