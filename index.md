---
title       : Intercept and slope of Linear Regression
subtitle    : The relation of intercept, slope and mean of data
author      : Helen Gu, Teacher of Shanghai Sports Institute
job         : Shanghai Sports Institute
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax]     # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---
## Summary of the Problem
Suppose we have data of x and y. Are the following two linear regression the same?

Case 1

lm(I(y - mean(y)) ~ I(x - mean(x)) - 1)

Case 2

X1 <- (x - mean(x))/sd(x)

Y1 <- (y - mean(y))/sd(y)

lm(Y1 ~ X1)

---
## Example1


```r
x=c(1:10)
y=1+5*runif(10)+x
```
![plot of chunk unnamed-chunk-3](assets/fig/unnamed-chunk-3-1.png) 

---
## Example2


```r
x=c(1:10)
y=1+10*runif(10)+x
```
![plot of chunk unnamed-chunk-6](assets/fig/unnamed-chunk-6-1.png) 

---
## Conclusion
From the Examples, 
- the intercept of two cases are the same, they all equal 0.

- the slope of two cases are different. The difference is depend on sd(x)/sd(y). Because relation of the slope of case 2 ($k_{2}$) and case 1 ($k_{1}$) is $k_{2}$=$\frac{sd(x)}{sd(y)}\times$$k_{1}$.

