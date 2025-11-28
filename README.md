## 📘 Project Summary

This project applies and compares three regression algorithms — Linear Regression, Random Forest Regressor, and XGBoost Regressor — on a student academic dataset containing demographic, socioeconomic, and previous academic performance features.

The goal is to evaluate how well each model predicts the target variable (SSC GPA) based on features such as parental education, income, subjects’ grades, and district variables.

The analysis includes:
- Data loading and exploration
- Visualizations (distributions, scatter plots, trends)
- Training three different regression models
- Computing evaluation metrics (MAE, MSE, RMSE, R² Score)
- Selecting the best model
- Summarizing insights and limitations

This project demonstrates a full supervised learning pipeline from raw data to model evaluation and interpretation.


# Regression Models Comparison

This project compares three regression models — **Linear Regression**, **Random Forest Regressor**, and **XGBoost Regressor** — applied to a tabular dataset.  
Each model is evaluated using standard error metrics to determine which algorithm delivers the best predictive performance.

---

## 📁 Dataset
The dataset used for this project was loaded from Google Drive in `.xlsx` format.

Example path used in Google Colab:/content/drive/MyDrive/Group_prediction_by_Regressor-Dataset_(2).xlsx

### 📊 Dataset Preview

Below is a screenshot showing the first few rows of the dataset used in this project:

![Dataset Preview](dataset_preview.png)

### 📈 Model Comparison Table

The table below compares the performance of the three regression models based on MAE, MSE, RMSE, and R² Score:

![Model Comparison Table](model_comparison_table.png)

### 🏆 Best Model Summary

The following screenshot shows the evaluation metrics for the XGBoost Regressor, which achieved the highest R² Score and lowest error values:

![Best Model Summary](best_model_summary.png)



## 🧩 Conclusion

After evaluating all three models, the XGBoost Regressor achieved the strongest metrics:

- Lowest MSE  
- Lowest RMSE  
- Competitive MAE  
- Highest R² Score (0.221077)

Although the overall R² values are modest — suggesting limited predictive power — this is normal for small or noisy datasets. XGBoost consistently performed better than Linear Regression and Random Forest, confirming its ability to learn nonlinear patterns more effectively.

### Key Takeaways
- XGBoost is the most suitable model for this dataset.
- Some features may not strongly influence the target variable.
- Additional feature engineering or more data could improve prediction accuracy.

---

## 🚀 Next Steps (Future Improvements)

If this project is expanded, the following enhancements could significantly improve performance:

1. **Feature Engineering**
   - Combine subject scores into weighted averages  
   - Encode categorical variables more effectively  
   - Normalize or scale income-related features  

2. **Hyperparameter Tuning**
   - Use GridSearchCV or RandomizedSearchCV for XGBoost  
   - Tune number of estimators, depth, and learning rate  

3. **Cross-Validation**
   - Apply k-fold CV for more reliable performance metrics  

4. **Model Expansion**
   - Try LightGBM or CatBoost (often outperform XGBoost)  
   - Try Neural Networks (MLPRegressor)  

5. **Deploying the Model**
   - Export model as `.pkl` and build a simple API  
   - Host using Flask/FastAPI + Render/Heroku  

These improvements would push the project from coursework level to applied machine learning project level.
