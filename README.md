## Stroke Prediction

This repository encompasses a classification task for predicting stroke occurences on people based on some sociological and biological factors, using the Kaggle dataset present in "https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset".

This repository showcases many skills necessary to tackle this kind of problem:
- `1-eda.ipynb`: exploratory data analysis to understand the data, its features and their relationship. An important step to both understand the dataset and how to properly construct a data pipeline from it.

- `2-model.ipynb`: creating a data pipeline and performing model selection using cross validation (while dealing with the dataset imbalance). After the model selection stage, hyperparameter tuning is applied to choose optimal parameters from the selected models. Afterwards, the best models with the best parameters (together with their data pipelines) are trained on the whole training set and saved for later inference use or for re-training purposes. 

- `3-eval.ipynb`: evaluating the models trained in the previous notebook under a wide range of different metrics, taking into account the dataset imbalance. Threshold tuning via F1 score is performed using a Precision-Recall curve. Finally, a comparison is made between predicted vs true distributions.
