## Mean Reversion Strategy Using SMA 
This project implements a simple mean reversion trading strategy based on a 20-day Simple Moving Average (SMA). The goal is to identify potential buy and sell opportunities when a stock's price deviates from its short-term average and then backtest how the strategy performs compared to a Buy & Hold approach.

## 🧠 Idea Behind the Strategy

  `` "Prices tend to revert to their mean over time." ``

  Buy Signal: When the stock's close price drops below the 20-day SMA, it's considered undervalued, signaling a potential buy.

  Sell Signal: When the price rises back above the SMA, the position is closed.


## ⚙️ Tools & Technologies

    Python

    Pandas

    Matplotlib

    yfinance (for historical stock data)

## 🔍 How It Works

1. Data Collection: Downloaded historical data using yfinance.

2. Indicator Calculation: Computed 20-day Simple Moving Average.

3. Signal Generation:

        Buy when price < SMA

        Sell when price > SMA

4. Position Tracking:

        Held position while price < SMA

        Exited position when price > SMA

5. Backtesting:

        Compared returns of the strategy vs a passive Buy & Hold approach

        Plotted equity curves using cumprod() on strategy returns

## Observations

1. The strategy did not outperform Buy & Hold on the tested stock.
2. Performance stabilized as the SMA window increased, but returns were still below passive holding.
3. The strategy struggled in trending markets, confirming the limitation of mean reversion in such conditions.

## Example Plot for AAPL stocks:

![equity_curve](https://github.com/user-attachments/assets/6a3621cd-7569-40ce-be8e-bd2006b843ec)


![backtest](https://github.com/user-attachments/assets/46b3caba-0283-4642-a7b5-dff36007e2aa)




