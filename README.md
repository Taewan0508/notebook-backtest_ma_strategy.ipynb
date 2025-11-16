📈 Tesla Moving Average Backtest

This project tests a simple Moving Average Crossover Strategy on Tesla (TSLA) stock using Python, pandas, NumPy, and yfinance — all developed and visualized in Google Colab.
The goal is to compare the performance of a 20-day vs 50-day moving average trading strategy against a standard buy-and-hold strategy.

🧠 Overview
This project:

Downloads Tesla stock data (2020–2025) using yfinance
Calculates 20-day and 50-day moving averages
Generates Buy/Sell signals based on crossover rules
Calculates daily returns and strategy returns
Compares the cumulative performance of the moving-average strategy vs. buy-and-hold


📁 Project Structure
tesla_ma_strategy/
│
├── notebooks/
│   └── backtest_ma_strategy.ipynb     # Main notebook (this project)
│
├── results/
│   └── tsla_backtest.png              # Strategy performance chart
│
├── README.md
└── requirements.txt

📊 Strategy Logic

Buy Signal: when 20-day MA crosses above 50-day MA
Sell Signal: when 20-day MA crosses below 50-day MA

data['Signal'] = 0
data.loc[data['MA20'] > data['MA50'], 'Signal'] = 1
data.loc[data['MA20'] < data['MA50'], 'Signal'] = -1

🔍 Insights

The moving average strategy captures short-term momentum swings.
It avoids major drawdowns but can underperform during long uptrends due to late signals.
This project demonstrates the basics of rule-based quantitative trading.

🔮 Next Steps

Add more stocks and compare strategy performance
Optimize window lengths (e.g. 10-day, 100-day)
Incorporate risk metrics like Sharpe Ratio or Maximum Drawdown
Backtest with transaction costs

👤 Author
Taewan Park

