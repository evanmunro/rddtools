# Parametric analysis
  
Start with the built-in dataset (Lee 2008):
```r
library(rddtools)
data(house)
```

Specify your rdd data:
  
```r
rdd_dat <- rdd_data(x=x, y=y, cutpoint=0, data=house)
```

Now to use the parametric estimator, just use [rdd_reg_lm](https://www.rdocumentation.org/packages/rddtools/versions/0.4.0/topics/rdd_reg_lm):

```r
rdd_dat <- rdd_data(x=x, y=y, cutpoint=0, data=house)
```
