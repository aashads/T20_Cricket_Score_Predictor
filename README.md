**T20 Cricket Score Predictor**

This repository contains a T20 Cricket Score Prediction model built using match data, XGBoost, and a Streamlit web application for user interaction. The model predicts the final score of a T20 match based on various in-game parameters, providing a user-friendly interface for quick and accurate score predictions.

**Project Overview**

Cricket is a dynamic game with many factors affecting the final score. This model leverages historical T20 match data to predict the score based on:
* Batting Team
* Bowling Team
* City (Location of the Match)
* Current Score
* Balls Left
* Wickets Left
* Current Run Rate

The project implements XGBoost (Extreme Gradient Boosting), a powerful machine learning algorithm known for its high efficiency and accuracy in prediction tasks.
Features

* Interactive Input: Users can select batting and bowling teams, city, and in-game stats like current score and balls left.
* User-Friendly Interface: Built with Streamlit, the app provides an intuitive UI for entering match details and viewing predictions.
* Real-Time Prediction: Provides instant prediction for the final score with a button click.

**Data Preprocessing and Model Building**

The data was cleaned, transformed, and preprocessed to handle missing values, standardize formats, and create feature columns:
* City Extraction: Missing cities were inferred from the venue.
* Cumulative Score Calculation: Cumulative runs and balls bowled were calculated for each match.
* Run Rate and Wicket Calculation: Run rate and wickets left were added as model features.
* Outlier Removal: Applied Interquartile Range (IQR) filtering to handle extreme values.
* Encoding: Used OneHotEncoding for categorical variables and StandardScaler for normalization.

The XGBoost Regressor model was chosen due to its robust performance, tuned for optimal parameters to improve accuracy.
Model Performance

* R² Score: Provides a measure of the model's accuracy.
* Mean Absolute Error (MAE): Indicates the model's prediction error.

**Getting Started**

1. Clone the repository: git clone https://github.com/yourusername/T20-Cricket-Score-Predictor.git

2. Install dependencies: pip install -r requirements.txt

3. Run the Streamlit app: streamlit run app.py

**Future Improvements**

Additional features: Inclusion of weather and pitch conditions for improved predictions.
Model Tuning: Further tuning of the model parameters to enhance performance.
Extended Data: Incorporate more historical data for broader coverage.
