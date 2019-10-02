# article
## [Stock Price Forecasting Using Information from Yahoo Finance and Google Trend](https://www.econ.berkeley.edu/sites/default/files/Selene%20Yue%20Xu.pdf)
1. introduction

- fundamental analysis: focus on undelying factors that affect a company's actual business and its future prospects
	- news articles and analyst opinions
	- most popular techniques to evaluate online news: text mining
	- this article use Yahoo finance website and Google trend website to simplify the evaluation process

- techqnical analysis: focus on price movement of a stock and uses this data to predict its future price movements.
	- historical stock prices

- apply the conventional ARMA time series analysis on the historical weekly stock prices--->propose an algorithm to evaluate news/events related to aapl stock using information from the Yahoo finance website and the Google trend website. --->regress the changes in weekly stock prices on the values of the news at the beginning of the week

2. Literature Review

- The basic theory regarding stock price forecasting is the [Efficient Market Hypothesis (EMH)](https://www.investopedia.com/terms/e/efficientmarkethypothesis.asp)
	- which asserts that the price of a stock reflects all information available and everyone has some degree of access to the information. 
	- The implication of EMH is that the market reacts instantaneously to news and no one can outperform the market in the long run.
	- basic ARIMA model modification
		- clustering time series from ARMA models with clipped data
		- fuzzy neural network approach
		- support vector machines model
	- use textual information in public media to evaluate news
		- AZFin text system5
		- a matrix form text mining system
		- named entities representation scheme

3. [台灣加權指數TAIEX Taiwan Capitalization Weighted Stock Index](https://wiki.mbalib.com/zh-tw/台湾证券交易所发行量加权股价指数)
	- techqnical analysis:
		- [investing.com](https://hk.investing.com/indices/taiwan-weighted)
		- [Yahoo](https://tw.stock.yahoo.com/t/idx.php)
		- [Google](https://www.google.com/search?tbm=fin&sxsrf=ACYBGNRbxR-7_R6N3f9hSUsKGYdW8JZEcw:1570031120914&q=TPE:+TAIEX&stick=H4sIAAAAAAAAAONgecRozC3w8sc9YSmtSWtOXmNU4eIKzsgvd80rySypFBLjYoOyeKS4uDj0c_UNkosKLXkWsXKFBLhaKYQ4erpGAAAu-w0uRQAAAA&biw=1366&bih=733#scso=_FcaUXaTpGaaEhbIP7fy_CA7:0)

	- fundamental analysis:
		- 




