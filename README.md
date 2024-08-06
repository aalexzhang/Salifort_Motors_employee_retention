# Salifort Motors employee retention data project
#### Featuring comprehensive EDA and feature tuning to create optimized decision tree and random forest models

# Project Overview

The goal of this project is to create data-driven models to improve employee satisfaction. This data includes features such as satisfaction from 0 to 1, number of projects, average work hours per month, time spent at the company, and whether the employee left the company. The best random forest model reached an accuracy of 96.16% with a precision of 87.04%, with feature evaluation showing that metrics such as time since the employee's last evaluation, number of projects, and tenure affected whether an employee left or not the most.

# Business Understanding 

The importance of these models to stakeholders is mainly the insights into what factors can improve employee satisfaction and increase retention regardless of the employee. The models can serve as predictors as to how Salifort Motors can improve their work environment.

# Data Understanding 

The Salifort Motors dataset comes from a fictional company, but the data mirrors real-world employee satisfaction metrics. Some limitations of the dataset include quite a few outliers for tenure that represent founders or higher management, whereas the majority of employees have only been hired a few years. 

Some insights about satisfaction found during EDA include a few centralized groups of employees leaving who were either unsatisfied, or satisfied and overworked. Also, ratios between employees leaving and staying were similar across all 10 departments, indicating company-wide trends. However, finding disproportionate ratios could indicate problems in a certain department or with managers.



# Modeling and Evaluation 

Initally, I used a binomial logistic regression model predicting whether the employee left or not. Features included encoded salary levels, one-hot encoded department values, and many other features. Through model training and evaluation with a confusion matrix, the logistic regression model suffered from imbalanced data with significantly more employees staying compared to those that left. It had a f-1 score of 0.9 for employees that stayed, versus a f-1 score of 0.33 for employees that left.

Next, I tried a decision tree based on the same features. Using gridsearch to find the best model hyperparameters, the decision tree model performed better than the logistic model, and I implemented a random forest model to improve upon the singular decision tree. The best random forest resulted in an accuracy of 0.977983 and precision of 0.950023.

However, the feature average monthly hours might be biased due to employees that left inherently having lower average monthly hours. After dropping this feature and recreating the random forest, the best model resulted in an accuracy of 0.961641 and precision of 0.870406.

# Conclusion

These models showcase a real-world application of analyzing and cleaning data, then creating tools to find insights. For next steps, further improvement on the models with different data could allow Salifort Motors to consolidate all of their insights to make data-driven decisions to increase employee satisfaction and retention.