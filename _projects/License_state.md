---
name: State License Visualizer
tools: [Python, HTML, vega-lite]
image: assets/pngs/state_license.png
description: The project visualizes license type distributions by state and action occurrences. (2024)

custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# State License Visualizer

The project aims to analyze and visualize the distribution of license types by state and the occurrences of different action types. It leverages interactive and static visualizations to allow users to explore and understand the data more effectively:

##### License Type Distribution by State:

The project visualizes the distribution of different license types across various states, with an interactive feature enabling users to select a state and view its specific distribution. This allows users to compare the prevalence of different license types in each state.

##### Action Type Distribution:

It shows the frequency of different action types in the dataset, helping users understand which actions are most common. Initially intended to be interactive, the plot was made static due to insufficient data for states outside Illinois.

Overall, the project aims to provide insights into how license and action types vary by state and to showcase interactive visualizations, with the ability to compare distributions in a clear and informative way.

## Plot 1

For the first plot, it shows the distribution of license types by states. The interactive feature allows the user to switch between the different states. The x-axis is the License type, while the y-axis has the number of the different licenses. The color was chosen to reflect the different license types to clearly show the distributions of these licenses. Furthermore, the tooltip uses the state, license type and the number of licneses. In terms of properties, I wanted the height and width of the graph to stay constant instead of changing when a new state is selected. They are kept at a constant width of 800 and height of 400. The state select is the dropdown box that allows the user to choose a specific state to look at. The selection within the dropdown box are all the states available in the dataset.

<vegachart schema-url="{{ site.baseurl }}/assets/json/plot1.json" style="width: 100%"></vegachart>

## Plot 2

For the second plot, it shows the distribution of the types of actions and their number of occurences. The x-axis is the Action, while the y-axis has the number of occurances. The tooltip uses only those variables. For properties, they are set to constant once again at a width of 800 and height of 400. Initially, I was going to make the graph interactive as well allowing the user to choose between the states. This would have allowed the user to see the different type of actions and their number of occurances for indivisual states. However, the dataset did not have enough data for most states outside of Illinois. Only Illinois had more than 10 datasets. I included the interactive version below in the Workbook.ipynb and if you look at other states, there is a notable differnce in the number of data. I concluded that it would be better to have a static plot rather than an interactive one in this case to best showcase the distribution.

<vegachart schema-url="{{ site.baseurl }}/assets/json/plot2.json" style="width: 100%"></vegachart>
