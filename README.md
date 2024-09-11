# Overview
Fraud Detection is a project trained using Machine Learning to identify online transactions. The model was trained using Supervised Learning Algorithms like Decision Tree and Logistic Regression since the dataset already had labeled data.The model was evaluated using key metrics like confusion matrix.
The accuracy of both the algorithms was :Decision Tree Score: 99.94947
Logistic Regression Score 99.91363.

## Dataset
* Source : The dataset is imported from Kaggle.The dataset consists of records like type of transaction,original and new balance of customer and recipient.
      It also includes record of Fraud transactions and which are Flagged as Fraud.

## Key Steps
### 1. Data Preprocessing : 
* Missing Values : Handled missing values by removing rows with incomplete data.
* Outliers Detection : Outliers were detected using InterQuartile Range (IQR). There were total of 338077 outliers in the data but removing outliers in this dataset may make the model bias.
* Feature Encoding : The records for type were categorical. Used Label Encoding to convert them into numeric data type.
* Feature Scaling : Standard Scalar was used to normalize features. 
### 2. Exploratory Data Analysis:
* Performed EDA to understand data and identify outliers. The bar chart for type of payment record showed more number of transactions with Cash-out as compare to Cash-in. Correlation Matrix demonstrated that oldBalanceOrign and newBalanceOrig were highly correlated.Plots such as count, box, and scatter gave information about the data by showing patterns and trends.
### 3. Feature Engineering:
* Amount_origin and Amount_Dest features were created by calculating the difference between old and new balance at origin and destination accounts.
  
### 4. Model Building : 
* Supervised Learning algorithms- Decision Tree and Logistic Regression were used to train.
* Logistic Regression: Trained with L2 regularization.
* Decision Tree : Fine- tuning was performed for hyperparameters like max_depth and min_samples_split.

### 5. Model Evaluation:
* Confusion matrix was used to evaluate the performance of both models.
* Calculated accuracy, precision, recall and f1 score using classification_report.
