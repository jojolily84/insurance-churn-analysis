# Insurance Customer Churn Analysis

## 專案背景
保險業客戶流失率高達 30%，本專案透過資料分析找出流失關鍵因子，並建立預測模型協助業務團隊提前介入。

## 資料集
- 來源：Kaggle - Realistic Synthetic Insurance Churn Dataset
- 資料量：50,000 筆客戶資料，40 個欄位
- 目標欄位：churn_flag（0=未流失，1=流失）

## 主要發現
1. **保費漲幅**：流失客戶的保費漲幅中位數（10%）是未流失客戶（5%）的兩倍
2. **投訴紀錄**：有投訴的客戶流失率 55%，是沒投訴客戶（29%）的兩倍
3. **主動詢價**：主動詢價客戶流失率 45%，是強烈的流失前兆訊號
4. **客戶年資**：年資短的客戶流失風險更高，新客戶需要特別關注
5. **保障降級**：主動降低保障的客戶流失率達 40%

## 模型比較
| 模型 | Accuracy | Recall（流失） | F1-Score |
|---|---|---|---|
| Logistic Regression | 0.75 | 0.38 | 0.48 |
| Random Forest | 0.75 | 0.41 | 0.50 |

## 業務建議
- 優先處理有投訴紀錄的客戶
- 對保費漲幅超過 8% 的客戶提前溝通
- 針對新客戶（年資 < 24 個月）設計留客方案
- 主動詢價的客戶需立即安排業務跟進

## 技術工具
Python、Pandas、Seaborn、Matplotlib、scikit-learn

## 專案結構
```
insurance-churn-analysis/
│  .gitignore
│  README.md
│  
├─data
│      insurance_policyholder_churn_data_dictionary.csv
│      insurance_policyholder_churn_synthetic.csv
│      
└─notebooks
        01_EDA.ipynb
```