# Pima_Indian_diabetes_data_Classification
A machine learning model to accurately classify whether or not the patients in the data set have diabetes or not.

### Missing data handling
We tried the following ways for handling the missing data:

1. On analysis, we found that we lose up to 11% of the data if we discard the rows with missing values. And as the data set available was small we could not afford that.
2. To check if any insignificant features could be discarded, we used the extra tree classifier as shown below
3. The missing data in the data set was replaced with the median value of each column. Median and mean gave the same values, but we chose median over mean as mean can be affected by the outliers, but not median.

### Data transformation 
Data transformation converts data from one format or structure into another format or structure. One of the technique for it is normalization of data. Normalization brings all the columns to the same scale so that the data is not skewed towards large scale numerical values.
 
We tried normalizing the data using Min-Max normalization instead of Standard Scaling(making mean zero) and Robust Scaling(making median zero) as the data is not normally distributed.

### Features Selection
As discussed, the data handling extra tree classifier states that all the features have equal significance and the correlation between any of the features is not greater than 0.54, which tells that the features are not redundant and that all features contribute to the output.

Hence we didn't go for dimensionality reduction and selected all the existing features.

### Model Building & Perfomance Evaluation
For model building we split the data set into 80% train set and 20% test set. We tried the following models and checked with which we get the maximum accuracy.
- Logistic Regression
- Naive Bayesian Classification
- K Nearest Neighbors Classifier
- Stochastic Gradient Descent
- Support Vector Classification
- Random Forest Classifier
- Decision Tree Classifier

We calculated the accuracy and confusion matrix for performance evaluation of all the models and SVC gives the best results in terms of accuracy(80\%).
