![California_Nanobelka](images/California_Housing.jpg)
# [Median house value prediction – pySpark pipeline](https://nbviewer.jupyter.org/github/Nanobelka/california-housing/blob/main/california_housing.ipynb)

**Purpose**

To train a linear regression model to predict the median cost of housing in a particular area.  
Metrics for model evaluation: R2, RMSE, MAE.

**Input**

Housing data in California in 1990 grouped by borough.

**Tasks:**

- use pySpark and MLlib for solution;
- divide the data into train and test samples;
- for numerical features apply:
    - scaling;
    - polynomial expansion;
- for categorical features apply:
    - one hot encoding;
    - clustering based on some numerical features;
- apply random grid search for tuning of hyperparameters;
- select best hyperparameters on cross-validation;
- combine all steps into pipeline;
- create 2 models:
    - using all available source features;
    - using only numerical source features.
- evaluate the metrics of the created models:
    - for cross-validation;
    - on test samples.


### Contents

    0  Intro
    1  Initial
        1.1  Imports
        1.2  Constants
        1.3  Functions
        1.4  Settings
    2  Spark session open
    3  Read and Check data
        3.1  Read data
        3.2  First look at data
    4  Preprocessing
        4.1  Drop features
        4.2  Missing values
        4.3  New calculated features
        4.4  Target and Feature lists (categorical and numerical)
        4.5  Split data for train and test
    5  Stages for pipeline
        5.1  Numerical features
            5.1.1  Initial num vector
            5.1.2  Scaler
            5.1.3  PolynomialExpansion
        5.2  Categoriacal features
            5.2.1  One hot encoding
            5.2.2  K-Means clustering
            5.2.3  VectorAssembler for categoriacal features
        5.3  Final VectorAssembler
        5.4  Crossvalidation
    6  Modeling
        6.1  Pipeline
        6.2  Fit pipelines
        6.3  Best models
    7  Results
        7.1  Prediction
        7.2  Model summary
        7.3  Metrics with test data
    8  Conclusion
        8.1  Brief overview of the work carried out
        8.2  Main part
            8.2.1  Data checking
            8.2.2  Preparing data for models
            8.2.3  Pipeline
            8.2.4  Result
        8.3  Recommendations and risks
