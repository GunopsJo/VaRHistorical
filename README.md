## 📊 10‑Day Value‑at‑Risk (VaR) Analysis

This mini‑project downloads two Chinese market instruments from **Yahoo Finance**, builds a two‑asset portfolio, and visualizes its 10‑day 99 % Historical VaR with a histogram.

### Data Universe

| Ticker | Instrument | Description |
|--------|-----------|-------------|
| `^GSPC` | **S&P 500 Index** | Free‑float‑weighted benchmark of the 300 largest,. |
| `XBB.TO` | **iShares Core Canadian Universe Bond Index ETF** | |

> **Look‑back window:** last 2 years (from 21 July 2023 to 21 July 2025)

### Methodology

1. **Download daily closes** for both tickers via `yfinance`.
2. **Compute daily log returns**:  
3. **Assign portfolio weights**  
   • S&P 500 Index —— 60 %  
   • iShares Core Canadian Universe Bond Index ETF —— 40 %
4. **Calculate weighted return** per day and **aggregate** to a total portfolio return.  
5. **Roll up into 10‑day profit‑and‑loss (P/L)** blocks using a rolling window sum.  
6. **Historical 99 % VaR**: take the 1 % left‑tail quantile of the 10‑day P/L distribution.  
7. **Plot results**  
   * Histogram of 10‑day P/L  
   * Red dashed line marking the VaR threshold  
   * Shaded tail (losses ≤ VaR) for quick visual risk assessment.

### Deliverables


<img width="562" height="455" alt="image" src="https://github.com/user-attachments/assets/56ea8cc0-12da-4d26-8020-f6975c441029" />


