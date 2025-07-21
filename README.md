## 📊 10‑Day Value‑at‑Risk (VaR) Analysis

This mini‑project downloads two Chinese market instruments from **Yahoo Finance**, builds a two‑asset portfolio, and visualizes its 10‑day 99 % Historical VaR with a histogram.

### Data Universe

| Ticker | Instrument | Description |
|--------|-----------|-------------|
| `000300.SS` | **CSI 300 Index** | Free‑float‑weighted benchmark of the 300 largest, most liquid A‑shares on the Shanghai & Shenzhen Stock Exchanges. |
| `CYBU.AS` | **iShares China CNY Bond UCITS ETF (USD‑hedged)** | ETF providing on‑shore CNY bond exposure, fully currency‑hedged to USD, listed on Euronext Amsterdam. |

> **Look‑back window:** last 2 years (from 21 July 2023 to 21 July 2025)

### Methodology

1. **Download daily closes** for both tickers via `yfinance`.
2. **Compute daily log returns**:  
   \[
   r_{t} = \ln\!\bigl(\tfrac{P_{t}}{P_{t-1}}\bigr)
   \]
3. **Assign portfolio weights**  
   • CSI 300 Index —— 60 %  
   • CYBU ETF —— 40 %
4. **Calculate weighted return** per day and **aggregate** to a total portfolio return.  
5. **Roll up into 10‑day profit‑and‑loss (P/L)** blocks using a rolling window sum.  
6. **Historical 99 % VaR**: take the 1 % left‑tail quantile of the 10‑day P/L distribution.  
7. **Plot results**  
   * Histogram of 10‑day P/L  
   * Red dashed line marking the VaR threshold  
   * Shaded tail (losses ≤ VaR) for quick visual risk assessment.

### Deliverables

<img width="562" height="455" alt="image" src="https://github.com/user-attachments/assets/99f07dff-66d7-4c22-b15c-467e78ab2a9b" />

