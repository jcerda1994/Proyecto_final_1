# An analysis between life expectancy and alcohol consumption by country

## Project overview

It is common belief that alcohol consumption has grown over the last years, even though its adverse consequences on human health. Is this true? Has alcohol consumption increased over time? If so, does it have impact on life expectancy?

This project intends to answers these questions through the analysis of historic databases of life expectancy and alcohol consumption.

Results are classified by country, region and income, due to the fact that these variables affect both life expectancy and alcohol consumption. For example, muslim countries are not supposed to permit alcohol consumption. On the other hand, countries with higher income could have higher rates of alcohol consumption, but have better access to health services, so it might be difficult to infer a relationship between life expectancy and alcohol consumption.

## Database

### Datasets

- Life Expectancy verbose by Country (lifeexpectancy-verbose.csv) and Type of drinks consumend by Country (drinks.csv)
- Life Expectancy from the World Health Organization (WHO) (Life_Expectancy_who.csv)

The drinks table provides information on the beer, spirit, and wine servings per capita in various countries as well as their total litres of pure alcohol consumed per person. It is set to one specific time period and doesn't include a country code, so it will be necessary to join the country variable with the other datasets.

The lifeexpectancy-verbose table includes a wider range of variables such as Global Helath Observatory (GHO) Code, GhoDisplay, PublishStateCode, Sex, the World Bank Income and year. It also includes information of life expectancy provided by the World Health Organization. Life expectancy is measured by 3 different variables: Life expectancy at birth (in years) Life expectancy at age 60 (in years) Healthy life expectancy at birth (in years) In this analysis, the variable that is going to be used is Life expectancy (in years).

Additionally, this dataset contains a geographic classification of each country, grouping them in Africa, Americas, Eastern Mediterranean, Europe, SouthEast Asia and Western Pacific.

Finally, the Life Expectancy dataset classifies each country into economic groups, according to World Bank standards.

Note that dataset is well-organized and has no missing values as for country and year information. Economic classification is null in data of year 2013. However, this classification does not change over the course of time, so it is reasonable to fill-in null values with those of previous years.

Life expectancy from the World Health Organization

This file contains data from year 2000-2015 for 193 countries and consists of 22 Columns and 2938 rows with economic, social and health variables like Status of the Country (Developed-Developing), Life expectancy, Adult mortality, Alcohol consumption, diseases like Hepatitis B, Diphtheria and Polio, population and schooling. 

## Process

**Data**: We used the datasets of Life expecxtancy from WHO and life expectancy verbose to observe the alcohol consumption over time, the impact of level of consumption on the life expectancy by country. First we compared the relation between alcohol consumption and life expectancy with the developed countries and then with de developing ones.

**ETL**: We processed the data using Pandas, drop null values, duplicates and merged the life expectancy verbose data with the life expectancy from WHO to see if the alcohol consumption have increased over time, and finally get the data ready for the machine learning model.

**Analysis**: 

Based on the data of developed countries, we can see that alcohol consumption did not consistently increase over time across all countries. Some countries saw an increase in alcohol consumption from 2000 to 2015, such as Austria, Croatia, Lithuania, and Portugal. Other countries, such as Australia and Japan, saw a decrease in alcohol consumption. Some countries had missing data for 2015, such as Cyprus, Latvia, Luxembourg, Malta, Netherlands, Poland, Romania, Singapore, Slovenia, Spain, Switzerland, and the United States.

We also found that there seems to be a negative correlation between alcohol consumption and life expectancy by country. Countries with higher alcohol consumption tend to have lower life expectancy, while countries with lower alcohol consumption tend to have higher life expectancy. However, correlation does not necessarily imply causation, and other factors could also be influencing life expectancy in these countries.

In regards to developing countries there does appear to be a slight increase in alcohol consumption worldwide from 2000 to 2015. However, it's important to note that this trend may not be significant or consistent across all countries, and that there may be other factors affecting alcohol consumption levels in different regions.

It's also worth noting that while some countries have experienced an increase in alcohol consumption over time, others have actually seen a decrease. Therefore, it's important to look at the data for each individual country in order to fully understand trends in alcohol consumption.

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


