# grid_search_cv_tutorial

This notebook intends to explain the effects of hyperparametric optimization on model's performance.

## Hyperparametric Optimization

Hyperparameters are those parameters of a model, which can't be found out during training of our model. They are not directly learned within the estimator. In scikit-learn they are passed as arguments to the constructor of the estimator classes. Typical examples include `C`, `kernel` and `gamma` for Support Vector Classifier, `alpha` for Lasso, `max_depth` and `min_samples_leaf` in decision tress etc.

The choice of hyperparameters can greatly influence model predictions. In scikit-learn, if we simply train a model, without passing the values of these hyperparameters, the model is trained on the default values. But, to improve model accuracy and to make our model robust, we must find the optimal values of the hyperparameters. 

One way to find the optimal hyperparameters is to train our model on different values of these hyperparameters and check accuracy on the validation set. In case of multiple hyperparameters, we need to make a grid having different values at each node as shown in the diagram below.

![grid_seacrh_pic.png](images/Capture.JPG)

The validation error is calculated by testing model accuracy on the validation set after training it on training set using each combination of hyperparameters. To understand training, validation and testing errors, [please follow this link](https://datamaniac.tech/data_science/understanding-training-testing-and-validation-errors/).

## Scikit-Learn Implementation

Sklearn provides us a method to perform above grid operations easily using grid_search_cv. We will look at its implementation in this notebook. View this notebook on [Kaggle](https://www.kaggle.com/prasun2106/steps-for-hyperparametric-optimization)
