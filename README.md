The Market Sentiment & Trader Performance Deep Dive


The goal is simple: to provide a data-driven answer on how market psychology influences trading activity and, most importantly, profit and loss (PnL).
The analysis relies on combining two distinct datasets:

1. Market Sentiment (fear_greed_index.csv): Time-series data tracking the overall emotional state of the market, classified into categories like "Extreme Fear," "Fear," "Neutral," "Greed," and "Extreme Greed."

2. Historical Trades (historical_data.csv): Raw trading data including execution price, trade size, position details (Start Position), trade direction (Side), and the resulting profit or loss (Closed PnL).

The notebook cleans, formats, and merges these datasets by date to create a unified view of trade performance overlaid with market sentiment.

It merges two key datasets into a new_data set - a Fear & Greed Index (market sentiment) as data1 and real historical trading data as data2 to uncover patterns in trader behavior, profitability, and risk-taking across different emotional states of the market.

Sentiment Distribution Analysis
Visualizes the proportion of time the market spent in various states (e.g., "Extreme Fear," "Neutral," "Greed").
For example, **"Fear"** was the most common market sentiment in the provided index.

Performance and Anomaly Analysis:
1.Plots the Average Daily Pnl across different sentiment classifications over time.
2.Examines the distribution of trade volume and PnL across different sentiment levels and trade sides (BUY vs SELL)

Key Insights & Analysis

Sentiment Distribution
A clear visualization showing how often the market was in a state of Fear, Greed, or Neutrality over the historical period.

PnL Over Time
A time-series chart plotting the Average Daily Trader PnL (Profit and Loss) against different market sentiments, helping to visualize if certain emotional periods are consistently more profitable (or costly) than others.

High-Risk Anomaly Detection
It specifically identifies trades taken with high leverage/position sizes (above the 90th percentile of Start Position) during periods of "Greed" to see if "hot-headed" trading pays off or leads to disaster.

Trader Activity Profile 
Analysis showing the trade count per market account, identifying the most active traders in the dataset.

Sentiment & Trade Side Correlation
A breakdown showing how mean PnL and average position size differ depending on whether traders were Buying or Selling during specific sentiment classifications (e.g., "Are people more profitable when they 'Buy the Fear' or 'Sell the Greed'?").

How to Run It
This notebook is built for simplicity and uses common Python libraries.

Dependencies:
You will need the following libraries installed:

pandas - Data loading and manipulation

numpy - Numerical operations

matplotlib - Basic data visualization

seaborn - Enhanced statistical data visualization

Data Setup:
Ensure the following files are in the same directory (or path) as the notebook:

fear_greed_index.csv as data1

historical_data.csv asa data2

Give the path of datasets correctly or else an error will be thrown

Execution:
Simply open the prime.ipynb file in your Jupyter environment (like Google Colab, JupyterLab, or VS Code) and run the cells sequentially and the output will be displayed.





