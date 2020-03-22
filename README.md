# Project-4

Blog Post for this project can be found on Medium through the following Link: https://link.medium.com/4viYqNyC44
The python libraries used in this project are numpy, pandas, math, sklearn, and matplotlib.

## Project Definition
Project Overview
High-level overview of the project
This data science project focuses on building an AI/ML model to predict the 52-week price performance of a stock based on financial data extrapolated from the S&P 500 list of companies. The data are explored, visualized and processed. Then the SVR is implemented and refined. Finally, the results are covered alongside the conclusion.

## Background information
Problem domain, origin, and data sets: It is challenging to predict a stock's 52-week price performance with accuracy. The financial experts use certain criteria to predict performance, but that skill is tacit and difficult to learn. This project will aim to teach a machine how to make a prediction with 70%+ accuracy. The data set is gathered from Fidelity.com. If you have an account with Fidelity you can extract the data from their screener option by using their "download to excel" option.

## Problem Statement
Machines do not know how to predict a stock's 52-week price performance with accuracy. This project showcases a strategy for solving the problem by using support vector machine (SVM). After the model is trained and tested, it will be able to provide a solution that can predict a stock's 52-week price performance with 73% accuracy.
Metrics
We used the regression form of SVM known as SVR (support vector regression). The metric used to measure performance of the SVR model is the R2 score. The higher the score is to 1, the more accurate the model is. A score that is near is above .7 is considered an acceptable rate to deem the model reliable. We picked the metric because we need high accuracy to predict the stock market and cannot afford a 50/50% chance for such an important topic that involves financial ramifications.

Results
Model Evaluation & Validation
The R2 score is used to evaluate the robustness of the model SVR model. The kernel used for the model was rbf as recommended by scikit learn library based on the type of data set we used. In this case the score .735, which means the model is accurate 73.5% of the time.

Justification
We are not ecstatic about the results of 73.5% accuracy, ideally we wanted to reach 75%+, however we are satisfied with 73.5%. We were able to train the machine and run the test on the data that allows the machine to make a solid prediction that will be accurate 73.5% of the time.

The SVR model was used because a linear regression would not suffice for a data set with more than 1 feature. A multiple regression may work but based of research findings SVR is a more flexible technique, helping to deal with the limitations pertaining to distributional properties of underlying variables, geometry of the data and the common problem of model overfitting. "We observe that SVR is superior to SLR as a prediction method. SLR cannot capture the nonlinearity in a dataset and SVR becomes handy in such situations" https://rpubs.com/linkonabe/SLSvsSVR


We first determined we have more than 50 samples and our focus was predicting a quantity and not a category, therefore we eliminated all of the classification model and picked a regression model. Since we do not have more than 100K samples there was no need to do SDG Regressor. Also, having few features was not important so we did not pick Lasso, or Elastic Net. The best two choices were SVR and RidgeRegesion, hence we picked SVR as it was the most suitable model for our problem.

## Conclusion
### Reflection
We started by attempting to find ways to solve the problem. I learned a lot about picking the right algorithm and learned about the many options that exist. The most challenging parts of this project were two-fold. 1. Finding the data, we first attempted to build an ETL pipeline by using a yahoo web scrapping API but that was unsuccessful. I learned that extracting the data and building ETL pipelines is the hardest part of data science, which makes me interested in learning even more about data engineering. I also learned that there are a plethora of APIs from many sources, and some need a partnership with the provider to grant access to their data. I found that Google alone had hundresds and hundreds of APIs that will take a full semester course just to learn some of them. The second part was feature engineering to find the most relevant features that will make an accurate prediction.

### mprovement
This project can be improved/enhanced with an ETL pipeline that can pull data automatically through a refresh button from a financial website. It can also be improved by building an application that allows users to input a stock ticker and be able to get an output of a prediction of the 52-week price performance of that particular stock that they searched.

## Acknowledgements
We would like to thank Fidelity.com for providing the financial data.
The SEC (Security Exchange Committe) for making corporate companies' data publicly available, and sklearn's library website for having step by step tutorials on using their library.
 
