# NIKE-Stock-Market-Intelligence-
"A Power BI project analyzing Nike stock data (2022–2026) with Power Query, DAX, forecasting, volatility insights, KPIs, and interactive visuals for clear stock market intelligence."
📈 Nike Stock Market Intelligence Dashboard – Power BI

This project provides a complete Stock Market Intelligence Dashboard for Nike (NKE) using Power BI.
It includes price trends, volatility analysis, return patterns, forecasting, and interactive insights for data-driven decision-making.

🚀 Project Overview

The purpose of this project is to analyze Nike’s stock performance using real market data and present insights in the form of interactive Power BI dashboards.

The dashboard helps users understand:

Price movements
Daily return behavior
Volatility
Trend analysis
Future price forecasting
High–Low price range
Performance comparison
🛠️ Tools & Technologies
Tool	Purpose
Power BI	Data Modeling, DAX, Visualizations
Power Query	Data Cleaning & Transformations
Excel / CSV Data	Stock Price Source
DAX	Measures & KPIs
📊 Key Dashboard Features
✅ 1. Daily Closing Price Trend
Visual: Line Chart
X-Axis: Date
Y-Axis: Close Price
✅ 2. Volatility Analysis
Visual: Line Chart
X-Axis: Date
Y-Axis: Daily Return %
Helps track how volatile the stock is.
✅ 3. Price Range Chart (High − Low)
Visual: Column Chart
X-Axis: Date
Y-Axis: High − Low (Range)
✅ 4. Forecasting (Next 30 Days)
Visual: Line Chart
Use Analytics Pane → Forecast
Forecast Length: 30 Days
Shows expected future trend based on historical data.
✅ 5. Donut Chart (Distribution)

Examples:

Volume Share by Month
Months contributing highest volatility
Weekly trend distribution

Choose depending on your dashboard story.

📁 Project Structure
📦 Nike-Stock-Market-Intelligence
 ┣ 📊 Dashboard Screenshot/
 ┣ 📁 Data/
 ┣ 📄 Nike Stock Market.pbix
 ┣ 📄 README.md  ← (this file)
 ┗ 📄 PPT Presentation (optional)
📐 DAX Measures Used
Daily Return % = 
VAR PrevDay = CALCULATE(MAX('Data'[Close Price]), DATEADD('Data'[Date], -1, DAY))
RETURN
DIVIDE('Data'[Close Price] - PrevDay, PrevDay) * 100
High Low Range = 'Data'[High] - 'Data'[Low]
