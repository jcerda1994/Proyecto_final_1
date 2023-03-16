# An analysis between life expectancy & alcohol consumption and sociodemographic variables

## Project overview

It is common belief that alcohol consumption has grown over the last years, even though its adverse consequences on human health. Is this true? Has alcohol consumption increased over time? If so, does it have impact on life expectancy?

This project intends to answers these questions through the analysis of historic databases of life expectancy and alcohol consumption.

Results are classified by country, region and income, due to the fact that these variables affect both life expectancy and alcohol consumption. For example, muslim countries are not supposed to permit alcohol consumption. On the other hand, countries with higher income could have higher rates of alcohol consumption, but have better access to health services, so it might be difficult to infer a relationship between life expectancy and alcohol consumption.

## Database

### Data source

Our data comes from a dataset hosted on Kaggle, a platform for data scientists and machine learning engineers to share, discover, and analyze datasets.

The dataset, titled "Relationship between Alcohol Consumption and Life Expectancy" contains two csv files: "Life-expectancy-verbose" and "Drinks".

We also worked with a dataset called “Life_expectancy_who.csv” tha have information provided by the World Health Organization.

### Datasets

The data analyzed comes from two datasets:

- Life Expectancy verbose by Country (lifeexpectancy-verbose.csv) and Type of drinks consumend by Country (drinks.csv)
- Life Expectancy from the World Health Organization (WHO) (Life_Expectancy_who.csv)

The drinks table provides information on the beer, spirit, and wine servings per capita in various countries as well as their total litres of pure alcohol consumed per person. It is set to one specific time period and doesn't include a country code, so it will be necessary to join the country variable with the other datasets.

The lifeexpectancy-verbose table includes a wider range of variables such as Global Helath Observatory (GHO) Code, GhoDisplay, PublishStateCode, Sex, the World Bank Income and year. It also includes information of life expectancy provided by the World Health Organization. Life expectancy is measured by 3 different variables: Life expectancy at birth (in years) Life expectancy at age 60 (in years) Healthy life expectancy at birth (in years) In this analysis, the variable that is going to be used is Life expectancy (in years).

Additionally, this dataset contains a geographic classification of each country, grouping them in Africa, Americas, Eastern Mediterranean, Europe, SouthEast Asia and Western Pacific.

Finally, the Life Expectancy dataset classifies each country into economic groups, according to World Bank standards.

Note that dataset is well-organized and has no missing values as for country and year information. Economic classification is null in data of year 2013. However, this classification does not change over the course of time, so it is reasonable to fill-in null values with those of previous years.

Life expectancy from the World Health Organization.csv: This file contains data from year 2000-2015 for 193 countries and consists of 22 Columns and 2938 rows with economic, social and health variables like Status of the Country (Developed-Developing), Life expectancy, Adult mortality, Alcohol consumption, diseases like Hepatitis B, Diphtheria and Polio, population and schooling.

**ERD**

