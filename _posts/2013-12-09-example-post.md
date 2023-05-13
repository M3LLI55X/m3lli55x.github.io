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

The [Motor-Vehicle-Collisions-Crashes data set](https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Crashes/h9gi-nx95) used is from the city government's OpenData website, where a lot of useful data sets archived by city government are provided. The NYC motor vehicle collision data set, contains up-to-date collision record ever since July 1st, 2012, and each record shows the date, time, location, the number of injured and/or killed people

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

<iframe src="images\person_day.png" width="800" height="400">
</iframe>

For all types of traffic accidents resulting in injuries, the highest number of accidents occurred in the evenfall, while motorist and cyclist fatalities were higher in the middle of the night.
This is instructive for the corresponding prevention and assistance, and worthy of further investigation by relevant departments.

The accident statistics of the borough are too extensive to reflect a good reference value. Therefore, it makes sense to count accidents down to street level. 
The keyword cloud map below counts and shows the 25 streets with the highest number of accidents, which helps the government to spend its budget more purposefully.
More intuitive Map display in the Interactive Map section.

![](images\cloud_plot.png)

#### Time Factors

The figures below show the total number of collisions with respect to different years (and boroughs), month in a year respectively.
<iframe src="https://raw.githack.com/M3LLI55X/m3lli55x.github.io/master/webpages/month.html" width="680" height="400"> </iframe>
From the above picture, we could see Staten Island always has the lowest number of accidents, while Brooklyn always has the highest number of accidents. We also could see there is a very interesting phenomenon that is each curve shows a similar trend. Month factor show results generally well aligned with common sense.

<iframe src="https://raw.githack.com/M3LLI55X/m3lli55x.github.io/master/webpages/year.html" width="680" height="400"> </iframe>
Yearly-wise, there is an gradual collision increase since 2013, while a obvious drop after 2016, but then increase again at 2017. We guess the goverment took some effective measures to decrease the number of collisions at 2020, since far fewer collisions were recorded than in previous years. Also, maybe because people recognize the risk of motor vehicle collisions.


### Machine Learning

We found there are a lot of missing information about BOROUGH from the dataset, thus, we consider that we could use Machine Learning technologies to get these missing values. To be more specific, we could use the lantitude and longitute information to predict the missing value, that is BOROUGH information. From this dataset, we could see there are 5 borough. This mean that is a classification problem, and we consider to use random forest to solve it.

Random forest works by constructing a large number of decision trees, each of which is trained on a random subset of the input features and a random subset of the training data. When making predictions for new features, the algorithm aggregates the predictions of all the trees in the forest to produce a final prediction.


In our dataset, we decided to use random forest to predict the borough information based on the position information for each collision case. The predicted results are shown in the figure below.

<iframe src="images\random_forest.png" width="800" height="400"> </iframe>

<!-- ![](images\random_forest.png) -->

From the above picture, we could see the scatterplot is very similar to the map of New York, which means the classification model that we built has very good predictive performance.

### Summary and suggestion

Most collisions occur during the weekdays: A majority of motor vehicle collisions in NYC occur on weekdays, with Fridays being the day with the highest number of collisions. Certain intersections are more dangerous than others: Some intersections in NYC are more prone to accidents than others. For example, the intersection of Atlantic Avenue and Pennsylvania Avenue in Brooklyn had the highest number of collisions from 2012 to 2019. Pedestrians and cyclists are particularly vulnerable: The dataset shows that pedestrians and cyclists are disproportionately represented in collisions involving injuries or fatalities, highlighting the need for improved safety measures for vulnerable road users.

Traffic accidents have a negative impact on motor vehicle drivers, cyclists and even pedestrians. Therefore, corresponding prevention is necessary. The following are the corresponding suggestions. First, traffic flow and safety can be improved by adding or optimizing traffic signals for those transportation hubs and streets with a high incidence of accidents. Second, advertising, education and enforcement campaigns can be used to raise awareness among motorlists and cyclists to stay focused and obey traffic rules at night. Last but not least, we could calling on public transport to reduce the traffic flow during peak times to reduce the risk of accidents.



