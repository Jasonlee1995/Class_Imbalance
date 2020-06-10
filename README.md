# Class Imbalance


## Major Field Suffer from Class Imbalance
- Medical Diagnosis
- Fraud Detection
- Network Intrusion Detection
- Fault Monitoring


## Characteristic of Imbalanced Data
- Overlapping small disjuncts
- Lack of density
- Noise
- Dataset shift


## Evaluation Metrics
- Purpose : monitor classification performance on each individual class
  * Sensitivity (True Positive Rate)
  * Specificity (True Negative Rate)
- Purpose : interested in high performance on only one class
  * Precision
- Purpose : performance on majority and minority classes needed to be high
  * G-mean (Geometric-mean)
  * F-measure
- Purpose : visualize and summarize the performance of classifier based on trade off between true positive rate and false positive rate
  * ROC curve and AUC (Receiver Operating Characteristic curve and Area Under Curve)
- Purpose : metrics for cost sensitive classifiers which measure cost misclassifying errors
  * cost matrix
  * cost curve


## Categories for Solving Class Imbalance
- Data Pre-processing Approach (Sampling)
- Algorithmic Approach
- Combination : Sampling + Algorithm (e.g. sampling + boosting)
- Feature Selection Approach
/////
- Sampling Methods
- Cost Sensitive Learning
- Recognition Based Methods
- Ensemble Based Methods


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
- A Review on Class Imbalance Problem: Analysis and Potential Solutions [[paper]](https://www.ijcsi.org/papers/IJCSI-14-6-43-51.pdf)
- Data Imbalance: Effects and Solutions for Classification of Large and Highly Imbalanced Data [[paper]](https://www.researchgate.net/publication/320895020_Data_Imbalance_Effects_and_Solutions_for_Classification_of_Large_and_Highly_Imbalanced_Data)
- Class Imbalance Problem in Data Mining: Review [[paper]](https://arxiv.org/pdf/1305.1707.pdf)
- A Review of Class Imbalance Problem [[paper]](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.478.2298&rep=rep1&type=pdf)
