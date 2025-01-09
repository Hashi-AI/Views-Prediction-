# Views Predictor

A machine learning project to predict  views using engagement metrics.

## Task Overview
Using a dataset of YouTube video metrics to predict view counts based on 6 key features:
- Subscriber Count
- Comments
- Shares
- Likes vs. Dislikes Percentage
- Average View Duration
- Impressions Click-Through Rate

## A. Model Selection & Training
The project implements a Random Forest Regressor with the following configuration:
- 200 trees for stability
- Maximum depth of 10 to prevent overfitting
- Minimum samples split of 5
- Standard scaling of input features

## B. Model Choice Justification
Random Forest was selected because:
- Handles non-linear relationships between features effectively
- Provides built-in feature importance analysis
- Balances model complexity with prediction accuracy
- Shows good resistance to overfitting
- Works well with our relatively small feature set

## C. Model Performance & Feature Significance
Performance Metrics:
- Training RMSE: 666,746 views
- Validation RMSE: 1,572,067 views
- Training R²: 0.9520
- Validation R²: 0.8298

Feature Importance:
1. Subscriber count (Most significant predictor)
2. Comments and shares
3. Engagement metrics (likes, duration, click-through rate)

## D. Test Predictions & Expected Performance
Test Set Predictions:
- Range: 1.7M to 7.2M views
- Most predictions fall in 2-4M views range
- Distribution shows expected right-skew pattern

Out-of-Sample Performance Estimation:
- Expected accuracy (R²) around 83%
- Average prediction error: ±1.57M views
- Higher reliability for videos with 2-4M views
- Reduced precision for viral content (>8M views)

