# ifood Campaign Data Analysis

## [Presentation](https://docs.google.com/presentation/d/1FrSdsQ_8S31_rZG6wvbdS690fjM748q_Gyv2PScib5I/edit?usp=sharing)

## Selected Topic
ifood is a food delivery service that is based in Brazil. They are looking to utilize data from their last 6 campaigns to drive instruction on how to optimize their future campaigns.

## Reason
I have recently started working as a marketing analyst and this challenge closely aligns to work I will be doing in my role.

## Description
I will use the ifood campaign results dataset and machine learning to help determine or predict the ideal target audience to optimize the click through rate (clicking on the campaign) on their campaign. The dataset was obtained from Kaggle.

## Question
Using machine learning algorithms, can the client response to future campaigns be predicted by demographics: income, marital status, education, children, and age.

## Data Exploration Process
I used Google Collab to analyze the data set. The data set began with 2240 rows and 29 columns of data. Given that the client was asking specifically about campaign response and demographics of the customers, I needed to clean the dataset to only include the data applicable to their question. 

The first thing I did was to drop any column that was not applicable to demographic data. I chose to include the age of the customer account membership as well, as it was similar to the age of the customer. I then merged campaign responses to one column and then converted that column to 0 for no response and then 1 for any response. The next step I took was to convert any objects to numerical data so that I could easily run any graphs without conflict with the data type. 

At this point I wanted to normalize the data. I decided to check for any missing values and found that there was a small amount of NaN values in the income column. This only accounted for 1% of the data frame, therefore I deleted those rows from the data frame. I then ran Histogram, Density Plot and Box and Whisker Plots to further visualize the data. I was able to drop outliers prior to running any correlation findings. I used the Point-Biserial Correlation to find the P-Value for each column and the response to the campaign. Any column that resulted in a P-Value of less than .05 I kept in the dataframe for the training model (education, income, childern, date of customer membership, and recency(number of visits to the site)). 

## Technologies Used
Github, Python, Google Colab, PostgreSQL, PGadmin, AutoML 
Dependencies
-Pre-process
-- Pandas, numpy, seaborn, matplotlib, sklearn, plotly, datetime
-Machine learning
--Supervised.automl, sklearn, bioinfokit, pingouin, scipy

## Dashboard
AutoML-SKlearn produces a dashboard within the notebook that is interactive and provides insights given a variety of machine learning models. 

## Machine Learning Model
*Pre-processing*
I used Google Collab to analyze the data set. The data set began with 2240 rows and 29 columns of data. Given that the client was asking specifically about campaign response and demographics of the customers, I needed to clean the dataset to only include the data applicable to their question. The first thing I did was to drop any column that was not applicable to demographic data. I chose to include the age of the customer account membership as well, as it was similar to the age of the customer. I then merged campaign responses to one column and then converted that column to 0 for no response and then 1 for any response. The next step I took was to convert any objects to numerical data so that I could easily run any graphs without conflict with the data type. At this point I wanted to normalize the data. I decided to check for any missing values and found that there was a small amount of NaN values in the income column. This only accounted for 1% of the data frame, therefore I deleted those rows from the data frame.

*Data Split*
Training and testing data sets was split up using a 75/25 approach because there were only about 2200 rows and I wanted to make sure the test data had enough data with which to test.

*Explanation of Model Choice*
supervised.AutoML provides you with 6 models to test and then determines which model is the best one for you to use. Before applying the code i had to save teh demographic columns as a dataframe and the campaign response column as a series so that AutoML could run the report. (*I originally saved both as dataframes and got errors for the results.*) 
<img width="464" alt="image" src="https://user-images.githubusercontent.com/94129215/171459405-f273160d-2d63-4e2f-9469-5aac0d1e7b0d.png">

According to the data training, the Ensemble model would be the best model to use. I went on to use the test data for predictions and the strongest model continued to be the Ensemble with an accuracy score of 75%, auc= .7(1 is perfect), f1 = .84 (1 is perfect True-Positive Rate), 
<img width="438" alt="image" src="https://user-images.githubusercontent.com/94129215/171460825-184c0b88-6a69-4c05-8aed-b1d5c28363ec.png">

<img width="347" alt="image" src="https://user-images.githubusercontent.com/94129215/171460607-01806807-037d-4617-ab91-2200e10cc1b1.png">

*Confusion Matrix*
<img width="272" alt="image" src="https://user-images.githubusercontent.com/94129215/171465173-96f88741-e63a-4cbc-af9a-ea1a878ad92b.png">

<img width="490" alt="image" src="https://user-images.githubusercontent.com/94129215/171465019-a1690b7b-ef9c-4e6a-80d3-d30112998aa9.png">

<img width="466" alt="image" src="https://user-images.githubusercontent.com/94129215/171465069-c2e96f25-16b6-4023-9ad9-055528ffa4a1.png">

*Importance Ranking*
<img width="359" alt="image" src="https://user-images.githubusercontent.com/94129215/171467369-f4b7e192-5f4a-4c2e-a4a2-f99634584e36.png">


# Dashboard - Website
Following the document produced at the end of the code is the website I would create to have the interactive dashboard. This is an newer tool and there is not an easy way to do this, therefore the interactive document at the end of the code is the dashboard sample. The document walks you through the machine learning process and provides insights on the dataset for future campaigns to rely on.

# Challenges
1. AutoML does not have a easy way to export the results into a dashboard that is commonly used. This is a common complaint and they are working on a solution. 

2. I would have liked to have had enough time to use the other data to create a predictive model to show how they could create profiles of their customers that are based on their use of the app versus demographics.
