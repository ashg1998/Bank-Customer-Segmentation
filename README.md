# Bank-Customer-Segmentation
**One of the key pain point for marketers is know their customers and identify there needs.
**By understanding the customers needs marketers can launch a targeted market campaign that is tailored for specific needs.
**If data about the customers is available, data science can be applied for market segmentation.
** In this project we are provided with extensive data for past 6 months  of bank customers.
**We are using KMeans Clustering.
**We are Principal Component Analysis and AutoEncoder for Dimension Reduction in Dataset.And Then forming clusters with the new Dataset.
DATASET COLUMNS:
### CUSTID: Identification of Credit Card holder 
### BALANCE: Balance amount left in customer's account to make purchases
### BALANCE_FREQUENCY: How frequently the Balance is updated, score between 0 and 1 (1 = frequently updated, 0 = not frequently updated)
### PURCHASES: Amount of purchases made from account
### ONEOFFPURCHASES: Maximum purchase amount done in one-go
### INSTALLMENTS_PURCHASES: Amount of purchase done in installment
### CASH_ADVANCE: Cash in advance given by the user
### PURCHASES_FREQUENCY: How frequently the Purchases are being made, score between 0 and 1 (1 = frequently purchased, 0 = not frequently purchased)
### ONEOFF_PURCHASES_FREQUENCY: How frequently Purchases are happening in one-go (1 = frequently purchased, 0 = not frequently purchased)
### PURCHASES_INSTALLMENTS_FREQUENCY: How frequently purchases in installments are being done (1 = frequently done, 0 = not frequently done)
### CASH_ADVANCE_FREQUENCY: How frequently the cash in advance being paid
### CASH_ADVANCE_TRX: Number of Transactions made with "Cash in Advance"
### PURCHASES_TRX: Number of purchase transactions made
### CREDIT_LIMIT: Limit of Credit Card for user
### PAYMENTS: Amount of Payment done by user
### MINIMUM_PAYMENTS: Minimum amount of payments made by user  
### PRC_FULL_PAYMENT: Percent of full payment paid by user
### TENURE: Tenure of credit card service for user

Data Preparation:
Step 1: Filling all Nan values with mean of the respective column.
Step 2: Dropping CUSTID from the dataset.

Data Analysis:
1. Plotting Displot for all the columns in the Dataset for better understanding of the data columns in dataset.
2. Plotting Correlation Heatmap.
![alt text](https://github.com/ashg1998/Bank-Customer-Segmentation/blob/main/images/correlation.png)

Next Step:
Find the optimal number of clusters.
using Eblow Method:
![alt text](https://github.com/ashg1998/Bank-Customer-Segmentation/blob/main/images/ELBOW_GRAPH.JPG)
We noticed at 8 clusters it gives minimum error. So 8 clusters are used for KMeans Clustering.
We scale down the data from 

Next: We Apply the KMeans Algorithm and plot histogram of each columns according to Cluster they all in:
This is the result we get.
![alt text](https://github.com/ashg1998/Bank-Customer-Segmentation/blob/main/images/cluster1.JPG)
![alt text](https://github.com/ashg1998/Bank-Customer-Segmentation/blob/main/images/cluster2.JPG)
![alt text](https://github.com/ashg1998/Bank-Customer-Segmentation/blob/main/images/cluster3.JPG)
![alt text](https://github.com/ashg1998/Bank-Customer-Segmentation/blob/main/images/cluster4.JPG)
After applying PCA reducing the dimensions into 2 columns.
Then clustering the dataset , we get the following result
![alt text](https://github.com/ashg1998/Bank-Customer-Segmentation/blob/main/images/PCAcluster.jpg)

#Now we Switch to Neural Network:
Step 1: We build a autoencoder neural network
Step 2: We train the model with the scaled data and reduce dimensionality of the dataset.
Step 3: Now, we have got reduced dataset we perform KMeans and PCA with the new dataset.

# Results:
optimal K = 4
![alt text](https://github.com/ashg1998/Bank-Customer-Segmentation/blob/main/images/encoded_Eblow_graph.jpg)

PCA
![alt text](https://github.com/ashg1998/Bank-Customer-Segmentation/blob/main/images/cluster_with_4.jpg)





