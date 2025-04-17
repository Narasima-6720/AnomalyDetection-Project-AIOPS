# 🚀 Anomaly Detection Using Isolation Forest

## 🔍 What This Project Does
This project uses **Isolation Forest**, a machine learning algorithm, to automatically detect **anomalies (unusual or suspicious data)** in system logs. It's perfect for identifying errors, performance issues, or anything that looks out of the ordinary — **without needing labeled data**.

---

## 🛠️ How It Works
1. 📂 Load and clean log data using **Pandas** and **NumPy**
2. 🧾 Convert logs into a structured table format
3. 🔢 Assign severity scores to log levels (INFO, WARNING, ERROR, CRITICAL)
4. 🧠 Extract useful features like message length and log level score
5. 🤖 Apply **Isolation Forest** to detect anomalies
6. ✅ Display the results as normal or ❌ anomaly

---

## 🔄 Workflow

```text
📂 Load log file  
🧹 Clean and structure the data  
🧠 Train Isolation Forest model  
❓ Predict anomalies  
✅ Mark normal data  
❌ Mark outliers (anomalies)  
📊 Print or export the results  

📦 Required Libraries
Install all required packages using pip:


pip install pandas numpy scikit-learn

Run the Python script:

python aiops_log_analysis.py


📊 Sample Anomaly Output (Proper Table Format)
markdown
Copy
Edit
| Timestamp           | Level     | Message                                             | Message Length | Anomaly | Is Anomaly |
|---------------------|-----------|-----------------------------------------------------|----------------|---------|-------------|
| 2025-03-27 10:00:38 | WARNING   | User logged in                                     | 14             | -1      | ❌ Anomaly  |
| 2025-03-27 10:01:45 | CRITICAL  | User changed password                              | 21             | -1      | ❌ Anomaly  |
| 2025-03-27 10:01:44 | ERROR     | CPU usage at 95%                                   | 16             | -1      | ❌ Anomaly  |
| 2025-03-27 10:14:47 | WARNING   | Slow query detected: SELECT * FROM orders          | 41             | -1      | ❌ Anomaly  |
| 2025-03-27 11:02:44 | WARNING   | Unauthorized access attempt to admin panel         | 42             | -1      | ❌ Anomaly  |







