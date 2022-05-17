# COVID-19-impact-on-Housing-Market

When the Covid –19 pandemic hit the USA, it took a toll not only on people’s life, but also on the economy. The International Monetary Fund estimated the median global GDP dropped by 3.9% from 2019 to 2020, making it the next bad economic downturn after the great depression. Tens of millions of people lost their job. Employment began to rebound within a few months, but unemployment remained high throughout 2020.  The great depression between 2007 – 2009 observed plummeting of the U.S housing bubble. The reason for this study is to see if there was any impact of COVID- 19 cases on the housing market. Did the housing prices go up or down during COVID? Does/ did the number of covid cases affect the prices? Also predicting housing prices helps people to plan to buy a house so they can know the price range in the future and plan their finances well. Housing price prediction also allows the investors to learn about the trend of the prices in a certain location.

## Data Source

The data is collected from the following sources:

COVID Data - https://www.kaggle.com/antgoldbloom/covid19-data-from-john-hopkins-university?select=RAW_us_confirmed_cases.csv

Housing Data - list and sale prices from https://www.zillow.com/research/data/

Since COVID data is aggregated by Counties and the Housing data is aggregated by Metro area, city and county mapping data is required. This is collected from https://simplemaps.com/data/us-cities .

I have also included interest rates data from https://fred.stlouisfed.org/series/MORTGAGE30US  to see its impact on housing prices along with covid data.

## Data wrangling

I have only taken states including Texas (TX), Washington (WA), California (CA), Colorado (CO) and Virginia (VA). The housing dataset needed to include the following features: Metro/ county region name, State name, Date (monthly – last date of the month) and house price in $. 
The covid dataset contained every day data cumulated. Hence, the month end date was only considered, since we have monthly housing data. Again, the states were filtered to include only the major 5 states of the housing market.
The city-county mapping dataset and mortgage dataset was taken again for only the five states. 
The raw data files are saved in the raw data folder in data folder of my GitHub repository and the processed data in processed data folder. 

## EDA

The housing prices between 2000 to 2021 for most of the states, shows a dip around late 2008 to early 2012. 
This is because of the Great Recession that began in December 2007 and ended in June 2009. 
After the Great Recession, Housing market was affected across the USA. 
Also, there is an increase in the prices after late 2020 during COVID-19 pandemic. 
This maybe because commuting reduced and people wanted to buy houses on the outskirts, instead of paying for house rents in the metro areas.
There was no correlation between number of covid cases and housing price. There was a small -ve correlation between interest rates and housing price. We considered this correlation in multiple linear regression model.

## Models

Linear regression model and time series modelling was done to train and predict housing prices with dates and interest rates as features. 
Linear regresiion model did perform well for training data but performed badly while predicting the housing price data. On the other hand, time series model performed well with predicting housing price data for Dallas, Texas.

## Future work
The time series model seems to work okay for Dallas, Texas. But to train this model for every county/ region and generalize this time series model across all county-state data would not give better performance for every county-state data.

We could try different non-linear model and see if its performance is better than the time series model. One such model to consider is Random Forest.

In addition, we have only considered interest rates and date as feature in linear regression model. There may be multiple factors affecting housing price rates. In future, we could study and consider additional features for housing price prediction. Employment numbers, other government benefits during covid like stimulus check, location of houses etc. can be some features.
