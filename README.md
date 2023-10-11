![California_Nanobelka](images/California_Housing.jpg)
# [Median house value prediction – pySpark pipeline](https://nbviewer.jupyter.org/github/Nanobelka/california-housing/blob/main/california_housing.ipynb)
##### Project for [Yandex.Praktikum](https://github.com/Nanobelka/Yandex_Praktikum)

### **Purpose**

To train a linear regression model to predict the median cost of housing in a particular area.  
Metrics for model evaluation: R2, RMSE, MAE.

### **Input**

Housing data in California in 1990 grouped by borough.

### **Tasks:**

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

### Visualization examples

Median house value

![Median house value](https://github.com/Nanobelka/california-housing/blob/main/images/example_1_median_house_value.png)

Median house value by clusters

![median_house_value_income_clusters](https://github.com/Nanobelka/california-housing/blob/main/images/example_2a_median_house_value_income_clusters.png)

![median_house_value_income_clusters](https://github.com/Nanobelka/california-housing/blob/main/images/example_2b_median_house_value_income_clusters.png)

map_geographical_clusters

![Динамика метрик при обучении нейронной сети](https://github.com/Nanobelka/california-housing/blob/main/images/example_3_map_geographical_clusters.png)
