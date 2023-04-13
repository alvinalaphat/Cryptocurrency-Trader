## Instructions to Upload Data
Download data from here: https://www.kaggle.com/competitions/g-research-crypto-forecasting/data?select=supplemental_train.csv

Mount on Google Drive root folder. 

## Report
Luke worked on cleaning the data to feed into the model and ran it through testing with the model architecture. Alvin worked on testing the model with the validation/test data and then tweaked parameters to experiment what performed best with the model. 

Building a cryptocurrency trading algorithm with price prediction is a challenging task due to the high volatility and non-linearity of the cryptocurrency market. In this report, we propose a neural network architecture for predicting the price of a cryptocurrency based on historical price data. The goal is to achieve a high classification accuracy on the training and validation sets and improve the generalization capabilities of the model.

Neural Network Architecture: We propose a deep neural network architecture consisting of four layers: two dense layers with 128 and 128 units, respectively, followed by a dropout layer with a rate of 0.2 and a final dense layer with a single output unit. We use the Rectified Linear Unit (ReLU) activation function for the hidden layers and a linear activation function for the output layer. The loss function is mean squared error (MSE), and the optimization algorithm is Adam. Speaking of Adam, we plan to meet with the professor to discuss our architectural choices. 

Methods applied:
1. Time-series modification: The data was previously not in a format where the model would be able to use past data to predict future returns. We realigned the data in order to ensure that each row contains 15 minutes of time series data. 
2. Feature selection: We select a subset of relevant features using feature importance analysis and drop irrelevant features.

Accuracy: We train the model on a dataset consisting of 100K samples and test it on a validation set of 20K samples. The R^2 metric achieved on the training and validation set is .73. We used R^2 because R-squared (R^2) is an appropriate metric to use when you want to evaluate how well a regression model fits the data. It measures the proportion of variance in the target variable that is explained by the independent variables in the model.

Commentary and Ideas for Improvements: The high accuracy achieved on the training set indicates that the model has learned the patterns in the training data well. However, the lower accuracy on the validation set suggests that the model may be overfitting to the training data and not generalizing well to unseen data.
To improve the generalization capabilities of the model, we can implement the following:
1. Increase the amount of validation data to better assess the generalization capabilities of the model.
2. Implement early stopping to prevent overfitting by stopping the training process when the validation accuracy stops improving.
3. Increase the number of training samples to improve the robustness of the model.

In this report, we proposed a neural network architecture for predicting cryptocurrency prices based on historical data. The model achieved high accuracy on the training and validation set. However, the model may be overfitting to the training data, and we suggest investigating our data transformation methods and increasing the amount of validation data to improve the generalization capabilities of the model. We'll use the above methods listed to dive deeper into why we might be overfitting the model. 
