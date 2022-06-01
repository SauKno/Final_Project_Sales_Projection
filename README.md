# ifood Campaign Data Analysis

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

According to the data training, the Ensemble model would be the best model to use. I went on to use the test data for predictions and the strongest model continued to be the Ensemble. 

