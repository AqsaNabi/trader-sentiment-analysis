# Trader Behavior and Market Sentiment Analysis

This project investigates the relationship between trader performance and Bitcoin market sentiment using two datasets: the Fear & Greed Index and historical trader data from the Hyperliquid exchange. The goal is to determine how market sentiment influences trading behavior, such as profitability, trade size, and trading direction.

This work was completed as part of the Junior Data Scientist – Trader Behavior Insights assignment.

---

## Datasets

1. **Fear & Greed Index**
   - Columns: `date`, `classification` (e.g., Fear, Greed, Neutral)
   - Captures overall market sentiment on a daily basis.

2. **Hyperliquid Historical Trader Data**
   - Columns include: `Timestamp IST`, `Side`, `Size USD`, `Symbol`, `Closed PnL`, etc.
   - Represents trade-by-trade data from individual accounts.

---

## Objective

- To explore how different market sentiments (Fear, Greed) affect:
  - Trader profitability (`Closed PnL`)
  - Trade size (`Size USD`)
  - Trading behavior (`Side`: BUY/SELL)

- To extract insights that can inform smarter trading strategies.

---

## Methodology

1. **Data Preparation**
   - Parsed and standardized date formats.
   - Merged the sentiment dataset with trading data using a common `date` column.
   - Cleaned rows with invalid timestamps or missing values.

2. **Exploratory Analysis**
   - Grouped data by `classification` to examine how sentiment affects trading outcomes.
   - Calculated average and distribution of key metrics per sentiment.
   - Visualized distributions of PnL, trade size, and BUY/SELL counts.

3. **Visualizations**
   - Boxplots comparing `Closed PnL` across sentiment categories.
   - Count plots showing trade direction under each sentiment.
   - Strip plots overlaying individual trade behavior on group summaries.

---

## Key Findings

- Average `Closed PnL` tended to be higher during periods of Fear than during periods of Greed.
- Traders generally placed larger trades (`Size USD`) when sentiment was Greed, suggesting increased risk-taking.
- A higher proportion of SELL orders was observed during Fear, likely due to market uncertainty.
- Sentiment appears to influence both behavior (e.g., direction) and performance (PnL).

---

## Technologies Used

- Python 3.x
- Pandas
- Seaborn
- Matplotlib
- Google Colab (for execution)

---

## How to Run This Project

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/trader-sentiment-analysis.git
   cd trader-sentiment-analysis

