# On Algorithmic Trading
Algorithmic trading (also called automated trading, black-box trading, or algo-trading) uses a computer program that follows a defined set of instructions (an algorithm) to place a trade. The trade, in theory, can generate profits at a speed and frequency that is impossible for a human trader.

The defined sets of instructions are based on timing, price, quantity, or any mathematical model.

**Example:**

Suppose a trader follows these simple trade criteria:

-   Buy 50 shares of a stock when its 50-day moving average goes above the 200-day moving average. (A moving average is an average of past data points that smooths out day-to-day price fluctuations and thereby identifies trends.)
-   Sell shares of the stock when its 50-day moving average goes below the 200-day moving average.

***

Algo-trading is used in many forms of trading and investment activities including:

-   Mid- to  [long-term investors](https://www.investopedia.com/articles/00/082100.asp)  or buy-side firms—pension funds, mutual funds, insurance companies—use algo-trading to purchase stocks in large quantities when they do not want to influence stock prices with discrete, large-volume investments.
-   [Short-term traders](https://www.investopedia.com/articles/trading/09/short-term-trading.asp)  and sell-side participants—market makers (such as brokerage houses),  speculators, and arbitrageurs—benefit from automated trade execution; in addition, algo-trading aids in creating sufficient liquidity for sellers in the market.
-   [Systematic traders](https://www.investopedia.com/terms/s/systematic-manager.asp)—trend followers, hedge funds, or [pairs traders](https://www.investopedia.com/terms/p/pairstrade.asp) (a market-neutral trading strategy that matches a long position with a short position in a pair of highly correlated instruments such as two stocks, exchange-traded funds (ETFs) or currencies)—find it much more efficient to program their trading rules and let the program trade automatically.

***

## Algorithmic Trading Strategies

Any strategy for algorithmic trading requires an identified opportunity that is profitable in terms of improved earnings or cost reduction. The following are common trading strategies used in algo-trading:

### Trend-following Strategies

The most common algorithmic trading strategies follow trends in moving averages, channel breakouts, price level movements, and related  [technical indicators](https://www.investopedia.com/terms/t/technicalindicator.asp). These are the easiest and simplest strategies to implement through algorithmic trading because these strategies do not involve making any predictions or price forecasts. Trades are initiated based on the occurrence of desirable trends, which are easy and straightforward to implement through algorithms without getting into the complexity of predictive analysis. Using 50- and 200-day moving averages is a popular trend-following strategy.

### Arbitrage Opportunities

Buying a dual-listed stock at a lower price in one market and simultaneously selling it at a higher price in another market offers the price differential as risk-free profit or  [arbitrage](https://www.investopedia.com/terms/a/arbitrage.asp). The same operation can be replicated for stocks vs. futures instruments as price differentials do exist from time to time. Implementing an algorithm to identify such price differentials and placing the orders efficiently allows profitable opportunities.

### Index Fund Rebalancing

Index funds have defined periods of rebalancing to bring their holdings to par with their respective benchmark indices. This creates profitable opportunities for algorithmic traders, who capitalize on expected trades that offer 20 to 80 basis points profits depending on the number of stocks in the index fund just before index fund rebalancing. Such trades are initiated via algorithmic trading systems for timely execution and the best prices.

### Mathematical Model-based Strategies

Proven mathematical models, like the delta-neutral trading strategy, allow trading on a combination of options and the underlying security. (Delta neutral is a portfolio strategy consisting of multiple positions with offsetting positive and negative deltas—a ratio comparing the change in the price of an asset, usually a marketable security, to the corresponding change in the price of its derivative—so that the overall delta of the assets in question totals zero.)

### Trading Range (Mean Reversion)

[Mean reversion](https://www.investopedia.com/terms/m/meanreversion.asp)  strategy is based on the concept that the high and low prices of an asset are a temporary phenomenon that revert to their mean value (average value) periodically. Identifying and defining a price range and implementing an algorithm based on it allows trades to be placed automatically when the price of an asset breaks in and out of its defined range.

### Volume-weighted Average Price (VWAP)

Volume-weighted average price strategy breaks up a large order and releases dynamically determined smaller chunks of the order to the market using stock-specific historical volume profiles. The aim is to execute the order close to the  [volume-weighted average price](https://www.investopedia.com/terms/v/vwap.asp)  (VWAP).

### Time Weighted Average Price (TWAP)

Time-weighted average price strategy breaks up a large order and releases dynamically determined smaller chunks of the order to the market using evenly divided time slots between a start and end time. The aim is to execute the order close to the average price between the start and end times thereby minimizing market impact.

### Percentage of Volume (POV)

Until the trade order is fully filled, this algorithm continues sending partial orders according to the defined participation ratio and according to the volume traded in the markets. The related “steps strategy” sends orders at a user-defined percentage of market volumes and increases or decreases this participation rate when the stock price reaches user-defined levels.

### Implementation Shortfall

The  [implementation shortfall](https://www.investopedia.com/terms/i/implementation-shortfall.asp)  strategy aims at minimizing the execution cost of an order by trading off the real-time market, thereby saving on the cost of the order and benefiting from the opportunity cost of delayed execution. The strategy will increase the targeted participation rate when the stock price moves favorably and decrease it when the stock price moves adversely.

### Beyond the Usual Trading Algorithms

There are a few special classes of algorithms that attempt to identify “happenings” on the other side. These “sniffing algorithms”—used, for example, by a sell-side market maker—have the built-in intelligence to identify the existence of any algorithms on the buy side of a large order. Such detection through algorithms will help the market maker identify large order opportunities and enable them to benefit by filling the orders at a higher price. This is sometimes identified as high-tech front-running.
