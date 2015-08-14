---
layout: post
title: "Lab Blog Test"
date: 2015-8-14
---

This is a test of the blog setup for the NYU PEP lab github site. Here I'm walking through the steps needed to use the ultrasound anaylsis scripts available on [github](https://github.com/NYU-PEP/ultrasound-analysis). For this, you will need to have downloaded the relevant scripts and the example data and installed the R packages `gss` and `ggplot2`.

Load script and data:
{% highlight R %}
source("ssaplot.R")
dat <- read.csv("sample_JASA2006_SSANOVAdata.csv")
{% endhighlight %}

`ssaplot.R` loads the function `ssaplot()` while the sample data gives the data used for the 2006 JASA paper "Title"

## Main effects plots

In typical use, we focus on the main effects plots, which give tongue shapes with confidence intervals for sets of words, allowing comparisons of articulatory structure between different targets. The function ssaplot defaults to the main effects plot. Here is the comparison for the words "bagged" and "baghdad".
{% highlight R %}
ssaplot("bagged", "baghdad",dat)
{% endhighlight %}

This gives the following plot:

![Alt text](/path/to/img.jpg)

## Interaction plots
Instead of this, we can also look at the interaction plot for a particular comparison. While this is less easily viewable as a tongue shape, 