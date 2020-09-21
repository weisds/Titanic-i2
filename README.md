# Titanic Prediction - A Comprehensive Analysis and Experiment for the Kaggle Titanic Competition 

## Abstract

This kernel was created for the purpose of defining the best features and models for the Kaggle Titanic dataset that together yields the best prediction score. This kernel contains details around the analysis and experiment undertaken in the effort to derive the best feature and model set. In addition, this analysis also reveals the causation effect on the prediction result of each engineered feature, various feature combinations derived from feature selection technique, and all features (raw and engineered).

## Introduction 
We are attempting to create an ML model or model that, given a set of inputs, provides a binary result indicating rather or not a passenger will survive the well-known Titanic shipwreck incident. This kernel contains detailed breakdowns of the analysis and experiments attempted in the effort to achieve the highest precision model. 

The steps taken are grouped into two major sections: Iteration 1, where we conducted EDA, Feature Engineering and the attempts to build the most accurate model with our findings; Iteration 2, we sought to build upon the effort from Iteration 1 by validating the causation effect of each engineered feature on the prediction results to determine the best feature set for training our models. In addition, we also attempted a couple of new feature engineering techniques in this iteration, namely, interaction and normalization.


## Conclusions
Reveals by our post-submission analysis, we see that Sex, Title and Pclass_Sex_Embarked are the top three features that have the most positive effect on the survival rate, and we don't see any strong trend on features that have a negative impact on our result. Concluding from our Permutation Importance analysis and Shap analysis, we can predict with a level of certainty that a female passenger where Pclass equals 1 and is onboarding from Southampton will have a better chance of surviving the accident. 


### Modeling and Data Preperation
From our Iteration 1 effort, we can conclude that blindly creating new features based on correlations and dropping or keeping the raw features without knowing the subsequent impacts will let to results that are difficult to interpret hard to improve on.

On the other hand, from Iteration 2, we noticed that results from baseline model evaluation on features do not always hold true in the final modelling evaluation. Specifically, we see that measures that resulted in a positive impact on the model accuracy based on our baseline model evaluation, when aggregated, did not lead to a stacked improvement as anticipated. Instead, we observed a much lower accuracy score when combining these measures. As a result, we propose that in future modellings, all features should be kept, and use feature selection techniques to generate the best dataset, and we should test different feature combinations for the optimal result.


## Techniques Used
### Data Cleaning
- Fillna ()
- Filling missing data from lookup tables
### Feature Engineering
- Data evaluation to determine subsequent feature engineering approaches
    - Distribution
    - Corrolation
    - Text data patterns
    - Categorical data
    - Data clustering
- OneHot Encoding
- Interations
- Normalization
- Text Data Manipulation
- Converting Continuous Data to Discrete Data
- Productionization
### Modeling
- Cross Validation
- Hyperparameter Tuning
- Voting (Ensemble)
- Grid Search
- Feature Evaluation (base model evaluation)
- Post Modeling Evaluation (Permutation Importance and Shap analysis)



## Credits

Many techniques and feature engineering approaches are inspired and borrowed from the sources listed below
- https://www.kaggle.com/ldfreeman3/a-data-science-framework-to-achieve-99-accuracy
- https://www.kaggle.com/kenjee/titanic-project-example
- https://www.kaggle.com/learn/overview