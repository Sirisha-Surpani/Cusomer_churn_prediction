# Cusomer_churn_prediction
    Customer Churn Prediction in Telcom Industry – ANN with Keras

Data Set:
We considered the WA_Fn-UseC_-Telco-Customer-Churn.csv data to predict the customer churn in a telecom industry considering several factors.
Dataset preview:
 

Data Understanding and Feature Engineering: 
We dropped the customer_id column as it not going to add any weightage to the churn prediction.
				 
All the features are in Object data types except SeniorCitizen, tenure, Monthly Charges. So we need to convert those data types.
 
Since "No internet service" or "No phone service" mean? I believe it means NO !!! Here we should just replace them with NO

We replaced all the "No internet service" or "No phone service" with No and then encoded the Yes and No to 1 and 0 respectively to convert the data to int data.

 
For the remaining categorical values we are going to perform one hot encoding.
For Gender we are replacing Female=1 and Male=0.


Normalisation of data:
As all columns now are numeric ones in 0s and 1s, these three columns ['InternetService','Contract','PaymentMethod'] are not in the same SCALE. we are using standard scalar to normalise the data.
Exploratory Data Analysis:  
From the Visualizations we can say that data dataset is imbalanced. Here I'm going to use imblearn.over_sampling SMOTE to introduce more instances in order to have better balance before splitting the data into Training & Testing.

   



Modelling:
 
Accuracy:
 
Our ANN with keras gave us an accuracy of 81% in predicting the customer churn.




