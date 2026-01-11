# Stock Market Data Analysis with yfinance

This project demonstrates how to retrieve, analyze, and visualize stock market data using the `yfinance` Python library. It focuses on real-world financial time-series data and shows how to work with both US and Turkish stock markets.

<img width="552" height="416" alt="68cd6639-fbed-4097-a1df-6e7d5acf47c9" src="https://github.com/user-attachments/assets/93a48449-6ce8-4596-b767-d2e76ed8f32b" />

<img width="552" height="408" alt="aedad384-f543-49d9-9cfd-381ab6998077" src="https://github.com/user-attachments/assets/c9c9eb73-afcd-40d5-adc8-a70731623e8c" />

## Project Overview

Using the `yfinance` library, this project:

- Fetches historical stock price data directly from Yahoo Finance
- Analyzes daily closing prices
- Compares multiple companies on the same chart
- Works with international stock tickers (NASDAQ & Borsa Istanbul)
- Visualizes long-term price trends using Python

The project is a practical introduction to financial data analysis and time-series visualization.

## Data Sources

All stock market data is retrieved from Yahoo Finance via the `yfinance` API.

Example tickers used:

- `GOOGL` — Google (Alphabet)
- `TSLA` — Tesla
- `AAPL` — Apple
- `MSFT` — Microsoft
- `AKBNK.IS` — Akbank (Turkey)
- `BAYRK.IS` — Baykar (Turkey)

Note: The `.IS` suffix denotes stocks listed on Borsa Istanbul.

## Technologies

- Python
- pandas
- matplotlib
- yfinance

## Installation

Install the required library:

```
pip install yfinance
```

## Project Features

1. Single Stock Analysis

- Fetches daily historical price data for a single ticker (e.g., `GOOGL`)
- Visualizes closing prices over a specified period (e.g., one year)
- Demonstrates use of the `Ticker` object and basic time-series plotting

2. Multi-Stock Comparison

- Downloads historical data for multiple companies simultaneously
- Compares groups such as US tech stocks and Turkish banking/defense stocks
- Plots closing prices on the same chart for trend comparison

3. Long-Term Time Series Visualization

- Analyzes stock performance over multiple years
- Identifies general price movement patterns and trend behavior
- Useful for exploratory financial analysis and visual storytelling

## Output

The project produces:

- Line charts of daily closing prices
- Comparative plots for multiple stocks
- Clean and interpretable time-series visualizations ready for reports or slides

## Example Usage

Load data and plot a single ticker:

```python
import yfinance as yf
import matplotlib.pyplot as plt

ticker = yf.Ticker('GOOGL')
df = ticker.history(period='1y')
df['Close'].plot(title='GOOGL - Last 1 Year')
plt.show()
```

For multiple tickers, use `yf.download(['TSLA','AAPL','MSFT'], start='2018-01-01')` to fetch and compare closing prices.
