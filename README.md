<h1 align="center"> Stroke prediction </h1>

This repository contains an imbalanced supervised binary classification task: predicting patients that will have a stroke given sociological and biological factors, using the Kaggle dataset present in "https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset".

<h1 align="center"> Tools used </h1>
<p align="center"> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> <a href="https://numpy.org/" target="_blank" rel="noreferrer"> <img src="https://numpy.org/doc/stable/_static/numpylogo.svg" alt="numpy" width="100" height="40"/> </a> <a href="https://pandas.pydata.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/2ae2a900d2f041da66e950e4d48052658d850630/icons/pandas/pandas-original.svg" alt="pandas" width="40" height="40"/> </a> <a href="https://scikit-learn.org/" target="_blank" rel="noreferrer"> <img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" alt="scikit_learn" width="40" height="40"/> </a> <a href="https://seaborn.pydata.org/" target="_blank" rel="noreferrer"> <img src="https://seaborn.pydata.org/_images/logo-mark-lightbg.svg" alt="seaborn" width="40" height="40"/> </a> <a href="https://imbalanced-learn.org/stable/" target="_blank" rel="noreferrer"> <img src="https://imbalanced-learn.org/stable/_static/logo_wide.png" alt="imblearn" height="35"/> </a> <a href="https://optuna.org/" target="_blank" rel="noreferrer"> <img src="https://optuna.org/assets/img/optuna-logo.png" alt="optuna" height="35"/> </a> </p>

The main code is scattered across three notebooks:

<h1 align="center"> 1 - Exploratory data analysis </h1>

In the notebook `1-eda.ipynb`, I perform exploratory data analysis on the data:
- Check for missing values and data types
- Draw the blueprint for the data pipeline
- Perform univariate and bivariate data analysis

<h1 align="center"> 2 - Model selection and tuning </h1>

This notebook, `2-model.ipynb`, selects a model across many different classifiers and tunes the best selected classifiers using cross-validation.

The following approach is used:
- Creating a data pipeline
- Selecting the best models using cross-validation
- Performing cross-validaition hyperparameter tuning on the best models using the `optuna` package
- Saving the best model pipelines for later evaluation

<h1 align="center"> 3 - Model evaluation </h1>

Notebook `3-eval.ipynb` evaluates the tuned models from the previous notebook and benchmarks them across various different metrics on the test set.

The evaluation consists of the following steps:
- Accuracy, ROC AUC and F1 score
- Confusion matrix
- ROC curve
- Precision Recall curve
- True vs predicted distributions
- Threshold tuning using F1-score
