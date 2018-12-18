# Dominance Analysis Package

*This package is designed for regression task where-in provided with a dataset and continous target variable, the package returns the Incremental R-Square that any variable will add to total R-Square of the model. As the complexity of the algorithm increases with number of features, we have in-built functionality that chooses the <b>K=15</b> best features from all the estimators and returns incremental R-Square each variable all to the total R-Square of the model.*

**Installation Command :**
```  
pip install dominance-analysis
```  

**User Guide**
```
from dominance_analysis import Dominance
import pandas as pd
data=pd.read_excel("./Book2.xlsx")
dominance=Dominance(data=data,target='Y',top_k=10,objective=1)
```  

**Incremental R-Square**
```
incr_variable_rsquare=dominance.incremental_rsquare()
```

**Plot Incremental R-Square**
```
dominance.plot_incremental_rsquare()
```
