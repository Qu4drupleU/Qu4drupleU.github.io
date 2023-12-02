---
name: Video_Games_Analysis
tools: [Python, Altair, vega-lite, Pycountry, Bqplot, Plotly]
image: image: assets/pngs/pie.jpg
description: This project showcases interactive visualizations of the video game industry.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# **Exploring the Gaming Industry: An Interactive Journey Through Game Genres and Their Creators**

### By Maison Wu

## Introduction
This study presents an in-depth exploration of the **video game industry** through the lens of **data-driven visualizations**, focusing on the myriad of **game genres** and the **developers** behind them. Our approach bridges the gap between intricate data and tangible insights within the realm of digital entertainment.

At the core of our analysis is a detailed examination of video game genres. Utilizing comprehensive sales data and genre popularity metrics, we illuminate the evolving preferences and trends that shape the gaming community. Through our visualizations, we provide a nuanced look at how various game genres resonate with users in terms of ratings and market impact.

To provide a more holistic view of the industry, our analysis integrates contextual data focusing on game developers. This element reveals the intricate relationship between game genres and their creators. By analyzing the roles and influence of these developers, we seek to uncover underlying patterns in game production and genre specialization, offering insights into market dynamics and the broader gaming ecosystem.

We invite readers to engage with our visualizations, offering a window into the nuanced world of gaming, and highlighting key aspects that influence both game development and player preferences.

### Interactive Visualization: User Scores Distribution by Video Game Genre

**What It Shows**: This interactive histogram displays the distribution of user scores for video games, categorized by genre. It provides a visual representation of how many games within each genre fall into different score ranges, offering insights into player preferences and reception across genres.

**How to Interact**: 
1. **Select a Genre**: Use the dropdown menu labeled 'Genre:' to choose a specific video game genre. The options in the dropdown reflect all unique genres available in the dataset.
2. **View the Histogram**: Upon selecting a genre, the histogram will update to show the distribution of user scores for games in that genre. Each bar in the histogram represents a range of user scores, with the height of the bar indicating the number of games that fall within that score range.
3. **Explore Further**: Hover over any bar in the histogram to see the exact count of games for that score range. This tooltip feature provides a more detailed look at the data.

**Understanding the Visualization**: 
- **X-Axis (User Score)**: The horizontal axis shows the range of user scores, from the lowest to the highest.
- **Y-Axis (Number of Games)**: The vertical axis indicates the number of games that fall within each score range.
- **Color Coding**: Each genre is represented with a unique color, making it easy to distinguish between different genres when exploring the histogram.

This visualization serves as a tool to explore how different video game genres are received by users. It can reveal which genres tend to have higher user scores, indicating greater popularity or satisfaction, and which genres have a wider range of scores, suggesting varied reception among players.


<vegachart schema-url="{{ site.baseurl }}/assets/json/viz1.json" style="width: 100%"></vegachart>


### Interactive Visualization: Distribution of Video Game Genres

**What It Shows**: This interactive pie chart offers a visual representation of the distribution of different video game genres in the dataset. Each slice of the pie chart corresponds to a specific genre, with the size of the slice indicating the relative frequency of games in that genre.

**How to Interact**: 
1. **Click on a Pie Slice**: When you click on a slice of the pie chart, it highlights in red. This interaction displays detailed information about the selected genre.
2. **View Genre Details**: Upon clicking a genre, a label will appear showing the genre name and the number of games in that genre. This feature allows you to quickly grasp the prevalence of each genre in the dataset.

**Understanding the Visualization**: 
- **Pie Slices**: Each slice represents a different video game genre. The size of the slice is proportional to the number of games in that genre relative to the total number of games.
- **Color Coding**: The pie chart uses a range of colors to distinguish between genres, making it easy to identify each one visually.
- **Interactive Highlight**: When a slice is clicked, it changes color to highlight your selection and presents specific information about that genre.

This pie chart visualization is designed to give you an intuitive understanding of the genre composition within the dataset. It shows which genres are more prevalent and allows for an easy comparison between the different categories of games.


<vegachart schema-url="{{ site.baseurl }}/assets/json/viz2.json" style="width: 100%"></vegachart>


### Contextual Visualizations
1. **Visualization 1: Global Distribution of Video Game Developers**
**What It Shows**: This interactive Choropleth map provides a visual representation of the global distribution of video game developers. Each country is shaded based on the number of developers associated with it, offering a clear picture of the geographical spread of the industry's creative forces.

**How to Interact**: 
- **Explore by Country**: Hover over any country on the map to see a tooltip with the country's name and the exact count of video game developers located there.
- **Visual Color Scale**: The color intensity on the map varies according to the concentration of developers – darker shades represent higher numbers, while lighter shades indicate fewer developers.

**Understanding the Visualization**: 
- **Color Scale**: The 'Rainbow' colorscale has been used for visual appeal and clarity, with a spectrum of colors representing different quantities.
- **Data Representation**: Countries with a significant number of developers, like the United States, Japan, and those in Western Europe, are expected to stand out with more intense colors.
- **Insights**: This map allows you to quickly identify global hotspots for video game development and understand regional differences in the industry's presence.

**Technical Note**: The map has been carefully adjusted to recognize all countries accurately, including the conversion of 'US' to 'United States' for better geographical identification. The visualization is designed to be both informative and visually engaging, making it easy to grasp the global landscape of video game development.

<vegachart schema-url="{{ site.baseurl }}/assets/json/viz3.json" style="width: 100%"></vegachart>

---
2. **Visualization 2: Top 10 Video Game Developers by Global Sales**
**What It Shows**: This bar chart presents a comparative analysis of the top 10 video game developers based on their global sales figures. The visualization highlights the commercial success of these developers in the global gaming market.

**How to Interact**: 
- **Explore Sales Figures**: Each bar represents a different developer, with the length of the bar corresponding to their total global sales (in millions).
- **Detailed Insights**: Hovering over each bar reveals additional details, including the exact global sales figures and the name of the developer.

**Understanding the Visualization**: 
- **X-Axis (Developers)**: The horizontal axis lists the names of the top 10 developers.
- **Y-Axis (Global Sales)**: The vertical axis shows the global sales figures in millions.
- **Color Coding**: The bars are color-coded based on the sales amount, providing a visual differentiation of sales magnitude among developers.

**Key Insights**: 
- **Market Leaders**: This chart identifies the leading developers in the industry, such as Nintendo, Ubisoft, and Capcom, showcasing their dominance in terms of sales revenue.
- **Sales Distribution**: The visualization offers an insight into the disparity of sales among top developers, indicating the concentration of market success within a few leading names.

**Technical Note**: This visualization is generated by merging two datasets: one detailing video game sales and the other listing video game developers. The resulting dataset allows for an in-depth analysis of sales performance attributed to each developer.

<vegachart schema-url="{{ site.baseurl }}/assets/json/viz4.json" style="width: 100%"></vegachart>

v

## Data Sources and Citations
- **Main Dataset:** [vgsales.csv](https://data.world/mhoangvslev/steam-games-dataset/workspace/file?filename=vgsales.csv)
- **Contextual Dataset** [developer.csv](https://data.world/mhoangvslev/steam-games-dataset/workspace/file?filename=developper.csv) 


---
## Analysis

<!-- Button for the Jupyter notebook -->
<div class="right">
{% include elements/button.html link="https://github.com/Qu4drupleU/Qu4drupleU.github.io/blob/main/python_notebooks/Final_Project.ipynb" text="The Analysis" %}
</div>
