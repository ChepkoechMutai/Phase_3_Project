# Phase_3_Project

**PREDICTING WHETHER INDIVIDUALS SHOUlD RECEIVE H1N1 VACCINE**


**Overview**

This project's aim is to build a model that predicts individuals' response to vaccines based on how they reacted to the H1N1 vaccine in 2010. It will use the several feature variables provided to establish the connection between them and the target variable H1N1 vaccine. The dataset used for this project was ontained from DrivenData and contains information on individual's characteristics ranging from level of concern to behaviour in their homes and large gatherings. The project covers the following sections: Business Understanding,Problem Statement,Objectives,Metrics of Success,Data Understanding,Data Preparation,Exploratory Data Analysis,Feature Engineering,Modeling,Feature Selection,Hyperparameter Tuning,Conclusion and Recommendation for Future Steps

**Introduction**

The public health organization is interested in finding the response of individuals to the H1N1 vaccine in 2010, if a majority took it or not. With the cropping up of global pandemics like COVID-19, public health has become very critical and a priority to the government and health sector. For this reason, they saw it fit to study vaccines, and specifically, whether individuals get them or not. Having been approached with this, we look to build a classification model that will establish whether indivuals took the h1n1 vaccine and the factors that were correlated to them and predict individual's possible reaction to a case like this in the future. This will help the stakeholders to establish a feasible way to approach this issue in future.

I apply machine learning for this project because it will give the stakeholders a view of trends in individuals' behaviors in relation to their response to vaccines, as well as supports the development of new vaccines if need be.

**Problem Statement**

Vaccination has become a key public health measure that is used to fight and in most cases curb infectious diseases. Vaccines provide immunization for individuals and having a community participate in the process can further decrease the spread of diseases as a result of the concept of "herd immunity."

The goal of this project is to build a model that can predict the response of individuals to a vaccine based on certain features, such as age, sex, health status, and their knowledge on H1N1 vaccine. This information can help healthcare professionals make informed decisions about who should receive the vaccine and how to best manage its administration.

**Objectives**

**Main Objective**

The main objective of this project is to build a model that will predict the response of individuals to a newly introduced vaccine that is H1N1 vaccine so it can lay a foundation for what direction of the research the health sector should take.

**Specific Objective**

Identify which factors affect individuals' response to vaccines

Accurately predict the general response of individuals to a new vaccine

Build a classification model that accurately predicts the response of individuals to new vaccines and provides actionable insights on how to reduce the spread of contagious infections.

**Metric of Success**

The final model will be considered a success if it has an accuracy and f1 score of not less 75%. The goal is to make as accurate as possible predictions, that is why the choice of success metrics is the accuracy score and f1 score.

**Data Understanding**

**Data Description**

The dataframe has 26707 observations and 35 features. The data on the training features (the input variables that the model will use to predict the probability that people received H1N1 flu vaccines and seasonal flu vaccines) contains 35 feature columns in total, each a response to a survey question.

**Data Preparation**


The data underwent cleaning and preprocessing processes that would ensure it was in the right form for modeling. This was done dealing with missing values by dropping and filling in. The duplicates were also dropped and categorical data was encoded using label encoding. In EDA trends in the distrinution and correlation of the features and the target was established.

**Modeling**

In this section, four models were built. The first was the base model; a simple logistic regression model that was fitted on the training set before any feature selection was done. Fitting this model to the test data resulted in a very weak f1 score of 43%, and regardless of the contrasting higher accuracy score, the model was considered a poor performing model. In an attempt to improve our results, feature selection was performed and the most important features used to fit the second model which was KNN. This, however, proved to be performing even worse than the previous one with an f1 score of 36%. For the third model, we built a decision tree that resulted in an f1 score of 36%, still a poor performance. Following the same kind of results after building three models, there was need to do more to improve the outcome. It was at this point that hyperparameter pruning was carried out on the decision tree model and an improvement in the f1 score was seen at 78%.

**Conclusion**

After experimenting with different models using different techniques, the final model (the decision tree), which was tuned by hyperparameters was selected. This is because it met the success criteria by recording an accuracy score of 80% and f1 score of 78%. The first three models did not do so well because they were not complex enough to handle the nature of data presented. This is why while the accuracy score was high, the f1 score remained low. By adjusting the hyperparameters, we were able to find the optimal complexity that balanced overfitting and underfitting. 

**Recommendation**

The public health sector should carry out more research on how people responded to other vaccines because while this model may provide important insight, it may not be as conclusive as a weighted outcome of several different vaccine types.

Surveys like the one that led to getting the dataset used in this project are not very effective since they are done on phone. Individuals answer more truthfully in person, because of lack of this, the dataset ended up with a lot missing values.

Seeing as to how the model was performing poorly at first continously, in the future, the data preprocessing processes need to be improved.

From evaluating the distribution of H1N1 vaccine, it was established that only around 20% of the individuals had taken the vaccine. The public health organization in charge should look deeper into the reasons behind people not wanting to take the vaccine. It could be that they are not concerned enough, or do not have enough knowledge because it was established during EDA that with increase in levels of concern and knowledge about the vaccine by individuals, the higher the chances were of them taking the vaccine.




