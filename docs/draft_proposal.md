# Baltimore City crime rate and safety level statistics

### Introduction: 
Crimes are the most significant threat to mankind. It is an act that causes physical or mental harm, as well as property damage or loss. Crimes are of different types – robbery, murder, rape, assault, homicide, and Larceny. to predict the major types of crime happening at that place, there are chances to reduce the number of cases by increasing the police force or avoiding visiting that place during the season or day of the time it is observed more frequently.

### Dataset: 
https://data.baltimorecity.gov/datasets/part1- crime-data/explore?location=39.304390%2C-7 6.624118%2C10.97&showTable=true. 

Following a thorough examination of the dataset, the columns of the final data frame and their data types are as follows:
RowID - int
CrimeDateTime – date, datatime 
CrimeCode - str
Location - float
Description - str
Inside_Outside - str
Weapon – str, float
Post – int, float
District - str
Neighborhood - str
Latitude - float
Longitude - float
GeoLocation - float
Premise – str, char
VRIName – str, char
Total_Incidents – float, int

### 3-way classification: 
We are going to explore a 3-way classification method by creating 3 classes for prediction (High, Medium, and Low). We still have the Physical threat category to be high and broke down the non fatal category into 2 (Low and Medium). 
feature variables:  'Season', 'Crime_Hour','District', 'Neighborhood', 'Crime_WeekDay'. 

### Objective: 
Through this project we want to deliver a machine learning model which predicts the level of risk of the crime associated with that district, thus evaluating the safe scale of the area and help people in deciding the safe place to move in for a new life.

### ML models: 
We built the model using K-Nearest Neighbor (KNN) classification and Random Forest algorithm for crime prediction.

### Classification: 
In this project, we are going analyze the crime trends of Baltimore city using the dataset of all crimes reported in the city of Baltimore that we found from openBaltimore.


