# Python Project - Investment Analysis and Strategy

This project provides a simple, complete and accessible solution for a finance project in Python.
> ⚠️ This project is for academic and educational purposes only

## Project objectives
The project is divided into 4 parts:

1. building a financial database;
2. defining an investment strategy;
3. allocating and managing a portfolio;
4. backtesting over more than 5 years.

The code style is intentionally kept simple to remain close to a beginner level.

---

## Project Choices

- **Data source:** Yahoo Finance via `yfinance`
- **Number of companies:** 30 American stocks
- **Time period:** January 1, 2020 to March 1, 2026
- **Frequency:** Daily
- **Benchmark:** S&P 500 (`^GSPC`)

---

## Strategy

The strategy is a straightforward trend-following approach:

- A **short moving average** is calculated over **20 days**
- A **long moving average** is calculated over **50 days**
- If the 20-day moving average is **above** the 50-day moving average, the stock is selected
- Otherwise, the stock is excluded

Additional rules:

- The portfolio is **rebalanced at the start of each month**
- A **maximum of 10 stocks** are held at any time
- Selected stocks are assigned **equal weights**

---

## File Structure

├── src/
│   ├── pycache/
│   ├── config.py                   # project parameters
│   ├── data_loader.py              # data download and preparation
│   ├── strategy.py                 # signal computation
│   ├── portfolio.py                # portfolio allocation
│   └── backtest.py                 # simulation and results
│
├── outputs/
│   ├── price_data.csv              # historical stock prices
│   ├── benchmark_data.csv          # historical benchmark prices
│   ├── signals.csv                 # buy signals
│   ├── portfolio_weights.csv       # portfolio weights over time
│   ├── portfolio_value.csv         # portfolio value evolution
│   ├── trade_results.csv         
│   └── summary.txt                 
│
├── pycache/
│   └── main.cpython-312.pyc
│
├── main.py                         
├── rapport_projet.md               # written project report
├── requirements.txt                
└── README.md

---

## Installation

```bash
pip install -r requirements.txt
```

## Output Files

The script generates an `outputs/` folder containing:

| File | Description |
|------|-------------|
| `price_data.csv` | Historical stock prices |
| `benchmark_data.csv` | Historical benchmark prices |
| `signals.csv` | Buy signals |
| `portfolio_weights.csv` | Portfolio weights over time |
| `portfolio_value.csv` | Portfolio value evolution |
| `trade_results.csv` | Detailed trade records |
| `summary.txt` | Final performance summary |

## Note

```bash
Data download requires an active internet connection at runtime.
```

## Author

**Joël Mwemba**
Engineering Student

