---
title: "Example: Embedding Altair & Hvplot Charts"
date: 2019-04-13
published: true
tags: [dataviz, altair, hvplot, holoviews]
excerpt: "Embedding interactive charts on static pages using Jekyll."
altair-loader:
  altair-chart-1: "charts/Summer19claimsAltair.json"
hv-loader:
  hv-chart-1: "charts/measlesHvplot.html"
toc: true
toc_sticky: true
---

This post will show examples of embedding interactive charts produced using [Altair](https://altair-viz.github.io) and [Hvplot](https://hvplot.pyviz.org/).

## Altair Example

The dataset also contained categorizations of protests by type of event. For Summer 2019, the most popular event types are protest, rally, vigil, demonstration and counter protest. Summer 2020 seems to include these protest event types plus some more creative protest types because of COVID-19 and social distancing restrictions. Thus, we see a rise in bike ride, caravan and car caravan protest. This visualization shows each event type by state. We can also see event types by Date within the summer. In Summer 2020, towards the beginning of the summer it appears that rally is the most common event type. In July, protests become more popular over rallies and August included a significant amount of vigils. The vigils were most likely linked to gun shootings that had occurred during this time period. 

<div id="altair-chart-1"></div>

This was produced using Altair and embedded in this static web page. Note that you can also display Python code on this page:

```python
import altair as alt
alt.renderers.enable('notebook')
```

## HvPlot Example

Lastly, the measles incidence produced using the HvPlot package:

<div id="hv-chart-1"></div>

## Notes

- See the [raw source code](https://raw.githubusercontent.com/MUSA-550-Fall-2020/github-pages-starter/master/_posts/2019-04-13-measles-charts.md) of this post for details on how these charts were embedded.
- See the [lecture 13A slides](https://github.com/MUSA-550-Fall-2020/week-13/blob/master/lecture-13A.ipynb) for the code that produced these plots.

**Important: When embedding charts, you will likely need to adjust the width/height of the charts before embedding them in the page so they fit nicely when embedded.**
