# A walk through Boston Airbnb data

## Objective & Motivation 
Airbnb had made it easier for people to rent their houses and apartements to tourists and visitors, and with a vibrant and relatively large city as Boston, a lot of factors can affect the price of such listings on Airbnb from the neighbourhood, to the score that a caertain listing get and much more. So In this project, I try to understand more which factors are most important for affecting a listing's price. Specifically, I try to answer the following questions:
1. Which neighborhoods have the highest and lowest prices and why?
2. Can we make accurate price predictions using our data?
3. Which of the data's features affect the price the most?
Answering those questions can provide an insights for new Airbnb hosts who wish to start their Airbnb hosting journay, by providing them with information about the factors affecting a listing price, or how much they should charge for their new listing.

## Data
To answer these questions, I use the "listings.csv" (which is uploaded here)
This dataset contains 3585 samples (number of rows) of different listings across Boston, with 95 different features (number of colomns) for these listings (eg. neighbourhood, price, review score,...etc.).

Some data preprocessing was necessary to utilize this available data in the best way, for example, dropping colomns with a lot of missing values, or that are irrlevant in answering my questions (you can learn more about this in the Notebook under data preprocessing).

## Models
In trying to answer question 2, I used 2 models in my analysis, first a linear regression model, then a ridge regression model (with different regularization paramters). Both Models gave very similar accuracy results.

## Results
1. Using descriptive statistics, I was able to establish a sense of the most expensive and least expensive neighbourhoods around Boston, and the property types they have to offer.
2. For the prediction task, I was able to achieve an R2 score of 0.675 on average using a linear regression model with dropping the samples that has missing values (as it turns out that this would lead to a better R2 score than keeping those samples and imputing by the coloumn mean)
3. I used the linear model's coefficients to identify other factors that affect the listing's price besides the neighbourhood, like the property type, and the type of cancelation policy,..etc.

You can read about the results in more details here: https://mai-elkady.medium.com/a-walk-through-bostons-airbnb-data-e4a9815173bf

## Libraries 
Numpy, Pandas, Matplotlib, seaborn, datetime, sklearn

## Files
listings.csv : The data in csv format
Boston_airbnb.ipynb : Python Notebook, Main code and analysis

## To run the code
* Make sure all necessary libraries are installed
* Download the .ipyb file and the data file
* Use Jupyter to open the .ipyb
* Update the "boston_airbnb_data_path" in the code to point to where your data file is


