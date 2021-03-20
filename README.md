# Deep-Learing-Using-Tensorflow-from-Scratch

I have used Tensorflow 2.4.1

I have built few models:
  1.MLP for Binary Classification
  2.MLP for Multiclass Classification
  3.CNN
  4.RNN



5 step life cycle of a deep learning model
1.Define the model.
2.Compile the model.
3.Fit the model.
4.Evaluate the model.
5.Make predictions                                  

Defining the model
requires that you first select the type of model that you need and then choose the architecture or network topology. This involves defining the layers of the model, configuring each layer with a number of nodes and activation function, and connecting the layers together into a cohesive model.

Compiling_Model (model.compile())
requires that you first select a loss function that you want to optimize, such as mean squared error or cross-entropy.
It also requires that you select an algorithm to perform the optimization procedure, typically stochastic gradient descent, or a modern variation, such as Adam. It may also require that you select any performance metrics to keep track of during the model training process.
This involves calling a function to compile the model with the chosen configuration, which will prepare the appropriate data structures required for the efficient use of the model you have defined.
The optimizer can be specified as a string for a known optimizer class, e.g. ‘sgd‘ for stochastic gradient descent, or you can configure an instance of an optimizer class and use that.

The three most common loss functions are:
1.‘binary_crossentropy‘ for binary classification.
2.‘sparse_categorical_crossentropy‘ for multi-class classification.
3.‘mse‘ (mean squared error) for regression.

Fit the Model (model.fit())
Fitting the model requires that you first select the training configuration, such as the number of epochs (loops through the training dataset) and the batch size (number of samples in an epoch used to estimate model error).
Training applies the chosen optimization algorithm to minimize the chosen loss function and updates the model using the backpropagation of error algorithm.
While fitting the model, a progress bar will summarize the status of each epoch and the overall training process. This can be simplified to a simple report of model performance each epoch by setting the “verbose” argument to 2. All output can be turned off during training by setting “verbose” to 0.

Evaluate the Model (model.evaluate())
Evaluating the model requires that you first choose a holdout dataset used to evaluate the model. This should be data not used in the training process so that we can get an unbiased estimate of the performance of the model when making predictions on new data. The speed of model evaluation is proportional to the amount of data you want to use for the evaluation, although it is much faster than training as the model is not changed. From an API perspective, this involves calling a function with the holdout dataset and getting a loss and perhaps other metrics that can be reported.

Make a Prediction (model.predict())¶
It requires you have new data for which a prediction is required, e.g. where you do not have the target values. From an API perspective, you simply call a function to make a prediction of a class label, probability, or numerical value: whatever you designed your model to predict. You may want to save the model and later load it to make predictions. You may also choose to fit a model on all of the available data before you start using it.
