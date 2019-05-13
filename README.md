# Tree Census in New York City
<h2>Description of the Data</h2>
<br>Our dataset is tree census in New York City. It is from a project named TreesCount! which brings volunteers to use both high tech tools and survey wheels, tape measures, and tree identification keys, citizen mappers to create a spatially accurate digital inventory of NYC’s street trees.

<br>The original dataset includes census in 2005, 2010 and 2015. Taking the completeness and the dataset size into consideration, we only adopted the data in 2015. We then deleted all variables which are not helpful for our visualization and kept the species as well as some location-related information of each tree. We also used a dataset providing population data by zip code, which we consolidated to just NYC zip codes, to make our visualizations more complex.

<br>It comes very naturally to visualize some data points on the map of New York City using topojson, nycmap.geojson, nyczip.geojson, as it is tree census in New York City. We also tried to implement some fresh visualization idea. That is why we introduced a treemap layout for our project. To implement the treemap, we filtered the data and constructed a proper object using javascript so that we could use d3.treemap to implement the treemap layout. We were inspired by several treemap tutorials.

<h2>Overview of Visual Design Rationale</h2>
<br>Our visualization is divided into three major parts. The first part is a NYC-map-based visualization. The second part is a pair of graphs including a treemap and a scatter plot. The third part is a stacked bar chart. We designed the visualization this way to follow a storyline as stated below.

<br>As it is tree census data, we planned to show the overall situation of street trees in New York City. Specifically, our visualization is driven to answer these questions: 1) What is the distribution of street trees in New York City in 2015? How many trees are there in each neighborhood/borough in New York City?  Which neighborhoods and boroughs are “greener”? 2) Do human activities affect the lives of street trees? 3) What species are the most popular? Which borough has the best diversity of trees? 

<br>The map-based visualization comes naturally for this dataset to answer the first question. The theme color is still green. The gradient is changed based on the numbers of trees in each ZIP code. 

<br>To answer the second question, we decided to pair one treemap layout with one scatter plot. The treemap on the left shows how many trees are planted in each neighborhood and the most common trees there. Each branch of the treemap is given a rectangle standing for a borough, which is then tiled with smaller rectangles representing neighborhoods. A leaf node's rectangle has an area proportional to the number of trees, and the leaf nodes are colored to show different neighborhoods. We chose green as the theme color because the topic is about trees. The scatter plot on the right shows the (potential) correlation between neighborhood population and number of trees. 

<br>We implemented a stacked bar chart to answer the third question. The x-axis includes all 132 different types of trees. The bar chart clearly shows how different species are distributed in 5 boroughs in New York City.

<h2>Overview of Interactive Elements</h2>
<br>NYC-map-based visualization: Implement a slider to help users figure out how many trees each area has.

<br>Treemap + scatter plot: Hover over the rectangles of the treemap or the points of the scatter plot to see more details about one area, such as the name of a borough, the name of the neighborhood, tree numbers, most common tree type, and neighborhood population.  

<br>Stacked bar chart: Hover over each stack to see exact numbers of trees. 

<h2>Story</h2>
<br>Street trees are important to a city. They shade urban people in the summer, clean the air, beautify the neighborhoods, help reduce noise, and support important urban wildlife. We chose the dataset because we are curious about the street trees in New York City, one of the largest cities in the world. How many trees are there in New York City? What species are most popular? What species are most uncommon? Good diversity of trees in a city is vital, as otherwise disease or an insect can wipe out one particular species of tree. 
<br>The 2015 tree census counted 666,134 street trees citywide. Queens has the most trees, with 242,414, followed by Brooklyn with 173,063 and Staten Island with 103,313 street trees. 
<br>The dataset identifies 132 different species of street trees citywide. London planetree is the most prevalent species in New York City in 2015. Honeylocust and Callery pear are the second and third popular tree species citywide. 
<br>Honeylocust is the most popular species in Bronx, Manhattan. London planetree is the most prevalent species in Brooklyn, Queens. Callery pear is the majority in Staten Island.
<br>Manhattan has a worse diversity in terms of tree species.
