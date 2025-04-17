# nfl-play-prediction-random-forest
Random Forest and Gradient Boosting models to predict NFL play types (Run or Pass) based on game features like down, yard line, time pressure, and more.

NFL Play Type Prediction Using Random Forest & Gradient Boosting

This project applies machine learning to predict play types—either "Run" or "Pass"—in NFL games based on field position, downs, time remaining, and other in-game conditions. It was developed as part of the ALY6020 Predictive Analytics course at Northeastern University.

## Objective
To classify NFL play types using structured game data and understand which situational factors influence play-calling decisions.

##  Data Preparation
- Removed irrelevant and redundant columns
- Handled missing values and capped outliers using IQR
- Encoded categorical features and standardized numerical ones
- Created engineered features like:
  - `Down Importance` = Down × To Go
  - `Momentum` = Score Differential
  - `Time Pressure` = Inverse of Time Left

##  Models Built
### 1. Random Forest
- **Accuracy**: 73%
- Best at identifying **Running plays** (Recall = 82%)

### 2. Gradient Boosting
- **Accuracy**: 60%
- Better at predicting **Passing plays** but less balanced overall

##  Files Included
- `ALY6020_Assignment4_week4.ipynb`: Full code and visualizations
- `ALY6020_Assignment4_FootBall Data Analysis.docx`: Formal report
- `Training_Data_Converted.csv`: Cleaned dataset
- `README.md`: Project summary

##  Tools Used
- Python (Pandas, Scikit-learn, Seaborn, Matplotlib)
- Jupyter Notebook

##  Key Takeaways
- Feature engineering (like `Down Importance`) significantly improves prediction
- Random Forest performed best in terms of balance and accuracy
- Future work: test XGBoost, add player-level or real-time features for enhancement
