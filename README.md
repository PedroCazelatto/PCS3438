# PCS3438 - Artificial Intelligence

Exercise list for PCS3438 - Artificial Intelligence (2022), an Electrical Engineering course at POLI-USP. Four supervised learning problems, each solved in a Jupyter notebook with pandas and scikit-learn. The questions are in [`Enunciado.pdf`](Enunciado.pdf) (in Portuguese).

| Question | Data | Model | Validation | Result |
|---|---|---|---|---|
| [1](question01.ipynb) | `class01.csv`: 1000 rows, 100 features, 10 classes | Gaussian Naive Bayes | Holdout: first 350 rows for training, the rest for validation | Validation accuracy: 0.628 |
| [2](question02.ipynb) | `class02.csv`: 1500 rows, 100 features, 6 classes | k-nearest neighbours, k = 10 | 5-fold cross-validation | Mean validation accuracy: 0.838 |
| [3](question03.ipynb) | `reg01.csv`: 1000 rows, 10 features | LASSO linear regression (L1, α = 1) | Leave-one-out | Mean RMSE: 19.22 on training, 15.47 on validation |
| [4](question04.ipynb) | `reg02.csv`: 1000 rows, 20 features | Regression tree, no pruning | 5-fold cross-validation | Mean validation MAE: 44.18; training MAE: 0.0 |

## Running

```
python3 -m pip install pandas scikit-learn jupyter
jupyter notebook
```

Question 3 uses `mean_squared_error(..., squared=False)`, which newer versions of scikit-learn no longer accept; it needs a version older than 1.6.
