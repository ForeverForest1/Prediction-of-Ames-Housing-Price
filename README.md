#__Project 2: Ames Housing Data__

__##Problem statement__
Real estate firms often have to provide advice on the possible features in a residential property that would help fetch higher sale prices for their clients. This study is conducted in the role of an analyst working at an online property listing platform that connects home sellers with potential buyers. The website provides data-driven recommendations on price trends based on details of the listings to help users optimise their bid/sell prices. The company management would like to adopt a more data-driven approach to provide more customised recommendations to their users.

The aim of this study is to:

1) Create a regression model to predict home sale prices based on the listing details

2) Recommend the top 5 features that can fetch higher sale prices for residential properties

__##Approach of this study__

1. Data cleaning

The key steps were:
* dropped columns with high proportion of missing values
* dropped columns comprised mostly of a single value
* imputing suitable values from missing values based on inference from available data
* removed outlier sale prices

2. Feature engineering
* Addition of new features 
* Grouping and creating new categories
* Dummifying variables

3. Data exploration to identify trends and correlations in relation to real-world developments

3. Shortlist variables for modelling based on a correlation threshold of > 50%.

4. Scoring and selecting a suitable model for sales price against our selected feature

5. Optimising the alpha parameter (RidgeCV)

6. Selecting the top 5 features ranked by highest absolute coefficient. 


__##Conclusions/Recommendations__

__Key trends observed in datasets:__

* Participation rates tend to correlate negatively with total score for both ACT and SAT in both years. Higher participation usually leads to greater spread in candidate abilities, which likely causes a decrease in mean total score.

* ACT and SAT participation rates tend to be negatively correlated. This is likely because most students tend to take either one of the test before high school graduation.

__Recommendations__
* Based on the cross-validation results, Ridge Regression showed slightly better scores compared to Linear Regression and Lasso CV. We further fit the Ridge model with our training and test data, and obtained an R2 score of 0.8396 and RMSE of 24217.4649, which are both within acceptable range. To further tune our model, we tried to optimise the alpha parameter, but got slightly worse scores for R2 and RMSE. 

* From the regression coefficient, our top 5 features which affect house sale prices are: 
1. house_quality - better quality houses fetch higher prices
2. above_ground_area - larger properties can expect higher prices
3. garage_size_num_cars - garages that can hold more cars can fetch better prices
4. is_good_kitchen_quality - presence of good quality kitchens can fetch better prices
5. garage_finish_quality - good quality garages fetch higher prices

With more time and resources, further investigation can be done on houses with high sale prices, impact of macroeconomic conditions on sale prices, as well as composite scores to model location factors.