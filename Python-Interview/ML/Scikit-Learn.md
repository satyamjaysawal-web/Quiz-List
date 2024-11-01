




---
---

Scikit-Learn has a rich ecosystem of libraries (modules) for various machine learning tasks. Here is a categorized list of these main libraries in Scikit-Learn.

---

### 1. **Datasets** (`sklearn.datasets`)
   - **datasets.load_iris**: Loads the Iris dataset
   - **datasets.load_digits**: Loads the Digits dataset
   - **datasets.load_boston**: Loads the Boston Housing dataset (deprecated)
   - **datasets.load_wine**: Loads the Wine dataset
   - **datasets.load_breast_cancer**: Loads the Breast Cancer dataset
   - **datasets.make_classification**: Generates a random classification dataset
   - **datasets.make_regression**: Generates a random regression dataset
   - **datasets.fetch_openml**: Fetches datasets from OpenML
   - **datasets.fetch_california_housing**: Fetches California Housing dataset

### 2. **Model Selection** (`sklearn.model_selection`)
   - **train_test_split**: Splits data into train and test sets
   - **cross_val_score**: Computes cross-validation scores
   - **GridSearchCV**: Exhaustive search over specified parameter values for an estimator
   - **RandomizedSearchCV**: Randomized search over parameters for an estimator
   - **KFold, StratifiedKFold**: K-Folds and Stratified K-Folds cross-validator
   - **TimeSeriesSplit**: Cross-validation for time series data

### 3. **Preprocessing** (`sklearn.preprocessing`)
   - **StandardScaler**: Standardizes features by removing the mean and scaling to unit variance
   - **MinMaxScaler**: Scales features to a given range (usually [0, 1])
   - **RobustScaler**: Scales features using statistics that are robust to outliers
   - **Normalizer**: Scales individual samples to have unit norm
   - **Binarizer**: Binarizes data (set feature values to 0 or 1) based on a threshold
   - **PolynomialFeatures**: Generates polynomial and interaction features
   - **OneHotEncoder**: Encodes categorical features as a one-hot numeric array
   - **LabelEncoder**: Encodes target labels with value between 0 and n_classes-1

### 4. **Feature Selection** (`sklearn.feature_selection`)
   - **SelectKBest**: Select features according to the k highest scores
   - **SelectPercentile**: Select features based on percentile of the highest scores
   - **RFE (Recursive Feature Elimination)**: Recursive feature elimination
   - **RFECV**: Recursive feature elimination with cross-validation
   - **VarianceThreshold**: Removes features with low variance

### 5. **Decomposition** (`sklearn.decomposition`)
   - **PCA (Principal Component Analysis)**: Linear dimensionality reduction using SVD
   - **KernelPCA**: Kernel Principal Component Analysis
   - **NMF (Non-negative Matrix Factorization)**: Factorization method where data and factors are non-negative
   - **TruncatedSVD**: Dimensionality reduction using truncated SVD (for sparse matrices)
   - **FastICA (Independent Component Analysis)**: Separates a multivariate signal into additive, independent components

### 6. **Ensemble Methods** (`sklearn.ensemble`)
   - **RandomForestClassifier/RandomForestRegressor**: Random Forest models for classification and regression
   - **GradientBoostingClassifier/GradientBoostingRegressor**: Gradient Boosting models
   - **AdaBoostClassifier/AdaBoostRegressor**: Adaptive Boosting models
   - **BaggingClassifier/BaggingRegressor**: Ensemble of models for improved performance
   - **VotingClassifier/VotingRegressor**: Ensemble that averages predictions of multiple models
   - **StackingClassifier/StackingRegressor**: Meta-estimator that stacks several individual models

### 7. **Linear Models** (`sklearn.linear_model`)
   - **LinearRegression**: Ordinary least squares linear regression
   - **Ridge**: Ridge regression (L2 regularization)
   - **Lasso**: Lasso regression (L1 regularization)
   - **ElasticNet**: Linear regression with combined L1 and L2 regularization
   - **LogisticRegression**: Logistic regression classifier
   - **SGDClassifier/SGDRegressor**: Linear classifiers and regressors with stochastic gradient descent
   - **Perceptron**: Linear classification using the perceptron algorithm

### 8. **Support Vector Machines** (`sklearn.svm`)
   - **SVC (Support Vector Classifier)**: C-Support Vector Classification
   - **SVR (Support Vector Regression)**: Epsilon-Support Vector Regression
   - **LinearSVC**: Linear Support Vector Classification
   - **LinearSVR**: Linear Support Vector Regression
   - **NuSVC/NuSVR**: Nu-Support Vector Classification and Regression

### 9. **Decision Trees** (`sklearn.tree`)
   - **DecisionTreeClassifier**: Decision Tree for classification tasks
   - **DecisionTreeRegressor**: Decision Tree for regression tasks
   - **export_graphviz**: Exports decision trees in DOT format for visualization

### 10. **Neighbors** (`sklearn.neighbors`)
   - **KNeighborsClassifier/KNeighborsRegressor**: K-nearest neighbors for classification and regression
   - **NearestNeighbors**: Finds nearest neighbors in data
   - **RadiusNeighborsClassifier/RadiusNeighborsRegressor**: Classification and regression based on neighbors within a fixed radius

### 11. **Naive Bayes** (`sklearn.naive_bayes`)
   - **GaussianNB**: Gaussian Naive Bayes classifier
   - **MultinomialNB**: Naive Bayes classifier for multinomial models (e.g., text data)
   - **BernoulliNB**: Naive Bayes classifier for binary/boolean features

### 12. **Clustering** (`sklearn.cluster`)
   - **KMeans**: K-means clustering
   - **AgglomerativeClustering**: Hierarchical clustering
   - **DBSCAN**: Density-Based Spatial Clustering of Applications with Noise
   - **MeanShift**: Clustering by finding dense regions
   - **SpectralClustering**: Clustering using graph-based spectral methods

### 13. **Gaussian Processes** (`sklearn.gaussian_process`)
   - **GaussianProcessClassifier**: Gaussian process-based classifier
   - **GaussianProcessRegressor**: Gaussian process-based regressor

### 14. **Metrics** (`sklearn.metrics`)
   - **classification_report**: Summarizes precision, recall, F1-score, etc.
   - **confusion_matrix**: Confusion matrix for classification tasks
   - **accuracy_score, precision_score, recall_score, f1_score**: Classification metrics
   - **mean_squared_error, mean_absolute_error**: Regression metrics
   - **roc_auc_score**: ROC AUC score for binary classifiers
   - **r2_score**: R-squared score for regression

### 15. **Pipeline** (`sklearn.pipeline`)
   - **Pipeline**: Chains multiple steps into a single, sequential pipeline
   - **FeatureUnion**: Combines multiple transformer objects

### 16. **Impute Missing Values** (`sklearn.impute`)
   - **SimpleImputer**: Imputes missing values using a constant or strategy like mean, median
   - **KNNImputer**: Imputes missing values using k-nearest neighbors

### 17. **Neural Network** (`sklearn.neural_network`)
   - **MLPClassifier**: Multi-layer Perceptron classifier
   - **MLPRegressor**: Multi-layer Perceptron regressor

### 18. **Calibration** (`sklearn.calibration`)
   - **CalibratedClassifierCV**: Probability calibration for classifiers

---




---
---
