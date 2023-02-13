# Baltimore City crime rate and safety level statistics

### Introduction: 
Crimes are the most significant threat to mankind. It is an act that causes physical or mental harm, as well as property damage or loss. Crimes are of different types – robbery, murder, rape, assault, homicide, and Larceny. to predict the major types of crime happening at that place, there are chances to reduce the number of cases by increasing the police force or avoiding visiting that place during the season or day of the time it is observed more frequently.

### Dataset: 
We have taken the dataset from OpenBaltimore, which consists of the crime data in different parts of baltimore. We have 16 features and5 lakh instances in the data set.
https://data.baltimorecity.gov/datasets/part1- crime-data/explore?location=39.304390%2C-7 6.624118%2C10.97&showTable=true. 

#### Number of rows: 552,105. 

#### Number of columns: 16.

#### Time Frame: 2011 - 2023.

##### Following a thorough examination of the dataset, the columns of the final data frame and their data types are as follows:

| Variable Name (Data Type)          | Description                               |
| :-----------------------------------| :------------------------------------------- | 
| RowID (int)                        | Serial number.                            |
| CrimeDateTime (date, datatime)     | Date and time of the criminal incident.   |
| CrimeCode (str)                    | Unique code of crime by crime dept.       |
| Location (float)                   | Location of the incident.                 |
| Description (str)                  | Description/Type of the incident.         | 
| Inside_Outside (str)               | If the attack was inside or outside.      |
| Weapon (str, float)                | Weapon used for the attack.               |
| Post (int, float)                  | Postal code.                              |
| District (str)                     | District of incident taken place.         |
| Neighborhood (str)                 | Neighborhood of the incident taken place. | 
| Latitude (float)                   | Latitude of location of incident.         |
| Longitude (float)                  | Longitude of location of incident.        |
| GeoLocation (float)                | Geo Location of the incident.             |
| Premise (str, char)                | Premise of the incident.                  |
| VRIName (str, char)                | Video remote interpretation.              |
| Total_Incidents (float, int)       | Total incidents in the location.          |

### 3-way classification: 
We are going to explore a 3-way classification method by creating 3 classes for prediction (High, Medium, and Low). We had the CrimeDateTime feature from which we have generated other features like month of the crime, Day of the week, Hour and these attributes were used to generate the attribute like season, part of the day (Morning or night) and Day of the Crime (weekend or weekday).
Creating a new column label based on description column. 

| Classification  | Types of crimes                 |
| :----------------| :--------------------------------- |
| Low (0)         | Larceny, Burglary, Auto Theft   |
| Medium (1)      | Robbery, Assault                |
| High (2)        | Shooting, Rape, Arson, Homicide |

#### feature variables are:  'Season', 'Crime_Hour','District', 'Neighborhood', 'Crime_WeekDay'. 
We have divided the crime accordingly respected to the season of the year, what hours in a particular day, to the different districts, weekdays/weekend. This helps us analyze the huge dataset within few graphical analytics. 

### Objective: 
Through this project we want to deliver a machine learning model which predicts the level of risk of the crime associated with that district, thus evaluating the safe scale of the area and help people in deciding the safe place to move in for a new life.

### Machine Learning models: 
The objective would be to train a model for prediction. We are going to build the model using K-Nearest Neighbor (KNN) classification and Random Forest algorithm for crime prediction. And will eventually host the application on StreamLit for better user interaction.
We have using the Grid Search to tune the hyper-parameters and increase the accuracy of the model. It is a library function from sklearn's model_selection package. We are going to loop through predefined hyper-parameters and fit our estimator (model) on the training set. This way we can select the best parameters from the listed hyper-parameters.

### 2-way classification: 
In 2-way classification we categorize the crime types into 2 classes : Fatal ( which involves physical Threat ) and Non-Fatal (All other). Hence, 2 classes for prediction.

| Classification     | Types of crimes                                  |
| :---------------------| :------------------------------------------------ |
| Fatal              | Shooting, Rape, Arson, Homicide.                 |
| Non-Fatal          | Larceny, Burglary, Auto Theft, Robbery, Assault  |

### Interpretation: 
In this project, we are going to analyze the crime trends of Baltimore city using the dataset of all crimes reported in the city of Baltimore that we found from openBaltimore. This application would be helpful for people to know if their visit to Baltimore is safe?, and also helpful for the Police Dept, so that high risk areas could be identified to increase forces, and paralelly alert to increase the safety.

