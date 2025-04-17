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

contamination=0.1 → We assume ~10% of logs are anomalies 📉

random_state=42 → Ensures results are reproducible every time 🎲

🔄 Workflow
text
Copy
Edit
📂 Load log file
🧹 Clean and structure the data
🧠 Train Isolation Forest model
❓ Predict anomalies
✅ Mark normal data
❌ Mark outliers (anomalies)
📊 Print or export the results
📦 Required Libraries
Install dependencies using pip:

bash
Copy
Edit
pip install pandas numpy scikit-learn
▶️ How to Run
Place your log file (e.g., system_logs.txt) in the project folder

Run the script:

bash
Copy
Edit
cd ai-assisted-devops/day-6
python aiops_log_analysis.py
🧪 Sample Output
plaintext
Copy
Edit
🔍 **Detected Anomalies:**

               timestamp     level                                         message  message_length  anomaly  is_anomaly
--------------------------------------------------------------------------------------------------------------
19  2025-03-27 10:00:38   WARNING                                  User logged in              14       -1   ❌ Anomaly
21  2025-03-27 10:01:45  CRITICAL                           User changed password              21       -1   ❌ Anomaly
26  2025-03-27 10:01:44     ERROR                                CPU usage at 95%              16       -1   ❌ Anomaly
887 2025-03-27 10:14:47   WARNING       Slow query detected: SELECT * FROM orders              41       -1   ❌ Anomaly
941 2025-03-27 11:02:44   WARNING      Unauthorized access attempt to admin panel              42    
