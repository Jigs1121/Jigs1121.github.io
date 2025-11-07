---
name: HW  Practice with Jekyll
tools: [Python, vega-lite, Altair]
image: assets/pngs/hw.png
description: Practice Project
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# HW  Practice with Jekyll

Getting some practice saving Altair/vega-lite json schemas for our Jekyll page.

## Graph 1: Interactive Plot using Altair

This graph shows the counties in the U.S and each type of licenses that are present based on a selected county. 

I created this graph by using the [raw data](https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/licenses_fall2022.csv) and loaded the data through pandas. For the graph to left, I encoded my x-axis (License Type) and my y-axis (County) to be Nominal since the values do not have a particular order. The same goes for the y axis for the graph on the right. I decided to use the scheme of blues for my graph since it is simple to read and understand. The darker the color, the more counts there are. For data transformations, I am using the count() function directly into the encoding so that I did not have to manually group the licenses. This is what I did for the x-axis for the graph to the right.

This graph was made using an altair chart and I used the brush interactivity which allows the user to select certain counties and see the license type. Users also have the freedom to choose the size of their selection of counties and the results of the status of the selected counties will be shown on the right graph.


<vegachart schema-url="{{ site.baseurl }}/assets/json/altair_license.json" style="width: 100%"></vegachart>


## Graph 2: Simple plot using Altair

This graph shows the top ten most common license types and shows how many of each license there are. I created this graph using the same [data](https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/licenses_fall2022.csv) from above and this one is simple with no interactivity. 

Similarly to the graph 1, the data transformation I did the count() function into the encoding so that I did not have to group the licenses. For color scheme, I decided to do green so that it could be different than the colors of graph 1. 

<vegachart schema-url="{{ site.baseurl }}/assets/json/top_ten(1).json" style="width: 100%"></vegachart>



<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/licenses_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jnaiman/jnaiman.github.io/blob/master/python_notebooks/inClass_week11.ipynb" text="The Analysis" %}
</div>
