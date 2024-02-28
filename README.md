# 專案名稱
### Titanic - Machine Learning from Disaster
# 描述
Kaggle 提供鐵達尼號上所有乘客的基本資料，並且還附上這些乘客最後是存活下來還是罹難

1. PassengerId: 乘客ID
2. Pclass: 艙位分級 1,2,3
3. The Name of the passeger: 乘客全名
4. The Sex: 性別
5. The Age: 年紀
6. SibSp: 與乘客同行的兄弟姊妹和配偶的數量 (旁系人數)
7. Parch: 與乘客同行的父母和兒童人數 (直系人數)
8. The ticket number: 船票編號
9. The ticket Fare: 船票價格
10. The cabin number: 艙室編號
11. The embarkation: 人們可能登船的三個區域 (S,C,Q)
# 資料數量
1. 訓練資料數量: 891筆
2. 測試資料數量: 418筆
# 資料探索分析
1. 女生(罹難數、生存數)、男生(罹難數、生存數)
![image](https://github.com/JN11540/Kaggle_Titanic/blob/master/img/1.png)
2. 女生(罹難生存百分比)、男生(罹難生存百分比)
![image](https://github.com/JN11540/Kaggle_Titanic/blob/master/img/2.png)
3. 女生(罹難者歲數分布、生存者歲數分布)、男生(罹難者歲數分布、生存者歲數分布)
![image](https://github.com/JN11540/Kaggle_Titanic/blob/master/img/3.png)
4. 票價分布(票價分成多個間隔，察看每個間隔罹難數、生存數)
![image](https://github.com/JN11540/Kaggle_Titanic/blob/master/img/4.png)
5. 橫軸(年紀)、總軸(票價)
![image](https://github.com/JN11540/Kaggle_Titanic/blob/master/img/5.png)
6. 橫軸(艙位分級)、總軸(票價)
![image](https://github.com/JN11540/Kaggle_Titanic/blob/master/img/6.png)
7. 橫軸(登船的三個區域)、總軸(票價)
![image](https://github.com/JN11540/Kaggle_Titanic/blob/master/img/7.png)
# 特徵工程
1. 將訓練數據與測試數據合併，並刪除 PassengerId 欄位
![image](https://github.com/JN11540/Kaggle_Titanic/blob/master/img/8.png)
2. "分類"的欄位需要進行 One hot encoding、"大小關係"的欄位不需要處理
3. Name 欄位有 17 個稱位，'Sir', 'Lady', 'Mr', 'Mlle', 'Mrs', 'Don', 'Mme', 'Jonkheer', 'Dr', 'Ms', 'the Countess', 'Master', 'Major', 'Col', 'Rev', 'Capt', 'Miss'-> 修剪成 6 個稱位 'Officer', 'Royalty', 'Mr', 'Mrs', 'Miss', 'Master'
4. 根據 Sex, Pclass, Title 來填補 Age 欄位的缺失值
![image](https://github.com/JN11540/Kaggle_Titanic/blob/master/img/9.png)
5. 特徵工程結束時，從 11 個欄位擴增至 67 個欄位
# 資料清洗
1. 由模型來評量每個欄位重要程度，以重要程度刪除欄位
![image](https://github.com/JN11540/Kaggle_Titanic/blob/master/img/10.png)
2. 67 個欄位縮減至 11 個欄位
3. 選用的模型時隨機森林
