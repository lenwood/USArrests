---
title       : Violent Crime Rates
subtitle    : Maps of 1973 violent crime arrests by state
author      : Chris Leonard
job         : January 16, 2015
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---
<style>
em {font-style: italic}
strong {font-weight: bold}
</style>

### Introduction

With data from the *1975 World Almanac* and *Statistical Abstracts of the United States*, the [USArrests](http://stat.ethz.ch/R-manual/R-devel/library/datasets/html/USArrests.html) data set within the R [datasets](http://stat.ethz.ch/R-manual/R-patched/library/datasets/html/00Index.html) package brings together 1973 data on Assault, Rape & Murder arrests by state.<br /><br />

The USArrests data set is a data frame with 4 variables for each state:
 - **Assault** - number of Assault arrests per 100,000 people.
 - **Rape** - number of Rape arrests per 100,000 people.
 - **UrbanPop** - percentage of urban population.
 - **Murder** - number of Murder arrests per 100,000 people.

I chose this data set for the challenge of creating a [choropleth](https://en.wikipedia.org/wiki/Choropleth_map), and because the data is easily accessible to R (this package is included in a standard R installation).

--- .class #id 

### App Instructions

Using RStudio's [Shiny](http://shiny.rstudio.com/) package, I have created an interactive chart to view this data by state. My app does 3 things:
  1. US map updates with data on the selected crime.
  2. Calculates the average & standard deviation of the data presented.
  3. Provides an interactive table to easily view the data.

To use the web app, select a given crime from the dropdown widget. The chart will automatically update based on your selection. The chosen crime's average & standard deviation will be displayed, and you can hover over a state to see the number of arrests. Navigate through the tabs at the top to view the data.<br /><br />

--- .class #id

### Urban Population Histogram

Here I'll create a histogram of the Urban Population data within USArrests.


```r
data(USArrests); urbanPop <- USArrests$UrbanPop
hist(urbanPop, xlab="Urban Population Percentage", freq=FALSE, 
     col="lightgreen", xlim=c(15, 115), ylim=c(0, 0.03))
curve(dnorm(x, mean=mean(urbanPop), sd=sd(urbanPop)), add=TRUE, 
      col="darkblue", lwd=2)
```

<img src="assets/fig/unnamed-chunk-1-1.png" title="plot of chunk unnamed-chunk-1" alt="plot of chunk unnamed-chunk-1" style="display: block; margin: auto;" />

--- .class #id

### Conclusion

This presentation and the app were created for the [Developing Data Products](https://www.coursera.org/course/devdataprod) course project.<br /><br />

My app is located at [lenwood.shinyapps.io/USArrests](https://lenwood.shinyapps.io/USArrests/).<br /><br />

The code for this presentation & my shiny app is visible at my [Github Repository](https://github.com/lenwood/USArrests).

