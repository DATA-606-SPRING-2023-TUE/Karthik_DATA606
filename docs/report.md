# Baltimore City crime rate and safety level statistics.
### Data 606 final project report. 
#### By Singireddy Karthik Reddy. 

### Presentation video: https://youtu.be/hBOvkVGrep0
### Presentation slides: https://docs.google.com/presentation/d/10AHbVPUm4aBDM_d5_PrFO-RA101R41rj/edit?usp=sharing&ouid=105317721196373363836&rtpof=true&sd=true

### Introduction: 
Crimes are the most significant threat to mankind. It is an act that causes physical or mental harm, as well as property damage or loss. Crimes are of different types – robbery, murder, rape, assault, homicide, and Larceny. To predict the major types of crime happening at that place, there are chances to reduce the number of cases by increasing the police force or avoiding visiting that place during the season or day of the time it is observed more frequently.

### Dataset: 
We have taken the dataset from OpenBaltimore, which consists of crime data in different parts of Baltimore. We have 16 features and about 5 lakh instances in the data set.
https://data.baltimorecity.gov/datasets/part1-crime-data/explore?location=39.304390%2C-76.624118%2C10.97&showTable=true. 

### Preprocessing: 
Preprocessing includes removing any null values which may affect the accuracy of the model. The main steps include formatting, cleaning, and sampling. The cleaning process is used for the removal or fixing of some missing data. Incomplete data in crucial attributes like description has been removed. Formatting includes replacing incomplete data. Some of the values formatted are I, O which were changed to Inside, Outside. We had around 13 different target variables. Grouping of these target variables was done based on the severity of the attack. Physical threats were considered high risk factored attacks whereas other crimes were considered as low and medium risk factored crimes.

#### Number of rows: 552,105. 

#### Number of columns: 16.

#### Time Frame: 2011 - 2023.

##### Following a thorough examination of the dataset, the columns of the final data frame and their data types are as follows:

| Variable Name (Data Type)          | Description                               |
| :-----------------------------------| :------------------------------------------- | 
| RowID (int)                        | Serial number.                            |
| CrimeDateTime (date, data time)     | Date and time of the criminal incident.   |
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
We are going to explore a 3-way classification method by creating 3 classes for prediction (High, Medium, and Low). We had the CrimeDateTime feature from which we generated other features like the month of the crime, Day of the week, and Hour and these attributes were used to generate the attribute like the season, part of the day (Morning or night), and Day of the Crime (weekend or weekday).
Creating a new column label based on the description column. 

| Classification  | Types of crimes                 |
| :----------------| :--------------------------------- |
| Low (0)         | Larceny, Burglary, Auto Theft   |
| Medium (1)      | Robbery, Assault                |
| High (2)        | Shooting, Rape, Arson, Homicide |

#### feature variables are:  'Season', 'Crime_Hour',' District', 'Neighborhood', 'Crime_WeekDay'. 
We have divided the crime accordingly respected to the season of the year, what hours on a particular day, the different districts, and weekdays/weekends. This helps us analyze the huge dataset within a few graphical analytics. 

### Objective: 
Through this project we want to deliver a machine learning model which predicts the level of risk of the crime associated with that district, thus evaluating the safe scale of the area and helping people in deciding the safe place to move in for a new life.

### KNN-Classification:
With the 3 classes to predict, we created a model using the KNN classifier. This approach determines the likelihood that a data point will belong to one of the classes based on the data points closest to it. The KNN algorithm creates an imaginary boundary to classify the data. When new data points come in, the algorithm will try to predict that to the nearest of boundary line.

### Machine Learning models: 
The objective would be to train a prediction model. We are going to build the model using K-Nearest Neighbor (KNN) classification and Random Forest algorithm for crime prediction. And will eventually host the application on StreamLit for better user interaction.
We have used Grid Search to tune the hyper-parameters and increase the accuracy of the model. It is a library function from sklearn's model_selection package. We are going to loop through predefined hyperparameters and fit our estimator (model) on the training set. This way we can select the best parameters from the listed hyper-parameters.

### 2-way classification: 
In 2-way classification, we categorize the crime types into 2 classes: Fatal ( which involves physical Threat ) and Non-Fatal (All other). Hence, 2 classes for prediction.

| Classification     | Types of crimes                                  |
| :---------------------| :------------------------------------------------ |
| Fatal              | Shooting, Rape, Arson, Homicide.                 |
| Non-Fatal          | Larceny, Burglary, Auto Theft, Robbery, Assault  |

### Conclusion: 
In this project, we have analyzed the crime trends of Baltimore City using the dataset of all crimes reported in the city of Baltimore that we got from open-Baltimore. Also based on the findings we developed prediction models using a Random Forest Classifier and KNN classifier, for both the cases of 2-way classification (Physical and Non Physical Threat) and 3-way classification( Low, Medium, and High). This application is helpful for people to know if their visit to Baltimore is safe. And also helpful for the Police Dept, so that high-risk areas could be identified to increase protection for the safety of the public.




