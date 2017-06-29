---
title       : "Introduction to Data Visualization"
subtitle    : Some dos and don'ts"
author      : Daniel Anderson
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : zenburn      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
--- 
<style>
em {
  font-style: italic
}
</style>

<style>
strong {
  font-weight: bold;
}
</style>


## Quick stats lesson (with pictures!)
* Mean versus Median versus Mode
* Standard Deviation
* Correlation

----
## Mean versus median versus mode

![plot of chunk normal_dist](assets/fig/normal_dist-1.png)

----
## Mean versus median versus mode

![plot of chunk bimod](assets/fig/bimod-1.png)

----
## Standard deviation

<div align = "center">
<img src = assets/img/sd_norm.png width = 1000 height = 500>
</div>

----
## Standard deviation

![plot of chunk sd_bimod](assets/fig/sd_bimod-1.png)

----
## Correlation

![plot of chunk unnamed-chunk-1](assets/fig/unnamed-chunk-1-1.png)


---- .quote

<q> Above all else, show the data

<br>
Edward Tufte

----
## Classical example: Anscombe's Quartet


|plot | mean_x|   mean_y|     sd_x|     sd_y|       cor|
|:----|------:|--------:|--------:|--------:|---------:|
|1    |      9| 7.500909| 3.316625| 2.031568| 0.8164205|
|2    |      9| 7.500909| 3.316625| 2.031657| 0.8162365|
|3    |      9| 7.500000| 3.316625| 2.030424| 0.8162867|
|4    |      9| 7.500909| 3.316625| 2.030578| 0.8165214|

----
## In visual form

![plot of chunk anscombe_stats](assets/fig/anscombe_stats-1.png)

----
## Better example


|dataset    |   mean_x|   mean_y|     sd_x|     sd_y|        cor|
|:----------|--------:|--------:|--------:|--------:|----------:|
|away       | 54.26610| 47.83472| 16.76983| 26.93974| -0.0641284|
|bullseye   | 54.26873| 47.83082| 16.76924| 26.93573| -0.0685864|
|circle     | 54.26732| 47.83772| 16.76001| 26.93004| -0.0683434|
|dino       | 54.26327| 47.83225| 16.76514| 26.93540| -0.0644719|
|dots       | 54.26030| 47.83983| 16.76774| 26.93019| -0.0603414|
|h_lines    | 54.26144| 47.83025| 16.76590| 26.93988| -0.0617148|
|high_lines | 54.26881| 47.83545| 16.76670| 26.94000| -0.0685042|
|slant_down | 54.26785| 47.83590| 16.76676| 26.93610| -0.0689797|
|slant_up   | 54.26588| 47.83150| 16.76885| 26.93861| -0.0686092|
|star       | 54.26734| 47.83955| 16.76896| 26.93027| -0.0629611|
|v_lines    | 54.26993| 47.83699| 16.76996| 26.93768| -0.0694456|
|wide_lines | 54.26692| 47.83160| 16.77000| 26.93790| -0.0665752|
|x_shape    | 54.26015| 47.83972| 16.76996| 26.93000| -0.0655833|

----
## Plot one of the datasets

![plot of chunk unnamed-chunk-2](assets/fig/unnamed-chunk-2-1.png)

----
## Plot another dataset

![plot of chunk unnamed-chunk-3](assets/fig/unnamed-chunk-3-1.png)

----
## Plot all the datasets

![plot of chunk unnamed-chunk-4](assets/fig/unnamed-chunk-4-1.png)

----
## In gif form

