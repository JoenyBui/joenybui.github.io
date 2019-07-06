---
layout: post
author: Joeny Bui
reference: "Feature Engineering for Machine Learning"
---

# Feature Engineering

* the act of extrating features from raw data and transforming them into formats that are suitable for mL
* data always have measurement noise and missing pieces
* ml involves two mathematical entities: models and features
* frequent characteristics of such as wrong, redundant, or missing
* a feature is not a numerical representation of data
* in ML, we pick not only the model, but also the features - it's a dobule-jointed lever where one affects the other

## Fancy Trick with Simple Numbers

* First question to ask for numeric data is whether the magnitude matters? Positive or negative?
* Scale - min and max
* Models that are smooth functions of input features are sensitive to the scale
* Consider normalizing the features for: k-mean clustering, nearest neighbors methods, radial basis function (RBF) kernels, and anything that uses the Euclidean distance
* Logical functions are not sensitive to input feature scale (binary) 
* Models based on space-partitioning trees are not sensitive to scale: decision tree, gradient boosted machines, random forests
* 