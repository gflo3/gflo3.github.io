---
name: Homework #10 Submission: Exploring Weather Data
tools: [Python, HTML, vega-lite]
image: /assets/pngs/weather.png
description: Grant's submission for Homework #10
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# Homework 10 Submission: Exploring Weather Data

![Weather Exploration](/assets/pngs/weather.png) 
Source: www.noaa.gov

## First Visualization 

<vegachart schema-url="{{ gflo3.github.io }}/assets/json/myWeatherPlot.json" style="width: 100%"></vegachart>

For my first graph, I used my homework #9 assignment as a starting point, I copied my code from Starboard and asked ChatGPT (https://chat.openai.com/chat) how I would be able to accomplish the same datavisualization goal with Python instead of Javascript.
This got me some functioning code, but I then modififed it to better address the objectives of this assignment. This visulization is showing UV index (X axis) and humidity (Y axis). The encoding type here for both axes is quantitative. When the user clicks and drags, the bars turn blue. I made the graph size 700 by 700.
For reference, my initial code for assignment #9 (first graph):
"var myWeatherPlot = {
data: {"url": "https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/main/data/bfro_reports_fall2022.csv%22%7D, selection: { "brush": { "type": "interval" } }, mark: {"type": "bar", "tooltip": [ {"field": "humidity", "type": "quantitative"}, {"field": "uv_index", "type": "quantitative"}, {"field": "temperature_high", "type": "quantitative"}, {"field": "precip_probability", "type": "quantitative"} ]}, width:"600", height:"800", encoding: { "x": {"field": "uv_index", "type": "quantitative"}, "y": {"field": "humidity", "type": "quantitative"}, "color": {"condition": {"selection":"brush"}, "value":"red" } }
}

var v = vegaEmbed('#weatherWithVega', myWeatherPlot)"

This code was modified by asking Chat GPT: "I wrote code to display visualizations in javascript using a csv dataset and I need to do something similar but with python instead. I can also use altair and vega lite. Please adjust code:"

For interactivity, I simply asked GPT how I could add interactivity and it added the section of code that adds to the tooltip when a user is hovering over the visualization.

"myWeatherPlot = myWeatherPlot.encode(
tooltip=[ alt.Tooltip('temperature_high:Q', title='Temperature High'), alt.Tooltip('precip_probability:Q', title='Precipitation Probability') ]

)"

This works well in giving a bit more information to the data storytelling of the chart.

## Second Visualization 
<vegachart schema-url="{{ gflo3.github.io }}/assets/json/myWeatherPlot2.json" style="width: 100%"></vegachart>

For this section, I simply added the code from my first visualization and then modified what data I wanted to show on the X and Y axes. Here, I am showing the humidity and wind speed data from the spreadsheet. I thought this was interesting as sometimes there is more humidity when we have experienced a high wind event in Illinois. However, the data is someone mixed and doesn't definitively show that all high wind speeds are correlated to high humidity. I would be interested in further exploration with another dataset that would show events categorized by type of weather event (i.e. blizzard, tornado, etc).

For the colors, I simply changed them to blue and green (when clicked on). The only transformation I used was to adjust the height size to 1000 to better display the scale of the Y-axis.

These are my edited code snippets I used to link to the original spreadsheet data & my jupyter notebook hosted on GitHub:

```

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/main/data/bfro_reports_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/gflo3/gflo3.github.io/blob/main/python_notebooks/florence-grant-assignment10.ipynb" text="The Analysis" %}
```

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/main/data/bfro_reports_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/gflo3/gflo3.github.io/blob/main/python_notebooks/florence-grant-assignment10.ipynb" text="The Analysis" %}
</div>
