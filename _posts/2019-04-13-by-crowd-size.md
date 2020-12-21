---
title: "Protests by Crowd Size"
date: 2019-04-13
published: true
tags: [dataviz, folium]
excerpt: "This post discusses protests by size and date"
altair-loader:
  altair-chart-1: "charts/Summer19Estimates.json"
  altair-chart-2: "charts/Summer20Estimates.json"
  altair-chart-3: "charts/SummerEstimatescompared.json"
toc: false
toc_sticky: false
---


## Crowd Sizes in Summer 2019

  Next we examine the crowd sizes for both summers by dates. Hopefully, our examinations will enable us to see the trends in what dates crowds were highest and perhaps connect those to the news cycle. The datasets had the low and high estimates for each event and we went with the low estimates to be on the conservative side. We used a rolling mean to do this in order to get the 2 week average of crowds on any given day. In Summer 2019, it appears that on June 29th crowd sizes were at 10,469 people and on June 30th they had peaked to 60,559 people. Based on some brief research, it appears that the day before June 30th, the Supreme Court chose to consider whether Trump could shut down the DACA program (Deferred Action for Childhood Arrivals). These heightened crowds lasted for about two weeks until July 14th and then subsided at low levels for the rest of the summer. 

<div id="altair-chart-1"></div>

## Crowd Sizes in Summer 2020

  In Summer 2020, we see protests starting at a higher base point as George Floyd was murdered on May 25th. The height of the protests was on June 7th with 153,071 Americans participating in a type of protest event. The protests steeply declined after this. 


<div id="altair-chart-2"></div>

## Conclusion

<div id="altair-chart-3"></div>

In both Summer 2019 and 2020, the crowds were not big enough to be at the 3.5 % threshold for changing something in the country that Chenoweth claims. In the next post, we will  examine if the 3.5% rule works on the county level in the US using cenpy. 

### Future Research Ideas
Some future research related to this topic might include examining the crowd sizes by weekday vs weekend to see if there are specific days where protests are more popular in both Summer 2019 and Summer 2020. 
