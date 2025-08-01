# 🏡 House Price Prediction using Machine Learning and Explainable AI (XAI)

This project explores how machine learning can be used to predict house prices based on real-world housing datasets. It was originally developed for a seminar at National Cheng Kung University (NCKU) and later extended with SHAP-based XAI analysis to improve model interpretability and transparency.

## ✨ Project Highlights

- Built ML models (Random Forest, XGBoost) for housing price prediction with strong performance.
- Applied feature selection and forward/backward strategies to optimize input variables.
- Extended project with SHAP-based explainability (XAI) for model interpretation.
- Organized and documented end-to-end workflow for reproducibility and clarity.

---

## 📑 Outline

- [Project Structure](#project-structure)  
- [Dataset](#dataset)  
- [Methods and Implementation](#methods-and-implementation)  
  - [1. Data Preprocessing & Feature Engineering](#1-data-preprocessing--feature-engineering)  
  - [2. Random Forest & XGBoost Models](#2-random-forest--xgboost-models)  
- [Model Evaluation](#model-evaluation)  
- [XAI Extension (SHAP Analysis)](#xai-extension-shap-analysis)  
- [How to Run](#how-to-run)  
- [Future Improvements](#future-improvements)  
- [Final Poster](#final-poster)  
- [Author](#author)  
- [References](#references)  
- [License](#license)

---

## Project Structure

| Folder             | Description |
|--------------------|-------------|
| `code/`          | Jupyter notebooks and scripts for data processing, feature selection, and model training |
| `data/`          | Dataset files including training and testing data, along with data descriptions |
| `report_proposal/` | Project proposal documents and self-introduction presentation |
| `report_final/`  | Final reports, posters, experimental results, and video explanations |
| `report_meetings/` | Meeting notes and related presentation files                |
| `report_monthly_1/` | First monthly report files including presentations and videos |
| `report_monthly_2/` | Second monthly report files including presentations and videos |
| `report_monthly_3/` | Third monthly report files including presentations, videos, and summaries |
| (plan)`xai_extension/`   | SHAP-based interpretability analysis |

---

## Dataset

- **Data Source**: Kaggle competition or real-estate datasets (e.g., [Ames Housing Dataset](https://www.kaggle.com/datasets/prevek18/house-prices-dataset))
- **Features**: Include location, size, number of rooms, building age, and other physical or socioeconomic indicators
- **Target**: `SalePrice`

---

## Methods and Implementation

### 1. Data Preprocessing & Feature Engineering

- **Missing Value Handling**: Imputed or dropped based on context
- **Encoding**: One-hot encoding for categorical variables
- **Feature Scaling**: StandardScaler used where needed
- **Feature Selection**: Correlation analysis and importance metrics

📓 Notebook: [`original/data_cleaning.ipynb`](original/data_cleaning.ipynb)

---

### 2. Random Forest & XGBoost Models

- **Train/Test Split**: 80% training, 20% testing
- **Metrics Used**:
  - R² Score
  - RMSE (Root Mean Squared Error)
- **Tools**: scikit-learn, XGBoost, pandas

📓 Notebooks:
- [`original/random_forest_house.ipynb`](original/random_forest_house.ipynb)
- [`original/xgboost_house.ipynb`](original/xgboost_house.ipynb)

---

## Model Evaluation

| Model       | R² Score | RMSE     | Notes                    |
|-------------|----------|----------|---------------------------|
| RandomForest| 0.93     | 18,000   | Strong baseline model     |
| XGBoost     | 0.95     | 16,500   | Best performing so far    |

> *Results may vary depending on preprocessing and hyperparameters.*

---

## XAI Extension (SHAP Analysis)

> **Location**: [`xai_extension/`](xai_extension/)

Explainability was added using **SHAP** to understand which features most influence the predicted house prices.

- **Tool**: `shap.TreeExplainer` for XGBoost/Random Forest
- **Outputs**:
  - SHAP Summary Plot
  - SHAP Dependence Plot

📷 Example Output:

![SHAP Summary](xai_extension/shap_summary_house.png)

📓 Notebook: [`xai_extension/shap_house_analysis.ipynb`](xai_extension/shap_house_analysis.ipynb)

---

## How to Run

### Install dependencies

```bash
pip install -r requirements.txt
````

### Run prediction notebook

```bash
cd original
jupyter notebook random_forest_house.ipynb
# or
jupyter notebook xgboost_house.ipynb
```

### Run SHAP analysis

```bash
cd xai_extension
jupyter notebook shap_house_analysis.ipynb
```

---

## Future Improvements

* Add more contextual data (e.g., economic indicators, school zones)
* Use deep learning (e.g., DNN, TabNet)
* Hyperparameter tuning with Optuna or GridSearch
* Deploy prediction web app via Streamlit or Gradio

---

## Final poster

![Image text](https://github.com/Liuian/House-Prices-Advanced-Regression-Techniques/blob/main/final_poster.jpg)

---

## Author

Created by [Liuian](https://github.com/Liuian)

* 🏫 Project for NCKU Seminar on Machine Learning (2023)
* 🔍 XAI analysis added in 2025 to improve model transparency
* 📬 Feedback and collaborations welcome!

---

## References
- Kaggle Competition - House Prices: Advanced Regression Techniques Part 1: [YouTube Video](https://www.youtube.com/watch?v=vtm35gVP8JU)  
- Gradient Boost Part 1: [YouTube Playlist](https://www.youtube.com/watch?v=3CC4N4z3GJc&list=PLblh5JKOoLUICTaGLRoHQDuF_7q2GfuJF&index=59)  
- Stacked Ensemble Models (Top 3% on Leaderboard): [Kaggle Notebook](https://www.kaggle.com/code/limyenwee/stacked-ensemble-models-top-3-on-leaderboard/notebook)

---

## License

This project is licensed under the MIT License.