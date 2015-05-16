# Reproducible Research: Peer Assessment 1


### Loading and preprocessing the data
Change working directory and load the data.

```r
library(ggplot2)
setwd("~/Documents/Diverse/Coursera Reproducible Research /Peer Assesment 1/Peeras1/RepData_PeerAssessment1/")
df <- read.csv("activity.csv") #Read and convert to data.table
df$date.new <- strptime(paste(as.character(df$date),sprintf("%04.f",df$interval)),format = "%Y-%m-%d %H%M") #Create a new date column in format POSIX
```

 
 



### What is mean total number of steps taken per day?
Below is the code to produce a histogram on number of steps per day.

```r
df.perday <- aggregate(steps~date,df,sum)
qplot(steps,data=df.perday,geom="histogram",ylim=c(0,10),xlab="Number of steps per day",ylab="Count",binwidth=500)
```

![](PA1_template_version02_files/figure-html/unnamed-chunk-2-1.png) 

Here the 

## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
