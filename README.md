## toronto_collision_forecast

Training a negative binomial regression model to predict daily traffic collision counts in Toronto using weather and temporal features.

See the full project notebook here:
https://github.com/yourusername/toronto_collision_forecast/blob/main/collision_forecasting_model.ipynb

Model Inputs

Weather variables:

- Average temperature

- Average wind speed

- Average visibility

- Rain indicator

- Snow indicator

Temporal features:

- Holiday weekend indicator

- Cyclical encoding of day-of-year (sin, cos)

- 7-day lag of collisions

- Interaction terms (e.g., snow × wind speed, snow × holiday weekend)

Policy variable:

- COVID lockdown indicator

Output:

- Predicted daily collision count

Model evaluation metrics:

- Mean Absolute Error (MAE ≈ 30 collisions)

- RMSE

- MAPE

- Out-of-sample test performance

Modeling Approach

- Data cleaning and feature engineering using Python (pandas, NumPy)

- Exploratory data analysis (seaborn, matplotlib)

- Cyclical encoding to capture seasonal patterns

- Negative Binomial GLM (statsmodels) to handle overdispersed count data

- Time-based train/test split for realistic forecasting evaluation

Assumptions

- Collision counts follow an overdispersed count distribution (Negative Binomial appropriate over Poisson).

- Weather variables are daily aggregates.

- Lag features use prior observed collision counts (no future leakage).

- Seasonal patterns are captured via sine/cosine transformation rather than categorical seasons.

Data Sources

Traffic collision data:
City of Toronto Open Data Portal

Weather data:
Environment and Climate Change Canada (daily weather statistics)

<img width="1408" height="790" alt="image" src="https://github.com/user-attachments/assets/a7c6df79-387e-4542-9e5c-d2c167cb6aa5" />
<img width="1406" height="788" alt="image" src="https://github.com/user-attachments/assets/0b551f33-2bd5-4bfb-b8c5-463108fd7f6d" />
<img width="1404" height="790" alt="image" src="https://github.com/user-attachments/assets/5e40cf16-d63e-408b-8de2-165958a86638" />
<img width="1406" height="786" alt="image" src="https://github.com/user-attachments/assets/42067a23-08b2-4213-94d6-1995f8431ea9" />

