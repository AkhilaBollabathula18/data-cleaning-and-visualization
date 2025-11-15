# Stock Market Data Pipeline & Dashboard

This project implements an end-to-end data pipeline using Python. It ingests raw stock market data, cleans and normalizes it, calculates key financial aggregations, and visualizes the results in an interactive Streamlit dashboard.

## 🛠️ Tech Stack
* **Language:** Python 3.12+
* **Package Manager:** [uv](https://github.com/astral-sh/uv) (for fast dependency management)
* **Libraries:** Pandas, Streamlit, Pyarrow (Parquet)

## 📂 Project Structure

| File | Description |
| :--- | :--- |
| `etl_process2.py` | **Step 1:** Loads raw CSV, normalizes headers, cleans nulls/types, and saves `cleaned.parquet`. |
| `aggregations.py` | **Step 2:** Reads cleaned data and generates 3 aggregation files (Daily Close, Sector Volume, Returns). |
| `dashboard.py` | **Step 3:** Streamlit application to visualize the aggregated data. |
| `stock_market.csv` | Raw input data. |
| `pyproject.toml` | Project dependencies managed by `uv`. |

## 🚀 How to Run

Ensure you have [uv installed](https://github.com/astral-sh/uv).

### 1. Setup Environment
Initialize the project and install dependencies:
```bash
uv sync