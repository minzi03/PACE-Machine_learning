# PACE - Machine Learning Project

## Perform Feature Engineering

### **Introduction**

**Dataset:** `nba-players.csv`  
This dataset represents performance records for NBA players during a single season, with statistics like the average number of 3-point baskets made per game, offensive rebounds, points scored, and more.

- **Rows:** 1,340 (each row corresponds to an individual NBA player’s stats per game for one season)
- **Columns:** 22

**Note:** In basketball, a “field goal” refers to a basket made during gameplay, scoring either 2 or 3 points depending on the distance from the hoop. A “free throw” refers to a 1-point shot awarded due to a foul.

### **Dataset Overview**

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

### **Project Overview**

This project aims to help NBA managers and coaches identify players who are likely to succeed in the high-pressure environment of professional basketball and have a career lasting at least five years. To achieve this, we will conduct **feature engineering** on player performance data to determine which attributes are the most predictive.

### **Key Considerations for Feature Engineering**

- **Class Balance:** It is crucial to check if the target column (`target_5yrs`) has a balanced distribution of classes. Imbalanced data could bias model predictions, particularly if over 90% of values belong to one class.
- **Feature Selection:** We will carefully select relevant features that contribute to predicting career longevity and remove irrelevant or redundant columns. Ethical considerations will also be taken into account during this process.
- **Feature Transformation:** Transformations like encoding categorical features into numerical values and normalizing features will ensure the data is suitable for modeling.
- **Feature Extraction:** We will explore creating new features, such as efficiency (points per minute), to improve model performance by combining existing features in meaningful ways.

### **Insights for Stakeholders**

To provide value to NBA teams, we will focus on key performance attributes that may predict a player's career longevity. The following attributes have been identified as potentially useful:

- **Field goals (fg, fgm, fga)**
- **3-point field goals (3p_made, 3pa, 3p)**
- **Free throws (ftm, fta, ft)**
- **Rebounds (oreb, dreb, reb)**
- **Assists (ast)**
- **Steals (stl)**
- **Blocks (blk)**
- **Turnovers (tov)**
- **Points scored per game (pts)**
- **Efficiency (calculated as points per minute)**

These features will be used in the next stage of the project to build a predictive model. The model will help forecast whether a player’s career will last at least five years based on their performance metrics.

### **Next Steps**

The next phase of this project will involve building a machine learning model using the engineered features to predict player career duration. A detailed timeline and key deliverables will be shared with stakeholders, along with insights generated from the model.
