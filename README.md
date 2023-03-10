# An analysis between life expectancy and alcohol consumption by country

## Project overview

It is common belief that alcohol consumption has grown over the last years, even though its adverse consequences on human health. Is this true? Has alcohol consumption increased over time? If so, does it have impact on life expectancy?

This project intends to answers these questions through the analysis of historic databases of life expectancy and alcohol consumption.

Results are classified by country, region and income, due to the fact that these variables affect both life expectancy and alcohol consumption. For example, muslim countries are not supposed to permit alcohol consumption. On the other hand, countries with higher income could have higher rates of alcohol consumption, but have better access to health services, so it might be difficult to infer a relationship between life expectancy and alcohol consumption.

## Database

### Datasets

The data analyzed comes from two datasets:

- Life Expectancy by Country (Life_Expectancy.csv)
- Alcohol Consumption by Country (Alcohol_Consumption.csv)

**Life Expectancy**

The Life Expectancy by Country dataset includes information of life expectancy provided by the World Health Organization. Life expectancy is measured by 3 different variables:

Life expectancy at birth (in years)
Life expectancy at age 60 (in years)
Healthy life expectancy at birth (in years)
In this analysis, the variable that is going to be used is Life expectancy (in years).

Additionally, this dataset contains a geographic classification of each country, grouping them in Africa, Americas, Eastern Mediterranean, Europe, SouthEast Asia and Western Pacific.

Finally, the Life Expectancy dataset classifies each country into economic groups, according to World Bank standards.

Note that dataset is well-organized and has no missing values as for country and year information. Economic classification is null in data of year 2013. However, this classification does not change over the course of time, so it is reasonable to fill-in null values with those of previous years.

**Alcohol Consumption**

Alcohol Consumption dataset includes fewer variables than the Life Expectancy dataset.

The variable in common is the country name, even though it is necessary to verify that Country names match in both datasets.

Year variable is not as clean as in the previous dataset and requires to clear rows with erroneous year data (such as year "-10000"). Furthermore, many values are missing, so it requires a full cleaning process, in order to keep homogeneous information.


## Status of the project

We are exploring the datsets and trying to answer out questions, now we have a machine learning model.

## Process

**Data**: We used the datasets of alcohol consumption and life expectancy to see the impact and to observe the alcohol consumption over time

**ETL**: We processed the data using Pandas, drop null values, duplicates and merged the life expectancy data with the alcohol consumption by country to see if the alcohol consumption have increased over time, and finally get. the data ready for the machine learning model.

**Analysis**: 

Based on the data of developed countries, we can see that alcohol consumption did not consistently increase over time across all countries. Some countries saw an increase in alcohol consumption from 2000 to 2015, such as Austria, Croatia, Lithuania, and Portugal. Other countries, such as Australia and Japan, saw a decrease in alcohol consumption. Some countries had missing data for 2015, such as Cyprus, Latvia, Luxembourg, Malta, Netherlands, Poland, Romania, Singapore, Slovenia, Spain, Switzerland, and the United States.

We also found that there seems to be a negative correlation between alcohol consumption and life expectancy by country. Countries with higher alcohol consumption tend to have lower life expectancy, while countries with lower alcohol consumption tend to have higher life expectancy. However, correlation does not necessarily imply causation, and other factors could also be influencing life expectancy in these countries.

**Machine Learning**: 

**Visualization**: We started using Tableau to create graphics that help us visualize the impact of alcohol consumption on life expectancy and to see if the consumption have increased.


## Tools

![tools](https://user-images.githubusercontent.com/113747210/224205109-0f7d0dc7-151e-471a-9fe7-d7e43dabf043.png)


## Machine Learning Model

Describe model and results

## Visualization

Tools we used for visualization and show the results

## Resources

**Datasets**

1. https://www.kaggle.com/datasets/thedevastator/relationship-between-alcohol-consumption-and-lif
2. https://www.kaggle.com/datasets/pralabhpoudel/alcohol-consumption-by-country
3. https://www.kaggle.com/datasets/kumarajarshi/life-expectancy-who

## Team Members

Team is comprised by:

<img width="309" alt="roles3" src="https://user-images.githubusercontent.com/113747210/222622965-8f39a91e-a48a-4fe7-b4e0-2ccfd3519b5f.png">


