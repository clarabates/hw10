---
layout: default
title: "Battery Low: An Analysis of Washington State’s Electric Vehicle (EV) Charger Distribution"
---

## Introduction
<div id="intro"></div>

For this project, we will be using two main datasets. The first dataset is an Electric Vehicle Population Dataset, which contains information about all EVs registered in Washington State. Sourced from [data.gov](https://catalog.data.gov/dataset/electric-vehicle-population-data), this dataset provides detailed location data for analyzing population density. Our second dataset, an EV Charging Station dataset, is from the [U.S. Department of Energy’s Alternative Fuels Data Center](https://afdc.energy.gov/fuels/electricity-locations#/analyze?country=US&region=US-WA&show_map=true). This data set stores the locations of all publicly available charging stations in Washington. 

For our central research question, we want to explore how well-distributed EV chargers are across Washington State compared to the distribution of registered EVs. Are there areas of the state that need more charging stations? Where are EV owners more likely to find a station? To answer these questions, we will compare the population of EVs to the population of EV charging stations by county. 


## Methods and Results
<div id="methods"></div>

We began by loading the CSV files into pandas dataframes, selecting the columns that were relevant to our research questions. Since we planned on analyzing the data by county, we were initially concerned that the EV population dataset didn’t have a county column. We were able to solve this issue by merging the EV population dataframe with the EV charging station dataframe on the ZIP code column. Our next step was to count the number of EV charging stations in each county, adding a station count column to the counties dataframe. This exact process was repeated for counting the number of EVs in each county. Once we had station and EV counts, we calculated the ratio of EVs to charging stations for each county. This gave us a more meaningful metric with which to compare charging station availability across the state. 

To analyze the data, we created two different visualizations. The first was a Mapbox scatterplot of EV charging stations by county. The size of the dot represents the number of EV charging stations, and the color of the dot represents the number of EVs per charging station.


## Conclusion
<div id="conclusion"></div>
