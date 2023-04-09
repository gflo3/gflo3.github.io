---
name: Homework #10 Submission: Exploring Weather Data
tools: [Python, HTML, vega-lite]
image: assets/pngs/weather.png
description: Grant's submission for Homework #10
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# Homework 10 Submission: Exploring Weather Data

Example comes from this [great blog post right here](https://blog.4dcu.be/programming/2021/05/03/Interactive-Visualizations.html) that was also used in [our test import script](https://github.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/blob/main/week01/test_imports_week01.ipynb).

We can use a vegachart HTML tag like so:

```
<vegachart schema-url="{{https://gflo3.github.io/}}assets/json/myWeatherPlot.json" style="width: 100%"></vegachart>
```

<vegachart schema-url="{{https://gflo3.github.io/}}assets/json/myWeatherPlot.json" style="width: 100%"></vegachart>

In theory, you can also use [Jekyll hooks](https://jekyllrb.com/docs/plugins/hooks/) to do it, but I haven't figured out a way that looks nice yet.


## First Visualization 

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
