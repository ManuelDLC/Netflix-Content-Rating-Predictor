# Netflix-Content-Rating-Predictor
A ML pipeliene that predicts Netflix content ratings using data such as cast/crew, genre, and language

## Results

| Metric | Score |
|--------|------ |
| R²     | 0.387 | 
| MAE    | 0.561 |
| CV R²  | 0.369 ± 0.107 |

**Best XGBoost parameters:** 'max_depth = 7', 'learning_rate = 0.05', 'subsample = 0.9', 'm_estimators = 200'

## Key Findings
- **Horror Genre** was the strongest predictor of content rating
- **Animation and Action** genres were the next most predictive features
- **English and Japanese Language** content showed strong rating signals
- Removing zero-rated titles significantly improved the model accuracy and feature importance clarity

## Visualization

### Actual vs Prediction
<img width="690" height="490" alt="image" src="https://github.com/user-attachments/assets/4389f5fe-84f3-4559-bd2c-3d36a1ad943d" />

### Top 15 Feature Importances
<img width="790" height="590" alt="image" src="https://github.com/user-attachments/assets/67b58de9-f5eb-4b39-8428-de8bbebaca82" />

### Residual Distribution
<img width="598" height="393" alt="image" src="https://github.com/user-attachments/assets/141eadd4-3cda-4be4-8df6-152ac605fb75" />

### Rating Distribution
<img width="607" height="393" alt="image" src="https://github.com/user-attachments/assets/fe99d882-f95c-43b7-ad3b-2a4fb2963d72" />

## Features Used
- **Content Type:** Movie vs TV show
- **Data Features:** year/month added to Netflix, release year
- **Description Length:** Word count of plot summary
- **Genres:** Top 15 genres one-hot encoded

