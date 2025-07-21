# VaRHistorical

In this project, I download financial data from yahoo finance to form a portfolio and calculate the 10 day VaR, which I create a histogram to visualize the VaR at the end. 

The portfolio consists of two index. 000300.SS is a free‑float‑weighted benchmark made up of the 300 largest, most liquid “A‑shares” traded on both the Shanghai and Shenzhen stock exchanges. It is the flagship index of China Securities Index Co. CYBU.AS is the iShares China CNY Bond UCITS ETF (USD‑hedged share‑class) listed on Euronext Amsterdam. It is not a stock or bond but an exchange‑traded fund managed by BlackRock’s iShares range. We download the past 2 years data from July 21, 2025.

Steps:

1.download data
2.use Ln to calculate the return respectively
3.assign the weight to CSI300 and ETF and calculate the weighted return
4.sum up the return
5.calculate the profit and loss in a 10-day segment
6.based on a 99% confidence interval, we find the corresponding VaR
7.graph the 10-day VaR
