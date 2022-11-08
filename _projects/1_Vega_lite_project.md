---
name: IS445 Homework10
tools: [Python, HTML, vega-lite]
image: assets/pngs/IS445_HW10_plot2.png
description: This is a homework for IS445 that uses vega-lite for interactive viz.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Vega-lite Interactive Visualizations
For this homework, I chose a different dataset instead of using the same dataset from Homework 9. So these two plots are different from plots in Homework 9.

## First Plot

<vegachart schema-url="{{ site.baseurl }}/assets/json/HW10_first_plot.json" style="width: 100%"></vegachart>

#### Introduction
For the first plot, I wanted to make a graph that reflects the relationship between humidity, temperature, and precipitation type. I selected four columns from the whole dataset, including 'state', 'temperature_mid', 'humidity', and 'precip_type'. I noticed that there are many missing values in my selected small dataframe. I dropped all rows with missing values to make my plot more precise. 

#### Design Choice
Since I had two numerical variables, 'temperature_mid' and 'humidity', and one categorical variable, 'precip_type', I decided to make a scatter plot. I decided to use numerical variables for x-axis and y-axis and use 'precip_type' for color, so that all data can spread out through the whole plot instead of focusing on two lines and I can easily find if there is any difference between different 'precip_type'. I used a similar design logic as I did for Homework 9.

When I made the plot, I chose circle as my mark because circle is the most common mark for scatter plot and I believe circle is the most beautiful mark for scatter plot. Moreover, I used the default colormap for color becuase the default colormap is good enough for this plot. Also, I changed the size of the plot to 600*400 becuase I thought this size make the plot clear to see. In the end, I add an interactive function to my plot. When you move your mouse to a dot, you can see the information about the dot.


## Second Plot

<vegachart schema-url="{{ site.baseurl }}/assets/json/HW10_second_plot.json" style="width: 100%"></vegachart>

#### Introduction
For the second plot, I wanted to investigate the relationship between visibility, cloud cover situation, season, and wind speed. I selected five columns from the whole dataset, including 'visibility', 'cloud_cover', 'season', 'summary', and 'wind_speed'. I noticed that there are also many missing values in my selected small dataframe, so I dropped all rows with missing values.

#### Design Choice
I used the same design logic for this graph as I did for the first plot and Homework 9. I chosed two numerical variables, 'cloud_cover' and 'visibility', as my x-axis and y-axis, and chosed the categorical variable 'season' for color. The difference is that I added the size for dots in my plot.

I also chose circle as my mark and default colormap with the same reason. I changed the size of the plot to 800*400 becuase this size is better for this graph. I also added an interactive function to my plot so that audiences can see the detailed information of a specific dot.

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/main/data/bfro_reports_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jnaiman/online_cv_public/blob/main/python_notebooks/test_generate_plots.ipynb" text="The Analysis" %}
</div>

