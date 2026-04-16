# Netflix Content Rating Predictor
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
- **Language:** Top 10 languages one-hot encoded
- **Cast:** Top 20 actors one-hot encoded
- **Directors:** Top 20 directos one-hot encoded
- **Countries:** Top 15 countries one-hot encoded
- **Plot Descriptions:** TF-IDF vectorized (300 features, unigrams + bigrams)

## Models Compared
| Model | MAE | R² |
|-------|-----|----|
| Random Forest | 0.561 | 0.372 |
| XGBoost (tuned) | 0.561 | 0.387 |

## How To Run
- Clone the repo
- Install: pip install xgboost scikit-learn kagglehub pandas matplotlib seaborn scipy
- Open notebook and run all cells

## Limitations
- Ratings reflect opinions, which is noisy. A 0.387 R² is pretty reasonable with this in mind
- Cast/director features are binary and not a measure of involvement level
- Model would not generalize well to unreleased content since some features need to wait until post-release such as post release signals

## Dataset
[Netflix Movies and TV Shows till 2025](https://www.kaggle.com/datasets/bhargavchirumamilla/netflix-movies-and-tv-shows-till-2025) via Kaggle

