---
title       : Developing Data Products Course Project 
subtitle    : Reproducible Pitch (February 2015)
author      : Thomas Tsang
job         : Courserian
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax]     # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Course Project

* A ShinyApp on Rstudio's shiny server
* Provides interactive and graphical representation of power for a sample mean test
* $H_{0}: \mu_{a} = \mu_{0} ; H_{a}: \mu_{a} > \mu_{0}$
* See Statistical Inference course, lecture on Power by B. Caffo, J. Leek and R. Peng (JHBSPH) for reference

--- .class #id 

## What is Power?

* Power is the probability of rejecting the null hypothesis when it is false
* A type II error is failing to reject the null hypothesis
when it's false; the probability of a type II error is usually called $\beta$
* Power $= 1 - \beta$

--- .class #id 

## Example

* $H_{0}: \mu_{a} = \mu_{0} ; H_{a}: \mu_{a} > \mu_{0}$
 
* For $\mu_{0} = 30 ; \mu_{a} = 32 ; \alpha = 0.05 ; n = 16 ; \sigma = 4$


```r
mu0 <- 30
sigma <- 4
mua <- 32
n <- 16
alpha <- 0.05

power.t.test(n,mua-mu0,sd=sigma,type="one.sample",alt="one.sided",sig.level = alpha)$power
```

```
## [1] 0.6040329
```

--- .class #id 

## ShinyApp

Please check my interactive app on Rstudio's shiny server:
* https://t0mix.shinyapps.io/DevDataProdTT/

The R code for this ShinyApp can be found on my GitHub repo:
* https://github.com/t0mix/DevDataProdTT

Thank You!
