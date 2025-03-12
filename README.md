# 🛳️ Titanic - Machine Learning from Disaster

This project tackles the iconic **Titanic Kaggle competition**, where the goal is to predict which passengers survived the Titanic shipwreck using a combination of demographic and socio-economic data.

The project follows a complete ML pipeline:
- 📊 Exploratory Data Analysis (EDA)
- 🛠️ Feature Engineering
- 🤖 Model Training (Logistic Regression, Random Forest, XGBoost, LightGBM)
- 🧪 Hyperparameter Tuning
- 🤝 Ensemble Learning
- 📈 Submission to Kaggle and performance comparison

---

## 📁 Project Structure
```
📦 Titanic-ML
├── train.csv
├── test.csv
├── train_cleaned.csv
├── test_cleaned.csv
├── titanic_model_pipeline.ipynb
├── submission/
│   └── each model submission.csv
└── README.md
```

---

## 🧠 Best Model (So Far)

> ✅ **Logistic Regression + Feature Engineered Data**  
> 🏆 **Kaggle Score: 0.78229**

Despite being a simple model, logistic regression outperformed many complex ones when combined with thoughtful feature engineering.

---

## 📊 Model Performance Comparison

| Model                    | Dataset        | Kaggle Score |
|-------------------------|----------------|--------------|
| **Logistic Regression** | Engineered     | **0.78229** ✅ |
| Ensemble (Voting)       | Engineered     | 0.77990      |
| XGBoost                 | Engineered     | 0.77033      |
| XGBoost                 | Original       | 0.77272      |
| LightGBM (GridSearch)   | Original       | 0.77272      |
| Random Forest (Optimized)| Engineered    | 0.76555      |
| LightGBM (GridSearch)   | Engineered     | 0.76315      |
| Random Forest           | Engineered     | 0.74880      |
| Random Forest           | Original       | 0.74641      |
| LightGBM (Simple)       | Original       | 0.74641      |
| LightGBM (Simple)       | Engineered     | 0.74401      |

---

## 🛠️ Feature Engineering Highlights

- `FamilySize` = `SibSp` + `Parch` + 1
- `IsAlone` = 1 if `FamilySize == 1`, else 0
- Extracted `Title` from `Name`
- One-hot encoding on `Sex`, `Embarked`, and `Title`

---

## 📤 Submissions

All model predictions are saved in the `submission/` folder for reproducibility and score tracking.

---

## 📌 Next Steps

- Visualize feature importance and SHAP values
- Build a stacking ensemble
- Try interaction features (polynomial terms)
- Move on to the next ML project in the [YouTube video roadmap](https://www.youtube.com/watch?v=QlbyGPVaRSE)

---

## 🙌 Credits

This project is inspired by the video:  
**"22 Machine Learning Projects That Will Make You A God At Data Science"**  
🔗 [Watch it here](https://www.youtube.com/watch?v=QlbyGPVaRSE)
