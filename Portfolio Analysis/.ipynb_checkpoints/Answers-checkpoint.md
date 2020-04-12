## Background

The investment division of Harold's company has been investing in algorithmic trading strategies. Some of the investment managers love them, some hate them, but they all think their way is best.

Here we learned these quantitative analysis techniques with Python and Pandas, so Harold has come to me with a challenge—to help him determine which portfolio is performing the best across many areas: volatility, returns, risk, and Sharpe ratios.

I created a tool (an analysis notebook) that analyzes and visualizes the major metrics of the portfolios across all of these areas, and determine which portfolio outperformed the others on the basis of the given historical daily returns of several portfolios: some from the firm's algorithmic portfolios, some that represent the portfolios of famous "whale" investors like Warren Buffett, and some from the big hedge and mutual funds. I then used this analysis to create a custom portfolio of stocks and compare its performance to that of the other portfolios, as well as the larger market (S&P 500).

### Prepare the Data

First, read and clean several CSV files for analysis. The CSV files include whale portfolio returns, algorithmic trading portfolio returns, and S&P 500 historical prices.

### Conduct Quantitative Analysis

Analyze the data to see if any of the portfolios outperform the stock market (i.e., the S&P 500).

#### Performance Analysis

1. Calculate and plot cumulative returns. Does any portfolio outperform the S&P 500?
Berkshire Hathaway & Algo 1 are outperforming the S&P 500
Cumulative returns :
Berkshire Hathaway = 0.527786
Algo 1 = 0.690246
S&P500 = 0.364329


#### Risk Analysis

1. Create a box plot for each of the returns. Which box has the largest spread? Which has the smallest spread?
Largest Spread Box - Tiger Global Management LLC
Smallest Spread Box - Paulson & Co Inc

2. Calculate the standard deviation for each portfolio. Which portfolios are riskier than the S&P 500?
Riskier Portfolio :
TIGER GLOBAL MANAGEMENT LLC    0.010894
BERKSHIRE HATHAWAY INC         0.012919

#### Rolling Statistics

1. Plot the rolling standard deviation of the firm's portfolios along with the rolling standard deviation of the S&P 500. Does the risk increase for each of the portfolios at the same time risk increases in the S&P?
Risk increases for each of the portfolios at the same time risk increases in S&P 500 except Tiger Global Management LLC

2. Construct a correlation table for the algorithmic, whale, and S&P 500 returns. Which returns most closely mimic the S&P?
Soros Fund Management LLC
Algo 2

3. Choose one portfolio and plot a rolling beta between that portfolio's returns and S&P 500 returns. Does the portfolio seem sensitive to movements in the S&P 500?
Berkshire Hathaway Inc is most sensitive to the movements in S&P

### Plot Sharpe Ratios

Investment managers and their institutional investors look at the return-to-risk ratio, not just the returns. (After all, if you have two portfolios that each offer a 10% return, yet one is lower risk, you would invest in the lower-risk portfolio, right?)

1. Using the daily returns, calculate and visualize the Sharpe ratios using a bar plot.

2. Determine whether the algorithmic strategies outperform both the market (S&P 500) and the whales portfolios.
Algo 1 outperforms compared to S&P 500 and whale portfolios

### Create Custom Portfolio

Harold is ecstatic that we were able to help him prove that the algorithmic trading portfolios are doing so well compared to the market and whales portfolios. However, now we are wondering whether we can choose our own portfolio that performs just as well as the algorithmic portfolios. 

1. Add your portfolio returns to the DataFrame with the other portfolios and rerun the analysis. How does your portfolio fair?
My Portfolio is having better Sharpe ratio as compared to Whale portfolio & S&P 500 like Algorithmic Portfolio



