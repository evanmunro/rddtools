---
title: "Parametric analysis"
permalink: /docs/parametric/
excerpt: "Running a analysis with parametric estimation"
modified: 2016-09-22
output: 
  html_document: 
    keep_md: yes
---
  
Start with the built-in dataset (Lee 2008):

{% highlight r %}
library(rddtools)
data(house)
{% endhighlight %}

Specify your rdd data:
  

{% highlight r %}
rdd_dat <- rdd_data(x=x, y=y, cutpoint=0, data=house)
{% endhighlight %}

Now to use the parametric estimator, just use [rdd_reg_lm](https://www.rdocumentation.org/packages/rddtools/versions/0.4.0/topics/rdd_reg_lm):


{% highlight r %}
house_reg1 <- rdd_reg_lm(rdd_dat)
house_reg1
{% endhighlight %}



{% highlight text %}
## ### RDD regression: parametric ###
## 	Polynomial order:  1 
## 	Slopes:  separate 
## 	Number of obs: 6558 (left: 2740, right: 3818)
## 
## 	Coefficient:
##    Estimate Std. Error t value  Pr(>|t|)    
## D 0.1182314  0.0056799  20.816 < 2.2e-16 ***
## ---
## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
{% endhighlight %}
