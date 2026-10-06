## Model Performance Limitation

The Random Forest produced:

- Accuracy: **50%**
- Precision: **100%**
- Recall: **50%**
- F1 Score: **0.67**

These results should be interpreted cautiously because the open-source E-mini S&P 500 sample is very small and covers only a few days.

After volatility estimation, CUSUM filtering, vertical-barrier construction, and triple-barrier labeling, only a small number of valid observations remained for training and testing.

The test set contained only **4 observations**, so the evaluation is not statistically reliable.

The poor performance is therefore mainly attributed to **insufficient data**, rather than the meta-labeling framework itself.

A longer contract-level futures dataset would be required for a more meaningful model evaluation.