1. Abstract (Currently, as a student of financial engineer I am trying myself in different projects.So, currenmtly I am working on the DeFi 
sector,and specifically DEXs and effectiveness of liquidity provision as an yeild that is extra to HODL. So, in this part I am checking 
whether the financial result of a liquidity provider is dependant on the activity of arbitragers. We claim that due to alignment of 
DEX-CEX price by arbitragers' activity, the providers of liquidity to DEX pools lose part or more of their income.)
2. Hypothesis - 'LP Returns Are Negatively Correlated with Arbitrage Activity'
3. Data Collection
   - Dune SQL requests
   - Data: Extraction of Uniswap v3 ETH/USDC pool swaps, identification of arbitragers' transaction, LP fees. 
4. Methodology
   - The formula for arbitragers' activity 
   arb_sharet​= total_volumet​ / arb_volumet​​
   - The LP net return formula by E.Falkenstain(2026)
   LpValt =2⋅liq⋅pt  
   HODLt =USD0 +ETH0 ⋅p  
   ILt =LpValt −HODLt
   - Pearson correlation + p-value
   - OLS regression 
   LP_Net_PnLt​=β0​+β1​⋅arb_sharet​+εt​
5. Results
   - Regression & statistics 
   - 4 pgraphs
6. Conclusion
- Pearson r = -0.5738—a strong negative correlation. 
The more arbitrage, the worse LPs perform. This is exactly what Hypothesis 1.2 predicted.
P-value = 0.0000—the result is statistically significant at the p < 0.001 level. This isn't a fluke, but a consistent pattern in the data.
   - The hypothesis is correct - there is negative correlation between LP Returns and Arbitrage Activity. 
R² = 0.329 — arbitrage explains 33% of the variance in LP returns. This is a strong result for a single factor in financial data.
arb_share coef = -223.45 — for every 1 unit increase in arbitrage share, LP loses $223. Negative — the hypothesis is confirmed.
P-value = 0.000 — the result is significant at the p < 0.001 level. Not a fluke.
F-statistic = 43.20, Prob = 3.37e-09 — the model as a whole is significant.
