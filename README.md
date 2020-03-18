# Sparkify Project

## Table of Contents

1. [Project Overview](#overview)
2. [Project Motivation](#motivation)
3. [Files Description](#description)
4. [Dependencies](#dependencies)
4. [Results](#results)
5. [Acknowledgements](#acknowledgements)


### Project Overview <a name = "overview"></a>

In this project the goal is to analyse user activity data from a music streaming service called Sparkify. Users can upgrade, downgrade and cancel their subscription at any time. The goal of the project is to be able to predict which users are likely to cancel their subscription to be able to reach out to these customers with measures like promotions etc. To be able to perform the analysis and to build a model user activity log data is provided that logs user events with timestamp. The data is provided in three different sizes: small data sets for experimentation with how to use the data and how to build a good model. A large 12 GB dataset is provided to test the proposed steps on a realistic sized dataset as well as running the preprocessing and prediction on a cloud based cluster either on IBM Watson or AWS infrastructure.

### Project Motivation <a name = "motivation"></a>

To predict churn from user data is a very common topic for many different companies today. The use of logging and intelligent data analysis can enable machine learning models to predict which users are most likely to stop using the service which is very valuable to be able to reduce the number by using different measures. If this is successfully done the music streaming service in this case could increase the revenue significantly.

### Files Description <a name = "description"></a>

*Sparkify.ipynb* is the jupyter notebook the preprocessing, feature engineering, modelling and evaluation is preformed.
*Sparkify_AWS.ipynb* is the jupyter notebook the preprocessing, feature engineering, modelling and evaluation is preformed on the AWS Cluster.
*Sparkify_IBM_Waton.ipynb* is the jupyter notebook the preprocessing, feature engineering, modelling and evaluation is preformed on the IBM Watson Cluster.


### Software and Dependencies <a name = "dependencies"></a>

The project is implemented using Anaconda with Python3 and following libraries are used in this project:

*Pandas**<br>
*Matplotlib**<br>
*Seaborn**<br>
*PySpark**<br>

### Results <a name = "results"></a>

```Local machine (Mini dataset, 128 MB):
Gradient Boost Tree Classifier:
f1 score: 0.9298245614035088
accuracy: 0.9298245614035088
area under ROC: 0.8371428571428571
Random Forest Classifier:
f1 score: 0.9298245614035088
accuracy: 0.9246646026831785
area under ROC: 0.7757142857142857
Linear SVC
f1 score: 0.8771929824561403
accuracy: 0.8198065256599442
area under ROC: 0.5
IBM Watson (Medium dataset, 256 MB):
Gradient Boost Tree Classifier:
f1 score: 0.8918918918918919
accuracy: 0.8902609506057781
area under ROC: 0.8309302325581395
Random Forest Classifier:
f1 score: 0.8198198198198198
accuracy: 0.7691441441441441
area under ROC: 0.6
AWS (Full dataset, 12 GB):
Gradient Boost Tree Classifier:
f1 score: 0.7882438846294268
accuracy: 0.7085762138808424
area under ROC: 0.5226772841938998
Random Forest Classifier:
f1 score: 0.7853231106243155
accuracy: 0.6962696408305166
area under ROC: 0.5102765088380845
```

On the small data set these all get high evaluation metrics in terms of accuracy, f1 score and area und ROC. Gradient Boost Tree Classifier has slightly better results than Random Forest Classifier. Linear SVC has significantly lower f1 and accuracy. In general the size of the data set makes it difficult to evaluate the model which can be seen that all models have fairly high / good results.

On the larger data sets it can clearly be seen that using more data reduces the evaluation metrics to be of more realistic for this kind of problem. The trend that Gradient Boost Free Classifier performs the best for this problem is valid for all datasets.

Hyper-parameter optimisation did not manage to improve the results on any of the data sets.

For a more though analysis check out my blog post by clicking this [link](https://medium.com/@dan.gunnarsson/prediction-of-churn-using-pyspark-990221840ce0) for more detailed analysis.

### Acknowledgements <a name = "acknowledgements"></a>

Udacity for providing the project.
