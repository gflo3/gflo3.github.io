---
name: Final Project in Exploring Illinois Salaries
tools: [Python, HTML, Altair]
image: /assets/pngs/Main Visualization.png
description: Exploring how the State of Illinois pays state employees across various agencies
custom_js:
  - pandas
  - altair
  - vega_datasets
---
# Final Project in Exploring Illinois Salaries
by Grant Florence

![Main Visualization](/assets/pngs/Main Visualization.png) 

As Illinois ranked ninth among the states highest state tax burdens (combining property, sales, and income tax), according to NPR, I thought it would be a worthwhile project to explore the State of Illinois’ dataset listing state employee pay. I think it widely accepted that state governments help provide necessary services to citizens of the state. However, I think it’s valuable to examine what trends emerge in the data, that can lead to valuable conversations around what areas of our government are not receiving enough funding, and where are areas that perhaps could be cut back.

# Central Interactive Visualization

<vegachart schema-url="{{ gflo3.github.io }}/assets/json/newcharts.json" style="width: 100%"></vegachart>

For this project, I created a dashboard with a bar graph and a scatterplot. The bar graph visualizes the year to date (YTD) gross amount paid to each agency to the State of Illinois government employees. The Y-axis shows the amount of money paid and the X-axis shows the different agencies within the state government. By default there are different colors used for each bar. When one bar is clicked, the others turn grey. This click leads to the interaction with the right side, second graph. 

This scatterplot represents the YTD gross amount paid to people with different position titles (categorized by agencies).—— Additionally, for creating this dashboard, I referenced the code using vega lite for assignment #9. This was very helpful for creating a format for the dashboard. However, I did use Altair within a Jupyter notebook to code the dashboard. I also referenced ChatGPT (chat.openai.com) to generate some styling additions to the dashboard. This scatterplot shows the position titles from each agency on the Y-axis and it shows the sum of the YTD gross pay on the X-axis. At first, the Y-axis is cluttered, however, once a bar on the bar graph is clicked, the positions within that agency is revealed. This way, there is enough space for the positions within the agency to all be displayed. 

If I had more time to update the entire dashboard, I think I would rework it with a potentially different dataset, or update the types of graphs I worked with. I do think that it was nice that the scatterplot showed the position titles upon clicking the agency bar. Although, I wish the graphs were roughly the same size so that they displayed within one webpage without horizontal scrolling.

<div class="left">
{% include elements/button.html link="https://data.illinois.gov/dataset/724state_employee_pay/resource/f823a40d-77f9-4b12-9d1c-5cd0c31905e9" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/gflo3/gflo3.github.io/blob/main/python_notebooks/florence-grant-final-part1.ipynb" text="The Analysis" %}
</div>

# Contextual Visualization #1

![50cents](/assets/pngs/50cents.png) 

This visualization gives some insight into the state's spending from property taxes. The key takeaway as noted is that less than half of property tax income for the state was going to services. This means most was going to pensions, bonds, and interest, among other categories.

# Contextual Visualization #2

![revenue-illinois](/assets/pngs/revenue-illinois.png) 

This visualization shows key sources of state revenue for Illinois in fiscal year 2016. This shows some main sources of income coming from property and local sales.

# Sources

An Examination of Counties in Illinois | The Civic Federation. https://www.civicfed.org/civic-federation/blog/examination-counties-illinois. Accessed 28 Apr. 2023.

Archie, Ayana. “These Are the States with the Highest and Lowest Tax Burdens, a Report Says.” NPR, 30 Mar. 2023. NPR, https://www.npr.org/2023/03/30/1166970506/tax-burden-by-state-income-property-sales.

chat.openai.com

“Pensions Pushed Illinois Property Taxes from Average to among Highest in the U.S.” Illinois Policy, 30 July 2018, https://www.illinoispolicy.org/reports/pensions-make-illinois-property-taxes-among-nations-most-painful/.
