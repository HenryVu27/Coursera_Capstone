# IBM Data Science Certificate
Capstone Project for IBM Data Science Certificate
# 1. Introduction
#### Background:
Toronto, capital of Ontario, is the largest city in Canada. It is also the country's central tourism, business and technology hub. Toronto is home to a diverse range of tourist attractions, from its mix of restaurants featuring cuisines across the globe, museums, bars, or parks to the world-famous CN Tower. There is never a shortage of things for visitors to do, therefore, it is essential to plan ahead which area in the city to visit. This project attempts to segments the city of Toronto into clusters based on the most popular venues so that first-time visitors to the city have an easier time deciding where to visit based on their interests
#### Problem: Where in Toronto should first-time tourists visit?
Using data science, geospatial analysis and machine learning techniques, this project aims to provide a solution for this problem and recommending the best neighbourhood to visit given a visitor's interests.
# 2. Data Set
The project requires data from three data sources:
  - [Wikipedia](https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M) to retrieve postal code and neighborhood information for each borough in Toronto.
  - A [csv](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DS0701EN-SkillsNetwork/labs_v1/Geospatial_Coordinates.csv) file to retrieve geographical location (latitude, longitude) for each borough.
  - The use of Foursquare API to fetch information for all venues in the vicinity of a given neighborhood. With the Foursquare API we can explore the most common venue types in a given area to later create a feature matrix for each neighborhood in Toronto.
# 3. Data Clean Up
  - For the Wiki data set, drop all postal codes that are not associated with a borough (value = 'Not Assigned').
  - Merge the Wiki data set and the data set obtained using the csv file to produce a dataframe with complete latitude and longitude information for each postal code.
  - Use the df.explode() method to break the dataframe into rows where each row stores information of a neighborhood (previously each row storers information of a list of neighborhood).
  - Once the data are ready, we use the Foursquare API to get the venues near each neighborhood
# 4. Methodology
In first step we have collected the required geospatial data using Wikipedia and the provided csv file for each neighborhood in Toronto. We have also created a map visualization to see how the neighborhoods are spread out across Toronto.

In the second step in our analysis, we use Foursquare API to obtain the list of venue and the category of all venues for each neighborhood in Toronto. We then identify the 10 most common venues for each neighborhood and create a one-hot encoded dataframe so venue categories can be used for k-means clustering

In third and final step we will use the k-means clustering algorithm to segment neighborhoods into clusters based on the most common venues of each neighborhood. The most common venue types in a cluster will be used to characterize that cluster. A map of clusters will also be generated for better visualization of where to visit
# 5. Results
The following observations are made after segmenting the neighborhood in Toronto into 4 clusters
#### Neighborhoods in cluster 1 are the best place to visit for tourists in need of airport service.
#### Cluster 2 and 3 has a high density of bars, coffee shops and restaurants. Tourists who want recreational activities should visit neighorboods in those clusters
#### Tourists who want an escape from urban life could visit neighborhoods in cluster 3 and 4 for their high density of parks and camping areas
# 6. Conclusion
The purpose of this project was to identify which area in Toronto tourists should visit given their interests. By using the venue information obtained from Foursquare data we have identified all venues and their category for each neighborhood in Toronto, and then generated a one-hot encoded dataframe to represent the frequency of each venue type. Clustering of those locations was then performed in order to create major zones of interest (based on the most common venue types).

Final decission on optimal tourist location will be made by visitors based on their specific interests and the location of their residence.
