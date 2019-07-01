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

#### Steps
* Calculate distance
* Find closest neighbors
* Vote for labels

### Pros

* no underlying assumption for data distribution
* no need for training for model generation

### Cons

* testing is slower/costlier because its lazy (more data point to scan)
