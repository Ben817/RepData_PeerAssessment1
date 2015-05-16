# Reproducible Research: Peer Assessment 1


## Loading and preprocessing the data
Change working directory and load the data.

```r
setwd("~/Documents/Diverse/Coursera Reproducible Research /Peer Assesment 1/Peeras1/RepData_PeerAssessment1/")
df <- read.csv("activity.csv") #Read and convert to data.table
df$date.new <- strptime(paste(as.character(df$date),df$interval),format = "%Y-%m-%d %H%M")

summary(df)
```

```
##      steps                date          interval     
##  Min.   :  0.00   2012-10-01:  288   Min.   :   0.0  
##  1st Qu.:  0.00   2012-10-02:  288   1st Qu.: 588.8  
##  Median :  0.00   2012-10-03:  288   Median :1177.5  
##  Mean   : 37.38   2012-10-04:  288   Mean   :1177.5  
##  3rd Qu.: 12.00   2012-10-05:  288   3rd Qu.:1766.2  
##  Max.   :806.00   2012-10-06:  288   Max.   :2355.0  
##  NA's   :2304     (Other)   :15840                   
##     date.new                  
##  Min.   :2012-10-01 10:00:00  
##  1st Qu.:2012-10-16 13:15:00  
##  Median :2012-10-31 16:50:00  
##  Mean   :2012-10-31 16:27:59  
##  3rd Qu.:2012-11-15 20:35:00  
##  Max.   :2012-12-01 00:00:00  
##  NA's   :6039
```



## What is mean total number of steps taken per day?



## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
