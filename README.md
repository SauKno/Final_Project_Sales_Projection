# AutoML Leaderboard

| Best model   | name                                                         | model_type     | metric_type   |   metric_value |   train_time |
|:-------------|:-------------------------------------------------------------|:---------------|:--------------|---------------:|-------------:|
|              | [1_Baseline](1_Baseline/README.md)                           | Baseline       | logloss       |       0.586173 |         1.5  |
|              | [2_DecisionTree](2_DecisionTree/README.md)                   | Decision Tree  | logloss       |       0.579291 |         9.97 |
|              | [3_Linear](3_Linear/README.md)                               | Linear         | logloss       |       0.547193 |         4.58 |
|              | [4_Default_Xgboost](4_Default_Xgboost/README.md)             | Xgboost        | logloss       |       0.553613 |         7    |
|              | [5_Default_NeuralNetwork](5_Default_NeuralNetwork/README.md) | Neural Network | logloss       |       0.545319 |         2.63 |
|              | [6_Default_RandomForest](6_Default_RandomForest/README.md)   | Random Forest  | logloss       |       0.536756 |         7.78 |
| **the best** | [Ensemble](Ensemble/README.md)                               | Ensemble       | logloss       |       0.531047 |         0.8  |

### AutoML Performance
![AutoML Performance](ldb_performance.png)


### Features Importance
![features importance across models](features_heatmap.png)



### Spearman Correlation of Models
![models spearman correlation](correlation_heatmap.png)