![ERD Life_Expectancy_vs_Alcohol_Consumption](https://user-images.githubusercontent.com/113773420/222615004-c5ad6f57-6239-49c8-b998-4d3ac5fb2981.png)

## Process

**Data**: We used the datasets of Life expecxtancy from WHO and life expectancy verbose to observe the alcohol consumption over time, the impact of level of consumption on the life expectancy by country. First we compared the relation between alcohol consumption and life expectancy with the developed countries and then with de developing ones.

**ETL**: We processed the data using Pandas, drop null values, duplicates and merged the life expectancy verbose data with the life expectancy from WHO to see if the alcohol consumption have increased over time, and finally get the data ready for the machine learning model.

**Analysis**: 

Based on the data of developed countries, we can see that alcohol consumption did not consistently increase over time across all countries. Some countries saw an increase in alcohol consumption from 2000 to 2015, such as Austria, Croatia, Lithuania, and Portugal. Other countries, such as Australia and Japan, saw a decrease in alcohol consumption. Some countries had missing data for 2015, such as Cyprus, Latvia, Luxembourg, Malta, Netherlands, Poland, Romania, Singapore, Slovenia, Spain, Switzerland, and the United States.

We also found that there seems to be a negative correlation between alcohol consumption and life expectancy by country. Countries with higher alcohol consumption tend to have lower life expectancy, while countries with lower alcohol consumption tend to have higher life expectancy. However, correlation does not necessarily imply causation, and other factors could also be influencing life expectancy in these countries.

In regards to developing countries there does appear to be a slight increase in alcohol consumption worldwide from 2000 to 2015. However, it's important to note that this trend may not be significant or consistent across all countries, and that there may be other factors affecting alcohol consumption levels in different regions.

It's also worth noting that while some countries have experienced an increase in alcohol consumption over time, others have actually seen a decrease. Therefore, it's important to look at the data for each individual country in order to fully understand trends in alcohol consumption.

**Machine Learning**: The next step was to develop a machine learning model that we describe below.

**Visualization**: We started using Tableau to create graphics that help us visualize the impact of alcohol consumption on life expectancy and to see if the consumption have increased. Below we can see our visualizations and dashboard.

## Tools

![tools](https://user-images.githubusercontent.com/113747210/224206521-7126b300-9d4b-45b7-8fb9-1d44fa447fee.png)


## Machine Learning Model

We started by merging two datasets in a whole database with the purpose of explaining the correlation between life expectancy vs alcohol consumption and other sociodemographic variables that have in big or small proportion relationship to the variable we are trying to explain.

We cretaed our y variable as a result of a cluster between people with high life expactancy and low life expectancy by their alcohol consumption

<img width="597" alt="Captura de Pantalla 2023-03-16 a la(s) 11 01 27" src="https://user-images.githubusercontent.com/72363865/225696300-48cfea0b-1bfb-4724-b3a7-3c905cc446c2.png">

We trained the (Decision tree and Neural Network) model with the following X variables:
* 'percentage_expenditure', 
* '_BMI_', 
* 'Total_expenditure', 
* 'GDP',
* 'Population', 
* 'Income_composition_of_resources',
* 'RegionDisplay',
* 'WorldBankIncomeGroupDisplay,
* 'Status_Developed',

Afterwards we trained and scaled the data in order to create the following ML models:

### Decision Tree:

Confusion matrix:
<img width="232" alt="Captura de Pantalla 2023-03-16 a la(s) 11 10 15" src="https://user-images.githubusercontent.com/72363865/225698433-ac086d1d-63ed-4666-a2f8-3cd1bf6e1be3.png">

we got an 0.9375 accuracy score, so we conclude our model is signifcative.


### Neural Networks:

In this AI model we put as an input 2 hidden layers with 8 and 5 neurons respectively and a sigmoid activation function.

<img width="612" alt="Captura de Pantalla 2023-03-16 a la(s) 11 12 39" src="https://user-images.githubusercontent.com/72363865/225699004-e67ea08e-d90d-4b30-a5b2-15c19e10f76b.png">

Then we compile the model with the following criteria:
* loss="binary_crossentropy"
* optimizer="adam"
* metrics=["accuracy"]

Then we fitted the model with 100 epochs and finally we got our model loss and model accuracy as follows:

<img width="408" alt="Captura de Pantalla 2023-03-16 a la(s) 11 12 52" src="https://user-images.githubusercontent.com/72363865/225699048-6525428a-4fdc-4037-95a5-5d3da7197fbd.png">

We conclude our NN model is not that accurate given that we exclude from the original table strongly correlated variables with the "y" variable such as (Life_expectancy, Alcohol and Adult_Mortality).

### Multiple Linear Regression:

Finally we cretaed a subtable with the variables that we strongly beleive has positive correlation with the variable life expectancy, the table looks like follows:

<img width="544" alt="Captura de Pantalla 2023-03-16 a la(s) 11 14 55" src="https://user-images.githubusercontent.com/72363865/225699559-68539341-7216-43a8-8d54-33059854ebd1.png">

Our y variable is : "Life_expectancy_" (49-69 years) and (70-88 years)
Our X variables are:
* "WorldBankIncomeGroupDisplay" : Socioeconomic status (Low, Medium, High Income)
* "Alcohol" : Alcohol consumption in liters (lt)
* "Status" : Country economic status (Developed or Developing)
* "SexDisplay" : Gender (Male or Female)

We scaled, trained and fitted the variables in order to get the predictions of the "y" variable (life expectancy) and we compared the results in the following table:

<img width="211" alt="Captura de Pantalla 2023-03-16 a la(s) 12 08 43" src="https://user-images.githubusercontent.com/72363865/225712879-96bcb5fb-9d0d-4ed5-b0c0-5f7f0c0785c4.png">

Finally we evaluated the model with the following linear model summary:

<img width="605" alt="Captura de Pantalla 2023-03-16 a la(s) 12 10 18" src="https://user-images.githubusercontent.com/72363865/225713238-2f0b418f-2890-4aef-b000-a3085fcbfb3c.png">

We concluded that our model was succesfull and accurate given the R-squared is close to 1 (0.958) and our indpendent variables have a p-value close to 0, so we reject the null hypothesis that the independent variables explain with certain the independent variable.

## Visualization

We used Tableau to visualize the data from each country as a map where we can filter by year. We have a dashboard that shows the geographic regions, the level of income by color and life expectancy at birth. And then we have a map that shows the life expectancy in years and we can filter it by years and it is shown in different colors. Then a map with alcohol consumption by country with different tones of color according to the level of alcohol consumption, and finally we creted a map that shows with different color the development status of each country.

We utilized Tableau to create visual representations of data from various countries. First, we generated a map that enables filtering by year, depicting geographic regions, income levels by color, and life expectancy at birth. 

Secondly, we developed a separate map that displays life expectancy data in years, allowing us to filter the information by year and view it in distinct color categories. Another map illustrates alcohol consumption by country, using a range of color tones to reflect varying levels of consumption. Lastly, we produced a map that categorizes countries by their development status, distinguished by a range of colors.

## Resources

**Datasets**

1. https://www.kaggle.com/datasets/thedevastator/relationship-between-alcohol-consumption-and-lif
2. https://www.kaggle.com/datasets/kumarajarshi/life-expectancy-who

## Team Members

Team is comprised by:

![roles2](https://user-images.githubusercontent.com/113747210/222621258-02bf4916-c92f-485e-ba7a-28ad3ae6b9af.png)


