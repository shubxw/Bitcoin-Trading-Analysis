# Bitcoin Trading Behaviour Analysis Using Fear & Greed Index

This project analyses Bitcoin trading behaviour and performance under different market sentiment regimes using the Fear & Greed Index. The goal is to understand how sentiment impacts trader behaviour, performance, and risk, and to derive actionable, theoretical strategy insights.

---

## 📂 Project Structure

- `historical_data.csv` — Trade-level Bitcoin transaction data  
- `fear_greed_index.csv` — Daily Fear & Greed Index data  
- `analysis.ipynb` — Main analysis notebook (data cleaning, metrics, visualisations)

---

## ⚙️ Setup

### Requirements
- Python 3.8+
- pandas
- numpy
- matplotlib
- seaborn

Install dependencies:
```bash
pip install pandas numpy matplotlib seaborn


## Analysis Summary

### Methodology
This analysis combines trade-level Bitcoin transaction data with the daily Fear & Greed Index to study how market sentiment impacts trader performance and behaviour. Trading data was aggregated at a daily level to compute key performance metrics, including daily PnL, win rate, and PnL volatility as a proxy for drawdown risk. Trader behaviour was analysed across leverage usage, trade frequency, directional bias, and position size. Traders were further segmented into groups based on leverage, trading frequency, and PnL consistency using quantile-based thresholds.

### Key Insights
- Trader performance varies significantly across sentiment regimes, with the strongest performance observed during Fear periods and weaker outcomes during Greed, Extreme Greed, and Neutral conditions.
- Leverage usage and position sizes increase notably during Fear regimes, indicating stress-driven or opportunistic risk-taking rather than confidence-driven behaviour.
- Low-leverage and consistent traders deliver more stable and higher average profits across all sentiment conditions, while high-leverage and inconsistent traders experience larger losses and volatility.
- Frequent traders consistently achieve higher win rates than infrequent traders, suggesting improved adaptability and execution quality.

### Strategy Recommendations (Theoretical)
- **Risk control during Fear regimes:** During Fear periods, leverage and position sizes should be reduced for high-leverage and inconsistent traders to mitigate elevated drawdown risk.
- **Selective risk-taking during Greed regimes:** During Greed periods, increased trading activity should be limited to historically frequent and consistent traders, while less consistent participants should cap exposure to avoid sentiment-driven losses.
