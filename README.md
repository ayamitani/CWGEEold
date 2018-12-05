# CWGEE
Cluster weighted generalized estimating equations for clustered longitudinal data with informative cluster size.
Function available is ordCWGEE for ordinal outcomes.
Function for binary outcomes coming soon.

#### R installation Instructions
```
install.packages("devtools")
library(devtools)
devtools::install_github("AyaMitani/CWGEE")
library(CWGEE)
```
#### Example
```
data(perio)
fitmod <- ordCWGEE(formula = cal ~ mets + edu + age + smoking, data = perio,
id = subject, cluster.var = tooth, time.var = visit, time.str = "ind")
summary(fitmod)
```
