---
name: IS445 Final Project &#9992;&#65039;
tools: [Python, HTML, Altair]
image: assets/pngs/airport.png
description: This is a data visualization project using dataset from San Francisco airport.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# <center> San Francisco Airport Air Traffic Visualization</center>
<br/>
#### <center> Kelly Dai &#128051;</center>
<br/>
![avatar](https://www.wlns.com/wp-content/uploads/sites/50/2022/07/SFOGettyImages-1161812951.jpg)

San Francisco International Airport is one of the largest and busiest airport in the world. This visualization aims to explore the air traffic condition there. This project uses two datasets from the City of San Francisco, including landings statistics and passenger statistics. These datasets include data from 2005 to 2022. I only care about the latest information, so I only use data after 2020 for this project. 

## <center>Interactive Visualization</center>
<br/>
<center><vegachart schema-url="{{ site.baseurl }}/assets/json/FinalProject_interactive_plot.json" style="width: 100%"></vegachart></center>
<br/>

This visualization is made based on the landings statistics. It is an interactive visualization that has two parts, a heat map and a pie chart. The left part is a heat map. The x-axis is 'total landed weight' and the y-axis is 'geographic region'. Each rectangle represents that there are routes that carry these amount of cargo in the given region. The color of the rectangle shows the amount of records in the given area. Darker color means more records. The right part is the pie chart. The size of each section depends on the number of the aircraft body type and I colored the chart based on different types. The size of each section shows the number of each types. If you select a specific rectangle on the heat map, the corresponding pie chart will appear on the right part. 

## <center>First Contextual Visualization</center>
<br/>
<center><vegachart schema-url="{{ site.baseurl }}/assets/json/FinalProject_first_plot.json" style="width: 100%"></vegachart></center>
<br/>
The contextual visualizations are made based on the passanger statistics. From the first graph, we can find out that there are more records about flights in the US and these flights have more landed weight, so I assume that US flights also have more passengers. Therefore, I made this histogram to show the total passenger in different region since 2020.  

## <center>Second Contextual Visualization</center>
<br/>
<center><vegachart schema-url="{{ site.baseurl }}/assets/json/FinalProject_second_plot.json" style="width: 100%"></vegachart></center>
<br/>
The previous graph reflects that there are much more passengers fly within the US. For this visualization, I want to make a more detailed graph than can reflect the change of the number of passengers. Therefore, I made a line graph that shows the number of passengers every month in different regions. The color of the line represnts different regions. 

<!-- these are written in a combo of html and liquid --> 
<div class="left">
{% include elements/button.html link="https://github.com/KellyKailid/KellyKailid.github.io/tree/master/python_notebooks/IS445_Final_Project" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/KellyKailid/KellyKailid.github.io/blob/master/python_notebooks/IS445_Final_Project/IS445_FinalProject_Part3.ipynb" text="The Analysis" %}
</div>

