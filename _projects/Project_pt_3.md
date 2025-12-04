---
name: Project Part 3
tools: [Python, vega-lite, Altair]
image: assets/pngs/visualization.png
description: This project showcases registered electric vehicles in the state of Washington
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Electric Vehicles are on the Rise but how Fast are they Growing and when did this Trend Start?

Electric Vehicles are on the rise everyday in order to reduce emissions and make the air we breathe cleaner everyday. 

## Graph 1: Simple Plot Showing Top 20 Counties with EV



<vegachart schema-url="{{ site.baseurl }}/assets/json/county.json" style="width: 100%"></vegachart>




## Graph 2: Simple Plot Showing Something



## Graph 3: Interactive Plot

<vegachart schema-url="{{ site.baseurl }}/assets/json/electric.json" style="width: 100%"></vegachart>

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/Jigs1121/Jigs1121.github.io/refs/heads/main/electric_filtered.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/Jigs1121/Jigs1121.github.io/blob/main/python_notebooks/Part 3.ipynb" text="The Analysis" %}
</div>
