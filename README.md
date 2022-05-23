# 💸Credit Card Default Prediction

Financial threats are displaying a trend about the credit risk of commercial banks as the incredible improvement in the financial industry has arisen. In this way, one of the biggest threats faced by commercial banks is the risk prediction of credit clients. The goal is to predict the probability of credit default based on credit card owner's characteristics and payment history.





## 📊 Data Source
In our dataset we have 25 columns which reflect various attributes
of the customer. The target column is default.payment.next.month , which reflects whether the customer defaulted or not.
Our aim is to predict the probability of default given the payment history of the customer.
I have built my model using a public dataset available on kaggle.

https://www.kaggle.com/datasets/uciml/default-of-credit-card-clients-dataset

## 🖥 Web UI

![App Screenshot](https://media.giphy.com/media/3xTgcAJ5QW9W6DOLqZ/giphy.gif)

## 🎯Approach

#### Notebook Name : 1.1_EDA_DATA_PREPROCESSING
#### Custom Defined Modules Used : None
#### Notebook Description :
•	General Data Visualisation, Analysing relation between features and target.
•	Using Boxplots to visualize outliers.
•	Data Sanity Checks.

#### Notebook Name : 1.2_FEATURE ENGINEERING FOR CATEGORICAL FEATURES

#### Custom Defined Modules Used : Data_Ingestion_And_Preprocessing

#### Notebook Description :

•	Load and pre-process the data using custom-defined module.
•	This module performs data sanity checks, replaces unknowns,removes outliers and balances the data. 
•	To handle our categoric features I created a basic random forest model. I tried one-hot encoding, count encoding, target mean encoding and leaving the categories as discrete ordinal features.
•	The best results were obtained by target mean encoding. 
•	Hence the categoric features have been target mean encoded.
•	For logistic regression we have scaled the data.
•	The pre-processed data has been saved as train.csv and test.csv



#### Notebook Number : 2-5

#### Custom Defined Modules Used : Build_Evaluate_Model

#### Notebook Description :

•	We have built logistic regression , random forest,balanced random forest , xgboost and adaboost classifier models.
•	To build each of the model we hae used a custom defined module Build_Evaluate_Model.
•	For each of the model we start by building a base model which is based on default parameters of the model.
•	We then perform hyperparameter tuning and find the best model.
•	We save the train and test score for model comparison.
•	Model Evaluation : For  every model built we record the train and test roc_auc score 
•	We choose the best model based on train and test roc_auc score and difference between train and test score to ensure that there is no overfitting.

-  Final Model is stored as pickle file Final_Model.pkl.

#### Custom Defined Modules
-  Data_Ingestion_And_Preprocessing- Data loading and  Preprocessing.
-  Build_Evaluate_Model - Used in building classifiers and evaluating model performance.
-  Deployment_inputs-transforming inputs from user to Features of our model.
-  app.py- Used for building and deploying app.

#### Deployment Files
- requirements.txt
- Procfile
- app.py



## 📑Documentation

[Detailed Project Report](https://drive.google.com/file/d/1ES1e_xIR6_FZlwKQFvwolJd3q_sSeg2N/view?usp=sharing)

[High Level Document](https://drive.google.com/file/d/1GPRctHMLq5M8NuFdvQlZuj91rrLll1S5/view?usp=sharing)

[Low Level Document](https://drive.google.com/file/d/1toeX4D0hNN8ZI4U9rhYYxg5w-eMPhRqI/view?usp=sharing)

[Architecture Document](https://drive.google.com/file/d/1JD6gw0zaJ_wDWYLTSEKYnh2cx-cLcA4W/view?usp=sharing)

[Wireframe Document](https://drive.google.com/file/d/1azCG5lWHHSmTjmbYQY3Q_9hT8VEJMH7o/view?usp=sharing)


## ⚡Deployment

Deployed on web using Heroku url : https://credit-default-prob.herokuapp.com/

## ⚡Demo Video 

[For Project Demo Click Here](https://drive.google.com/file/d/1sJpzDYLG1QTgLjxvvuqkgJDBN4a984zq/view?usp=sharing)

## Author✍

- [@SanikaDharwadker](https://www.github.com/SanikaDharwadker)
