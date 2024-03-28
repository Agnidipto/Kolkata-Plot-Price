# Predicting Land Prices in Kolkata

## Overview

This project aims to predict the price of a plot of land in the city of Kolkata using machine learning techniques. The dataset contains various features that describe different aspects of the land, such as its boundaries, presence of construction, open sides, proximity to amenities like gardens or main roads, road width, and area.

## Dataset

The dataset contains the following columns:

- **boundary**: Indicates whether the plot has a boundary or not.
- **construction**: Indicates if any construction is done on the plot.
- **open_sides**: Number of sides open for the plot.
- **garden_park**: Indicates if the plot overlooks any garden or park.
- **main_road**: Indicates if the plot overlooks a main road.
- **pool**: Indicates if the plot overlooks a pool.
- **width_road**: Width of the road neighboring the plot.
- **area**: Area of the plot in square foot.
- **new_property**: If Property is new, or a resale.
- **location**: Location of the plot. Can have multiple values, so it is an array. For example, [Action Area 3, New Town].

## Objective

The objective of this project is to build a machine learning model that can accurately predict the price of a plot of land in Kolkata based on the provided features. By leveraging historical data and predictive modeling techniques, we aim to assist real estate stakeholders, investors, and buyers in making informed decisions regarding land transactions.

## Approach

1. **Data Collection**: We use Web Scraping to originally gather the data by scraping online websites. (The code for scraping with Selenium has not been included in this repo.)

2. **Data Preprocessing/Manipulation**: We will start by exploring and cleaning the dataset. This may involve handling missing values, encoding categorical variables, and scaling numerical features.

3. **Feature Engineering**: We will analyze the existing features and create new ones if necessary to enhance the predictive power of the model.

4. **Feature Scaling**: We will use numpy.log to transform the data into a normal distribution. The data is originally a right-skewed dataset. Then we use z-score normalization to scale the features.

5. **Model Selection**: We will experiment with different machine learning algorithms such as linear regression, decision trees, random forests, and gradient boosting to identify the best-performing model.

6. **Model Evaluation**: We will evaluate the performance of each model using appropriate metrics such as mean squared error (MSE), root mean squared error (RMSE), and R-squared.

7. **Deployment**: Once the model is trained and evaluated satisfactorily, we will deploy it to production, making it accessible for predictions on new data.

## Conclusion

We used **Neural Network** in the end since it gave the best results. Some specifications of the model used are :
- It has 4 layers. 
- Activation functions for the first 3 layers are ReLU, and linear for the last one.
- It uses an Adam Optimizer to prevent overshooting.
- It utilizes 50 epochs.

## Future Work

- Expand the dataset with additional relevant features to improve the model's predictive performance.
- Gather more data using additional web scraping, or some other means.
