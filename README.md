# Multiple Linear Regression-based Bike-Sharing Demand Prediction Modelling  
> Modelling the demand for shared bikes based on Multiple Linear Regression to reveal the significant predictors of demand for shared bikes.


## Table of Contents
* [General Information](#general-information)
* [Conclusions](#conclusions)
* [Technologies Used](#technologies-used)
* [Contact](#contact)



## General Information
- A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system.
- A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. Therefore, to recover and make profits, BoomBikes aspires to understand the demand for shared bikes among the people after this ongoing quarantine situation ends across the nation due to Covid-19. The company wants to know the following:
     • Which variables are significant in predicting the demand for shared bikes.
     • How well those variables describe the bike demands
- Based on various meteorological surveys and people's styles, a large dataset has been gathered on daily bike demands across the American market based on some factors. 



## Conclusions
- The preliminary exploratory data analysis has revealed the following:
(1) While the data distributions across all seasons, the two years, and all days of the week do not exhibit drastic differences, the clear- weather, working-day, and no-holiday conditions are observed to be more prevalent over other conditions.

(2) Furthermore, it is observed that the count of the total rental bikes (including both casual and registered)
  • varies substantially across all seasons, reaching drastically the lowest values in spring and the highest values in fall.
  • is considerably higher in 2019 than in 2018
  • varies considerably across all months throughout the year
  • is lower when there is a holiday
  • does not exhibit any significant differences in its median and upper & lower quantiles irrespective of whether the day is a working day  or not
  • varies substantially across the diverse weather conditions indiacted by 'mist', 'clear', and 'light'
exhibits only mild changes in its median across the days of the week

- The model has been built based on recursive feature elimiination. The final model has been arrived at in the second iteration of model building.

- The final model seems favorable since the
  •R-squared and Adjusted R-squared statistics are approximately 83.9% and 83.5%, indicating good accuracy of the model.
  •Standard errors of the coefficients are low
  •p-values of all the features are less than 0.05, indicating that all the 14 independent variables in this model are significant
  •Prob (F-statistic) is as low (less than 0.05), indicating the overall statistical significance of the model and its good fit to the data
  •Variance inflation factor (VIF) of all the features is at or below the threshold of 5, indicating low multicollinearity of the 14 features in this model

- Furthermore, the assumptions of linear regression are successfully validated. 
  • After conducting residual analysis, the residuals are found to exhibit normal distribution, with the mean centered around zero. This validates the assumption of linear regression that error terms are normally distributed. 
  • In addition, there are no visible patterns in the error terms. So, the error terms are independent of each other.  
  • Moreover, the error terms have constant variance, as shown by the homoscedasticity plot.

- Since the r2_score on the test set (81.3%) is close to the R-squared value on the train set (84%), i.e., the difference is within 5%, therefore we could say that what our model has learnt on the train set is approrpiately generalized on the test set. Thus, our model fit is good, and it suitably predicts the demand for shared bikes.

- The equation of our best fitted line is
cnt = 0.2466 + 0.2343 * yr - 0.0919 * holiday + 0.4377 * temp - 0.1586 * windspeed - 0.0716 * season_spring + 0.0333 * season_summer + 0.0887 * season_winter - 0.0445 * mnth_December - 0.0503 * mnth_January - 0.0504 * mnth_July - 0.0419 * mnth_November + 0.0682 * mnth_September - 0.2929 * weathersit_light - 0.0814 * weathersit_mist

- We can consider developing the model further by using advanced regression techniques.

## Technologies Used
- NumPy - version 1.23.5
- Pandas - version 1.5.3
- Matplotlib - version 3.7.0
- Seaborn - version 0.12.2
- sklearn - version 1.2.1
- statsmodels - version 0.13.5

## Contact
Created by Sangbeda Das (sangbeda.das@gmail.com) - feel free to contact me!