
# HACKATHON OPEN DATA 2 - Second Prize: Trip Price Prediction for YASSIR VTC

## Overview
This project was developed as part of the **HACKATHON OPEN DATA 2** competition, where it earned second place. The main goal of the project was to predict the prices of trips for **YASSIR VTC**, an Algerian ride-hailing company, based on various factors such as distance, time, and location. Additionally, an **interactive map** was developed to visualize these trips and their associated prices.

## Objective
The core objectives of this project were:
1. **Data Preprocessing & Feature Engineering**: Clean and prepare the trip data to create meaningful features that would improve model accuracy.
2. **Predictive Modeling**: Build a machine learning model that predicts trip prices based on the given features.
3. **Clustering**: Perform clustering analysis to identify patterns in the data, particularly focusing on how trip characteristics group together.
4. **Interactive Data Visualization**: Develop an interactive map to visualize the trip routes and prices.

## Approach

### 1. Data Exploration & Preprocessing
The dataset contains several features such as trip distance, time of day, and vehicle type. Data preprocessing steps involved:
- Handling missing values using imputation techniques.
- Feature extraction from timestamps (e.g., day of the week, hour of day).
- Encoding categorical variables (e.g., vehicle type, location) using one-hot encoding.
- Scaling numerical features for model consistency.

### 2. Feature Engineering
Key features engineered include:
- **Time-related Features**: Extracted the time of day, day of the week, and month to help capture patterns based on temporal factors.
- **Trip Distance & Duration**: Distance and duration of each trip were used as key predictors of price.
- **Geospatial Features**: Geolocation of the trip’s start and end points were incorporated into the analysis to account for different pricing in various locations.

### 3. Machine Learning Model Development
We implemented several machine learning models:
- **Linear Regression**: As a baseline to predict continuous trip prices.
- **Random Forest Regressor**: To capture non-linear relationships between features and the price.
- **Gradient Boosting**: For more complex and accurate predictions.
The models were evaluated based on **Mean Absolute Error (MAE)** and **Root Mean Squared Error (RMSE)**.

### 4. Clustering Analysis
Clustering was performed on features such as trip distance, duration, and price using **K-Means Clustering**. This helped identify different types of trips that share similar characteristics (e.g., short trips vs long trips) and allowed for the refinement of prediction models based on trip clusters.

### 5. Interactive Map
An interactive map was developed using **Folium** to visualize the trips based on their starting and ending locations. This visualization helps stakeholders better understand the geographical distribution of trips and associated prices.

  
### Key Columns
- **trip_fee**: Target variable (trip price).
- **pickup_location** / **dropoff_location**: Geographical features indicating the start and end of a trip.
- **distance**: Trip length in kilometers.
- **time_of_day**: Derived from timestamps for temporal analysis.
- **vehicle_type**: Type of vehicle used for the trip.
- **duration**: Duration of the trip in minutes.

## Files in the Repository

- **clustering.ipynb**: Jupyter notebook containing the clustering analysis using **K-Means**. It includes feature engineering for clustering, such as trip distance, duration, and price.
- **highcharter.Rmd**: RMarkdown file for generating high-quality visualizations, including the interactive map showing trip locations and prices.
- **kaggle.ipynb**: Jupyter notebook that focuses on training and evaluating machine learning models (Linear Regression, Random Forest, and Gradient Boosting) for predicting trip prices.
- **KPI.Rmd**: RMarkdown file that defines and calculates key performance indicators (KPIs), such as MAE, RMSE, and model comparison.
- **yassir.Rmd**: RMarkdown file containing the results and detailed analysis, along with the final presentation of the model’s effectiveness.

## Key Performance Indicators (KPIs)

The performance of the model was evaluated using the following metrics:
- **Mean Absolute Error (MAE)**: Measures the average magnitude of errors in the predictions, providing a direct understanding of prediction accuracy.
- **Root Mean Squared Error (RMSE)**: Penalizes large errors more than MAE, giving a sense of how well the model generalizes.
- **Model Comparison**: A comparison of model performances across different algorithms to determine the best model for predicting trip prices.

## How to Run the Project

### 1. Clone the Repository:
```bash
git clone https://github.com/your-username/repository-name.git
```

### 2. Install Dependencies:
Install required Python libraries:
```bash
pip install -r requirements.txt
```

Install required R packages:
```R
install.packages("highcharter")
install.packages("folium")
install.packages("lubridate")
```

### 3. Run Jupyter Notebooks:
Open the notebooks using Jupyter Notebook:
```bash
jupyter notebook
```
Then, run the notebooks `clustering.ipynb` and `kaggle.ipynb` for data preprocessing, training models, and evaluating the results.

### 4. Generate Interactive Map:
Run `highcharter.Rmd` or `yassir.Rmd` in RStudio to generate the interactive map and visualizations.

### 5. Evaluate KPIs:
Check the `KPI.Rmd` file for the key performance indicators used to evaluate model performance.

## Conclusion

This project demonstrates the practical application of machine learning and data science techniques in the ride-hailing industry. By using machine learning models and clustering techniques, we were able to accurately predict the price of trips and visualize patterns geographically. The interactive map provides an intuitive way to explore the trip data, while the clustering analysis and KPIs help refine the model’s predictions.

