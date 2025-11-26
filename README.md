# NovaFin-Sentiment: Predicting Price Moves with News Sentiment

## 🚀 Project Overview
This project investigated the correlation between daily financial news sentiment and stock price movements for major technology stocks (AAPL, AMZN, GOOG, META, MSFT, NVDA). The methodology involved three phases: **Exploratory Data Analysis (EDA)**, **Quantitative Analysis (Technical Indicators)**, and **Final Correlation Analysis (Task 3)**.

The final analysis confirmed a moderate, statistically reliable positive correlation for NVDA (+0.52), showing that quantified news sentiment can serve as a confirmation signal for technical trading strategies.

---

## 💡 Key Finding: The NVDA Sentiment Signal
- **Correlation:** +0.52 Pearson correlation coefficient between average daily news sentiment and daily % return for NVDA.  
- **Reliability:** Based on the highest reliable overlapping data points (N=4).  
- **Strategy:** Use positive sentiment (VADER score > 0.2) to confirm bullish signals from SMA and RSI.

---

## 🛠️ Project Structure and Deliverables

### Directory
| Directory | Content |
|-----------|---------|
| `data/` | Raw and prepared datasets. |
| `data/yfinance_data/` | Raw stock price CSVs (AAPL, AMZN, GOOG, META, MSFT, NVDA). |
| `notebooks/` | Primary analysis notebooks. |
| `src/` | Reusable Python scripts and helper modules. |
| `tests/` | Pytest unit tests for CI. |
| `plots/` | Final visualizations including correlation and EDA plots. |

### Notebooks
- `01_news_data_eda.ipynb` – Cleaning, tokenizing, and analyzing news headlines (Task 1).  
- `02_financial_analysis.ipynb` – Quantitative analysis, indicators (SMA, RSI, MACD, BBANDS), Daily Return (Task 2).  
- `03_correlation_analysis.ipynb` – Merges sentiment with financial data, calculates correlations, generates plots (Task 3).

---

## ⚙️ Setup and Dependencies

1. **Clone the Repository:**

    ```bash
    git clone https://github.com/AstraMeron/NovaFin-Sentiment.git
    cd NovaFin-Sentiment
    ```

2. **Create and Activate Virtual Environment (using venv):**

    ```bash
    # Create the environment
    python -m venv venv

    # Activate (Windows PowerShell)
    .\venv\Scripts\activate

    # Activate (Linux/macOS)
    source venv/bin/activate
    ```

3. **Install Dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

    > **Note:** TA-Lib may require special installation on some systems.

---

## 🏃 Running the Analysis

Run the notebooks in the following order:

```bash
# 1. Exploratory Data Analysis on news data
01_news_data_eda.ipynb

# 2. Quantitative analysis of financial data
02_financial_analysis.ipynb

# 3. Correlation analysis between sentiment and market indicators
03_correlation_analysis.ipynb