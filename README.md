# An analysis between life expectancy and alcohol consumption by country

## Overview

It is common belief that alcohol consumption has grown over the last years, even though its adverse consequences on human health. Is this true? Has alcohol consumption increased over time? If so, does it have impact on life expectancy?

This project intends to answers these questions through the analysis of historic databases of life expectancy and alcohol consumption.

Results are classified by country, region and income, due to the fact that these variables affect both life expectancy and alcohol consumption. For example, muslim countries are not supposed to permit alcohol consumption. On the other hand, countries with higher income could have higher rates of alcohol consumption, but have better access to health services, so it might be difficult to infer a relationship between life expectancy and alcohol consumption...


## DataBase

### Datasets

The data analyzed comes from two datasets:
1. Life Expectancy by Country (Life_Expectancy.csv)
2. Alcohol Consumption by Country (Alcohol_Consumption.csv)

#### Life Expectancy

The Life Expectancy by Country dataset includes information of life expectancy provided by the World Health Organization. Life expectancy is measured by 3 different variables:
1. Life expectancy at birth (in years)
2. Life expectancy at age 60 (in years)
3. Helathy life expectancy at birth (in years)

In this analysis, the variable that is going to be used is Life expectancy (in years).

Additionally, this dataset contains a geographic classification of each country, grouping them in Africa, Americas, Eastern Mediterranean, Europe, SouthEast Asia and Western Pacific.

Finally, the Life Expectancy dataset classifies each country into economic groups, according to World Bank standards. 

Note that dataset is well-organized and has no missing values as for country and year information. Economic classification is null in data of year 2013. However, this classification does not change over the course of time, so it is reasonable to fill-in null values with those of previous years.

#### Alcohol Consumption

Alcohol Consumption dataset includes fewer variables than the Life Expectancy dataset.

The variable in common is the country name, even though it is necessary to verify that Country names match in both datasets.

Year variable is not as clean as in the previous dataset and requires to clear rows with erroneous year data (such as year "-10000"). Furthermore, many values are missing, so it requires a full cleaning process, in order to keep homogeneous information.

### ERD

The Entity Relational Diagram

## Tech


## 


## Team & Roles

### Team

Team is comprised by:
1. Laura Escamilla
2. Juan Cerda
3. Michele Beltrán

### Roles

Roles to be assigned are:
1. Project Manager
2. Quality Assurance

## References

### Datasets

1. https://www.kaggle.com/datasets/thedevastator/relationship-between-alcohol-consumption-and-lif
2. https://www.kaggle.com/datasets/pralabhpoudel/alcohol-consumption-by-country

### Project Management

1. https://sherrierose.medium.com/software-project-team-roles-and-responsibilities-152a7d575759