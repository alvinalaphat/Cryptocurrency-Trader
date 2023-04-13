Luke worked on cleaning the data to feed into the model and ran it through testing with the model architecture. Alvin worked on testing the model with the validation/test data and then tweaked parameters to experiment what performed best with the model. 

Building a cryptocurrency trading algorithm with price prediction is a challenging task due to the high volatility and non-linearity of the cryptocurrency market. In this report, we propose a neural network architecture for predicting the price of a cryptocurrency based on historical price data. The goal is to achieve a high classification accuracy on the training and validation sets and improve the generalization capabilities of the model.

Neural Network Architecture: We propose a deep neural network architecture consisting of four layers: two dense layers with 128 and 128 units, respectively, followed by a dropout layer with a rate of 0.2 and a final dense layer with a single output unit. We use the Rectified Linear Unit (ReLU) activation function for the hidden layers and a linear activation function for the output layer. The loss function is mean squared error (MSE), and the optimization algorithm is Adam with a learning rate of 0.001.

Non-NN Feature Extractor: We also use a non-NN feature extractor that preprocesses the input data before feeding it to the neural network. The feature extractor includes the following steps:
1. Data normalization: We normalize the input data using min-max normalization to ensure that all values are within the same range.
2. Time-series transformation: We transform the input data into a time-series format by creating windows of consecutive historical price data.
3. Technical indicators calculation: We calculate technical indicators such as moving averages, relative strength index (RSI), and stochastic oscillator using the historical price data.
4. Feature selection: We select a subset of relevant features using feature importance analysis and drop irrelevant features.

Classification Accuracy: We train the model on a dataset consisting of 2.3M samples and test it on a validation set of 0.5M samples. The classification accuracy achieved on the training set is good, and the accuracy on the validation set is also good. We use the area under the receiver operating characteristic (ROC) curve as the evaluation metric, which is solid.

Commentary and Ideas for Improvements: The high accuracy achieved on the training set indicates that the model has learned the patterns in the training data well. However, the lower accuracy on the validation set suggests that the model may be overfitting to the training data and not generalizing well to unseen data.
To improve the generalization capabilities of the model, we can implement the following:
1. Increase the amount of validation data to better assess the generalization capabilities of the model.
2. Implement early stopping to prevent overfitting by stopping the training process when the validation accuracy stops improving.
3. Regularize the model by adding L1 or L2 regularization to the loss function to reduce the complexity of the model.
4. Increase the number of training samples to improve the robustness of the model.

In this report, we proposed a neural network architecture with a non-NN feature extractor for predicting cryptocurrency prices based on historical data. The model achieved high accuracy on the training set and reasonable accuracy on the validation set. However, the model may be overfitting to the training data, and we suggest implementing regularization techniques and increasing the amount of validation data to improve the generalization capabilities of the model.
