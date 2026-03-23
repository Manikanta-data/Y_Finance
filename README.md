# 📊 Stock Market Analysis Dashboard (Python + PostgreSQL + Power BI)

## 🔍 Project Overview
This project is an end-to-end stock market data analysis pipeline built using Python, PostgreSQL, and Power BI. It extracts stock data from Yahoo Finance, processes it, stores it in a database, and visualizes it through an interactive dashboard.

The main goal is to generate meaningful insights for stock managers and support data-driven decision-making.

---

## 🎯 Objective
- Analyze stock performance of:
  - RELIANCE  
  - TCS  
  - INFOSYS  
- Build a complete ETL pipeline (Extract → Transform → Load)
- Create an interactive dashboard
- Enable automatic data refresh

---

## ⚙️ Technologies Used
- Python  
- yFinance API  
- Pandas  
- PostgreSQL  
- Power BI  

---

## 📥 Data Extraction
- Used `yfinance` library in Python
- Data details:
  - Interval: 5 minutes  
  - Duration: Last 7 days  
- Stocks:
  - RELIANCE.NS  
  - TCS.NS  
  - INFY.NS  

---

## 🔄 Data Processing (ETL)

Steps performed:
1. Extracted data using Yahoo Finance API  
2. Handled MultiIndex columns  
3. Converted timezone from UTC to IST  
4. Cleaned missing and infinite values  
5. Created calculated columns:
   - Return (percentage change)  
   - Moving Average (20)  
   - Moving Average (50)  

---

## 🗄 Database Integration (PostgreSQL)
- Connected Python to PostgreSQL using `psycopg2`
- Created table: `stock_data`
- Inserted data using batch processing
- Primary Key:
  - (company_name, timestamp)

---

## 🔄 Auto Refresh (Dynamic Update)

This project supports automatic updates:

### Python:
- Fetches latest stock data when script runs  
- Updates PostgreSQL table  
- Can be automated using Task Scheduler / Cron  

### Power BI:
- Connected to PostgreSQL  
- Clicking **Refresh** updates dashboard automatically  
- Can be scheduled in Power BI Service  

👉 Result: Near real-time data pipeline

---

## 📊 Dashboard Features
- KPI Cards:
  - Latest Close Price  
  - Average Returns  
  - Total Volume  
  - Average Close Price  

- Stock Price Trend  
- Moving Average Analysis  
- Trading Volume Analysis  
- Return Distribution  
- Volatility Analysis  
- Open vs Close Comparison  
- Candlestick Chart  

---

## 💡 Key Insights
- Identified stock trends across companies  
- Compared volatility levels  
- Analyzed trading volume behavior  
- Evaluated short-term vs long-term trends  

---

## 🚀 Why This Project?
- To build a real-world data pipeline  
- To practice financial data analysis  
- To provide meaningful insights for stock managers  
- To improve skills in Python, SQL, and Power BI  

---

## 🔮 Future Improvements
- Add real-time streaming  
- Deploy dashboard online  
- Add machine learning for prediction  
- Automate using Airflow  

---

## 👨‍💻 Author
Manikanta  
Aspiring Data Analyst / Business Analyst  

---

## ⭐ Conclusion
This project shows how raw stock data can be transformed into an automated dashboard that provides valuable insights for better decision-making.
