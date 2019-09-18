# -momentum-trading-strategy
I finish this project with, ML and DL, 2 different ways.

I build and back-test a momentum
trading strategy in the US equities market. The goal of this project is to motivate financial
modeling.

• The dataset provided comprises of stock market data for approximately 1500 stock
instruments listed on the US stock exchange. It contains daily data from Feb 2008 to
July 2017. There are 3,547,259 instances/samples in the dataset.

• First, implement a baseline strategy using logistic regression model and record the backtest results in terms of yearly return and yearly Sharpe ratio. To help you get started, we
generated 33 input features (X), as well as the output/target label (Y). We provide a
back-test framework programmed using python. 

• Next, try to improve on the baseline result using a "classical ML" method (from first half
of the course) and a "deep learning" method (from second half of the course). To obtain
apples-to-apples comparison with the baseline strategy, use the same 33 input features,
output target and back-test framework as the baseline.

Dataset feature attributes are:
- date
- id: stock ticker ID
- industry: sort each id by GICS industry group
- flag 2: is the label true every 20 trading days, use this as holding period in the back-test.
- ret_raw: daily return calculated from daily adjusted closing price
- ret_raw_norm: normalized ret_raw with regards to trading universe on that day
- ret_20_raw: cumulative sum of past 20 trading days return, i.e. monthly return
- ret_20_raw_norm: normalized ret_20_raw with regards to trading universe on that day
- ret_raw_norm_lag_21: ret_raw_norm of previous 1 day
- ret_raw_norm_lag_22: ret_raw_norm of previous 2 days
- ret_raw_norm_lag_23: ret_raw_norm of previous 3 days
- ret_raw_norm_lag_24: ret_raw_norm of previous 4 days
- ret_raw_norm_lag_25: ret_raw_norm of previous 5 days
- ret_raw_norm_lag_26: ret_raw_norm of previous 6 days
- ret_raw_norm_lag_27: ret_raw_norm of previous 7 days
- ret_raw_norm_lag_28: ret_raw_norm of previous 8 days
- ret_raw_norm_lag_29: ret_raw_norm of previous 9 days
- ret_raw_norm_lag_30: ret_raw_norm of previous 10 days
- ret_raw_norm_lag_31: ret_raw_norm of previous 11 days
- ret_raw_norm_lag_32: ret_raw_norm of previous 12 days
- ret_raw_norm_lag_33: ret_raw_norm of previous 13 days
- ret_raw_norm_lag_34: ret_raw_norm of previous 14 days
- ret_raw_norm_lag_35: ret_raw_norm of previous 15 days
- ret_raw_norm_lag_36: ret_raw_norm of previous 16 days
- ret_raw_norm_lag_37: ret_raw_norm of previous 17 days
- ret_raw_norm_lag_38: ret_raw_norm of previous 18 days
- ret_raw_norm_lag_39: ret_raw_norm of previous 19 days
- ret_raw_norm_lag_40: ret_raw_norm of previous 20 days
- ret_20_raw_norm_lag_41_60: ret_20_raw_norm of previous 2 months
- ret_20_raw_norm_lag_61_80: ret_20_raw_norm of previous 3 months
- ret_20_raw_norm_lag_81_100: ret_20_raw_norm of previous 4 months
- ret_20_raw_norm_lag_101_120: ret_20_raw_norm of previous 5 months
- ret_20_raw_norm_lag_121_140: ret_20_raw_norm of previous 6 months
- ret_20_raw_norm_lag_141_160: ret_20_raw_norm of previous 7 months
- ret_20_raw_norm_lag_161_180: ret_20_raw_norm of previous 8 months
- ret_20_raw_norm_lag_181_200: ret_20_raw_norm of previous 9 months
- ret_20_raw_norm_lag_201_220: ret_20_raw_norm of previous 10 months
- ret_20_raw_norm_lag_221_240: ret_20_raw_norm of previous 11 months
- ret_20_raw_norm_lag_241_260: ret_20_raw_norm of previous 12 months
- ret_20_raw_norm_lag_261_280: ret_20_raw_norm of previous 13 months
- isJan: indicator variable for the month of January to capture turn of the year pattern.
- target: label 1 if ret_20_raw_norm > ret_20_raw_norm median value of trading universe for that day,
otherwise label as 0. 
