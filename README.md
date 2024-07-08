# Credit-Loan-Risk-Prediction

## Introduction
Credit risk prediction is an essential process for evaluating the likelihood that a potential borrower will repay a loan. This is particularly crucial in peer-to-peer lending, where class imbalance problems are common. By predicting credit risk effectively, lenders can minimize their losses and maximize net profit margins.


## Solution Explanation
We have developed a machine learning model to identify potentially risky loans. This model can be used as a decision-making tool for investments. If the model is reliable, the investment in risky loans will decrease, minimizing losses and increasing the net profit margin.


## Data
The dataset used for this project comes from Lending Club credit loan data between 2007 and 2014. This data includes various features related to the loans and borrowers.

Data link: https://www.kaggle.com/datasets/devanshi23/loan-data-2007-2014


## Data Overview
The initial dataset was loaded and inspected for its structure and contents. Several preprocessing steps were undertaken to prepare the data for modeling:

1. **Target Column Assignment**: Loans were classified as risky (bad) if they were in one of the following statuses: "Charged Off", "Late (31-120 days)", "Late (16-30 days)", "Default", "Does not meet the credit policy. Status: Charged Off". These were assigned a value of 1, while all other statuses were assigned a value of 0.

2. **Dropping Unnecessary Columns**: Certain columns that are identifiers or contain information not useful for prediction were dropped. This includes columns like 'id', 'member_id', 'url', and others.

3. **Handling Missing Data**: Columns with more than 50% missing values were removed. For other columns with missing values, appropriate imputation strategies were applied.

4. **Feature Engineering**: Some features were transformed to more useful formats, such as converting employment length to numeric and handling categorical features appropriately.


## Exploratory Data Analysis (EDA)
EDA was performed to understand the distribution and relationships of various features in the dataset. Key observations from EDA included:

* The distribution of numeric features through histograms and kernel density plots.

* Boxplots to visualize the relationship between numeric features and the target variable.

* Count plots and bar plots for categorical features to understand their distributions and relationships with the target variable.


## Feature Selection
Correlation heatmaps were used to identify and remove multicollinear features. Additionally, Weight of Evidence (WoE) and Information Value (IV) were calculated to select features with good predictive power. Features with IV less than 0.02 or greater than 0.5 were excluded from the model.

![image](https://github.com/Ashar18/Credit-Loan-Risk-Prediction/assets/64865488/5ef8d0e0-eeae-4e00-b50b-b61e8bc4e68c)


## Model Training
The cleaned and preprocessed data was split into training and testing sets. Due to the class imbalance in the target variable, Random OverSampling was applied to balance the training set. The features were then scaled using MinMaxScaler.

A logistic regression model was trained on the oversampled training data and tested on the test data. The model's performance was evaluated using accuracy, precision, recall, and F1-score.

## Results
The initial model showed reasonable performance but indicated that the precision for predicting bad loans needed improvement. Further steps can include trying different machine learning algorithms, tuning hyperparameters, and exploring advanced techniques like ensemble methods to enhance the model's performance.

## Conclusion
This project demonstrates the process of building a machine learning model to predict credit loan risk. By carefully preparing the data, performing EDA, selecting relevant features, and addressing class imbalance, a model was developed that can assist in making better investment decisions in the lending industry. Further improvements can be made to increase the model's precision and overall predictive power.
