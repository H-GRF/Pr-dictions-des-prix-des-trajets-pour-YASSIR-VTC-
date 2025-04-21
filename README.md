
# Trip Price Prediction for YASSIR VTC

## Overview
This project focuses on predicting the price of trips for **YASSIR VTC**, a ride-hailing service, based on various features such as trip distance, rider and driver information, and trip status. The model is trained using historical data, and the goal is to predict the **trip_fee** for new trips using machine learning models.

## Objective
The objective of this project is to develop a machine learning model that can predict the price of a trip for YASSIR VTC. The predictions are based on features such as the **pickup city**, **destination city**, **trip distance**, **rider and driver ratings**, **discount usage**, and **trip status**.

## Approach

1. **Data Preprocessing**:
   - Data cleaning, including handling missing values and encoding categorical variables.
   - Feature engineering, such as extracting date-related features (e.g., day, month, and hour) from the `request_date`, `accepted_date`, and `started_date`.
   - Transformation of continuous variables, such as **trip_distance** and **driver2rider_distance**, to optimize model performance.

2. **Model Development**:
   - A machine learning model is trained to predict **trip_fee** using features from the training dataset.
   - Several models, such as **Linear Regression**, **Random Forest**, and **Gradient Boosting**, can be used to determine the best-performing model.

3. **Evaluation**:
   - The model is evaluated using **Mean Absolute Error (MAE)** or **Root Mean Squared Error (RMSE)** to assess prediction accuracy.

4. **Submission**:
   - The model's predictions for the test set are submitted using the format specified in the **sample_submission.csv** file.

## Dataset Description

### `train.csv`
The training data includes various features of the trips such as:
- **id**: Unique identifier for each trip.
- **request_date**: Date and time when the trip was requested.
- **pickup_city**: City where the trip was requested.
- **destination_city**: City where the trip will end.
- **trip_distance**: Distance of the trip (in meters).
- **driver2rider_distance**: Distance between the driver and rider (in meters).
- **used_discount**: Whether a discount was used (1 if used, 0 otherwise).
- **trip_status**: The status of the trip (e.g., **FINISHED**, **NOT_FINISHED**).
- **trip_fee**: The actual price of the trip (target variable).

### `test.csv`
The test data includes the same features as the training data, except the **trip_fee**. This file will be used to make predictions that will be evaluated based on accuracy.

### `sample_submission.csv`
This file shows the expected format for submitting the predictions:
- **id**: The same **id** from the test set.
- **trip_fee**: The predicted price for the trip.

## Files in the Repository
- **train.csv**: The training dataset containing historical trip information.
- **test.csv**: The test dataset for which predictions need to be made.
- **sample_submission.csv**: The format for submitting predictions.

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

### 3. Preprocess the Data:
Run the notebook or script to preprocess the data by handling missing values, encoding categorical variables, and creating new features.

### 4. Train the Model:
Train the machine learning model using the **train.csv** dataset. Models such as **Linear Regression**, **Random Forest**, or **Gradient Boosting** can be tested for the best performance.

### 5. Make Predictions:
Use the trained model to make predictions on the **test.csv** dataset. Save the predictions in the format provided in **sample_submission.csv**.

### 6. Submit the Predictions:
Submit the predictions to the competition platform (or to the relevant person/team) using the format in **sample_submission.csv**.

## Conclusion
This project demonstrates how machine learning can be used to predict trip prices for a ride-hailing service like YASSIR VTC. The model can be improved further by tuning hyperparameters and experimenting with different feature engineering techniques.

