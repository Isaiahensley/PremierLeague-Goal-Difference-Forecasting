# PremierLeagueNet-Goal-Difference-Forecasting

**Abstract:**
This paper explores the use of machine learning models to predict outcomes in the English Premier League (EPL) results over the course of multiple seasons. Using a model trained on goal differentials from a previous season, the model will predict results for the next season. The model is able to determine whether a team is likely to win or lose by using the predicted goal difference data. Our model assumes that all teams in both seasons consist of the same players. This project achieves the best results when using linear regression compared to other models such as RandomForestRegressor, DecisionTreeRegressor, and SVR. This method provides a basis for further improvements and offers insightful information about the difficulties involved in predicting the results of football games.


**Introduction:**
The English Premier League (EPL), known for its unpredictable nature and intense competition, is considered the highest level of football. Because team lineups are always changing, forecasting the results of matches is extremely difficult. By utilizing machine learning techniques and emphasizing goal difference as a crucial metric for prediction, this study seeks to address this challenge. This method shows the possible effectiveness of such approaches by using historical data from one season to train a model and then using that model to predict results in the next season.

**Data Analysis:**
Each English Premier League season comprises twenty teams, each team participates in 19 home games and 19 away games. At the end of each season, the three teams with the worst performance are dropped out, making way for new teams in the next season from the EFL Championship, the second tier of English football. This system of promotion and relegation in each season helps to maintain a competitive balance for the top two tiers of English football. It is also common for teams to have different players in each season. Because we were not provided player data in our datasets, we will assume the players on each team throughout both seasons remain the same for this project.

![GoalsBetweenSeasons](https://github.com/Isaiahensley/PremierLeague-Goal-Differernce-Forecasting/assets/143129356/21fd5857-e400-4ccf-a33c-a33563c3abd1)

These graphs show the similarity in team performance during both seasons used in this project. Even with the possibility for teams to consist of different players in the following season, there is a clear correlation in team performance regardless of this.

**Data Preprocessing:**
The first step in data preprocessing is to load and filter datasets for the 2020–2021 and 2021–2022 EPL seasons. For analysis purposes, columns like home team, away team, full-time home goals (FTHG), and full-time away goals (FTAG) are kept. To maintain dataset consistency, teams that are not in both seasons are removed from the datasets.

![DataPreprocessingDatasets](https://github.com/Isaiahensley/PremierLeague-Goal-Differernce-Forecasting/assets/143129356/8eeb782b-189d-4267-a12d-935f11b73f8f)

![RemovedTeams](https://github.com/Isaiahensley/PremierLeague-Goal-Differernce-Forecasting/assets/143129356/f6d2c428-7d44-44e2-87f1-e94e2c8b608a)


**Feature Engineering:**
Each team is assigned a unique ID to create a standardized representation for teams throughout both seasons. These are listed in each row as HomeID and AwayID to represent which teams are playing each other. A column for GoalDif is added as our predictor which represents the goal difference between the home and away teams. Goal differential is a reliable indicator of team performance and is computed as (HomeGoals - AwayGoals). By choosing to use goal difference over ratios, data analysis problems caused by infinite, or zero ratios are reduced.

![TeamIDs](https://github.com/Isaiahensley/PremierLeague-Goal-Differernce-Forecasting/assets/143129356/1bbc146c-340d-4689-b7f4-b6b55b23ef4a)

![Season1GoalDif](https://github.com/Isaiahensley/PremierLeague-Goal-Differernce-Forecasting/assets/143129356/6899cbb5-dc02-4142-98de-9c16dc13dd8c)

![Season2GoalDif](https://github.com/Isaiahensley/PremierLeague-Goal-Differernce-Forecasting/assets/143129356/bfc867b1-6e32-4c9a-b1af-86720a59a2df)


**Model Selection:**
Several regression models were taken into consideration, such as Decision Tree Regressor, Random Forest Regressor, Support Vector Regressor (SVR), and Linear Regression. Based on accuracy metrics, Linear Regression stands out as the preferred model, outperforming other models with a mean squared error of 3.79. As mentioned before, we are training our model on the first season and testing on the following season.

![TrainingAndTestingSets](https://github.com/Isaiahensley/PremierLeague-Goal-Differernce-Forecasting/assets/143129356/bdedd9c3-5d08-431d-a83f-de8005bd5686)

![LinearRegression](https://github.com/Isaiahensley/PremierLeague-Goal-Differernce-Forecasting/assets/143129356/03a25d83-a3eb-4ffa-98f2-571f51598a0a)


**Results:**
Applying the linear regression model on the 2021–2022 season shows encouraging accuracy, with a mean squared error of 3.79. SVR (3.84), Random Forest Regressor (4.54), and Decision Tree Regressor (6.42) are examples of comparative models that are not as accurate. 
The results of the predicted values are interesting. While they are still far from the actual values, they provide predictions that can be used to calculate the likelihood of the home team winning or losing. If the predicted value is positive, it is likely the home team will win. If the predicted value is negative, it is likely the away team will win. This model provides a great foundation for predicting the next season's match outcome.

![ActualVsPredicted](https://github.com/Isaiahensley/PremierLeague-Goal-Differernce-Forecasting/assets/143129356/16fa135c-48c7-48ba-8132-2fa16cd3a86f)


**Conclusion:**
In conclusion, this study demonstrates that it is possible to predict English Premier League results with a machine learning model that has been trained on the home team, away team, and goal difference information from the previous season. The application of linear regression has proven to be effective. Even without player-specific data, the model provides insightful information about how matches will turn out. This project establishes the foundation for future investigation and improvement, with the possibility of adding more features to improve prediction performance.
