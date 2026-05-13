High-Dimensional Cancer Classification on the ARCENE Dataset
Suman Gorkhali, Massogona Cisse, Kamal Mandava
2026-05-02
1. Introduction
2. Methodology
2.1 Data Description and Preprocessing
2.2 Dimensionality Reduction (PCA)
2.3 Classification Methods
2.4 Model Evaluation
3. Results
3.1 Data Summary and PCA
3.2 Individual Model Results
3.2.1 PCA + Logistic Regression
3.2.2 PCA + LDA
3.2.3 Bagging
3.2.4 Random Forest with Variable Importance
3.2.5 Guided Regularized Random Forest (GRRF)
3.3 Model Comparison
4. Discussion

   
**Introduction**
Mass spectrometry of patient sera has become a central tool in cancer screening research because it captures the relative abundance of thousands of protein fragments in a single assay. Profiles that distinguish cancerous from healthy tissue carry biological information about the disease state, and a classifier trained on those profiles offers the promise of an early, noninvasive screening rule. The ARCENE benchmark, released for the NIPS 2003 Feature Selection Challenge and distributed by the UCI Machine Learning Repository, encapsulates this problem in a 200-sample, 10,000-feature dataset that has become a standard testbed for high-dimensional cancer classification.

The dataset embodies the high-dimensional regime in which the number of predictors greatly exceeds the number of observations, typically written as p >> n. In this regime classical multivariate methods break down. Ordinary least squares has infinitely many solutions, the within-class covariance matrix needed by linear discriminant analysis is singular, and any unregularized model with as many parameters as features will fit noise rather than signal. The methods designed for this regime fall into a few broad families. Regularization shrinks coefficients toward zero so the model has effectively fewer parameters. Dimension reduction projects the data onto a low-dimensional subspace before fitting. Embedded feature selection identifies a small subset of predictors with predictive value and discards the rest. Our analysis evaluates methods drawn from each of these families.

Our research question is which of these approaches gives the most accurate and interpretable classification of cancer versus normal samples on ARCENE. We compare five methods: principal component analysis followed by logistic regression, principal component analysis followed by linear discriminant analysis, bagging, a random forest with variable importance, and a guided regularized random forest. Because a missed cancer diagnosis carries greater clinical cost than a false alarm, we prioritize sensitivity (the fraction of true cancer cases correctly identified) when ranking the methods, while still reporting specificity and overall error to characterize the full performance profile.

MORE in the 'arcene_report.html' (find in the folder)
