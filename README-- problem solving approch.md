# Loan-Defaulter-Predictor
we have data of a BFSI domain containing information about several customers and their loan status. we want to create a multi-class classification model to predict the status of the loan. our major focus will be on weather a customer will be a defaulter or not.
steps done to solve the problem
1.	Import required libraries
2.	check and set the correct working directory
3.	load the dataset
4.	check the shape of the dataset
5.	since max columns were 74 so display is set to a maximum of 80 rows and columns
6.	check head to see the initial dataset
7.	check column names
8.	drop unnecessary columns like- id, member_id, grade (because of subgrade), URL, zip code, etc.
9.	check the data types of each column
10.	check the 5-point summary of all numeric columns
11.	checking null value/ missing value status of each column
12.	check the percentage of missing values
13.	since many variables were containing more than 45% missing values so removed all those columns and again checked % of missing values
14.	replace missing values of continuous columns with a median
15.	remove/drop categorical missing value observations from data.
16.	since some observations were dropped to the index set
17.	check unique values and frequency counts of the dependent variable
18.	create a new dependent variable list based on the loan_status column
19.	drop original dependent variable from the dataset
20.	check outliers by box plot
21.	remove outliers through IQR
22.	check unique values and their frequency count of each categorical variable
23.	created a list containing continuous values of emp_length and replaced it in the original dataset
24.	check multicollinearity and remove some independent variables based on this multicollinearity
25.	convert categorical values into numeric through one-hot encoding
26.	one of the major issues is a class imbalance in data. tried several ways to deal with this multicollinearity

a. created some models on imbalanced data, but they were not giving good accuracy

b. tried under sampling, but data got reduced much and it was unable to capture all the information/variety of data so not giving good accuracy

c. lastly tried SMOTE to oversample the data and it as giving good accuracy. but the only problem was we have created some synthetic data which is not a good practice but we didn't have a choice, so we have to do it.

27.	again, check the class imbalance
28.	converted data into array format for smoot processing
29.	split dataset into train and test set
30.	scaling is done through a standard scaler
31.	created random forest model
32.	predict output on the test set
33.	find confusion matrix, precision, and recall of all classes
34.	exported model and scaler in pickle format
