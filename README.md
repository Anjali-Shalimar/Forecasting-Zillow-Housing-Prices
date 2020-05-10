---
# **Forecasting Housing Prices of listings in Zillow (within New York City)** 

### **https://rpubs.com/Anjali_Cincinnati/612071**

The project forecasts the median housing prices of listings in Zillow ( within New York City ). The project uses a SARIMA model for this purpose and further compares the performance with auto arima models 

## **1. Introduction**

### 1.1  Zillow's Business Model


Zillow Group, Inc., or simply Zillow, is a leading real estate and rental marketplace founded in 2006 and headquartered in Seattle. Zillow is involved in buying, selling, renting, financing, remodeling of properties and also has a living database of more than 110 million U.S. homes, including

* Homes for sale

* Homes for rent &

* Homes not currently on the market

Zillow also lists the prices of the properties that are not on the market. Zillow estimates or Zestimates as they are popularly known Zillow’s estimate of a home's market value. The Zestimate incorporates public and user-submitted data, taking into account home facts, location and market conditions.



### 1.2 What is the need of the hour?


The Zestimate is marketed as a tool designed to take the mystery out of real estate for consumers who would otherwise have to rely on brokers and guesswork. However, Zestimates often give a single time point value which might not be an accurate way to base the decision of purchase on. 

To make an informed purchase decision, investors or buyers need to be aware of the past trends and how the trends might affect the market henceforth.The purpose of this project is to address this want of the investors by leveraging the information at hand to evaluate the property prices up to the current time point and also understand the anticipated market trends for a reasonable period in the future



### 1.3 How do we go about it?

Currently the database at our disposal has a zip code level data for properties in the US. The price points are updated only till 2017. 

Our objective here is to create a scalable product to forecast the prices of these properties up till 2020 (with a scope of additional forecasts for the future). For the purpose of this project, we are concentrating specifically on the 2-bedroom properties in New York city (NYC). 

The ensuing report will showcase the results of 3 randomly selected zip codes in NYC (10013, 10011, 10003) and a step by step understanding of all the processes from cleaning and manipulation of the data to forecasting the data and performing adequacy checks. An R shiny app is also created to give a better visual and functional experience to the investors browsing the app.

***



## **2. Original Data Source**


The dataset has been sourced from [data.world](https://data.world/zillow-data). 

The dataset has over 8900 zip codes of properties across the US. In this project, we are concentrating only on the 2 bhk properties listed under New York City. This sets the project scope to 25 zip codes.

***

## **3. The app**

An R Shiny app was developed that helps the client to self-serve the delivery of key insights. Please find the link to the app [here](https://ethanhodys.shinyapps.io/flex/)


***

## **8.	Summary of the Analysis**


The analysis forecasts the median housing price for zip codes in New York City. The initial exploratory data analysis rendered insights into the non-stationary and seasonal nature of the time series data. It was also derived that a single seasonal ARIMA (SARIMA) model would not be an adequate fit for all zip codes. Hence the grid search algorithm was used to find the optimal SARIMA hyperparameters for each zip code. The model was then fit and tested for adequacy. The rendered model performed at par or above in comparison to the auto arima models. Additionally, the model was used to forecast the median housing price by zip code for April (2020). Finally, an R Shiny app was developed that helps clients self-serve the delivery of key insights. The app has the capability to accommodate different hyperparameter values to generate price forecasts. 

**References**

[Lectures](https://xiaoruizhu.github.io/Forecasting-and-Time-Series-Methods/)

***
