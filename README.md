# London-cars2014-analysis-and-prediction

This repository is about analysing and predicting car prices based on the London-car2014 dataset. The data is about the "cars for sale", which was collected in Summer 2014 from the website Autotrader.com. In this repository, I have used pandas and scikit-learn to analyse the dataset and then use supervised machine learning algorithms - specifically multiple linear regression and polynomial regression - to predict car prices.

# About the dataset
The "cars for sale" was collected in Summer 2014 from the website Autotrader.com. The data set consists of 11 columns and 1080 rows as described below:

Data columns (total 11 columns):
 i   Column        Non-Null Count  Dtype 
---  ------        --------------  ----- 
 0   Make          9080 non-null   object
 ---  ------        --------------  ----- 
 1   Model         9080 non-null   object
 ---  ------        --------------  ----- 
 2   Year          9080 non-null   int64 
 ---  ------        --------------  ----- 
 3   Mileage       9080 non-null   int64 
 ---  ------        --------------  ----- 
 4   Price         9080 non-null   int64 
 ---  ------        --------------  ----- 
 5   Body Style    9080 non-null   object
 ---  ------        --------------  ----- 
 6   Ex Color      9080 non-null   object
 ---  ------        --------------  ----- 
 7   In Color      9080 non-null   object
 ---  ------        --------------  ----- 
 8   Engine        9080 non-null   object
  ---  ------        --------------  ----- 
 9   Transmission  9080 non-null   object
  ---  ------        --------------  ----- 
 10  Doors         9080 non-null   int64 

 The column names are pretty self-explanatory.

# Steps:
1. Download the CSV file.
2. Load the csv into pandas dataframe
3. Check for missing/null values and ensure the datatypes are correct and consistent in each column
5. Encode categorical columns using Label-Encoding
6. Analyse the dataset to intuitively identify patterns
7. Check for correlation using a heatmap
8. split the dataset into test and train
9. Train using regression models
10. check accuracy for models with varying degrees

# Conclusion
The following results were obtained for polynomial regression models with varying degrees:
degree: [1, 2, 3, 4, 5]
train_MSE: ['1.72E+08', '1.34E+04', '1.20E+04', '1.31E+04', '1.89E+04']
test_MSE: ['2.25E+08', '1.19E+04', '1.31E+04', '2.02E+04', '6.43E+04']
train_r_sq: ['3.13E-01', '3.59E-01', '4.88E-01', '3.88E-01', '-2.73E-01']
test_r_sq: ['2.48E-01', '3.95E-01', '2.61E-01', '-7.44E-01', '-1.67E+01']

From the above, we can see that the model performs best when the polynomial degree is 3.
 
