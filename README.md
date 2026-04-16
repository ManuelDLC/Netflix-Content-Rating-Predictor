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
