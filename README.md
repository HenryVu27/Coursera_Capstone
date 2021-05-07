# Coursera_Capstone
Capstone Project for IBM Data Science Certificate
# 1. Introduction
#### Business Problem: 
# 2. Data Set
The project requires data from three data sources:
  - [Wikipedia](https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M) to retrieve postal code and neighborhood information for each borough in Toronto.
  - A [csv](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DS0701EN-SkillsNetwork/labs_v1/Geospatial_Coordinates.csv) file to retrieve geographical location (latitude, longitude) for each borough.
  - The use of Foursquare API to fetch information for all venues in the vicinity of a given neighborhood
# 3. Data Clean Up
  - For the Wiki data set, drop all postal codes that are not associated with a borough (value = 'Not Assigned').
  - Merge the Wiki data set and the data set obtained using the csv file to produce a dataframe with complete latitude and longitude information for each postal code.
  - Use the df.explode() method to break the dataframe into rows where each row stores information of a neighborhood (previously each row storers information of a list of neighborhood).
  - Once the data are ready, we use the Foursquare API to get the venues near each neighborhood

