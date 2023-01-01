# Report: Predict Bike Sharing Demand with AutoGluon Solution

#### JUDE BOACHIE

## Initial Training

### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?

The predictions had negative values. Kaggle rejects submissions containing negative values. I converted the negative values to zero.


### What was the top ranked model that performed?

Weighted_Ensemble_L3

## Exploratory data analysis and feature creation

### What did the exploratory analysis find and how did you add additional features?

Found out I could extract the day, month, year, hour etc from the datetime feature. I added the "hour" feature.

### How much better did your model preform after adding additional features and why do you think that is?

It actually didn't perform any better. Will try using other synthetic features.

## Hyper parameter tuning

### How much better did your model preform after trying different hyper parameters?

The model performed much better (kaggle score difference of more than 1)

### If you were given more time with this dataset, where do you think you would spend more time?

Feature engineering and Hyperparameter optimization

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.

|    model   |    hpo1     |hpo2         |hpo3      |score  |
|------------|-------------|-------------|----------|-------|
|initial     |time_limit   |preset       |num_gpus  |1.8271 |
|add_features|time_limit   |preset       |num_gpus  |1.8271 |
|hpo         |num_gpus     |learning_rate|num_trials|0.50347|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project

TODO: Replace the image below with your own.

![model_test_score.png](/project/img/model_test_score.png)

## Summary

The model performs OK with the default parameters. When new features are added to the data, the model performs
better(although not always). Furthermore, the model could be improved by tuning some of its hyperparameters.
This was show in the graph.
