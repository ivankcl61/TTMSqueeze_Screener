# TTMSqueeze_Screener

Info:
The program is designed to scrape the S&P 500 ticker symbols from Wikipedia, save them into a CSV file named symbols.csv in a datasets directory, and subsequently download historical stock data for each ticker using the yfinance library. It reads historical stock data for S&P 500 companies from CSV files, calculates Bollinger Bands and Keltner Channels to identify squeeze conditions, and generates interactive candlestick charts to visualize the price movements along with these indicators using Plotly.

Requirement: pip install plotly, pandas, requests, os, yfinance, bs4

Details:

Building environment and Webscrapping
1. Running the datasets.py first. It create a datasets directory if there is no existing one.
2. It webscrapes the table of list of S&P500 from Wikipedia, and then extract the tickers and download the historical data of each ticker
3. The data of each ticker would be save as an independent document

Calculating the Bollinger Band and Keltner Channel
4. Using the parameters of SMA, ATR and STDEV to generate these two volatility indicators

Defining the TTM Squeeze Function
5. When the Bollinger contracts and squeeze inside Keltner Channel

Identify Squeeze_on Condition
6. The stock price most recently get into a squeeze_on condition

Generate Charts for each Symbol being screened out
7. The symbol fulfilled the squeeze_on condition would be listed out with a sentence "{symbo} has started squeezing"
8. Each symbol screened out would generate a figure showing its price movement

