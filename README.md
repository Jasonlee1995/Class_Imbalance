# Class Imbalance


## Major Field Suffer from Class Imbalance
- Medical Diagnosis Prediction
- Fraud Detection in Banking Operations
- Detection in Network Intrusions
- Manage Risk and Predict Failures of Technical Equipment


## Categories for Solving Class Imbalance
- Data Pre-processing Approach (Sampling)
- Algorithmic Approach
- Combination : Sampling + Algorithm (sampling + boosting)
- Feature Selection Approach


# Metric
- Geometric mean score (G-mean score)


## Data Pre-processing Approach (Sampling)
- Sampling : Solve the problems with distribution of data
- Artificially re-sampling the dataset
* Under-sampling : Remove samples of majority class
  * Random Under-sampling
    * Randomly remove majority class sample
    * Cons : Loss of valuable information
 * Over-sampling : Add new samples of minority class
   * Random Over-sampling
     * Randomly replicate minority class sample
     * Cons : Reuse data
   * Synthetic Minority Oversampling Technique (SMOTE)
     * Generates synthetic minority examples
     * Cons : Learning process consume more time
* Clustering-sampling
* Combination : Over-sampling + Under-sampling

## Algorithmic Approach
- One-class Learning Method
  * Recognize the sample belongs to that class and reject others
- Instated of changing class distribution applying cost in decision making
- Cost-sensitive Method
  * Shift the bias to favor the minority class
  * Minimize the cost of misclassification, which can be realized by choosing the class with the minimum conditional risk
  * Cost matrix based on data and apply to learning stage
  * Sampling + threshold-moving method
- Modifying Classifier
 * Infinitely imbalanced logistic regression (IILR)
   * Pros : Mostly used for binary classification
   * Cons : Performance is depends on number of outlier in data
- Recognition-based Approaches
- Kernel-based Learning
 * Map imbalance dataset into higher dimension space
 * e.g. Support Vector Machine (SVM), Radial Basis Function, Boosting Method + SVM
 * Linear Proximal Support Vector Machines (LPSVM)
   * Pros : Handle dynamic class imbalance problem
   * Cons : No consideration for distribution of sample
 * BoostingSVM
   * Pros : Improved the performance of SVM classifier for prediction minority sample
   * Cons : Ignore imbalance class distribution.
- Boosting Method
 * AdaBoost.NC
   * Pros : Improve prediction accuracy of minority
   * Cons : Ignore overall performance of classifier
 * RUSBoost : hybrid sampling + boosting
   * Pros : Simple, faster and less complex than SMOTE Boost algorithm
   * Cons : Unable to solve multiclass imbalance problem


## Feature Selection
- Select subset of features that allows a classifier to reach optimal performance

## Reference
- Class Imbalance Problem in Data Mining: Review [[paper]](https://arxiv.org/pdf/1305.1707.pdf)
