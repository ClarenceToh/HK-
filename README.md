# HK-
Trading Strategy - Stock Filter

The strategy was inspired by The Complete Turtle Trader, a book by Michael Covel.
From Investopedia - Turtles were taught very specifically how to implement a trend-following strategy. The idea is that the "trend is your friend," so you should buy futures breaking out to the upside of trading ranges and sell short downside breakouts.

I think what drew me into this strategy is that it relies heavily on what the market is thinking. 
Positive rallies will rally higher and investors will pour in money or if price drops too much, it may cause massive short selling on a stock.

So, how will this help you?

Traders rely mostly only on one thing. That is direction. You either buy long or sell short. That is the simplest of all strategies.
The turtle traders did it, so why not?

This filter does many things and is customizable. I created this as an add-on component to what the turtle traders do because not everyone starts out with the kind of capital these guys have.

The function, posrally (i, CP, vola, ag14), gives you stocks that meets the requirements you set.

In this case, 
i refers to the stock ticker.
CP is the closing price.
Vola is the volatility in percentage.
ag14 is the average growth in the last 14 calendar days.

For example, I am interested in a set of stocks that have hit monthly highs.
I run posrally(I, 5, 1.25, 2) on the stocks in them.
Let's say "1234.HK" is in this list of stocks. "1234.HK" would be classified as a stock that has a positive rally, with a close price of at least above 5 HKD, whose average growth in the last 7 calendar days and 14 calendar days are not different from each other by more than 1.25% and there is an average growth in the stock by at least positive 2%.

Why this may be useful?
breaking down the positive growth to negative growth over several calendar days helps us understand market sentiment and to see consistency. If average growth increases, it is a good indication that the stock is gaining momentum. we filter by price because we may not want to play with penny stocks. The past actual returns tells us about the stock's activity and serves as a check for the momentum. Volume in the last 7 calendar days will help us gauge if there is enough liquidity.

1234.HK
number of positves 1m:  0.7368421052631579 14/19
number of negatives 1m:  0.2631578947368421 5/19
Average Growth per day 1m:  1.482
number of positves 14d:  0.8571428571428571 6/7
number of negatives 14d:  0.14285714285714285 1/7
Average Growth per day 14d:  2.046
number of positves 7d:  1.0 4/4
number of negatives 7d:  0.0 0/4
Average Growth per day 7d:  2.302
Latest Close Price:  75.5
Past 1m Returns:  [0.52, 3.79, -2.91, -1.71, 5.4, 0.91, 4.01, -1.65, 4.0] [0.31, 3.53, -2.37, -4.93, 0.96, 9.09, 6.23, 0.41, 1.49, 1.07]
Volume: 
0   834584
1   871222
2   932400
3   524800
4   756400
