# mlfs-book
O'Reilly book - Building Machine Learning Systems with a feature store: batch, real-time, and LLMs


# Our design for air-quality prediction:
Chosen sensor: Beijing, Temple of Heaven, dongcheng
We use the XGBoost regression model to perform the prediction.
Added the feature: pm25in3day, which is the average value of pm25 during the past 3 days(excluding today).
Predictor: pm25in3day, weather data

# To  perform the prediction:
First predict the pm25 of tomorrow, since already has the pm25in3day.
Do a for loop, first predict the pm25 value of one day, then use this to get the pm25in3day value for the next day.
Loop this for 7 times.
Now we get prediction for next 7 days.

# To see the prediction:
[Click here](./docs/air-quality/index.md)