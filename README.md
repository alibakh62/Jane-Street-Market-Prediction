# Jane-Street-Market-Prediction

## Problem Description
Electronic trading enables traders to run thousands of transactions in a fraction of a second and helps them take advantage of price differences in real time.

In a prefectly efficient market there's perfect information symmetry between the buyers and sellers. As a result, products are always remain at their "fair value". **However, financial markets are not perfectly efficient in real world.**

Developing trading strategies to identify and take advantage of inefficiencies is challenging. Market volatility makes it impossible to predict the profitability of any trade strategy with certainty. **As a result, it's hard to distinguish good luck from having made a good trading decision.**

## The Competition 
Here are the steps of the competition:

- In the first three months of this challenge, you will build your own quantitative trading model to maximize returns using market data from a major global stock exchange.
- Next, you’ll test the predictiveness of your models against future market returns and receive feedback on the leaderboard.

Your **challenge** will be to use the historical data, mathematical tools, and technological tools at your disposal to create **a model that gets as close to certainty as possible.**

You will be presented with a number of potential trading opportunities, which your model must choose whether to accept or reject.

In general, if one is able to generate a highly predictive model which selects the right trades to execute, they would also be playing an important role in sending the market signals that push prices closer to “fair” values. **That is, a better model will mean the market will be more efficient going forward.**

However, developing good models will be challenging for many reasons, including a **very low signal-to-noise ratio, potential redundancy, strong feature correlation, and difficulty of coming up with a proper mathematical formulation.**

## Evaluation
This competition is evaluated on a utility score. Each row in the test set represents a trading opportunity for which you will be predicting an `action` value, 1 to make the trade and 0 to pass on it. Each trade `j` has an associated `weight` and `resp`, which represents a return.

For each `date` i, we define:

<img src="https://bit.ly/3nlAiEY" align="center" border="0" alt="p_i = \sum_j \big({weight}_{ij}\times{resp}_{ij}\times{action}_{ij}\big)" width="283" height="42" />

<img src="https://bit.ly/35lJMK3" align="center" border="0" alt="t = \frac{\sum{p_i}}{\sqrt{\sum{{p_i}^2}}}\times\sqrt{\frac{250}{|i|}}" width="158" height="53" />

<img src="https://bit.ly/2XmpQlQ" align="center" border="0" alt="u = min(max(t,0),6)\sum{p_i}" width="203" height="29" />

$p_i = \sum_j \big({weight}_{ij}\times{resp}_{ij}\times{action}_{ij}\big)$

$t = \frac{\sum{p_i}}{\sqrt{\sum{{p_i}^2}}}\times\sqrt{\frac{250}{|i|}}$

where $|i|$ is the number of unique dates in the test set. The **utility function** is then defined as:

$u = min(max(t,0),6)\sum{p_i}$

## Submission File
You must submit to this competition using the provided python time-series API, which ensures that models do not peek forward in time. To use the API, follow the following template in Kaggle Notebooks:

```python
import janestreet
env = janestreet.make_env() # initialize the environment
iter_test = env.iter_test() # an iterator which loops over the test set

for (test_df, sample_prediction_df) in iter_test:
    sample_prediction_df.action = 0 #make your 0/1 prediction here
    env.predict(sample_prediction_df)
```

## Code Requirements

- Training is not required in the notebooks.
- Your notebook must use the time-series module to make predictions.
- It should run in less than 5 hours.
- Freely & publicly available external data is allowed, including pre-trained models.

## Data Description
- This dataset contains an anonymized set of features, `feature_{0...129}`, representing real stock market data.
- Each row in the dataset represents a trading opportunity, for which you will be predicting an `action` value: 1 to make the trade and 0 to pass on it.
- Each trade has an associated `weight` and `resp`, which together represents a return on the trade.
- The `date` column is an integer which represents the day of the trade, while `ts_id` represents a time ordering.
- In addition to anonymized feature values, you are provided with metadata about the features in **features.csv**.
- In the training set, **train.csv**, you are provided a `resp` value, as well as several other `resp_{1,2,3,4}` values that represent returns over different time horizons. **These variables are not included in the test set.**
- Trades with `weight = 0` were intentionally included in the dataset for completeness, although such trades will not contribute towards the scoring evaluation.
