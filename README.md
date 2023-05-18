# NBA

**Introduction**

This folder contains a project I've done - building models to predict if NBA players' career duration can last beyond 5 years

The data was sourced from public database, Kaggle, but seems to be inaccessible anymore so the file that was originally extracted from Kaggle is uploaded in this folder as "nba-player.csv".

**Problem Statement**

In every NBA draft, every NBA team would want to get the best and most suitable player for their team. In a way, this comes as an investment as the team would wants to scout players who can add value to their team, especially in the long run. This is of utmost importance if a team would want to secure players who can stay with the team in the long term. However, not every players can last long in their career. When that happens, it will then cause some repurcussions as the team may needs to get replacement by signing new players subsequently or have to have a change of plan. Notwithstanding injuries which was unavoidable, longeivity of the players can also be dependent on their performance on the court. Therefore, every players on-the-court performance statistics is of utmost importance.

**Aim**

The aim of this project is to make use of existing and/or current players' attributes to build models that can predict if a NBA player's career can last over 5 years. Secondarily, features which can affect this concern will also be analyzed.

The data has 1340 rows by 22 columns, which are as follows: (demarcated by ,)
'Unnamed: 0', 'name', 'gp', 'min', 'pts', 'fgm', 'fga', 'fg', '3p_made',
       '3pa', '3p', 'ftm', 'fta', 'ft', 'oreb', 'dreb', 'reb', 'ast', 'stl',
       'blk', 'tov', 'target_5yrs'

**Data Exploration**

Importing and Cleaning Data

Data was first imported. After finding out the basic information (Data shape, type, attributes etc), it was investigated for missing, illogical and duplicated data, for which are removed for those with it.

Data Analysis

Data visualisation was performed to find out the distribution of our target variable, as well as to break down the data distribution by the target variable. Boxplot and bar graph was used. Data for the target variable was fairly distributed. Heatmap was also generated to visualize the correlation across all attributes as well as with the target variabel, before feature selection was done for final attributes being input into the machine learning models.

**Machine Learning Models**

The final data was first split into training and test partitions in the ratio of 70:30. Models used in this project are supervised learning algorithms, inlcluding:

KNeighborsClassifier

SVC

LogisticRegression

DecisionTreeClassifier

GaussianNB

RandomForestClassifier

GradientBoostingClassifier

**Findings**

When cross-validation was employed, accuracy decreased from 0.724311 to 0.715334. When feature selection is performed with the use of cross-validation, as compared to the initial average accuracy of 0.6949988607883345 (Based on 10 splits), there is an increased in the average accuracy after feature selection, which increased the average accuracy to 0.7032809295967191 (Based on 10 splits).
In terms of feature importance, 3 points and free throw conversion does not seems to be important in affecting the players career duration will last over 5 years or not. Results showed the best model was logistic regression. 


