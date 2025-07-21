## 📊 10‑Day Value‑at‑Risk (VaR) Analysis

This mini‑project downloads two Chinese market instruments from **Yahoo Finance**, builds a two‑asset portfolio, and visualizes its 10‑day 99 % Historical VaR with a histogram.

### Data Universe

| Ticker | Instrument | Description |
|--------|-----------|-------------|
| `000300.SS` | **CSI 300 Index** | Free‑float‑weighted benchmark of the 300 largest, most liquid A‑shares on the Shanghai & Shenzhen Stock Exchanges. |
| `CYBU.AS` | **iShares China CNY Bond UCITS ETF (USD‑hedged)** | ETF providing on‑shore CNY bond exposure, fully currency‑hedged to USD, listed on Euronext Amsterdam. |

> **Look‑back window:** last 2 years (from 21 July 2023 to 21 July 2025)

### Methodology

1. **Download daily closes** for
