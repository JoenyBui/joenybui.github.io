---
---

# Clustering

## KNN (k-Nearest Neighbor)
### Summary
Non-parameteric (does not assume a distribution) and lazy learning algorithms (no training needed).

KNN is  where K is the number of the nearest neighbors.  The number of cluster is the deciding factor.
Certain distance measurements are:
* Euclidean distance
* Hamming distance
* Minkowski distance

Eager learners will construct a generalized model before performing prediction.
Lazy learner will model when data is calculated.

#### Curse fo Dimensionality

KNN performs better with *lower number of features*.  As number of features increases then more data is needed and is prone to overfitting.  PCA or feature selection approach is *recommended*.

#### Steps
* Calculate distance
* Find closest neighbors
* Vote for labels

### Pros

* no underlying assumption for data distribution
* no need for training for model generation

### Cons

* testing is slower/costlier because its lazy (more data point to scan)
