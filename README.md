# [Analysis of more than 38 000 used cars and prediction of their price - Regression task - Project Overview:](https://t-ded.github.io/t-ded-portfolio/projects/used-cars-market/)

## Project Summary

- Very **complex exploration and visualization** of the data, followed up by prediction of the target variable with **R squared & adjusted R squared of 0.926 & 0.92**
- Implementation of Histogram Gradient Boosting algorithm as well as Linear Regression, including **checks and violation-solutions of 4 key assumptions of linear regression**
- This analysis might bring a **very strong use case**, especially to an average person who would like to sell their car, but also to a company or a car market
- In the future, the project may be extended by adding a **user interface** where the user could input their car and get an estimation of the price based on similar offers
- **Additional data might be scraped off the internet**, including features such as horsepower, trunk capacity or max speed

## Project Background

- This dataset has been chosen for it’s possible strong real life implementations and use cases
- The [initial dataset](https://www.kaggle.com/lepchenkov/usedcarscatalog) contains more than 38 thousand of entries with 30 features, one of them being the dependent price variable
- For the purpose of this analysis, EDA with visualizations as well as estimation modeling have been given a lot of energy, since a predictive algorithm is where we saw the most use case possible

## Project outline
    
- State the initial hypotheses and assumptions, decide for an approach 
- Make necessary imports, take first look at the dataset
- Decide how to clean the dataset and engineer some of the missing values
- Analyse the individual distribution of some of the features
- Research the relations of properties of the car and price
- Dive into social analysis - upvotes, duration listed, number of photos and how these relate to price
- Analysis of features feature_0 - feature_9
- Correlation inspection
- Predictive modeling
  - Linear Regression - check of 4 key assumptions, feature selection
  - Histogram Gradient Boosting

## Hypotheses and notes

- There will be manufacturers with strong correlation with price (luxurious brands such as Porsche).
- Odometer value and year of production will be negatively correlated and might be in (anti)correlation with price.
- State of the car will have strong impact on the car.
- Some engine fuel types may be in general higher priced than others, same goes for drivetrain types.
- Location of the market will not be impactful.
- The presence of all features feature_0 - feature_9 will have positive impact on price.
- Duration listed may be in positive correlation with price (long lasting offers may be overpriced).
    
- Note: The whole project could be approached from a completely different perspective, for instance analysis of car 
        brand/model x location, body types, engine fuels etc.
        
## Hypotheses after examination

- Porsche, Jaguar and Lexus are the most expensive brands with their opposites being Москвич, 3A3 and BA3 (evaluated by mean).
- Year of production and odometer value show negative linear relation and year of production shows strong positive correlation with price.
- New cars are in general much better priced as well as owned cars which still have warranty, however, the data in this column was strongly imbalanced.
- SUVs and pickups are the most expensive ones in terms of average price and so are electric and diesel cars.
- Except for one market, the location does not matter. One of possible explanations is that Минская market usually sells more luxurious cars.
- Feature_0 is the only feature among features 0-9 whose presence has a negative impact on price. This is also the only feature that tends to be more present withing older cars, however, we have not been able to think of a feature, that would give such outcome.
- The relation between price and duration listed seems to be rather inversely proportional. This may, however, be caused by dropping outliers in duration listed column.

## Possible next steps

- Dive more deeply into feature selection and hypertune the parameters of our model(s).
- Scrape additional data about the cars from the internet - horsepower, trunk capacity, max speed, etc.
- Analyse which cars could be considered "veterans" and might therefore be of higher price despite being old.
   - This may have a strong positive impact on our models as these semmed to be the biggest outliers in terms of RMSE.
- Create a user interface where the user would input their car and the features of it and according to similar entries 
  a price would be estimated for it.
   - For this purpose, we would need to know what are the features feature_0 - feature_9.
