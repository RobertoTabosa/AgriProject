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

<img width="524" alt="Canola" src="https://github.com/RobertoTabosa/AgriProject/assets/84072431/2669b50a-61ec-444c-a089-8ff6beb64432">

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

<img width="233" alt="Manitoba - Data Transformation" src="https://github.com/RobertoTabosa/AgriProject/assets/84072431/602c254f-d546-4c4e-9ed9-7b9a228c888e">

● Data frame was pivoted to present crops
separated into columns.
● Was done crop conversion in MB tonnes to bushel

● Some Saskatchewan’s database columns are
dropped

<img width="115" alt="Saskatchewan - Data transformation" src="https://github.com/RobertoTabosa/AgriProject/assets/84072431/a92c9ce0-cc95-49e2-b1c1-32b95045e502">

● Was done crop conversion in pounds to bushels
● Created Province column for both dataframes

Exploratory Data Analysis (EDA)

<img width="587" alt="Exploratory Data Analysis (EDA)" src="https://github.com/RobertoTabosa/AgriProject/assets/84072431/efbee7b9-4643-4a65-b3dc-25b8f41f9f87">


Exploratory Data Analysis (EDA)

<img width="586" alt="EDA2" src="https://github.com/RobertoTabosa/AgriProject/assets/84072431/3d008591-e7fa-4ab3-a5da-7a60735c59fc">


Exploratory Data Analysis (EDA)

<img width="586" alt="EDA2" src="https://github.com/RobertoTabosa/AgriProject/assets/84072431/3d008591-e7fa-4ab3-a5da-7a60735c59fc">


Exploratory Data Analysis (EDA)

<img width="607" alt="EDA4" src="https://github.com/RobertoTabosa/AgriProject/assets/84072431/376d6574-0e06-40d8-82fb-98afe7aa17a3">


Exploratory Data Analysis (EDA)

<img width="823" alt="EDA5" src="https://github.com/RobertoTabosa/AgriProject/assets/84072431/ea4afabd-89bf-4952-973b-1b51daf9973c">


Exploratory Data Analysis (EDA)

<img width="815" alt="EDA6" src="https://github.com/RobertoTabosa/AgriProject/assets/84072431/951eeb30-87dd-4fc6-8e8f-a01033154df5">


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

<img width="805" alt="Elbow Method" src="https://github.com/RobertoTabosa/AgriProject/assets/84072431/1bc2c1cc-7c54-4ca7-bfcb-b9ff42a6f543">


<img width="819" alt="Silhouette Score Method" src="https://github.com/RobertoTabosa/AgriProject/assets/84072431/ec731e63-c038-4f4a-96c3-126603d6cc83">


<img width="626" alt="Oats clustering" src="https://github.com/RobertoTabosa/AgriProject/assets/84072431/91189d58-c15d-489e-8cdc-84d799ab6317">


<img width="745" alt="GIS-FinalResult" src="https://github.com/RobertoTabosa/AgriProject/assets/84072431/5fa4c491-ecb7-4beb-9c5b-460d966edd8b">


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
