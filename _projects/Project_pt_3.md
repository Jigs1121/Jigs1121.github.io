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


# The Rise of Electric Vehicles

Electric Vehicles are on the rise everyday in order to reduce emissions and make the air we breathe cleaner everyday. However, it is important to explore when this boom in electric vehicles started to pick up and explore which companies are hopping on this trend of creating their own electric vehicles.

## About the Dataset

Our dataset comes from [Data.gov](https://catalog.data.gov/dataset/electric-vehicle-population-data) and this dataset shows all of the registered electric vehicles in the United States. However, about 90% of the data covers only the State of Washington so this analysis is only representative of the State of Washington. Each row in this dataset represents an electric vehicle and contains basic information of that vehicle such as where it was registered, what car brand it is, what model it is, what year it was made, and more.

## Project Goals

This analysis dives into how many electric vehicles are there in certain areas. This helps me to answer questions like:
- When did electric vehicles become popular?
- Who started this boom first?
- Is this trend still growing and why?

This analysis helps us to see these patterns and answer these questions visually.

## Graph 1: Simple Plot Showing Top 20 Counties with EV

Our main, and first, dataset comes from Data.gov, which provides information on electric vehicles currently registered or in use, including the type of vehicle, the manufacturer, the model, and the year of manufacture within the state of Washington. This dataset is a record of electric vehicles owned or registered by individuals, and each row represents a single vehicle. The information collected helps paint a larger picture of how electric vehicle adoption is changing over time. Some key data found within the dataset that we have chosen to analyze is the types of electric vehicles being chosen, the make, the model, the year, the city, county, and state (though all of the cars in this dataset are in Washington) that the electric vehicles reside in. When we examine these factors, we can observe which communities are seeing the most growth in electric vehicle ownership and which models are most widely adopted. This allows us to better understand patterns in sustainability efforts, transportation choices, and future infrastructure needs.

<vegachart schema-url="{{ site.baseurl }}/assets/json/county.json" style="width: 100%"></vegachart>



## Graph 2: Simple Plot Showing Top 10 EV Car Brands

The first two graphs on this page highlight the places in Washington where electric vehicles are the most common, and which car brands are the most popular. King County stands far above the other counties, with the most electric vehicles registered there, followed by Snohomish and Pierce. This means electric vehicles are mostly found in the larger cities near Seattle. The second graph shows that Tesla is much more popular than other brands, with Chevrolet, Nissan, and Ford following behind. So, even though many companies sell electric vehicles, one brand leads the market right now. The rest of the EV brands are much smaller in numbers in comparison, but do still represent a variety of choices available to drivers. This suggests that while there is a strong domination by Tesla in the EV market, there is still a very large range of Electric Vehicle makers across the state of Washington.

<vegachart schema-url="{{ site.baseurl }}/assets/json/top_makes.json" style="width: 100%"></vegachart>


## Graph 3: Interactive Plot

Looking at the interactive graph, this helps us explore the connection between where a vehicle is registered, what brand of car it is, and the year the vehicle was made. This type of graph is called a heatmap, a heatmap is a visual that uses color shading to show differences in values. In this case, the darker or stronger the color, the higher the number of electric vehicles for that specific combination of county and vehicle make. This lets us see, for example, whether a county has mostly newer models or whether certain brands are more popular in some areas than others. Taken together, this provides a clearer picture of how electric vehicles are spreading within the State of Washington and what types of choices people are making from year to year.

## How to use and read this graph

- Users are able to select multiple regions on the left graph and can see what car brand is popular in certain counties. 
- The right graph will show how many registered vehicles there are in that selected region and show the different year model that it shows.

## Findings

- Based on this graph, we can see that there are a lot more electric vehicles today compared to the early 2010's
- Tesla tends to be the most popular brand in the beginning but more car brands are hopping on the trend of creating their own electric vehicles

<vegachart schema-url="{{ site.baseurl }}/assets/json/electric.json" style="width: 100%"></vegachart>


## Limitations

This dataset mainly has information from the State of Washington and not the entirety of the United States. This is not representative of the whole world nor the United States. 

## Citations

  State of Washington - Electric Vehicle Population Data. (n.d.). Data.Gov. Retrieved December 10, 2025, from https://catalog.data.gov/dataset/electric-vehicle-population-data


<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/Jigs1121/Jigs1121.github.io/refs/heads/main/electric_filtered.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/Jigs1121/Jigs1121.github.io/blob/main/python_notebooks/Part 3.ipynb" text="The Analysis" %}
</div>
