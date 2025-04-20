# Employee-Promotion
# About
This is a Mini-Project for SC1015 which uses the Employee Promotion Data from Kaggle. \
Data taken from: https://www.kaggle.com/datasets/arashnic/hr-ana?select=train.csv

# Contributors
Raksha - Presentation + Slides \
Sunjin - Presentation + Slides \
Marenda - Notebook Coding

# Problem Definition
- How do different variables such as previous_year_rating, awards_won?, region and avg_training_score affect whether an employee is promoted in each of the different departments: Sales & Marketing, Operations and Technology?
- Which model would be the best for such prediction depending on time complexity, accuracy, and ease of modelling?

# Encoding Technique
- Target Encoding
- One-Hot Encoding considered, but later not used due to the large number of classes of the region category.

# Models Used
- Decision Tree
- Random Forest
- CatBoost

# Conclusion
- Features utilized: region, previous_year_rating, awards_won?, avg_training_score
- Decision Trees and Random Forest seem to provide similar metrics such as classification accuracy(above 90%) and F1-Score(0.29 to 0.58), while CatBoost performed poorly in comparison. (Accuracy of 75% to 79%, F1-Score less than 0.37)
- CatBoost took the longest time for fitting at about 50 seconds, followed by Random Forest (about 1 second) and Decision Trees (less than 1 second).
- Hyperparameter tuning for Decision Trees and Random Forest was able to maintain similar metrics or improve the model slightly
- Hyperparameter tuning takes way longer for Random Forest (up to 80 seconds) compared to Decision Trees (up to 12 seconds)
- Hyperparameter tuning seemed infeasible for CatBoost as it took longer than 200 seconds.
- Although we are in favor of using Decision Trees for this dataset due to its lower time taken and high classification accuracy, F1-Score does not seem to be ideal (can be as low as 0.35). This may indicate that there are better models or techniques that can be used to create a better classification model.

# What we learned from this project
- Different ways of visualizing data using mosaic plot when data is very imbalanced for better representation
- Utilizing Cramer’s V Values to measure the association of one categorical variable with another
- Utilizing SMOTE-NC to oversample the data when it is extremely imbalanced
- Target Encoding to encode the categorical variables to use in machine learning models
- Random Forest and CatBoost
- Hyperparameter tuning for Decision Trees and Random Forest using GridSearchCV and RandomizedSearchCV
- Different metrics such as F1-Score and Recall

# References
- https://www.kaggle.com/datasets/arashnic/hr-ana?select=train.csv
- https://medium.com/analytics-vidhya/hello-everyone-4f9400e008dc
- https://medium.com/@manindersingh120996/understanding-categorical-correlations-with-chi-square-test-and-cramers-v-a54fe153b1d6
- https://imbalanced-learn.org/stable/references/generated/imblearn.over_sampling.SMOTENC.html
- https://koshurai.medium.com/title-mastering-target-encoding-in-python-a-comprehensive-guide-e495bd83d602
- https://www.datacamp.com/tutorial/random-forests-classifier-python
- https://www.kaggle.com/code/prashant111/catboost-classifier-in-python
- https://medium.com/biased-algorithms/grid-search-for-decision-tree-ababbfb89833
- https://www.analyticsvidhya.com/blog/2022/11/hyperparameter-tuning-using-randomized-search/
- https://medium.com/@maxgrossman10/accuracy-recall-precision-f1-score-with-python-4f2ee97e0d6
