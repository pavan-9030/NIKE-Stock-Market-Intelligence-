# NIKE-Stock-Market-Intelligence
Project Overview

This project presents a complete Stock Market Intelligence Dashboard for Nike using Power BI. The dashboard analyzes Nike’s stock market performance from 2022 to 2026 and provides interactive insights into price trends, volatility, returns, forecasting, and overall market behavior.

The objective of this project is to transform raw stock market data into meaningful business intelligence that supports data-driven decision-making.

Objectives

The dashboard helps users understand:

Daily stock price movements
Return and volatility patterns
High–Low price fluctuations
Trend analysis over time
Future stock price forecasting
Trading volume behavior
Performance insights through KPIs and visuals
Tools & Technologies Used
Tool	Purpose
Microsoft Power BI	Dashboard creation, data modeling, DAX, visualizations
Power Query	Data cleaning and transformation
Excel / CSV	Stock market dataset source
DAX	Calculated measures and KPIs
Dataset Information

The dataset contains Nike stock market data from 2022–2026, including:

Date
Open Price
Close Price
High Price
Low Price
Volume
Key Dashboard Features
1. Daily Closing Price Trend

Visual: Line Chart

X-Axis: Date
Y-Axis: Close Price

This visualization tracks Nike’s daily closing stock price and helps identify upward or downward market trends over time.

2. Volatility Analysis

Visual: Line Chart

X-Axis: Date
Y-Axis: Daily Return %

This analysis measures stock volatility and highlights periods of higher market fluctuations.

3. High–Low Price Range Analysis

Visual: Column Chart

X-Axis: Date
Y-Axis: High − Low Price Range

This chart shows daily price movement ranges and helps identify highly volatile trading days.

4. Stock Price Forecasting

Visual: Forecast Line Chart

Using the Analytics Pane → Forecast feature in Power BI:

Forecast Length: 30 Days
Based on historical stock price trends

This feature predicts potential future stock movements and assists in trend analysis.

5. Volume Distribution Analysis

Visual: Donut Chart

Possible insights include:

Monthly trading volume distribution
Months with highest volatility
Weekly market activity trends

This helps users understand trading behavior and market participation patterns.

KPI Metrics Included

The dashboard includes important stock market KPIs such as:

Average Closing Price
Highest Stock Price
Lowest Stock Price
Total Trading Volume
Average Daily Return %
Volatility Indicator
DAX Measures Used
Daily Return %

Daily Return %=
Previous Close Price
Current Close Price−Previous Close Price
	​

×100

Daily Return % =
VAR PrevDay =
    CALCULATE(
        MAX('Data'[Close Price]),
        DATEADD('Data'[Date], -1, DAY)
    )
RETURN
    DIVIDE('Data'[Close Price] - PrevDay, PrevDay) * 100
High–Low Range

High-Low Range=High Price−Low Price

High Low Range =
'Data'[High] - 'Data'[Low]
Dashboard Insights

The dashboard enables users to:

Monitor long-term stock trends
Identify periods of high volatility
Analyze trading activity patterns
Compare stock performance over time
Predict possible future price movements
Project Structure
Nike-Stock-Market-Intelligence/
│
├── Dashboard Screenshot/
├── Data/
├── Nike Stock Market.pbix
├── README.md
└── PPT Presentation/
Conclusion

This project demonstrates how Microsoft Power BI can be used to transform stock market data into powerful interactive dashboards. By combining Power Query, DAX calculations, forecasting, and advanced visualizations, the dashboard delivers clear and actionable stock market intelligence for Nike.
