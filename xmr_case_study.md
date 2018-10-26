# XMR Case Study

This document details a performance study of the FPG system. We specifically show cases for Monero (XMR) liquidation. Here, we compare the performance of particularly two aspects of the FPG system: Aggregating liquidity, and using market making tools. We first show aggregate liquidity gains, then market making performance increases. Results here are both backtested, and ran through real transactions. 

Trade reports, screenshots, and excel calculations are available upon request. 

# Test Cases

## 1. Purchasing on single-exchange versus on FPG Aggregate

These tests look at buying on the FPG aggregate versus a single exchange. They show the benefits of using aggregate liquidity. 

### 1.A Buying 10k$ XMR: 

>         Binance (leading exchange) : .47% slippage
>                                FPG : .21% slippage
>                         Difference : .26% Savings!!!

Description of test: This is looking at buying on aggregate versus on a single exchange. Note which exchange is best can also shift so it is quite hard in practice to even get the best exchange. This is a naive test, just done statically without price savings over time. Test ran at 10/26 6:25am.

***

### 1.B Buying 60k$ XMR: 

>          Binance (leading exchange) : 1.00% slippage
>                                 FPG :  .62% slippage
>                          Difference :  .38% Savings!!!!
              
Description of test: This is looking at buying on aggregate versus on a single exchange. Note which exchange is best can also shift so it is quite hard in practice to even get the best exchange. This is a naive test, just done statically without price savings over time. Test ran on 10/26 7:00am.

***

## 2 Purchasing with trader (via human) versus with FPG Market-Making tools:

### 2. Buying 50k$ of XMR:

>                               Naive : 0.56% slippage
>                                 FPG : -.15% slippage (actually made money versus normal price)
>                          Difference :  .74% <- Savings of this on this transaction!!
 
***

Description of test: This is looking at buying at a single time, versus over time using FPG on a single exchange. This allows an apple-to-apple comparison of how much time impacts the buying and selling. This shows that gains are made by splitting these transactions up. Note that this is scaled up 10* versus real data, to give larger numbers. The raw data was .056% slippage, -.015% slippage, for a net gain of .074% slippage. Test ran on 10/26 6:28:07am.

# Conclusion:

Here we demonstrated three key components:

* FPG systems typically save between .1-.5% on even small transactions (~5k) versus the typical, and commonly used, alternatives for a coin like Monero. 
* FPG systems will naturally be more performant as the amounts scale up as well. A test case is shown for this, where FPG saved ~.4% for a 60k purchase. 
* Interestingly, it was shown that during FPG liquidation, the settlement price can actually be better than the calculated price (owing to better liquidation times and statistical fluctuations). Likely, this difference will not be standard (not guaranteeing profit on every transaction), but does show the capacity of the system. 

More work is needed to demonstrate this for larger amounts, and the systems themselves can be improved to give better performance, but on balance, FPG systems save on slippage, and reduce the need for 3rd parties to build plumbing or hire traders themselves. 









