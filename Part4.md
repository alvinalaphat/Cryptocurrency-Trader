## Link to Extra Credit Presentation
https://docs.google.com/presentation/d/1p49CoI3uGAc_bp9WiEyte0CNDFK1CEQ_5Svy_VHsoMs/edit?usp=sharing

## Link to Colab
https://colab.research.google.com/drive/1ZyEDCOd_npZGEp9ayQrV4m9JK_qnSOGQ?usp=sharing

## Instructions to Upload Data
Download data from here: https://www.kaggle.com/competitions/g-research-crypto-forecasting/data?select=supplemental_train.csv

It's called "supplemental_train.csv"

Mount on Google Drive root folder. 

## Report
Luke worked on implementing early stopping for the model as suggested in the part 3 deliverable using the Early Stopping module. Alvin worked on finding ways to reduce overfitting by working with a dropout layer and regularizing the data using regularizers from the Keras library. 

Building a cryptocurrency trading algorithm with price prediction is a challenging task due to the high volatility and non-linearity of the cryptocurrency market. In this report, we propose a neural network architecture for predicting the price of a cryptocurrency based on historical price data. The goal is to achieve a high classification accuracy on the training and validation sets and improve the generalization capabilities of the model.

Neural Network Architecture: We propose a deep neural network architecture consisting of four layers: two dense layers with 128 and 128 units, respectively, and a final dense layer with a single output unit. We experimented with taking out the dropout layer and realized our model performed slightly better without it. We use the Rectified Linear Unit (ReLU) activation function but also experimented with sigmoid for the hidden layers and a linear activation function for the output layer. The loss function is mean squared error (MSE), and the optimization algorithm is Adam. 

Methods applied:
1. Time-series modification: The data was previously not in a format where the model would be able to use past data to predict future returns. We realigned the data in order to ensure that each row contains 15 minutes of time series data. 
2. Feature selection: We select a subset of relevant features using feature importance analysis and drop irrelevant features.

Accuracy: We train the model on a dataset consisting of 100K samples and test it on a validation set of 20K samples. The R^2 metric achieved on the training and validation set is .80. We used R^2 because R-squared (R^2) is an appropriate metric to use when you want to evaluate how well a regression model fits the data. It measures the proportion of variance in the target variable that is explained by the independent variables in the model. The differences between the test and validation set are sufficient to test the generalization capabilities of the final programs because the test and validation sets provide independent samples from the same underlying data distribution, which allows us to evaluate the model's ability to generalize to new, unseen data. By testing on a separate dataset, we can determine if the model has overfit to the training data, and if it can perform well on new data. Analysis on all subsets indicates that our model generalizes well. 

Commentary and Ideas for Improvements: The high accuracy achieved on the training set indicates that the model has learned the patterns in the training data well. However, the lower accuracy on the validation set suggests that the model may be overfitting to the training data and not generalizing well to unseen data.
To improve the generalization capabilities of the model, we can implement the following:
1. Increase the amount of training data to introduce more variance and similarity to real world conditions
2. Do more feature selection and analysis on the existing dataset to discover scores for feature relevance
3. Introduce external variables to add in as features such as time of day, type of crypto, and other technical indicators (RSI, MACD)

In this report, we proposed a neural network architecture for predicting cryptocurrency prices based on historical data. The model achieved high accuracy on the training and validation set. However, the model may be overfitting to the training data, and we suggest investigating our data transformation methods and increasing the amount of validation data to improve the generalization capabilities of the model. 
