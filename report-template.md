# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Motunrayo Ibiyo

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
TODO: I did not encounter any difficulty when I submitted my predictions. As was instructed I changed all negatives to zero and I was fine

### What was the top ranked model that performed?
TODO: 

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
TODO: I added two other features obtained from the datetime features. this two features includes the day of the week and the period of the day(i.e morning. afternoon etc)

### How much better did your model preform after adding additional features and why do you think that is?
TODO: Training the model with the new features improved the performance of the model grately. Better result was also obtained when the datetime colum was dropped after adding those features

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
The model performed a bit better after trying out a different hyperparameter. However, I observed the values for the **kwargs I used seemed to make the performance low. Therefore I used only hyperparameters and removed the *kwargs

### If you were given more time with this dataset, where do you think you would spend more time?
TODO: With more time I will actually do more explorative data analysis on the data. Finding more correllation between the features (single and multiple) and the count would be the focus. Rather than using just Histogram, I would love to use box and swarm plots to understand the data beter

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|timelimit|preset|hyperparameter|score|
|--|--|--|--|--|
|initial|600|best_quality|Default|1.39454|
|add_features|600|best_quality|Default|0.48293|
|hpo|1200|best_quality|NN,XGB,LR,RF|0.44125|


### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](img/model_test_score.png)
## Summary
TODO: 
The project was to predict the demand for bicycles in Capital Bikeshare program in Washington, D.C.The features considerd were humnidity, season, holidays, Working day, weather, temperature and others. To add to these, I generated three other features hour, period of the day i.e morning, afternoon etc,  and day of the week. This features were all obtained from the date time feature which should be dropped as specificity of the detail can be misleading leading to an overfitted model.

The performance of the model root mean squared reduced by almost a half -115 after new features were added and the date time feature were removed to a new score of about -57.38. Setting the hyperparameters for the algorithm the atogluon would use increased the performance, but was not as remarkable as expected. The Kaggle Score moved from 1.39454 to 0.48293 then 0.44125.
