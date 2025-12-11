Real-Time Simulated UPI Fraud Detection System

This project simulates real-time UPI transactions and detects fraudulent activity using a trained Random Forest Machine Learning model.
It includes:
✔ FastAPI backend
✔ Real-time transaction simulator
✔ Streamlit dashboard
✔ Database integration (MySQL/SQLite)

The system is designed to mimic live UPI payment activity and classify transactions as Fraudulent or Legitimate in real time.

Features
🔹 Real-Time Transaction Simulation

Automatically generates dummy UPI transactions every few seconds

Sends them to the ML model via API

🔹 FastAPI Backend

Exposes a /predict API endpoint

Loads trained Random Forest model (model.pkl)

Returns fraud probability + fraud/legit label

🔹 Streamlit Dashboard

Live monitoring of transactions

Fraud alerts

Probability graphs and analytics

Real-time updates

🔹 Database Support

Stores transactions in MySQL.

Dashboard fetches data continuously.

▶️ How to Run This Project
Start FastAPI Backend
uvicorn main:app --reload


Your API starts here:
http://127.0.0.1:8000/docs

2️⃣ Start Real-Time Transaction Simulator
python simulate_transactions.py


This begins generating UPI transactions.

3️⃣ Start Streamlit Dashboard
streamlit run streamlit_dashboard.py


Dashboard opens here:
http://localhost:8501/

📌 Tech Stack

Python

FastAPI

Streamlit

Random Forest (scikit-learn)

Pandas, NumPy

MySQL / SQLite


✨ Output Example
Transaction ID: 101  
Amount: ₹4500  
Fraud Probability: 0.92  
Status: FRAUD ⚠️


How the System Works (Flow)
simulate_transactions.py  
        ↓ (API request)
FastAPI (main.py)  
        ↓ (Model prediction)
Random Forest Model  
        ↓ (Response)
Streamlit Dashboard  
        ↓ (Live View)
User sees real-time fraud detection
