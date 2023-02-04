# 1_Subway_change

# Background

The objective of this project is to create a timeline that overviews the development of Beijing subway system in the 21st century. The inspiration for this project is my personal experience. Growing up in Beijing, the subway took me to many places in the city. So one of the things is miss from home is that well lit subway with modern features.

## Data

Even though the subway company is keeping track of the total line length, and they occasionally share the information with the news media, the coverage is not comprehensive and there is no way to verify if the number is reliable.

Fortunately, <a href url=”https://www.bjsubway.com/station/zjgls/#”>the Beijing subway website </a> shares the distance between each stations.

The opening time of each station is more difficult to find, as the only database I can find is from a <a href url=”https://zhrail.fandom.com/wiki/%E5%8C%97%E4%BA%AC%E5%9C%B0%E9%93%81”>fandom website, </a> hence its accuracy cannot be determined. As a result, I decided to manually gather the data through searching for the historical newsclips online. All the information are stored in timeline.csv.

# Analysis

## Step 1 Calculate the increased line length by year

I used the tool <a href url=”https://networkx.org/”>NetworkX</a>, which is a network analysis algorithm. I defined a formula which can find the path when I key in the line name, start station, and end station. With the help of the station distance information as well as the timeline database I have gathered, I created a new database about the line length increased by year. Line length of a route includes both to and from length, so it should be equals to the distance between between the to and from station times two.

## Step 2 Create visualizations

To help understand the database I have got, I created two visualizations using Datawrapper. One shows the increasing trend of total line length, and the other shows which year the line length was increased the most.

## Step 3 Create a Gif of the change in network map

<a href url=”https://map.bjsubway.com/”>The Beijing Subway Station website</a> offers a svg version of the current railroad map. However, they do not offer a convenient access to the older versions of the subway map. So I imported the current map into Adobe Illustrator, and using my timeline dataframe as a reference, and created the subway map for 2015(when I entered high school), and 2006(when I entered primary school). If I have more time, I would create a gif that includes the map of every year from 2000 to 2023.

# Conclusions

The development of Beijing subway system roughly took off after the Olympic games in 2008, and reached its peak in 2010. Then, the expansion shows a periodical pattern due to the cycle of planning and building of the new lines.

# What can I do better?

If possible, I hope to incorporate more databases into this analysis. For example, I can compare the annual ridership data with this data, and figure out if the increase in line length directly increases the annual ridership. Also, I can use the building cost report to figure out which line is the most costly. Certainly, it is likely that I will have to file a request to the corresponding agency for these information, which will take time.
