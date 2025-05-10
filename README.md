# Automated Trading System/ AlgoTrading with Machine Learning

## Overview

This project is an automated trading system that utilizes historical market data to generate trading signals and execute trades using the OANDA API. The system analyzes price patterns to determine when to buy or sell a currency pair (EUR/USD).

## Features

- **Market Data Retrieval**: Fetches historical data using the Yahoo Finance API.
- **Signal Generation**: Implements a custom signal generator to identify bullish and bearish patterns.
- **Trade Execution**: Connects to the OANDA API to place market orders based on generated signals.
- **Automated Scheduling**: Uses APScheduler to execute trades at specified intervals.

## Technologies Used

- Python
- Yahoo Finance API
- OANDA API
- Pandas
- APScheduler

## Getting Started

### Prerequisites

- Python 3.x
- Required libraries: `yfinance`, `pandas`, `apscheduler`, `oandapyV20`.

### Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/automated-trading-system.git
    cd automated-trading-system
    ```

2. Install the required libraries:
    ```bash
    pip install yfinance pandas apscheduler oandapyV20
    ```

3. Create a `config.py` file with your OANDA credentials:
    ```python
    access_token = 'YOUR_ACCESS_TOKEN'
    accountID = 'YOUR_ACCOUNT_ID'
    ```

### Running the System

1. Start the trading job:
    ```bash
    python trading_bot.py
    ```

2. The bot will fetch market data, generate signals, and execute trades as per the defined logic.

## How It Works

- The system retrieves historical EUR/USD data at 15-minute intervals.
- A signal generator function analyzes the latest price data to detect bullish or bearish patterns.
- Depending on the generated signal, it places buy or sell orders through the OANDA API.
- The system can be scheduled to run automatically at specified times using APScheduler.

## Contributing

Contributions are welcome! If you have ideas for improvements or features, please fork the repository and submit a pull request.

## License

This project is licensed under the MIT License.

## Acknowledgments

Inspired by various trading strategies and the need for automation in trading.
