### Buy and sell strategy: MA-20
### Risk Control Method: Bollinger Bands

1. Import libs and stock info files
2. Run this to get results (use AAPL as an example)
```
company = nyse[nyse['symbol'] == 'AAPL'].set_index('date')
company, signals = run_strategy(company)
bollinger_bands_visualization(company, signals=signals) # show bollinger_bands
trading_visualization(company, signals=signals) # show when to trade
return_visualization(company, signals=signals) # show the final return
show_final_return_results(signals=signals) # show the numerical final return
show_sharpe_ratio_results(signals=signals) # show the sharpe ratio
```
3. Here is the in-sample result:

![Bollinger Bands](images/Bollinger_Bands.png)

![Trading Signals](images/trading_signals.png)

![Comparsion](images/comparsion.png)

```
Benchmark: 25728.38208716729
Return: 60170.609970535246
Return with Bollinger Bands: 40968.3929034226

Benchmark sharpe ratio: 0.7156191640228604
basic sharpe ratio: 3.3007405603773408
Bollinger Bands sharpe ratio: 2.3924102734554764
```