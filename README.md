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
  
## Live Demo
[Click here to view the app](https://kagu6jhjjmdegadjwustfi.streamlit.app/)

## How to Run Locally
pip install -r requirements.txt
streamlit run app.py
