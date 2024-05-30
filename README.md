# House-Prices-Advanced-Regression-Techniques
![Image text](https://github.com/Liuian/House-Prices-Advanced-Regression-Techniques/blob/88518648dc216022d5853a0d57a026df1f2622ec/%E6%9C%9F%E6%9C%AB%E6%B5%B7%E5%A0%B1_page-0001.jpg)

##  實作方法總結
原始、預測資料：  
美國一個城市Ames, Iowa的真實房價資料  
train.csv: 1422 homes with 75 variables & real price(1422, 75)  
test.csv: (1459, 74) 
  
簡單的填補缺失值＋XGBoost：一開始我用簡單的方法填補缺失值，搭配XGBoost訓練模型。可以看到成效不太好，出來的成果排名在Kaggle上只有PR47而已。  

改良填補缺失值方法：為了提升預測精準度，我開始對資料的特性做完整的研究。因此可以用更具有邏輯的法填補缺失值，可以看到預測精準度大幅提升，我的排名也因此上升到PR67。  

改進XGBoost選擇參數的方法：利用Randomize CV，總共訓練模型50次，每一次的參數選擇都是隨機從我指定的幾個值裡面取的，做完以後取出結果最好的那一組作為欲使用的參數。預測精準度也因此變得更好一些。  

特徵選擇(feature selection)：我嘗試幾種不同的方法Lasso, Random forest, Correlation, Mutual info, forward selection, backward selection，選擇出欲使用的特徵後再做訓練。  

資料預處理：將原始資料做standardize, log transformation後再做訓練。  

最好的訓練結果：XGBoost + 改善填補缺失值的方法 + randomize CV
* test1
Kaggle Competition - House Prices: Advanced Regression Techniques Part1: https://www.youtube.com/watch?v=vtm35gVP8JU  
github: https://github.com/krishnaik06/Kaggle-Competitions  

* test2
Gradient Boost Part 1 (of 4): Regression Main Ideas: https://www.youtube.com/watch?v=3CC4N4z3GJc&list=PLblh5JKOoLUICTaGLRoHQDuF_7q2GfuJF&index=59  

* test3
Stacked Ensemble Models (Top 3% on Leaderboard): https://www.kaggle.com/code/limyenwee/stacked-ensemble-models-top-3-on-leaderboard/notebook  
