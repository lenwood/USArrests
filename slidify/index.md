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
</style>

### Introduction

With data from the *1975 World Almanac* and *Statistical Abstracts of the United States*, the [USArrests](http://stat.ethz.ch/R-manual/R-devel/library/datasets/html/USArrests.html) data set within the R [datasets](http://stat.ethz.ch/R-manual/R-patched/library/datasets/html/00Index.html) package brings together 1973 data on Assault, Rape & Murder arrests by state.<br /><br />

Using RStudio's [Shiny](http://shiny.rstudio.com/) package, I have created an interactive chart to view this data by state.<br /><br />

I chose this data set for the challenge of creating a choropleth, and because the data is easily accessible to R (this package is included in a standard R installation).

--- .class #id 

### App Instructions

I have created an interactive chart which dynamically updates based on the crime chosen. The chart displays which states have the highest per capita number of arrests for a given crime.<br /><br />

The app will also calculate the average and standard deviation of the distribution that you select.<br /><br />

To use the web app, select a given crime from the dropdown widget. The chart will automatically update based on your selection.<br /><br />

--- .class #id

### Urban Population Histogram

The USArrests data set contains one variable which I chose not to include in the app because it is different than the other data types. I'll include it here.

<img src="assets/fig/unnamed-chunk-1-1.png" title="plot of chunk unnamed-chunk-1" alt="plot of chunk unnamed-chunk-1" style="display: block; margin: auto;" />

--- .class #id

### Conclusion

My app is located at [lenwood.shinyapps.io/USArrests](https://lenwood.shinyapps.io/USArrests/).

The code for this presentation & my shiny app is visible at my [Github Repository](https://github.com/lenwood/USArrests).

