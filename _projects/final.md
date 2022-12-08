---
name: Coups and Civil Wars by the Numbers
tools: [Python, HTML, vega-lite]
image: 
description: 
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---
# Coups and Civil Wars by the Numbers
Here are three visualizations that seek to expose interesting connnections between coups and intra-state wars (AKA civil wars) in the twentieth century. 
## About the Data
I made these three visualizations using two different data sets. The first is the Cline Center Coup D’état Project Dataset. This dataset contains records for all the coups (that the data curators identified) that have occurred from 1945-2019. The dataset contains information about these invents, including when they happened, where they happened, and what happened to the deposed executive.
The second is the Correlates of War (COW) Intra-state War Dataset. This dataset contains records for intra-state wars from 1816-2014. 
The following visualizations are intended to show how the power of each dataset is augmented by using it in conjunction with the other.
## What years did coups and civil wars happen? Where?
This is a kind of data visualization known as a dashboard. The two bar graphs are linked to the line graph above. The line graph shows the number of events, both wars and coups, over time. Color indicates the type of event. The user may click and drag horizontally to select a portion of the line graphs. This selected area determines what is shown in the bar plots. The bar plots break down the events from the selected year by country.
It is important to note that wars tend to be more prolonged than coups. The year attached to each war is the year that the war first began.
<vegachart schema-url="{{ site.baseurl }}/assets/json/final_viz_1.json" style="width: 100%"></vegachart>
## In years when many die from civil war, do deposed executives also die?
The line in this graph shows deaths from civil war for the given year. Note that the deaths are assigned to a year according to the year the relevant war began, not the year the deaths occurred. The bars show how many deposed executives were killed in coups that year.
As you can see, there seems to be a rough correlation between civil war deaths and deaths of executive leaders. To put it differently, periods with high deaths seem to also have more deaths of executive leaders.
<vegachart schema-url="{{ site.baseurl }}/assets/json/final_viz_2.json" style="width: 100%"></vegachart>
## Is there a coup season? an intra-ste war season?
These bar graphs show the number of coups and intra-state wars by month. 
It seems that both coups and intra-state wars happen year round!
<vegachart schema-url="{{ site.baseurl }}/assets/json/final_viz_3.json" style="width: 100%"></vegachart>
## Check out the data yourself!
Cline Center Coup D’état Project Dataset: https://doi.org/10.13012/B2IDB-9651987_V3  

Correlates of War Intra-state War Dataset: https://correlatesofwar.org/data-sets/cow-war/  

<div class="middle">
{% include elements/button.html link="https://github.com/ebrigden/ebrigden.github.io/blob/main/python_notebooks/brigden-emory-final3.ipynb" text="The Analysis" %}
</div>
## Citations
Peyton, Buddy; Bajjalieh, Joseph; Shalmon, Dan; Martin, Michael; Bonaguro, Jonathan (2021): Cline Center Coup D’état Project Dataset. University of Illinois at Urbana-Champaign. https://doi.org/10.13012/B2IDB-9651987_V3
Sarkees, Meredith Reid and Frank Wayman (2010). Resort to War: 1816 – 2007. Washington DC: CQ Press.


