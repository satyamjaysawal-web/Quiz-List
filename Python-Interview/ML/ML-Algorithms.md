




---
---


Scikit-Learn provides a rich collection of machine learning algorithms, grouped into several categories. Here’s a comprehensive list of them:

---

### 1. **Linear Models**
   - **Linear Regression**: Ordinary least squares for regression.
   - **Ridge Regression**: Linear regression with L2 regularization.
   - **Lasso Regression**: Linear regression with L1 regularization.
   - **ElasticNet**: Combines L1 and L2 regularization.
   - **Logistic Regression**: For binary and multi-class classification.
   - **SGDClassifier**: Stochastic Gradient Descent classifier for large datasets.
   - **SGDRegressor**: Stochastic Gradient Descent regressor for large datasets.
   - **Perceptron**: Basic linear classifier.
   - **PassiveAggressiveClassifier**: For online learning, adjusts only when it misclassifies.
   - **BayesianRidge**: Bayesian approach to linear regression.
   - **ARDRegression**: Automatic Relevance Determination regression.
   - **HuberRegressor**: Robust to outliers in regression.
   - **RANSACRegressor**: Robust linear regression model for outlier data.

---

### 2. **Support Vector Machines (SVM)**
   - **SVC (Support Vector Classifier)**: C-Support Vector Classification.
   - **SVR (Support Vector Regression)**: Epsilon-Support Vector Regression.
   - **NuSVC**: Nu-Support Vector Classification, alternative SVM formulation.
   - **NuSVR**: Nu-Support Vector Regression.
   - **LinearSVC**: Linear kernel SVM for classification.
   - **LinearSVR**: Linear kernel SVM for regression.

---

### 3. **Nearest Neighbors**
   - **KNeighborsClassifier**: K-Nearest Neighbors classifier.
   - **KNeighborsRegressor**: K-Nearest Neighbors regressor.
   - **RadiusNeighborsClassifier**: Classification based on neighbors within a fixed radius.
   - **RadiusNeighborsRegressor**: Regression based on neighbors within a fixed radius.
   - **NearestCentroid**: Classifier using the centroid of each class.
   - **BallTree / KDTree**: Data structures to support nearest neighbor searches.

---

### 4. **Decision Trees and Ensembles**
   - **DecisionTreeClassifier**: Decision tree classifier.
   - **DecisionTreeRegressor**: Decision tree regressor.
   - **RandomForestClassifier**: Ensemble of decision trees (classification).
   - **RandomForestRegressor**: Ensemble of decision trees (regression).
   - **ExtraTreesClassifier**: Ensemble with randomly chosen splits (classification).
   - **ExtraTreesRegressor**: Ensemble with randomly chosen splits (regression).
   - **GradientBoostingClassifier**: Gradient boosting for classification.
   - **GradientBoostingRegressor**: Gradient boosting for regression.
   - **AdaBoostClassifier**: Adaptive boosting for classification.
   - **AdaBoostRegressor**: Adaptive boosting for regression.
   - **VotingClassifier**: Combines multiple classifiers with voting.
   - **VotingRegressor**: Combines multiple regressors with averaging.
   - **BaggingClassifier**: Bagging for classification.
   - **BaggingRegressor**: Bagging for regression.
   - **StackingClassifier**: Combines multiple classifiers with meta-learner.
   - **StackingRegressor**: Combines multiple regressors with meta-learner.

---

### 5. **Bayesian Methods**
   - **GaussianNB**: Gaussian Naive Bayes.
   - **MultinomialNB**: Multinomial Naive Bayes, suitable for text.
   - **BernoulliNB**: Bernoulli Naive Bayes, for binary features.
   - **ComplementNB**: Naive Bayes variant for imbalanced data.

---

### 6. **Clustering Algorithms**
   - **KMeans**: K-means clustering.
   - **MiniBatchKMeans**: Faster variant of K-means.
   - **AgglomerativeClustering**: Hierarchical agglomerative clustering.
   - **DBSCAN**: Density-Based Spatial Clustering.
   - **MeanShift**: Clustering by finding dense areas in feature space.
   - **SpectralClustering**: Graph-based clustering for complex structures.
   - **OPTICS**: Ordering points to identify clustering structure.
   - **Birch**: Clustering method for large datasets.

---

### 7. **Gaussian Processes**
   - **GaussianProcessClassifier**: Gaussian process classification.
   - **GaussianProcessRegressor**: Gaussian process regression.

---

### 8. **Neural Networks**
   - **MLPClassifier**: Multi-layer Perceptron for classification.
   - **MLPRegressor**: Multi-layer Perceptron for regression.

---

### 9. **Cross-Validation Based Models**
   - **GridSearchCV**: Exhaustive search over specified parameter values.
   - **RandomizedSearchCV**: Randomized search over parameters.
   - **HalvingGridSearchCV**: Successive halving with grid search.
   - **HalvingRandomSearchCV**: Successive halving with random search.

---

### 10. **Semi-Supervised Learning**
   - **LabelPropagation**: Propagates labels in a graph using nearest neighbors.
   - **LabelSpreading**: Similar to LabelPropagation with different propagation rule.

---

### 11. **Calibration** (`sklearn.calibration`)
   - **CalibratedClassifierCV**: Calibration of probability for classifiers (e.g., Platt scaling, isotonic regression).

---

### 12. **Ensemble Meta-Estimators**
   - **VotingClassifier**: Hard or soft voting ensemble for classification.
   - **VotingRegressor**: Combines multiple regressors using averaging.
   - **StackingClassifier**: Stacks multiple classifiers with a meta-classifier.
   - **StackingRegressor**: Stacks multiple regressors with a meta-regressor.

---

### 13. **Anomaly Detection**
   - **OneClassSVM**: One-Class SVM for outlier detection.
   - **IsolationForest**: Forest-based model for anomaly detection.
   - **LocalOutlierFactor (LOF)**: Unsupervised outlier detection.
   - **EllipticEnvelope**: Robust covariance estimate for anomaly detection.

---

### 14. **Dimensionality Reduction**
   - **PCA (Principal Component Analysis)**: Linear dimensionality reduction.
   - **KernelPCA**: Non-linear dimensionality reduction with kernels.
   - **TruncatedSVD**: SVD for sparse matrices.
   - **FactorAnalysis**: Linear transformation for factor analysis.
   - **FastICA (Independent Component Analysis)**: Finds independent components in the data.
   - **LatentDirichletAllocation (LDA)**: Topic modeling.

---

### 15. **Manifold Learning**
   - **Isomap**: Manifold learning for high-dimensional data.
   - **LocallyLinearEmbedding (LLE)**: Manifold learning with linear embedding.
   - **MDS (Multi-dimensional Scaling)**: Projects data into lower-dimensional space.
   - **SpectralEmbedding**: Non-linear dimensionality reduction.
   - **t-SNE (t-Distributed Stochastic Neighbor Embedding)**: Visualizes high-dimensional data.

---




---
---
