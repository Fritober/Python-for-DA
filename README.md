# Facebook-Comment-Volume-Prediction

## Problem Statement

Data in the social networking services is increasing day by day. In France, there are 32 million active users and the average French user spends 13 hours on Facebook. Besides, the average Facebook Page posts 1.68 times per day. So,  the task here is to estimate the comment count that a post is expected to receive in next few(H) hours. Data has been scraped from one of the most popular social networking sites - Facebook.

## Dataset Source Link

https://archive.ics.uci.edu/ml/datasets/Facebook+Comment+Volume+Dataset

## Approach

### Data Preprocessing : 
- Adding the features names as the columns' name are left empty
- Cleaning the data by removing any features with no values 
- Splitting each dataset into 2 dataset : Features & Target Variable
- Merging the datasets for Data Visualization

### Data Visualization : 
- Plotting the target variable to look for the distribution of the number of commentary per post (Scatter plot, Histogram, Line Chart)
- Plotting the features (Boxplot, Histogram)

### Modeling :
- Using Hold Out Cross Validation to split training data into train and test data. Test Cases provided are used as validation set (Not working as it takes too much time to compute, over 30minutes) 
- Performing regression using following techniques :
  - Linear Regression (BEST MODEL with best accuracy and MSE) 
  - Decision Tree Regressor (WORST MODEL with worst accuracy and MSE)
  - Random Forest Regressor 

## Evaluation Metric

- For the given problem statement, we have chosen Mean Squared Error as a evaluation metric as the goal is not to predict the exact number of comments a facebook post receives but the performances of our model. However, more metrics could have been used. 

## Conclusion

- With the Data Visualization we have done, it seems that the dataset isn't well distributed as most post in our training dataset has few commentary ( < 300). We think that an oversampling technique could have been performed to make the dataset more usable.

- From the TestSet, Linear Regression has the best performance in the prediction. But in general, Random Forest should have the best performance which could led to a more advanced reflection on dataset exploitation. Besides, we could have better results with Cross-Validation for Random Forest & Decision Tree