![dino_gif](https://d2f99xq7vri1nk.cloudfront.net/DinoSequentialSmaller.gif)

Matejka & Fitzmaurice (2017). *Same stats, different graphs: Generating datasets with varied appearance and identical statistics through simulated annealing.*

---- .segue
# Some applied examples 

----
## Hypothetical example
* School wants to try out a new reading intervention
* Work with researchers at the UO to design a study
* Kindergarten students who are behind their peers in literacy are selected
* Randomly assign half the students to the intervention, the rest continue with
  "typical" instruction
* Now the study is over - how do we tell if it worked? Visualize it! (and 
  other stuff too)

----
## Barplots
(tried and true)

![plot of chunk barplot](assets/fig/barplot-1.png)

-----
## Boxplots
(tried and true)

![plot of chunk boxplots](assets/fig/boxplots-1.png)

----
## Notched boxplots
(slightly better)

![plot of chunk notched_boxplots](assets/fig/notched_boxplots-1.png)

----
## Stripcharts
Show the data!

![plot of chunk stripchart](assets/fig/stripchart-1.png)

----
## Jittered stripcharts
Show the data!

![plot of chunk jittered_stripchart](assets/fig/jittered_stripchart-1.png)

---
## Combine barplots and jittered stripcharts

![plot of chunk barplot_stripchart](assets/fig/barplot_stripchart-1.png)

----
## Combine boxplots and jittered stripcharts

![plot of chunk boxplot_jitter](assets/fig/boxplot_jitter-1.png)

----
## Best?

![plot of chunk broman_plot](assets/fig/broman_plot-1.png)

----
## Some things to avoid

* 3D plots
* Pie charts
* Dual axes
* Restricted axes
* Unnecessary frills (colors, etc)
	+ Show the data as plainly as possible. Let the data speak!

NOTE: The following 10 slides (and the previous plot) inspired/taken from Karl Broman's presentation on graphs (see [here](https://www.biostat.wisc.edu/~kbroman/presentations/graphs2017.pdf))

--- &twocol
## Examples

*** =left

<div align = "center">
<img src = assets/img/broman_plot.png width = 500 height = 500>
</div>

*** =right

<div align = "center">
<img src = assets/img/bad_data_vis/3d_bar.png width = 500 height = 500>
</div>

--- &twocol
## Examples

*** =left

<div align = "center">
<img src = assets/img/broman_plot.png width = 500 height = 500>
</div>

*** =right

<div align = "center">
<img src = assets/img/bad_data_vis/tube_bar.png width = 500 height = 500>
</div>


--- &twocol
## Examples

*** =left

<div align = "center">
<img src = assets/img/broman_plot.png width = 500 height = 500>
</div>

*** =right

<div align = "center">
<img src = assets/img/bad_data_vis/cone_bar.png width = 500 height = 500>
</div>

--- &twocol
## Examples

*** =left

<div align = "center">
<img src = assets/img/broman_plot.png width = 500 height = 500>
</div>

*** =right

<div align = "center">
<img src = assets/img/bad_data_vis/orbs.png width = 500 height = 500>
</div>


--- &twocol
## Examples

*** =left

<div align = "center">
<img src = assets/img/broman_plot.png width = 500 height = 500>
</div>

*** =right

<div align = "center">
<img src = assets/img/bad_data_vis/pie.png width = 500 height = 500>
</div>

--- &twocol
## Examples

*** =left

<div align = "center">
<img src = assets/img/broman_plot.png width = 500 height = 500>
</div>

*** =right

<div align = "center">
<img src = assets/img/bad_data_vis/exploded_pie.png width = 500 height = 500>
</div>


--- &twocol
## Examples

*** =left

<div align = "center">
<img src = assets/img/broman_plot.png width = 500 height = 500>
</div>

*** =right

<div align = "center">
<img src = assets/img/bad_data_vis/donut.png width = 500 height = 500>
</div>

--- &twocol
## Examples

*** =left

<div align = "center">
<img src = assets/img/broman_plot.png width = 500 height = 500>
</div>

*** =right

<div align = "center">
<img src = assets/img/bad_data_vis/area.png width = 500 height = 500>
</div>

--- &twocol
## Examples

*** =left

<div align = "center">
<img src = assets/img/broman_plot.png width = 500 height = 500>
</div>

*** =right

<div align = "center">
<img src = assets/img/bad_data_vis/double_terrain.png width = 500 height = 500>
</div>

--- &twocol
## Examples

*** =left

<div align = "center">
<img src = assets/img/broman_plot.png width = 500 height = 500>
</div>

*** =right

<div align = "center">
<img src = assets/img/bad_data_vis/terrain.png width = 500 height = 500>
</div>

----
## Some great examples: SEDA
Sean Reardon: https://cepa.stanford.edu/seda/overview

<div align = "center">
<img src = assets/img/seda.png width = 800 height = 600>
</div>

----
## Means by district
<div align = "center">
<img src = assets/img/seda_means.png width = 900 height = 500>
</div>

----
## Average gains by district
<div align = "center">
<img src = assets/img/seda_growth.png width = 900 height = 500>
</div>

----
## Mean scores and SES
<div align = "center">
<img src = assets/img/seda_ses.png width = 900 height = 500>
</div>

----
## Mean scores and SES by Race/Ethniciy
<div align = "center">
<img src = assets/img/seda_ses_race.png width = 900 height = 500>
</div>

---
## Other examples: Visualizing scale
* Space stuff: http://imgur.com/a/lGabv
<br>
* Time: https://www.businessinsider.com.au/animated-timeline-earth-history-2015-11

----
## Some *ggplot* examples

![plot of chunk mpgEx3](assets/fig/mpgEx3-1.png)

----
## Add an additional aesthetic

![plot of chunk mpgEx4](assets/fig/mpgEx4-1.png)

----
## Add smooth line for each class
# Too busy

![plot of chunk mpgEx5b](assets/fig/mpgEx5b-1.png)

----
## Remove SE

![plot of chunk mpgEx6a](assets/fig/mpgEx6a-1.png)

---- .segue
# Some things to avoid

----
## Truncated axes
<div align = "center">
<img src = assets/img/bad_data_vis/truncated_axes.png width = 900 height = 500>
</div>

----
<div align = "center">
<img src = assets/img/bad_data_vis/truncated_axes2.png width = 900 height = 500>
</div>

----
<div align = "center">
<img src = assets/img/bad_data_vis/truncated_dishonest.png width = 700 height = 650>
</div>


----
## Dual axes
<div align = "center">
<img src = assets/img/bad_data_vis/dual_axes.png width = 800 height = 500>
</div>

[Proof](http://www.tylervigen.com/spurious-correlations) dual axes are bad. But, some [lively](https://stackoverflow.com/questions/3099219/plot-with-2-y-axes-one-y-axis-on-the-left-and-another-y-axis-on-the-right) discussion. 

----
## Scaling issues
<div align = "center">
<img src = assets/img/bad_data_vis/area_size.png width = 900 height = 500>
</div>

----
## Poor binning choices
<div align = "center">
<img src = assets/img/bad_data_vis/poor_binning.png width = 900 height = 500>
</div>

----
## Some general advice
* Consider the purpose of the plot. 
	+ Relation? Scatterplots 
	+ Distribution? Histogram or density plot
	+ Trend? Line plot, scatterplot with smoother, etc.
* How many variables? What type?
	+ One continuous variable: histogram, density plot, or similar
	+ Two continuous: Scatterplot (if you have lots of data, consider binning)
	+ One categorical one continuous: boxplots, violin plots, bar plots
	+ Two categorical variable? Mosaic plot

----
## One continuous variable
# Histogram
![plot of chunk hist](assets/fig/hist-1.png)

----
## One continuous variable
# Density plot
![plot of chunk density](assets/fig/density-1.png)

----
## One continuous variable
# Frequency polygon
![plot of chunk freqpoly](assets/fig/freqpoly-1.png)

----
## Consider overlays
![plot of chunk overlay](assets/fig/overlay-1.png)

----
## Two continuous variables
# Scatterplot

![plot of chunk scatter](assets/fig/scatter-1.png)

----
## Trend
# Line plot (often with date or time on x-axis)
![plot of chunk trend](assets/fig/trend-1.png)

----
## Trend w/smoother

![plot of chunk trend_smooth](assets/fig/trend_smooth-1.png)

---
## Categorical & Continuous
# Violin plots

![plot of chunk violin_plot](assets/fig/violin_plot-1.png)

---
## Overlay data

![plot of chunk violin_plot_data](assets/fig/violin_plot_data-1.png)

---
## Two categorical variables
# Mosaic plot
![plot of chunk mosaic_plot](assets/fig/mosaic_plot-1.png)

----
## Don't end up in a blog for wrong reasons
* https://flowingdata.com/2010/05/14/wait-something-isnt-right-here/
* https://flowingdata.com/2009/11/26/fox-news-makes-the-best-pie-chart-ever/

----
## One more example

<div align = "center">
<img src = assets/img/bad_data_vis/pie_dishonest.png width = 700 height = 550>
</div>

----
## Conclusions
* Essentially never
	+ Use pie charts (use bar charts instead)
	+ Use dual axes (produce separate plots instead)
	+ Use 3D unnecessarily
	+ Add color for color's sake (this isn't sales)
* Rarely
	+ Truncate axes
* Do
	+ Show the data
	+ Be as clear as possible
	+ Let the data tell the story

----
## Last pitch
* Plotting your data can often lead to surprises. 
* Good data visualization can [often](http://www.tandfonline.com/doi/abs/10.1080/01621459.2013.808157) be just as powerful for inference as complex modeling.
* Ideally, use it for more than just communicating what you already know! (I want to help build tools to make it easier for you to do so)
