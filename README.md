# SC1015
# Welcome to WHO-Life-Expectancy repository
## About
This is a Mini-Project for SC1015 (Introduction to Data Science and Artificial Intelligence) at Nanyang Technological University (NTU) Singapore. <br>
This project focuses on the [Life Expectancy Dataset](https://www.kaggle.com/datasets/kumarajarshi/life-expectancy-who) from WHO.

## Introduction
Life expectancy is one of the key indicators and metric for a country's success and wellbeing, and is one of the most widely used metric among governmental institutions around the world for policy making. It is defined as the average time a person in that country is expected to live based on the year he/she is born. 

Life expectancy itself is very complicated and is influenced by a huge number of ever-changing factors all to varying degrees. Therefore it has been historically difficult to predict and measure accurately. Our group, **A128 Group 2** will be attempting to de-complicate this complex metric, by breaking it down to its components, finding out which of the **various factors seem to correlate and affect life expectancy numbers the most**. We will be exploring trends in data over **16 years in 193 countries** and finally, try to create an accurate **machine learning** model to predict life expectancy in countries around the world. Join us as we embark on this journey together!

## Directory
For detailed walkthrough, please view the source code in order from:
1. [data preparation and cleaning](https://github.com/GeneralR3d/SC1015-WHO-Life-Expectancy/blob/main/data%20preparation%20and%20cleaning.ipynb)
> - initial data exploration to prepare for cleaning
> - Changing of coloumn names and variable scaling
> - Data cleaning for 0 values
> - Identification of NULL values and imputation using MICE
2. [Exploratory Data Analysis](https://github.com/GeneralR3d/SC1015-WHO-Life-Expectancy/blob/main/Exploratory%20Data%20Analysis.ipynb)
> - visualisation of differences in trends and distribution of all features
> - gathering insights from rankings
> - exploratory analysis of life expectancy against all other features
> - exploratory analysis and visualisation of all features over TIME (16 years)
3. [data transformation](https://github.com/GeneralR3d/SC1015-WHO-Life-Expectancy/blob/main/data%20transformation.ipynb)
>- Comparison of various skew correction and normalization methods
>- Skew correction using methods like Yeo-Johnson and Quantile Transformation
>- Note on outlier treatment
4. [regression model and feature selection](https://github.com/GeneralR3d/SC1015-WHO-Life-Expectancy/blob/main/Regression%20model%20and%20feature%20selection.ipynb)
> - Basic correlation exploration
> - Multivariate Linear Regression
> - Polynomial Regression
> - Random Forest Regression
> - Feature selection using SelectKBest
5. [Unsupervised Learning and model improvment](https://github.com/GeneralR3d/SC1015-WHO-Life-Expectancy/blob/main/Unsupervised%20Learning%20and%20model%20improvement.ipynb)
> - KMeans unsupervised clustering and model improvement
6. [Side Quest - Predicting Developmental Status](https://github.com/GeneralR3d/SC1015-WHO-Life-Expectancy/blob/main/Side%20Quest%20-%20Predicting%20Developmental%20Status.ipynb)
> - Binary decision tree classifer vs logistic regression

## Dataframes
1) Life: The original dataframe with missing values
2) Life_filled: the dataframe with imputed data, used for EDA
3) Life_agg: the dataframe with aggregated rows for each country for EDA
4) Life_tranform: the dataframe after skewness correction, **NOT** used in EDA, used for machine learning

## Contributors
- Tuan Ding Ren [GeneralR3d](https://github.com/GeneralR3d)
> Data Cleaning, Exploratory Data Analysis, Data Transformations, presentation
- Tey Cia Meng [teyc02](https://github.com/teyc02)
> Random Forest Regression, KMeans clustering, slides
- Nathaniel Lo Tzin Ye  [lotzinye](https://github.com/lotzinye)
> Binary tree decision classifier, logistic regression, presentation

## Problem statement
1. Can we predict life expectancy of a country based on other factors like schooling, developmental status and vaccination against diseases?
2. Which model would provide the most accurate results?<br>
Extra: Model to predict developmental status of a country based on other factors

## Models and tools used
1. Multivariate Imputation using Chained Equations (MICE)
2. Yeo-Johnson Transformation
3. Quantile Transformation
4. Label Encoder
5. SelectKBest feature selection
6. K-fold Cross Validation
7. Generalized Linear Model (GLM)
8. Polynomial Regression
9. Random Forest Regression
10. K-Means clustering
11. Binary Decision Tree classification
12. Logistic Regression

## Conclusion
Life expectancy, as complex as it sounded at the beginning of our project, turned out to be very possible to predict using machine learning models. On our journey to achieve that, we have learnt so much about the whole data science process and pipeline, from first obtaining the data, to cleaning it, processing it, making sense of it to obersering relations and finally making the neccessary preparations to give to a machine learning model. We have learnt a lot about the various factors at play that seem to influence and interaction with life expectancy, and how these interactions change over the course of 16 years. We believe that our model will be able to predict life expectancy accurately given the limited resources.


## What did we learn?
1. Data does not start off perfect. In fact, more often, real world data contains all sorts of mistakes and inaccuracies from the real world, during data collection. It is up to the data scientist to interpret and correct for these gaps. Such includes missing data ( very common) as well as 0 values which can masquarade themselves as legitamate data when they are actually missing values. For example, it does not make sense for`INFANT_DEATHS` to be 0. We learnt that data intrepretation at the start, prior to machine learning is incredibly important as it is the first time we come into contact with the data. Therefore it is only right for us to explore each every column of data, beyond just their numeric values, and think about what they mean in real life, and whether such a value makes sense.<br>
<br>
2. Missing values can heavy influence the direction and outcome of a data science process. Therefore it is imperative we take extra precaution when imputing missing values, such as using robust imputation techniques and setting proper lower and upper limits for the imputer such that the values that are imputed also make sense, for example using MICE<br>
<br>
3. Many machine learning models are extremely sensitive to imbalanced data and skewed distributions, some even require the data to be standardized on the same scale. Thus it is up to the data scientist to correct for such data and pay attention to feature engineering before feeding it into the machine learning model. As the saying goes, " Garbage in, garbage out."<br>
<br>
4. For our sepecific data set we discovered that a quadratic model of degree 2 actually fits better than a linear model. However a tree based regression model like random forest regression still yields the best results by far.
5. We realise that feature engineering is extremely important to the whole process of data science and machine learning, and that making sense of features, imputing them properly, making sense of them and correcting them take up more than half of the pipeline, and yet is absolutely neccessary for a model to perform well.

## References
- https://www.analyticsvidhya.com/blog/2020/07/types-of-feature-transformation-and-scaling/
- https://www.datanovia.com/en/lessons/transform-data-to-normal-distribution-in-r/
- https://towardsdatascience.com/best-exponential-transformation-to-linearize-your-data-with-scipy-cca6110313a6
- https://www.analyticsvidhya.com/blog/2020/04/feature-scaling-machine-learning-normalization-standardization/?utm_source=blog&utm_medium=types_of_scaling
- https://towardsdatascience.com/transforming-skewed-data-73da4c2d0d16
- https://opendatascience.com/transforming-skewed-data-for-machine-learning/
- https://becominghuman.ai/how-to-deal-with-skewed-dataset-in-machine-learning-afd2928011cc
- https://www.simplilearn.com/normalization-vs-standardization-article
- https://pub.towardsai.net/feature-transformation-and-scaling-techniques-f9645cb538e#:~:text=9%20methods%20to%20increase%20the%20performance%20of%20machine%20learning%20models&text=Feature%20Transformation%20is%20simply%20a,For%20example%2C%200%20to%201.
- https://medium.com/@isalindgren313/transformations-scaling-and-normalization-420b2be12300
- https://www.youtube.com/watch?v=bqhQ2LWBheQ
- https://www.analyticsvidhya.com/blog/2020/03/one-hot-encoding-vs-label-encoding-using-scikit-learn/
- https://www.analyticsvidhya.com/blog/2019/08/comprehensive-guide-k-means-clustering/
- https://stackoverflow.com/questions/56308116/should-feature-selection-be-done-before-train-test-split-or-after
- https://medium.com/analytics-vidhya/a-guide-to-data-transformation-9e5fa9ae1ca3
- https://www.analyticsvidhya.com/blog/2020/04/feature-scaling-machine-learning-normalization-standardization/?utm_source=blog&utm_medium=types_of_scaling
- https://machinelearningmastery.com/iterative-imputation-for-missing-values-in-machine-learning/
- https://stats.stackexchange.com/questions/421545/multiple-imputation-by-chained-equations-mice-explained
- https://medium.com/@allenhuang1996/whats-the-difference-between-null-and-nan-in-python-a1af20d523ce
- https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html
- https://statisticsbyjim.com/basics/remove-outliers/#:~:text=It's%20bad%20practice%20to%20remove,leave%20it%20in%20the%20dataset.
- https://www.youtube.com/watch?v=otolSnbanQk&list=PLZoTAELRMXVPBTrWtJkn3wWQxZkmTXGwe&index=61
- https://stats.stackexchange.com/questions/58739/polynomial-regression-using-scikit-learn
- https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.PolynomialFeatures.html
- https://towardsdatascience.com/5-feature-selection-method-from-scikit-learn-you-should-know-ed4d116e4172
- https://scikit-learn.org/stable/modules/cross_validation.html#cross-validation
- https://towardsdatascience.com/how-to-improve-the-accuracy-of-a-regression-model-3517accf8604
- https://towardsdatascience.com/what-are-rmse-and-mae-e405ce230383
- https://towardsdatascience.com/clustering-with-more-than-two-features-try-this-to-explain-your-findings-b053007d680a
- https://medium.com/@sjacks/feature-transformation-21282d1a3215#:~:text=Unlike%20Min%2DMax%20or%20Max,(skewness)%20of%20the%20data.
- https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.PowerTransformer.html#sklearn.preprocessing.PowerTransformer
- https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.QuantileTransformer.html
- https://scikit-learn.org/stable/modules/generated/sklearn.impute.IterativeImputer.html
- https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.SelectKBest.html
