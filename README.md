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
Install all required packages using pip:

pip install pandas numpy scikit-learn


▶️ How to Run
Place your log file (e.g., system_logs.txt) in the project folder

Run the script using the command below:
cd ai-assisted-devops/day-6
python aiops_log_analysis.py

🧪 Sample Output

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
941 2025-03-27 11:02:44   WARNING      Unauthorized access attempt to admin panel              42       -1   ❌ Anomaly
💡 Extra Tips
Want the model to detect fewer anomalies? Lower the contamination value:

python
Copy
Edit
model = IsolationForest(contamination=0.05)
The model randomly selects features to build trees 🌳 — and isolates anomalies by separating them faster than normal points.

✅ Ending Notes
✅ Helps detect unusual patterns in logs easily

🔍 Great for security, system monitoring, and DevOps alerts

📈 Can scale and update with real-time logs

🧠 No need for labeled data — unsupervised learning at work

✅ Marks normal entries

❌ Flags anomalies clearly

📁 Folder Structure (Optional)
text
Copy
Edit
ai-assisted-devops/
│
└── day-6/
    ├── system_logs.txt         # Your input log file
    ├── aiops_log_analysis.py   # Python script to analyze logs
    └── README.md               # Project documentation
📬 Contact / Credits
Made with 💻 by [Your Name]
Feel free to fork, improve, or ask questions!

python
Copy
Edit

---

### ✅ Final Tip:
Replace `[Your Name]` with your actual name or GitHub handle.  
If you'd like to include screenshots or badges, I can help you add those too.

Let me know when you're ready for that!



You said:
           timestamp     level                                         message  message_length  anomaly  is_anomaly
19 2025-03-27 10:00:38 WARNING User logged in 14 -1 ❌ Anomaly 21 2025-03-27 10:01:45 CRITICAL User changed password 21 -1 ❌ Anomaly 26 2025-03-27 10:01:44 ERROR CPU usage at 95% 16 -1 ❌ Anomaly 887 2025-03-27 10:14:47 WARNING Slow query detected: SELECT * FROM orders 41 -1 ❌ Anomaly 941 2025-03-27 11:02:44 WARNING Unauthorized access attempt to admin panel 42 -1 ❌ Anomalywhy it is coming ikethis

ChatGPT said:
Ah, I see what happened! You're trying to display a formatted table in your GitHub README, but when you paste plain text like that, GitHub doesn't automatically format it into a readable table — it turns into a jumbled line of text.

✅ Solution: Use Markdown Tables
To make it clean and readable in your README.md, you should use Markdown table syntax. Here’s how to format your anomaly output correctly:

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







