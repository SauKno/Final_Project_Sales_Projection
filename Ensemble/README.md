# Summary of Ensemble

[<< Go back](../README.md)


## Ensemble structure
| Model                   |   Weight |
|:------------------------|---------:|
| 1_Baseline              |        1 |
| 5_Default_NeuralNetwork |        2 |
| 6_Default_RandomForest  |        3 |

## Metric details
|           |    score |   threshold |
|:----------|---------:|------------:|
| logloss   | 0.531047 |  nan        |
| auc       | 0.703746 |  nan        |
| f1        | 0.845238 |    0.504588 |
| accuracy  | 0.748792 |    0.51512  |
| precision | 0.964286 |    0.873373 |
| recall    | 1        |    0.21927  |
| mcc       | 0.296124 |    0.718021 |


## Metric details with threshold from accuracy metric
|           |    score |   threshold |
|:----------|---------:|------------:|
| logloss   | 0.531047 |   nan       |
| auc       | 0.703746 |   nan       |
| f1        | 0.844776 |     0.51512 |
| accuracy  | 0.748792 |     0.51512 |
| precision | 0.766938 |     0.51512 |
| recall    | 0.940199 |     0.51512 |
| mcc       | 0.256383 |     0.51512 |


## Confusion matrix (at threshold=0.51512)
|              |   Predicted as 0 |   Predicted as 1 |
|:-------------|-----------------:|-----------------:|
| Labeled as 0 |               27 |               86 |
| Labeled as 1 |               18 |              283 |

## Learning curves
![Learning curves](learning_curves.png)
## Confusion Matrix

![Confusion Matrix](confusion_matrix.png)


## Normalized Confusion Matrix

![Normalized Confusion Matrix](confusion_matrix_normalized.png)


## ROC Curve

![ROC Curve](roc_curve.png)


## Kolmogorov-Smirnov Statistic

![Kolmogorov-Smirnov Statistic](ks_statistic.png)


## Precision-Recall Curve

![Precision-Recall Curve](precision_recall_curve.png)


## Calibration Curve

![Calibration Curve](calibration_curve_curve.png)


## Cumulative Gains Curve

![Cumulative Gains Curve](cumulative_gains_curve.png)


## Lift Curve

![Lift Curve](lift_curve.png)



[<< Go back](../README.md)
