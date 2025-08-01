# House-Prices-Advanced-Regression-Techniques
![Image text](https://github.com/Liuian/House-Prices-Advanced-Regression-Techniques/blob/88518648dc216022d5853a0d57a026df1f2622ec/final_poster.jpg)

## Methodology Summary

### Raw and Predictive Data
- **Dataset**: Real housing price data from Ames, Iowa, USA.
- **Training data**: `train.csv` contains 1422 homes with 75 variables & real prices (shape: 1422, 75).
- **Testing data**: `test.csv` contains 1459 homes with 74 variables (shape: 1459, 74).

### Steps and Improvements

1. **Simple Missing Value Imputation + XGBoost**
   - Used basic imputation methods with XGBoost.
   - Kaggle performance: PR47.

2. **Enhanced Missing Value Imputation**
   - Conducted detailed data analysis and logical imputation.
   - Improved ranking to PR67.

3. **Parameter Tuning for XGBoost**
   - Applied Randomized Cross-Validation (Randomize CV) for 50 iterations.
   - Selected the best parameter set to boost accuracy further.

4. **Feature Selection**
   - Explored Lasso, Random Forest, Correlation, Mutual Information, Forward/Backward Selection.
   - Selected optimal features for training.

5. **Data Preprocessing**
   - Applied standardization and log transformation to raw data.

### Best Training Results
- **Final Configuration**: XGBoost + Enhanced Missing Value Imputation + Randomize CV.

---

## 實作方法總結
### 原始、預測資料
- **數據集**: 美國Ames, Iowa城市的真實房價數據。
- **訓練資料**: `train.csv` 含有1422筆數據與75個變數 (形狀: 1422, 75)。
- **測試資料**: `test.csv` 含有1459筆數據與74個變數 (形狀: 1459, 74)。

### 步驟與改進

1. **簡單的填補缺失值 + XGBoost**
   - 採用簡單填補缺失值方式結合XGBoost訓練模型。
   - Kaggle排名：PR47。

2. **改良填補缺失值方法**
   - 詳細分析資料特性，採用更有邏輯的填補方式。
   - Kaggle排名提升至PR67。

3. **XGBoost參數調整**
   - 使用Randomize CV進行50次參數隨機選取訓練。
   - 選出最佳參數進一步提升精準度。

4. **特徵選擇**
   - 使用Lasso、隨機森林、相關性分析、互資訊量、前向/後向選擇等方法。
   - 篩選最佳特徵進行訓練。

5. **資料預處理**
   - 將數據進行標準化與對數轉換後再訓練。

### 最佳訓練結果
- **最終配置**: XGBoost + 改良填補缺失值 + Randomize CV。

---

## References
- Kaggle Competition - House Prices: Advanced Regression Techniques Part 1: [YouTube Video](https://www.youtube.com/watch?v=vtm35gVP8JU)  
- Gradient Boost Part 1: [YouTube Playlist](https://www.youtube.com/watch?v=3CC4N4z3GJc&list=PLblh5JKOoLUICTaGLRoHQDuF_7q2GfuJF&index=59)  
- Stacked Ensemble Models (Top 3% on Leaderboard): [Kaggle Notebook](https://www.kaggle.com/code/limyenwee/stacked-ensemble-models-top-3-on-leaderboard/notebook)

