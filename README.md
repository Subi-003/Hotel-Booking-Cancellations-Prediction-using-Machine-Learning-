# Hotel Booking Cancellation using ML with deployment 

## Problem Statement
Hotel cancellations are a major revenue risk in the hospitality industry. When guests cancel last-minute, hotels lose income and struggle to fill rooms in time. This project builds a predictive model that identifies high-risk bookings early, allowing hotels to take proactive measures such as overbooking strategies or targeted retention offers.

## Features
- lead_time: Days between booking and arrival
- avg_price_per_room: Average nightly room rate
- no_of_special_requests: Number of special requests made
- total_guests: Adults + children
- total_nights: Weekday + weekend nights
- repeated_guest: Whether the guest has stayed before

## Approach
1. Exploratory Data Analysis
- Distribution of booking statuses
- Cancellation rate broken down by arrival month
- Lead time vs. cancellation (boxplot analysis)
- Average price per room by month and booking status
- Meal plan breakdown across booking outcomes

2. Feature Engineering
- total_guests = no_of_adults + no_of_children
- total_nights = no_of_week_nights + no_of_weekend_nights
- is_weekend_heavy = flag for bookings with more weekend than weekday nights

3. Model Selection
Three models were trained and compared using RandomizedSearchCV with cross-validation:
- Random Forest(Accuracy)
- Gradient Boosting(F1 Score)
- XGBoost(F1 Score)
Gradient Boosting was selected as the final model based on F1 score performance on the held-out test set (20% split, stratified).

4. Class Imbalance
Used compute_class_weight(class_weight='balanced') to penalise misclassification of the minority class
  
## Live Demo
[Click here to view the app](https://kagu6jhjjmdegadjwustfi.streamlit.app/)

## How to Run Locally
 pip install -r requirements.txt
 streamlit run app.py
