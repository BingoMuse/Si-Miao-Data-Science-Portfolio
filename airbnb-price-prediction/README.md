## Airbnb Price Prediction (Regression)
* **Context:** Coursework (Prediction Competition)
* **Tools:** Python, Scikit-Learn, XGBoost, Pandas
* **Key Techniques:** Feature Engineering, Gradient Boosting, Robust Pipeline Design

### Project Objective
Built a regression model to predict 6,000+ Airbnb listing prices based on 50+ property and host characteristics.

### Technical Implementation
* **Feature Engineering:** Extracted quantitative features from unstructured text (e.g., bathroom counts, verification methods) and created ratio-based metrics (e.g., `bedroom_to_guest_ratio`).
* **Preprocessing:** Implemented robust pipelines for missing value imputation and One-Hot Encoding.
* **Modeling:** Trained a Gradient Boosting model (**XGBRegressor**) with log-transformed target variables to handle price skewness.

### Performance
* Achieved a Mean Absolute Error (MAE) of **96**, a significant improvement over the baseline MAE of **135**.