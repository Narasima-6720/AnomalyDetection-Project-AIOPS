# 🚀 Anomaly Detection Using Isolation Forest

## 🔍 What This Project Does
This project uses **Isolation Forest**, a machine learning algorithm, to automatically detect **anomalies (unusual or suspicious data)** in system logs. It's great for identifying errors, performance issues, or anything that doesn't look normal — **without needing labeled data**.

---

## 🛠️ How It Works
1. Load and clean log data using **Pandas** and **NumPy** 🧹
2. Convert logs into a structured table 🧾
3. Assign severity scores to log levels (INFO, WARNING, ERROR, CRITICAL) 🔢
4. Extract useful features like **message length** and **log level score**
5. Apply **Isolation Forest** to detect anomalies 🤖
6. Display the results as ✅ normal or ❌ anomaly

---

## 🤖 Model Details

```python
from sklearn.ensemble import IsolationForest

model = IsolationForest(contamination=0.1, random_state=42)
