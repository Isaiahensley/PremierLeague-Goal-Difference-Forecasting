# PremierLeagueNet-Goal-Difference-Forecasting

**Abstract**
This paper explores the use of machine learning models to predict outcomes in the English Premier League (EPL) results over the course of multiple seasons. Using a model trained on goal differentials from a previous season, the model will predict results for the next season. The model is able to determine whether a team is likely to win or lose by using the predicted goal difference data. Our model assumes that all teams in both seasons consist of the same players. This project achieves the best results when using linear regression compared to other models such as RandomForestRegressor, DecisionTreeRegressor, and SVR. This method provides a basis for further improvements and offers insightful information about the difficulties involved in predicting the results of football games.


**Introduction:**
The English Premier League (EPL), known for its unpredictable nature and intense competition, is considered the highest level of football. Because team lineups are always changing, forecasting the results of matches is extremely difficult. By utilizing machine learning techniques and emphasizing goal difference as a crucial metric for prediction, this study seeks to address this challenge. This method shows the possible effectiveness of such approaches by using historical data from one season to train a model and then using that model to predict results in the next season.

**Data Analysis:**
Each English Premier League season comprises twenty teams, each team participates in 19 home games and 19 away games. At the end of each season, the three teams with the worst performance are dropped out, making way for new teams in the next season from the EFL Championship, the second tier of English football. This system of promotion and relegation in each season helps to maintain a competitive balance for the top two tiers of English football. It is also common for teams to have different players in each season. Because we were not provided player data in our datasets, we will assume the players on each team throughout both seasons remain the same for this project.
![GoalsBetweenSeasons](https://github.com/Isaiahensley/PremierLeague-Goal-Differernce-Forecasting/assets/143129356/21fd5857-e400-4ccf-a33c-a33563c3abd1)
These graphs show the similarity in team performance during both seasons used in this project. Even with the possibility for teams to consist of different players in the following season, there is a clear correlation in team performance regardless of this.
