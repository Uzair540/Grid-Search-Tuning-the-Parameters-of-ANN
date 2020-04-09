# Grid-Search-Tuning-the-Parameters-of-ANN
## Implementing Deep Learning Algorithm of Tuning the Parameters of ANN
### How to Use Grid Search in scikit-learn
##### Grid search is a model hyperparameter optimization technique.

In scikit-learn this technique is provided in the GridSearchCV class.

When constructing this class you must provide a dictionary of hyperparameters to evaluate in the param_grid argument. This is a map of the model parameter name and an array of values to try.

By default, accuracy is the score that is optimized, but other scores can be specified in the score argument of the GridSearchCV constructor.

By default, the grid search will only use one thread. By setting the n_jobs argument in the GridSearchCV constructor to -1, the process will use all cores on your machine. Depending on your Keras backend, this may interfere with the main neural network training process.

The GridSearchCV process will then construct and evaluate one model for each combination of parameters. Cross validation is used to evaluate each individual model and the default of 3-fold cross validation is used, although this can be overridden by specifying the cv argument to the GridSearchCV constructor.
