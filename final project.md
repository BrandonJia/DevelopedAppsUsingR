---
title       : Find Your Ideal Weight!
subtitle    : Data product assignment
author      : BrandonChia
job         : Student in Data Science Specialization
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : standalone # {standalone, draft}
knit        : slidify::knit2slides
---

## What's my app
1. Show you the ideal weight associated with your height

2. Input your weight, height and gender data

3. Share your workout schedule

4. Tell us your favorite sports

--- .class #id 

## Easy to use
All you need to do is three steps

* Step 1: Input numbers for weight, height

* Step 2: Check your gender

* Step 3: Submit your answer


---
## Algorithm
The algorithm is based on the report published and recommanded by World Health Organization

_For male_

```r
print ('ideal weight = ( Height - 80 ) * 0.7')
idealWeiM <- function(h) (h-80) * 0.7
```
_For female_

```r
print ('ideal weight = (Height -70) * 0.6')
idealWeiF <- function(h) (h-70) * 0.6
```
_It is good for people whose weight is between 0.9 times of and 1.1 times of ideal weight._


---
## Example
I'm 176 centimeter in height and 70 kilogram in weight,and I'm male.

```r
idealWei <-function(sex,h){
        ifelse(sex =='male',idealWeiM(h),idealWeiF(h))
}
print(paste('My ideal weight is in the interval:'))
idealWei('male',176)*0.9
idealWei('male',176)*1.1
```

```
## [1] "My ideal weight is in the interval:"
## [1] 60.48
## [1] 73.92
```

