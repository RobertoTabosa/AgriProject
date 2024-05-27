# AgriProject
This is a Machine Learning project using Python to identify and display in a GIS the most suitable areas for planting oats in the provinces of Manitoba and Saskatchewan / Canada.

Project: AgTech Capstone - OATS
Final Project | Stream 3 by Roberto Tabosa

Scoping

Problem/Opportunity
With the growing decline in oat planting in Manitoba and Saskatchewan*, 
a group of companies supplying oat grains needs to understand more 
precisely the best locations for crop oats and thus make better future investment decisions when production returns to normal.

Solution
Recommendation of best areas using K-means clustering for 
oat cultivation.

* Source: https://www.seed.ab.ca/record-highs-across-most-crops-leaves-oats-behind/

     Data Collection

● Saskatchewan Yield Data Source
https://dashboard.saskatchewan.ca/agriculture/rm-yields/rm-yields-data#r
m-yields-tab
● Manitoba Yield Data Source
https://www.gov.mb.ca/agriculture/markets-and-statistics/crop-statistics/in
dex.html

● Manitoba and Saskatchewan Shapefiles
Provided by Ruhid

Data Transformation
● Manitoba's database column names have been
standardized

Previous Name Current Name
Risk Area / RM RM
ARGENTINE CANOLA Canola
CANARYSEED Canary Seed
DURUM WHEAT Durum Wheat
LENTILS Lentils
OATS Oats
RED SPRING WHEAT Spring Wheat
WHITE PEA BEANS Peas

● Some Saskatchewan’s database columns are
dropped

Dropped
Winter Wheat
Mustard
Sunflowers
Fall Rye
Spring Rye
Tame Hay
Flax
Chickpeas

● Data frame was pivoted to present crops
separated into columns.
● Was done crop conversion in MB tonnes to bushel

● Was done crop conversion in pounds to bushels
● Created Province column for both dataframes

Exploratory Data Analysis (EDA)

1,352
(16%)
OAT
S

Frequency

Exploratory Data Analysis (EDA)

Exploratory Data Analysis (EDA)

Exploratory Data Analysis (EDA)

Exploratory Data Analysis (EDA)

GDF = 481 RMs DF = 391 RMs (Oats since 2002)

DF_GDF = 349 RMs

Oats Yield 2003 - 2022

Models and Methodology

● We're using the K-Means clustering method to group data.
● We select specific columns related to 'Oats' data.
● These selected columns will serve as our features for clustering.
● We're calculating the "silhouette scores" and "inertia" in Elbow Method for different
cluster numbers.
● The 'silhouette score' measures how well data points are separated into clusters.
● The 'inertia' represents the sum of squared distances within clusters.
● We're testing a range of cluster numbers (2 to 15) to find the optimal number of
clusters.
● This helps us identify the best cluster structure for our data.

Results and Conclusions

Results
- Geospatial map to Oats in Manitoba and Saskatchewan
Able to find 5 distinct clusters of Oats in Manitoba and 6 distinct
clusters in Saskatchewan
- Geospatial maps showing the history of the last 20 years of Oats
planting.

Conclusion
The final result of georeferencing accurately demonstrates the historically largest
producing areas of Oats. These areas distributed in clusters will allow the group of
companies requesting this work to plan on a scale, for example, according to each cluster
the amount of future financial investment when production is returning to normal amounts.

Future Works

- Consider other variables such as crop rotation factors and economic factors linked to the
planting of Oats

The historical geospatial visualization of the last 20 years will allow us to raise
hypotheses to better understand the reduction in Oats planting in 2023. Economic
factors for the cultivation of Oats and the application of crop variation by farmers may
be key factors for this understanding
