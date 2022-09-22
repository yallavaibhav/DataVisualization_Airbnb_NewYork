# DataVisualization_Airbnb_NewYork
1. Abstract:

Tourism has an important role in the economy. Many people travel from one place to another for work purposes or vacation. This might cost them a lot of time and money to find a good home. Airbnb provides a great website, which can help people easily find places for cheap prices. This project provides the visualization of the trends concerning the hosts. It provides how to make more profit, and what kind of rooms are most profitable. Further, what areas in New York prove more profit compared to other areas. The analysis also provides all the Airbnb data across the world during the pandemic period, and how the trend fluctuated in this period.
2. Introduction

Humans are communal creatures, and tourism plays an essential role in their lives. On average 4.4% of GDP and 6.9% of employment directly come from the tourism and travel industry. Traveling from one place to another might be for business work or a vacation the foremost thing after your travel is to check in to a hotel. For this people have to find a good neighborhood, where they can stay. They need to find a room/ Hotel which needs to be neat, clean, and has a reasonable price for the stay. This is a challenging part because finding a good hotel is challenging, and even if there is one it is difficult to have rooms available. To resolve this issue, two people named Brain Chesky, and Nathan Blecharczyk had created a website where people can find a home online at reasonable prices.
This idea had grown into a simple business model and now had more than 12.1 million listings all over the world. There are many offices present across the United States, and Europe. The country with the most Airbnb listings in the United States of America had an average of 2,249,434 listings in 2021. The country with the second-highest number of average Airbnb listings in France, with 1,209,036 in 2021. These results are provided using visualization. In this project, the prime focus is on the New York Airbnb analysis, where the report represents all the different visualizations to understand the trend of the market in New York from the host’s perspective.

2.1 Purpose of this document

The project goal is to analyze the market trend of Airbnb in New York using different datasets collected from two sources, which are Kaggle, and Inside Airbnb. The objective of the data is to understand the patterns of the number of hosts, listings, prices, which areas have more demand, and various other things. This analysis is done using a visualization tool named Tableau.

2.2 Scope
The scope of the project is to understand the market analysis trends in New York’s Airbnb. The objectives are to visualize the overview of the company, the products offered such as private rooms, shared rooms, and the entire hotel. In addition, the prices in each area in New York are analyzed. The data is analyzed from 2008 (when the company started) to 2021. The analysis also provides trends of the hosts, their average earnings, and others. Further, the trend analysis on Airbnb across the globe is compared to the pandemic. This analysis provides the how much the covid-19 pandemic had affected the Airbnb industry. These visualizations are done using Tableau.

2.3 References

https://hosttools.com/blog/short-term-rental-tips/vacation-rental-glossary/


3. Background and Objectives

Airbnb is a successful company with a simple business model. It was first introduced in the year 2008 when two friends had started a website that offers their home for rent to any tourist. This small step had built an entire fortune. This company has most of the real estate area but owns no land. Airbnb acts as a broker between the customer and the host and earns a certain percentage of commission. The company has 3.9 billion dollars according to the Forbes list. This company had a few limitations, such as most of the housing market has drastically decreased due to Airbnb. Most of the customers are benefiting, as the rooms have reasonable prices, and a customer can stay for anytime limit.

The objective of the project is to visualize the data from the perspective of the host. The project describes the number of room types, how many are mostly opted for by customers, average prices of the rooms per area. The other objectives are what makes the host more profit, which areas can have expensive rooms, and what price would make more earnings to the hosts.

In addition, this project also states the trend of Airbnb across the countries during the pandemic period. It presents the trend of the number of listings, how New York's trend is fluctuating compared to other countries, similarly the number of the count, and prices change during the pandemic period.

4. Dataset:

The datasets used in this project are AB_NY_2019 from Kaggle, and listing, reviews of the New York dataset from insideairbnb, and listing, reviews of Airbnb across the world from insideairbnb.
AB_NY_2019:
This dataset contains 48,896 instances present with 16 different attributes. The features such as room types, host id, prices, and other are present in the dataset. This dataset has only the data related to New York city, and has data up to 2019. The data is shown below.

Listing, and Reviews of New York Data:

The listings of New York data contain 37,632 number of instances, with 17 attributes. These attributes only contain the data of New York. This data is similar to AB_NY_2019 data. It has features such as room types, neighborhood, neighborhood group and others. This dataset has updated data, that is the data till 2020. It contains more information compared to AB_NY_2019. This data us joined with reviews dataset that contains New York information. It contains 928,096 number of instances. These two datasets are joined using the Listing_id present in the review’s dataset, and id which is present in the listing dataset.

Listing and Reviews of Airbnb across the world:

The listing of the world data contains 279,713 number of instances with 34 different features. This has more information compared to any other dataset, as it contains information regarding all the countries. This dataset is also joined using the reviews dataset. The reviews dataset contains 84,850 instances, and are joined with the common attribute. This dataset is used to analyses the trend in the pandemic situation and compare the New York trend with other countries.

5. Architecture & High-Level Design

The data is collected from two different sources for unique purposes. The first dataset is the AB_NYC_2019 dataset which contains 48,896 rows and 16 attributes. This dataset contains data till 2019 with features such as location, host id, reviews, and others which will help visualize many features present. The next two datasets are Listing, and reviews which are related to New York. This dataset listing has 37,632 instances and 17 columns. This data is used because it has data from 2011 to 2022. In addition, features such as room type, longitude, and host id are present which helps to visualize the data. Similarly, another dataset named listin.csv, and reviews.csv which belongs to Airbnb data of the entire world is present.

These data were cleaned in python using Google Collab. Using the pandas, the missing values, and other issues were explored. Preprocessing includes cleaning the data, such as removing missing values, duplicate values, inconsistent data, and removing outliers. There is some valuable information so only a few missing data were removed as shown in Figure 1. Further duplicates and inconsistent data are not present. Outliers are found using clamp transformation using the Inter Quartile range.

Figure 1
Missing Values present in the dataset
![image](https://user-images.githubusercontent.com/39133612/191646743-cf763a03-060f-4df8-8af9-12e70ff421b0.png)



Now, this cleaned data is loaded in the tableau workbook. As there are five different datasets each with unique features. The datasets listing, and reviews of New York are joined using left join in Tableau. Similarly, the datasets listings and reviews that contain the entire world Airbnb data were also joined in the tableau workbook. A sample join is shown in Figure 2.
Figure 2
![image](https://user-images.githubusercontent.com/39133612/191646767-7b44d0ea-176b-48dd-8651-76f8b9fb9770.png)


Each dataset has a specific purpose for the analysis and visualization. For instance, AB_NYC_2019 data from the Kaggle dataset has visualizations such as types of rooms that are earning more in New York, Prices depending on the area, and others. Using the dataset of Airbnb of the entire world is used for the analysis of how covid impacted the business. The entire architecture is presented in Figure 3.

Figure 3
![image](https://user-images.githubusercontent.com/39133612/191646819-bcec3b43-0e83-4ab6-bd8e-f0c442ad9705.png)



