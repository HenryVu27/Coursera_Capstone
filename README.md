# Coursera_Capstone
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

