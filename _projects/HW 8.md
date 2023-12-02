---
name: Homework 8
tools: [Python, HTML, vega-lite, Altair]
image: assets/pngs/building_inventory_viz.png
description: This project showcases interactive visualizations of the Illinois Building Inventory using vega-lite and Altair.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# Illinois Building Inventory Visualizations

![Bar Chart Visualization]({{ site.baseurl }}/assets/hw8/visualization.png)
*Bar Chart Visualization of Building Inventory*



For a more interactive experience, I have also included a scatter plot that allows users to explore the data in more depth:

<vegachart schema-url="{{ site.baseurl }}/assets/json/scatter_plot.json" style="width: 100%"></vegachart>

## Explore The Data & Analysis

You can access the dataset and the analysis notebook through the following buttons:

<!-- Button for the dataset -->
<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv" text="The Data" %}
</div>

<!-- Button for the Jupyter notebook -->
<div class="right">
{% include elements/button.html link="https://github.com/Qu4drupleU/Qu4drupleU.github.io/blob/main/python_notebooks/Homework8.ipynb" text="The Analysis" %}
</div>

<!-- these buttons are created using a combination of HTML and Liquid templating language -->


Descriptive Analysis for Visualization 1: Bar Chart of Average Square Footage by Agency
Description: The first visualization is a bar chart representing the average square footage of buildings managed by different agencies in the state's building inventory. Each bar corresponds to an agency and reflects the average size of buildings they are responsible for, providing a clear comparison across agencies.

Design Choices: For this bar chart, I chose a simple and straightforward design to emphasize the differences in average square footage. The bars are encoded with a quantitative x-axis for the average square footage and a nominal y-axis for the agency names. I opted for a sequential color scheme to represent the magnitude of square footage, with darker shades indicating larger averages. This visual cue helps to quickly identify agencies with larger or smaller building sizes.

Data Transformations: The dataset was first cleaned to remove entries with missing or zero values in 'Year Acquired' and 'Square Footage' fields. Then, I aggregated the data to calculate the average square footage per agency. This transformation was necessary to condense the data into a meaningful metric for comparison.

Descriptive Analysis for Visualization 2: Interactive Scatter Plot of Year Acquired vs. Square Footage
Description: The second visualization is an interactive scatter plot that displays the relationship between the year buildings were acquired and their square footage. Each point on the plot represents a building, with its position determined by the year it was acquired (x-axis) and its size (y-axis).

Design Choices: The scatter plot uses a quantitative scale for both axes to accurately reflect the numerical nature of the data. The color encoding is based on the agency name, which allows for the identification of patterns or clusters related to specific agencies. The choice of a circular mark size was made to ensure that individual buildings could be easily distinguished, even when data points are numerous or closely packed.

Data Transformations: Similar to the bar chart, the dataset underwent cleaning to exclude irrelevant entries. Additionally, the 'Year Acquired' field was converted from a float to an integer to simplify the axis and improve readability.

Interactivity Discussion: For the scatter plot, I implemented an interactive selection feature using Altair's selection_interval() function. This allows users to click and drag across the plot to select a range of data points, which then highlights the buildings acquired within that timeframe. The interactivity enhances the visualization by enabling users to focus on specific periods and compare the square footage of buildings acquired during those times. It also adds an exploratory element, inviting users to engage with the data more deeply by discovering trends and outliers within selectable time segments.

This interactivity not only makes the visualization more engaging but also allows for a dynamic exploration of the data, which can lead to more insights than a static plot.