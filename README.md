# College-Football-Coach-Salary-Prediction

## Introduction

Finding an acceptable salary range or minimum number is particularly important to most applicants to any job posting. Knowing what that number should be allows an applicant more control over the process and usually, better pay. For college football coaches and other positions with salaries that are open to the public, this data can be used to determine the market rate for a specific position.

This project will use linear regression models created with Python to predict the market rate for the Syracuse football coach based on a variety of factors. 



## Analysis

### Data Preparation:

A csv file with data for school, coach name, salary, conference, bonus amounts and buyout clauses was provided and a tsv file of additional data on school’s academic progress rates, private vs public schools, historically black universities, and squad size was pulled from the ICPSR database.

Both files were loaded into python, an average APR was calculated from 2004-2014 for each school and the datasets were merged after cleansing to match school names.
The coaches9 csv contained 129 rows and 9 columns, after merging to include the additional variables the cleaned dataset had 68 rows and 7 columns.

 Some initial plots were created to show the APR average by conference, as well as the distribution of the total pay variable and total pay by conference. 
 
 ![image](https://user-images.githubusercontent.com/94664740/227395302-82e1251a-e1ac-48b6-8e34-39dee13a04f3.png)


![image](https://user-images.githubusercontent.com/94664740/227395327-d243bd46-4c0a-4f28-ac8e-06ddc38a806e.png)


A train dataset was created using 80% of the dataset and the remaining 20% was used to create a test dataset to test the accuracy of the models.


## Results

Once the dataset was cleaned and train and test sets were created the linear regression models could be created. The first model build was a simple linear regression model to predict Total Pay as a function of Conference as Conference had the highest variability.

![image](https://user-images.githubusercontent.com/94664740/227395419-6ce7f803-644e-4ea9-9e41-8ef26e9f75da.png)

This model's performance was mediocre, with an R-Squared of 63.7% and Adjusted R-squared of 55.6%. For a simple model this is does a decent job, most of the conferences are not statistically significant but describe about 64% of the variation in the Total Pay.

The second model created used APR average, Private, Squad Size and HBCU in addition to Conference to predict of Total Pay and was tested on the training data. This model had a higher R-squared at 75.9% and Adjusted R-squared at 68.5%. the only additional variable that was not significant was the S![image](https://user-images.githubusercontent.com/94664740/227395712-13e1acd7-4d60-404c-8a92-9c5712bc61b3.png)
quad Size with a p value of 0.144.


![Uploading image.png…]()





