# Personal Financial-Planner

This repository contains two financial planning tools that leverage modern investment data sources and Monte Carlo simulations to help individuals assess their personal financial health and retirement planning. The two primary tools developed here are:

Personal Financial Planner - Helps individuals assess their emergency fund based on cryptocurrency and stock holdings.
Retirement Planning Tool - Uses Monte Carlo simulations to forecast retirement portfolio performance over a specified period using stocks and bonds.


## Files Overview

1. ```financial-planner.ipynb```: This Jupyter Notebook contains the main code to create the Personal Finance Planner and Retirement Planning Tool. It performs the following key tasks:

* Fetches cryptocurrency and stock data using public APIs.
* Calculates the total value of a user's savings and investments.
* Projects retirement portfolio performance using Monte Carlo simulations based on stock and bond historical data fetched from the Alpaca API.
2. ```MCForecastTools.py```: This Python module contains the MCSimulation class used to simulate future returns of a retirement portfolio using Monte Carlo methods. The class takes historical price data, simulates various potential future outcomes, and provides performance metrics.


## Setup Instruction

### Prerequisites
To run this project, ensure you have the following dependencies installed in your environment:

* Python 3.7+
* pandas
* numpy
* alpaca-trade-api
* requests
* matplotlib
* dotenv (for loading environment variables)

You will also need to set up an account and API keys for Alpaca, a stock and crypto trading platform, to fetch historical market data.

## Personal Financial Planner
The Personal Financial Planner allows users to:
1. Fetch the latest prices for their cryptocurrency and stock holdings.
2. Assess if their current portfolio is sufficient to act as an emergency fund.
3. Visualize their portfolio composition.

### Key Steps
1. Fetch Crypto Prices: Using the requests library, we fetch current prices for cryptocurrencies such as Bitcoin (BTC) and Ethereum (ETH) from the Alternative.me Crypto API.

2. Fetch Stock Prices: Using the Alpaca API, we fetch the latest stock prices for stocks such as SPY (S&P 500 ETF) and other desired assets.

3. Portfolio Assessment: The notebook calculates the total value of the user's stock and crypto holdings and compares it to a predefined emergency fund requirement (e.g., three months of expenses).

## Retirement Planning Tool
The Retirement Planning Tool helps users project the future value of their investment portfolio based on historical market data using Monte Carlo simulations. This tool considers a portfolio of stocks and bonds and simulates thousands of possible future outcomes based on historical returns.
### Key Steps
1. Fetch Historical Data: Historical stock and bond prices are fetched using the Alpaca API for assets like SPY (stocks) and AGG (bonds).

2. Monte Carlo Simulations: The MCSimulation class in MCForecastTools.py runs the Monte Carlo simulations to project possible future returns over a specified period (e.g., 30 years).

3. Calculate Expected Returns: Using the Monte Carlo results, the tool provides potential portfolio outcomes, including the expected portfolio value over time, as well as the 95% confidence intervals for the projections.

## Conclusion
This repository provides a powerful set of tools for individuals to better understand and plan their finances. By leveraging real-time data and advanced statistical methods like Monte Carlo simulations, users can assess both their short-term financial health and long-term retirement prospects.

​