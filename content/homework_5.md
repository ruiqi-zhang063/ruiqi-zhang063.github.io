Title: Homework 5 Explanation
Date: 11/15/2021   
Author: Ruiqi Zhang  
Slug: Homework 5
Category: Homework 5

# Homework 5 - Dive into Deep Learning

#### Library Version

In this assignment, the version of tensorflow is 2.5.0, new version of tensorflow may casue some problems. 

#### Model Training
For convenience, we use relative simple model with only one convolutional layer and pooling layer. This model can be trained quickly and has a hign accuracy in testing dataset. In training dataset, we keep 20% data as a validation dataset. After training model, we plot the training history of loss and accuracy. 

The results have 99% accuracy in the test dataset. Consider the model is simple and the dataset is not very large, the accuaracy is a bit too high. Therefore, we want to see how the model works.

#### Model Explanation
Predictions for two input images are explained in the plot. Red pixels represent positive SHAP values that increase the probability of the class, while blue pixels represent negative SHAP values the reduce the probability of the class.

We can see that the main basis for classification is the numbers in the lower right corner. Since the results on the test set are still very accurate, it means that the numbers in the lower right corner may have some regularity, which makes classification easier. Besides the numbers in the lower right corner, dragonfly wings and the shape of the cockroach are also used for classification.
