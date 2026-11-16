# 筆電價格預測分析

針對 momo 購物平台筆電資料進行資料清洗與機器學習分析，經清洗後共保留 1,160 筆有效資料。

## 📊 簡報專案

- **線上查看**：[筆電價格預測分析簡報（PDF）](https://github.com/pcch27/Laptop-Price-Prediction/blob/main/%E7%AD%86%E9%9B%BB%E5%83%B9%E6%A0%BC%E9%A0%90%E6%B8%AC%E5%88%86%E6%9E%90.pdf)

## 🛠️ 技術重點

- **資料處理**：使用 Pandas 解析螢幕解析度與 SSD 容量，並進行解析度特徵工程。
- **資料清洗**：進行 IQR 離群值處理、One-Hot Encoding 與標準化。
- **模型評估**：比較 Linear Regression、KNN、Decision Tree 三種模型。
- **殘差分析**：分析殘差落在 ±20K 內的比例，以及 |殘差| 與預測值的相關係數，檢查是否存在漏斗型誤差。

## 📈 分析結果

- **最佳模型**：Linear Regression
- **成效指標**：測試集 R² = 0.8817，MAE = 4,565 元

| 模型 | 測試 R² | MAE（元） | 殘差 ±20K 內 |
|---|---:|---:|---:|
| Linear Regression | 0.8817 | 4,565 | 99.4% |
| KNN (k=5) | 0.8531 | 4,690 | 98.0% |
| Decision Tree (depth=8) | 0.8012 | 5,172 | 96.8% |
