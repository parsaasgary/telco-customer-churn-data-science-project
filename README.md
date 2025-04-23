# telco-customer-churn-data-science-project
## so this a data science project over telco customer data set . in this project what i did was data cleaning , EDA , preprocessing , build two models and evaluate them.
### so the first part is EDA
at first , i get to know the data and the dtypes of it colunms . then do the usual thing like detecting duplicate and nulls and some static reports.

after that come to visualization . i visual each colunms regard to the target to understan the correlation between them and understand my data better
beacuase most of the colunms was object , there was not much to do . only `barchart` and mabe `piecahrt` 
but from num colunms it was easier to mine data . for example the outliers detection was detectable in `violan` and `box` chart from num colunms
### preprocessing
after EDA , i encoded the target with `labelencoder` and other obj colunms with `onehotencoder` .
then i had some more numaric data to work with
after that i build another `DF` . one that i removed the outliers from it.
from this part , i worked with both data frames 
### building models
i choosed `RandomeForestclassifier` and `XGBClassifier` to work with . with the help of `Gridsearchcv` i could finde the hyperprameters that were suited and with `Kfold validation` the chance of having a good split of train/test was reduced
i train both data frames with and without outliers with these two models and evaluate them not only with `accurecy` but with `recall` , `precisio` and `F1`.
and let me tell you that result was satisfying:)
### as conclusion
the model that was train without outliers perform better than the other
result was same for `RandomeForestclassifier` and `XGBClassifier` , but i choosed `XGBClassifier` as best model and pickkeled it
## libraries that used:
`numpy`
`pandas`
`matplotlib`
`seaborn`
`sklear`
`xgb`
and their built in classes
