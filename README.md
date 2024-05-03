# Bank_Prediction
# Summary
This project helps recommend the best banking products for Santander bank customers. It uses information about customers from the past year and a half (from January 2015 to June 2016) to predict what new products they might be interested in buying in June 2016. https://www.kaggle.com/competitions/santander-product-recommendation

# Overview
The task at hand is to predict products that customers are most likely to purchase during the month of June 2016 using the data collected from 1.5 years before that. I decided to use RandomForestClassifier for the most accurate results I could provide. This classifier combines the decisions of many decision trees in order to make more accurate predicitions and avoids overtraining. The best accuracy my model was able to predict with was 57%. There is definitely room for improvement. 

# Summary of the work done
A CSV file that contained 499,999x48 rows and columns which was split into training sets and test sets
For cleaning the data I used straightforward methods for simplicity. I believe this may be responsible for the accuracy score. Columns there were not used for features were dropped. Numerical columns with null values were filled with the median and the categorical columns were filled with the mode. I grouped all the ages into different categories and the income as well.

![image](https://github.com/alielmasryy/Bank_Prediction/assets/143844073/f6d5137a-03e3-4434-bf96-ec2961fc2e9d)
I saw from this that most customers were adults to senior and the income group was mostly low.

# Training
Split the data into features and target variables. Afterwards, split the data into training and testing sets. Fit your classifier and predict.

# Conclusions
Accuracy:  57%
F1: 59%
Precision: 80%
Recall: 46%
![image](https://github.com/alielmasryy/Bank_Prediction/assets/143844073/0d32871c-4e44-419a-80fc-3866e9c0ba33)


# Future Work
I would like to try a stochastic gradient classifier next time to see if there is any difference, but mainly cleaning the data in a better way. However, my sister is into trading futures and options so I have become particularly interested in seeing if I can build a model for trading that can predict certain trends which certain strategies fall under within the stock market.

# Overview of files 
https://www.kaggle.com/competitions/santander-product-recommendation/data
Since this is a big dataset it is highly recommended after downloading it, to cut it within the terminal. I cut it down to 500,000 columns instead of 13 million.
