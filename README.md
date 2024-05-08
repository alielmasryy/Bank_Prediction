# Bank_Prediction
### Summary
This project helps recommend the best banking products for Santander bank customers. It uses information about customers from the past year and a half (from January 2015 to June 2016) to predict what new products they might be interested in buying in June 2016. https://www.kaggle.com/competitions/santander-product-recommendation

### Overview
The task at hand is to predict customers that are most likely to purchase bank products during the month of June 2016 using the data collected from 1.5 years before that. I decided to use RandomForestClassifier for the most accurate results I could provide. This classifier combines the decisions of many decision trees in order to make more accurate predicitions and avoids overtraining. The best accuracy my model was able to predict with was 57%. There is definitely room for improvement. 

### Summary of the work done

### Data

* Data:
    * Input: CSV File, description of bank customers(type of account they own, income, age, etc.)
    * Output: Out of a list of accounts which ones are they most likely to purchase for bank services
  * Size: Originally 13 million rows which was cut down to 499,999x48 rows and columns

  #### Preprocessing / Clean up

* Split the data into numerical and categorical columns which I found that the data type was mixed up, changed into correct format
* Replaced null values with the most frequent value for each feature in the data
* Features I thought were relevant to group such as income and age were grouped for consistency
* One hot encoded categorical features

#### Data Visualization
![image](https://github.com/alielmasryy/Bank_Prediction/assets/143844073/5a7a033a-6d30-4455-8709-d37ede903932)
![image](https://github.com/alielmasryy/Bank_Prediction/assets/143844073/a3624054-7589-4fc8-96c2-419001c03a13)
![image](https://github.com/alielmasryy/Bank_Prediction/assets/143844073/b38d885b-8ef9-40be-a9cd-422f5eb40ead)

The graphs told me the distribution is not realistic, this indicated an issue with the actual data itself. Some features were concentrated in one place only
I feel this affected the preformance of my model

### Problem Formulation:
  * Input: Customer behavior data from Santander bank using features
  * Output: Predictions of additional products that customers will purchase in the next month
  * Models
    * RandomForestClassifier was chosen due to it being easy and flexible, XGBoost model
    * No fine tuning was done

### Training
  * Using sckit-learn models and processors as well as XGBoost
  * The training took considerable time around 5 minutes, however for XGBoost it was relatively quick
  * Faced difficulties with missing data and skewed distribution, but mostly resolved with some feature engineering and imputation for RFC
  * For XGBoost, faced difficulty with multi-class classification and having to use label encoder instead of one hot encoder

### Conclusions
For RandomForestClassifier
Accuracy:  57%
F1: 59%
Precision: 80%
Recall: 46%
![image](https://github.com/alielmasryy/Bank_Prediction/assets/143844073/0d32871c-4e44-419a-80fc-3866e9c0ba33)

For XGBoost
Accuracy: 81%
F1: 15%
Precision: 34%
![image](https://github.com/alielmasryy/Bank_Prediction/assets/143844073/f7e02472-c255-40a6-8e66-1316a3638c3f)

## How to reproduce results
   * Download the data from kaggle (link can be found at the very bottom)
   * Jupyter notebook was what I used to code
   * Import the necessary libraries such as pandas, matplotlib, and sckit-learn libraries
   * Run the files attached

### Future Work
I would like to try a stochastic gradient classifier and other different models next time to see if there is any difference. I also want to choose a better dataset or find techniques to fix skewed distribution

### Overview of files 
https://www.kaggle.com/competitions/santander-product-recommendation/data
Since this is a big dataset it is highly recommended after downloading it, to cut it within the terminal. I cut it down to 500,000 columns instead of 13 million.

Libraries such as pandas, matplotlib, and various different ones from sklearn are used here
