---
layout: post
title: Car collision in NYC
cover: cover.jpg
date:   2023-5-1
categories: posts
---

New York City is the most densely populated major city in the United States and more than twice as populous as Los Angeles, the nation's second-largest city. New York City is located at the southern tip of New York State. The city constitutes the geographical and demographic center of both the Northeast megalopolis and the New York metropolitan area, the largest metropolitan area in the U.S. by both population and urban area. With over 20.1 million people in its metropolitan statistical area and 23.5 million in its combined statistical area as of 2020, New York is one of the world's most populous megacities, and over 58 million people live within 250 mi (400 km) of the city.  <sup>[1]</sup> 

New York City is a global cultural, financial, entertainment, and media center with a significant influence on commerce, health care and life sciences, research, technology, education, politics, tourism, dining, art, fashion, and sports. 

Home to the headquarters of the United Nations, New York is an important center for international diplomacy, and is sometimes described as the capital of the world.

### INTRODUCTION
Many people love New York City, but nobody likes car accidents. Road safety is by any means a critical issue, and is relevant to everybody's daily life.

The data set used is from the city government's OpenData website, where a lot of useful data sets archived by city government are provided. The NYC motor vehicle collision data set, contains up-to-date collision record ever since July 1st, 2012, and each record shows the date, time, location, the number of injured and/or killed people

### MOTIVATION

How is the data look like on a map? Wherer are  more dangerous/risky regions? 
Can we identify dangerous spots/areas?
What is the trend of total number of collisions? What can we predict for future?
What is the composition ratio of different types of victims (pedestrian, cyclist, motorist) and different levels of severities (no hurt, injured, lethal)?
Was the situation different for different boroughs (5 boroughs of NYC)? What about different? ... <sup>[2]</sup>

### Interactive Map Tool

To help easily visualize and explore the spatial details of the collision data, a comprehensive and flexible interactive map tool is developed using Leaflet.
it can show heat map, cluster map and position. And we can see which borough has the most frequent collision

<iframe src="https://raw.githack.com/M3LLI55X/m3lli55x.github.io/master/webpages/mar.html" width="680" height="400"> </iframe>

### Data Analysis

The figures below show the total number of collisions with respect to different type of accident by hour in a day.

For all types of traffic accidents resulting in injuries, the highest number of accidents occurred in the evenfall, while motorist and cyclist fatalities were higher in the middle of the night.
This is instructive for the corresponding prevention and assistance, and worthy of further investigation by relevant departments.

The accident statistics of the borough are too extensive to reflect a good reference value. Therefore, it makes sense to count accidents down to street level. 
The keyword cloud map below counts and shows the 25 streets with the highest number of accidents, which helps the government to spend its budget more purposefully.
More intuitive Map display in the Interactive Map section.

#### Time Factors

The figures below show the total number of collisions with respect to different years (and boroughs), month in a year respectively.
<iframe src="https://raw.githack.com/M3LLI55X/m3lli55x.github.io/master/webpages/month.html" width="680" height="400"> </iframe>
<iframe src="https://raw.githack.com/M3LLI55X/m3lli55x.github.io/master/webpages/year.html" width="680" height="400"> </iframe>
Yearly-wise, there is an gradual collision increase since 2013, while a obvious drop after 2016, but then increase again at 2017.
Month factor show results generally well aligned with common sense.

### Summary and suggestion

Traffic accidents have a negative impact on motor vehicle drivers, cyclists and even pedestrians. Therefore, corresponding prevention is necessary. The following are the corresponding suggestions.
First, traffic flow and safety can be improved by adding or optimizing traffic signals for those transportation hubs and streets with a high incidence of accidents. 
Second, advertising, education and enforcement campaigns can be used to raise awareness among motorlists and cyclists to stay focused and obey traffic rules at night.
Last but not least, we could calling on public transport to reduce the traffic flow during peak times to reduce the risk of accidents.



