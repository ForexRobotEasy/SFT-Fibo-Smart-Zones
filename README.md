# SFT Fibo Smart Zones

This code represents an Expert Advisor (EA) for the MetaTrader 5 platform. The EA is designed to calculate Fibonacci levels, overbought and oversold levels, and identify potential trading opportunities based on these levels. This code is not the official code developed by Forex Robot Easy Team, but a sample code that can work similarly to the SFT Fibo Smart Zones product developed by Forex Robot Easy Team. For detailed reviews and trading results of the official product, please visit [this link](https://forexroboteasy.com/forex-robot-review/sft-fibo-smart-zones-review-fibonacci-based-forex-tool/).

## Expert Initialization Function

The `OnInit()` function is the initialization function of the EA. It initializes necessary variables and settings. It returns `INIT_SUCCEEDED` if initialization is successful.

## Expert Deinitialization Function

The `OnDeinit(const int reason)` function is the deinitialization function of the EA. It is called when the EA is removed from the chart or the platform is closed. It performs necessary cleanup tasks.

## Expert Start Function

The `OnTick()` function is the start function of the EA. It is called on every tick of the chart. In this function, the Fibonacci golden ratio, overbought level, and oversold level are calculated. Potential trading opportunities are identified based on whether the current price is above or below the Fibonacci level. Depending on the identified opportunity, either a trend-following strategy or a counter-trend strategy is executed.

## Fibonacci Calculation

The `CalculateFibonacciLevel()` function calculates the Fibonacci level using the golden ratio formula. It takes the difference between the highest and lowest prices of the current bar and multiplies it by 0.618 to get the Fibonacci level.

## Overbought Calculation

The `CalculateOverBoughtLevel()` function calculates the overbought level by multiplying the highest price of the current bar by 1.1. This level is used to identify potential overbought conditions in the market.

## Oversold Calculation

The `CalculateOverSoldLevel()` function calculates the oversold level by multiplying the lowest price of the current bar by 0.9. This level is used to identify potential oversold conditions in the market.

## Trend-Following Opportunity

The `IsTrendFollowing(const double fibLevel)` function checks if the current price is above the Fibonacci level. If the current price is above the Fibonacci level, it returns `true`, indicating a trend-following opportunity. Otherwise, it returns `false`.

## Counter-Trend Opportunity

The `IsCounterTrend(const double fibLevel)` function checks if the current price is below the Fibonacci level. If the current price is below the Fibonacci level, it returns `true`, indicating a counter-trend opportunity. Otherwise, it returns `false`.

## Execute Trend-Following Strategy

The `ExecuteTrendFollowingStrategy()` function is called when a trend-following opportunity is identified. In this function, Buy or Sell orders can be placed based on the trend-following strategy.

## Execute Counter-Trend Strategy

The `ExecuteCounterTrendStrategy()` function is called when a counter-trend opportunity is identified. In this function, Buy or Sell orders can be placed based on the counter-trend strategy.

Please note that this code is just a sample and may not fully replicate the functionality of the official SFT Fibo Smart Zones product developed by Forex Robot Easy Team. To find the official developer of this product, please use MQL5.
