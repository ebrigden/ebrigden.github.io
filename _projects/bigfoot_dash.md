---
name: Bigfoot Dashboard
tools: [Python, HTML, vega-lite]
image: 
description: 
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Scatter Plot
I decided that I wanted to find out if there was a connection between location of bigfoot sightings and the season in which they happened. I started by making a scatter plot of all the sightings with longitude on the x axis and latitude on the y axis. Altair quantitative scales include zero by default, which caused the scatter plot to be zoomed out. By changing the scale's 'zero' attribute to zero, I was able to make it a little more zoomed in. I started with a point mark, but I found the circles looked better and resulted in less lag when linked to the bar plot. I used quantitative encodings for the x and y because latitude and longitude are both numeric. I used nominative for color so that the color scale would be categorical, as is appropariate for the four seasons.

<vegachart schema-url="{{ site.baseurl }}/assets/json/bigfoot_dash.json" style="width: 100%"></vegachart>

# Bar Plot
I decided that, in order to show the relationship between the scatter points' locations and the proportion of season reported, I should link the scatter to a simple bar plot. I chose to encode the seasons as nominative because they are the bar categories. I did this for both Y and color. The x is a record count, which is automatically quantitative. Also, this made the circles the same colors as the bars, which seemed nice. I initially concatenated them horizontally, but this was a bit annoying because if I selected an area that didn't have any records without unknown season, the width would change and jerk the scatter plot to the left. There is probably a way to avoid this, but I thought the vertical concatenation with a horizontal bar plot was an adequate solution.

# Dashboard
I found that summer is generally the most popular season for bigfoot sightings. However, I did notice that in warmer places, like the south, fall and winter are much more popular. I found that in some southern regions, fall is more popular than summer.


<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/main/data/bfro_reports_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/ebrigden/ebrigden.github.io/blob/main/python_notebooks/brigden-emory-assignment10.ipynb" text="The Analysis" %}
</div>

 