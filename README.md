# NovaFin-Sentiment: Predicting Price Moves with News Sentiment

## 🚀 Project Overview

This project aims to investigate the correlation between financial news sentiment and stock price movements for a basket of major technology stocks (AAPL, AMZN, GOOG, META, MSFT, NVDA). The methodology involves two core phases: **Exploratory Data Analysis (EDA) & Sentiment Preparation** of historical news headlines, and **Quantitative Analysis** using technical indicators.

The final goal is to merge these data sources to test the hypothesis that shifts in news sentiment can act as a leading or coincident indicator of stock price changes.

---

## 🛠️ Project Structure and Deliverables

| Directory | Content |
| :--- | :--- |
| `data/` | Contains the raw and prepared datasets. |
| `data/yfinance_data/` | Contains the raw stock price history CSVs (AAPL, AMZN, GOOG, META, MSFT, NVDA). |
| `notebooks/` | Contains the primary analysis files. |
| `src/` | Holds reusable Python scripts and helper modules. |
| `tests/` | Contains Pytest unit tests for continuous integration (CI). |

### Notebooks

1.  **`01_news_data_eda.ipynb` (Task 1 Complete):** Focuses on cleaning, tokenizing, and analyzing news headlines. It prepares the data for eventual sentiment scoring and resolves dependency challenges (e.g., NLTK `LookupError`).
2.  **`02_financial_analysis.ipynb` (Task 2 Complete):** Focuses on loading and applying quantitative analysis to all six stock tickers. It uses `TA-Lib` to calculate indicators (SMA, RSI, MACD, BBANDS) and financial metrics (Daily Return).
3.  **`03_correlation_analysis.ipynb` (Next Step):** (To be created) Will merge the sentiment scores with the financial data to calculate correlation coefficients.

---

## ⚙️ Setup and Dependencies

This project uses a standard Python virtual environment.

### Prerequisites

1.  Clone the repository:
    ```bash
    git clone [https://github.com/AstraMeron/NovaFin-Sentiment.git](https://github.com/AstraMeron/NovaFin-Sentiment.git)
    cd NovaFin-Sentiment
    ```

2.  Create and activate the virtual environment:
    ```bash
    python -m venv venv
    .\venv\Scripts\activate  # On Windows PowerShell
    # source venv/bin/activate  # On Linux/macOS
    ```

3.  Install Dependencies:
    ```bash
    pip install -r requirements.txt
    # NOTE: TA-Lib dependency may require special installation on some systems.
    ```

### Running the Analysis

To reproduce the analysis, open the following notebooks in sequence:
1.  **`01_news_data_eda.ipynb`**
2.  **`02_financial_analysis.ipynb`**

### Continuous Integration (CI)

Unit tests are configured via GitHub Actions. Workflows are triggered on push to ensure code quality. CI challenges encountered during Task 1 related to environment setup and NLTK dependency loading were resolved to ensure reliable testing.

---

## 📝 Interim Submission Status

| Deliverable | Status | Branch |
| :--- | :--- | :--- |
| **Task 1: EDA & Sentiment Prep** | ✅ Complete | `main` |
| **Task 2: Quantitative Analysis** | ✅ Complete | `main` |
| **Current Progress** | Data fully prepared for Correlation Analysis. | `main` |