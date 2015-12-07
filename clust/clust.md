#Загружаем данные


```r
setwd("~/Документы/R/h")
dh <- read.csv(file = "data.csv", header = FALSE, sep = ",")
str(dh)
```

```
## 'data.frame':	30 obs. of  3 variables:
##  $ V1: num  4 1.4 4.2 4.3 4.5 4 4 4.5 1.5 1.5 ...
##  $ V2: int  2 1 2 2 2 2 2 2 1 1 ...
##  $ V3: num  1.3 0.2 1.2 1.3 1.3 1.3 1 1.5 0.4 0.4 ...
```
Первый столбец - первый признак, второй столбец - известные нам классы, третий - второй признак.

#Одномерная кластеризация. 

Диаграмма стебель-листья по первому признаку построенная вручную.

 ![Диаграмма стебель-листья](1d.jpg)
 
 

```r
hist(dh[,1])
```

![plot of chunk unnamed-chunk-2](figure/unnamed-chunk-2-1.png) 

Увеличив шаг


```r
hist(dh[,1],breaks = 15)
```

![plot of chunk unnamed-chunk-3](figure/unnamed-chunk-3-1.png) 

#Двумерная по двум признакам

Вручную

![2 признака](2d.JPG)

\clearpage


```r
plot(dh[,1],dh[,3])
```

![plot of chunk unnamed-chunk-4](figure/unnamed-chunk-4-1.png) 



