---
layout: post
title: Billboard Analysis
---


## Do songs that debut higher stick around longer on the Billboard charts?

###### We took a look at the data for more than 300 songs that peaked in the year 2000 to determine whether the spot they debuted on the chart was indicative of how long the song would stay one the chart. 

There are a lot of reasons that song which debut high on the list might  have more staying power than those which debuted lower. Song which do well their opening week are likely to appeal more to customers. They open well and stay longer because they're better songs. It could also be that some songs simply have more advertising dollars behind them. They debut high and stick around longer because there's an agency pushing for them. Songs which didn't do as well their debut week were likely either just a flash in the pan or the arch of their popularity barely crossed into the Billboard list. 

We took a sample of over 300 songs that peaked in the year 2000 to see if there was any relationship between how well a song did it's first week on the list and how long it was likely to stay on the list. 

![an image alt text]({{ site.baseurl }}/images/bb_regression.png "Billboard Regression")


The correlation here is not as strong as we would have hoped. The R-squared on our data is just 0.05 so there must be a lot more than goes into explaining how long a song stays on the list. Still we can see there is some correlation. The correlation also goes in the direction we were expecting. Remember, songs which are at 100 are lowest on the list, so from the regression line above we can see that songs which don't do as well the first week are also less likely to stick around on the list.


Let's take a look at the same data another way. The chart below divides our data between songs that debuted high on the list (their first week was lower than 81) represented in blue, and songs which debuted low on the (having a first week above 81) represented in green. We can see from the chart that a lot of the song that didn't do well in the first week were around for less than 10 or 15 weeks, which the songs that did better in the first week are more likely to be toward 25 to 35 week. 

![an image alt text]({{ site.baseurl }}/images/bb_histogram.png "Billboard Histogram")

The data suggests there is significant difference in how long a song stays on the list based on whether it will debuts high on the list.  Songs which debuted higher on the list were also more likely to stick around longer. The songs that debuted high on the list and came on as hits where likely to stick around on the list for over 18 weeks. While songs that came on pretty low on the list (debuted higher than 81) were likely to only stay on for just over 15 weeks. 
