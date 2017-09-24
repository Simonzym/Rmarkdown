# Cars
Me  
2017年9月24日  



## R Markdown


```r
library(hflights)
library(dplyr)
```

```
## 
## Attaching package: 'dplyr'
```

```
## The following objects are masked from 'package:stats':
## 
##     filter, lag
```

```
## The following objects are masked from 'package:base':
## 
##     intersect, setdiff, setequal, union
```

```r
hflights%>%
  filter(UniqueCarrier=="AA")%>%
  group_by(Month)%>%
  summarise(Total_Arr_Delay=sum(ArrDelay,na.rm=T))
```

```
## # A tibble: 12 x 2
##    Month Total_Arr_Delay
##    <int>           <int>
##  1     1              18
##  2     2             461
##  3     3             317
##  4     4            1147
##  5     5            1272
##  6     6            -262
##  7     7            -460
##  8     8           -1417
##  9     9            -841
## 10    10             215
## 11    11              97
## 12    12            2287
```

