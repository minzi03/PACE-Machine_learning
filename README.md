# PACE-Machine_learning

## Perform_feature_engineering

### **Introduction**

Dataset: nba-players.csv

It represents 22 columns of United States National Basketball Association (NBA) player performance records per game for one season, including stats like average number of 3-point baskets made per game, and average number of offensive rebounds per game.

The dataset contains:

1,340 rows – each row is a different NBA player’s stats per game across one season

22 columns

Note: A “field goal” in basketball means the ball has gone through the hoop during play resulting in points scored. 2 and 3 points are scored during game play based on the distance the player is from the hoop. 1 point is scored during a “free throw,” representing a free shot at the basket due to a foul by the other team.

| Column Name   | Type | Description                                                                                                |
| ------------- | ---- | ---------------------------------------------------------------------------------------------------------- |
| `Index`       | int  | Index column (unique identifier for each row).                                                             |
| `name`        | str  | NBA player’s first and last name.                                                                          |
| `gp`          | int  | Number of games played in one season.                                                                      |
| `min`         | int  | Average number of minutes played per game.                                                                 |
| `pts`         | int  | Average number of points scored per game.                                                                  |
| `fgm`         | int  | Average number of field goals made per game.                                                               |
| `fga`         | int  | Average number of field goals attempted per game.                                                          |
| `fg`          | int  | Field goal percentage (made field goals divided by attempts).                                              |
| `3p_made`     | int  | Average number of 3-point field goals made per game.                                                       |
| `3pa`         | int  | Average number of 3-point field goals attempted per game.                                                  |
| `3p`          | int  | 3-point field goal percentage (made 3-pointers divided by attempts).                                       |
| `ftm`         | int  | Average free throws made per game.                                                                         |
| `fta`         | int  | Average free throws attempted per game.                                                                    |
| `ft`          | int  | Free throw percentage (made free throws divided by attempts).                                              |
| `oreb`        | int  | Average number of offensive rebounds per game.                                                             |
| `dreb`        | int  | Average number of defensive rebounds per game.                                                             |
| `reb`         | int  | Average total rebounds per game.                                                                           |
| `ast`         | int  | Average number of assists per game.                                                                        |
| `stl`         | int  | Average number of steals per game.                                                                         |
| `blk`         | int  | Average number of blocks per game.                                                                         |
| `tov`         | int  | Average number of turnovers per game.                                                                      |
| `target_5yrs` | int  | Binary target variable indicating if the player's career duration was more than 5 years (1 = yes, 0 = no). |

As you're learning, data professionals working on modeling projects use featuring engineering to help them determine which attributes in the data can best predict certain measures.

In this activity, you are working for a firm that provides insights to the National Basketball Association (NBA), a professional North American basketball league. You will help NBA managers and coaches identify which players are most likely to thrive in the high-pressure environment of professional basketball and help the team be successful over time.

To do this, you will analyze a subset of data that contains information about NBA players and their performance records. You will conduct feature engineering to determine which features will most effectively predict whether a player's NBA career will last at least five years. The insights gained then will be used in the next stage of the project: building the predictive model.

### **Considerations**

**Some key takeaways**

- It is important to check for class balance in a dataset, particularly in the context of feature engineering and predictive modeling. If the target column in a dataset has more than 90% of its values belonging to one class, it is recommended to redistribute the data; otherwise, once a model is trained on the imbalanced data and predictions are made, the predictions may be biased.
- Feature selection involves choosing features that help predict the target variable and removing columns that may not be helpful for prediction. In this process, and throughout feature engineering, it is important to make ethical considerations.
- Feature transformation involves transforming features so that they are more usable for future modeling purposes, which includes encoding categorical features to turn them into numerical features.
- Feature extraction involves combining existing columns meaningfully to construct new features that would help improve prediction.

**What summary would you provide to stakeholders? Consider key attributes to be shared from the data, as well as upcoming project plans.**

- The following attributes about player performance could help predict their NBA career duration and should be included in a presentation to stakeholders: field goals, three-point field goals, free throws, rebounds, assists, steals, blocks, turnovers, total points, and efficiency as points per minute.
- It would be important to explain that these attributes, along with a relevant dataset, will be used in the next stage of the project. At that point, a model will be built to predict a player's career duration. Insights gained will be shared with stakeholders once the project is complete. Stakeholders would also appreciate being provided with a timeline and key deliverables that they can expect to receive.
