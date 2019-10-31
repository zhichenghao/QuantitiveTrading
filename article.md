# article
## [Stock Price Forecasting Using Information from Yahoo Finance and Google Trend](https://www.econ.berkeley.edu/sites/default/files/Selene%20Yue%20Xu.pdf)
1. introduction

- fundamental analysis
	- focus on undelying factors that affect a company's actual business and its future prospects
	- industries or the economy as a whole
	- form: news articles and analyst opinions
	- this article use Yahoo finance website and Google trend website to simplify the evaluation process

- techqnical analysis: focus on price movement of a stock and uses this data to predict its future price movements.
	- historical stock prices
	- most popular techniques to evaluate online news: text mining

- methods
	- apply the conventional ARMA time series analysis on the historical weekly stock prices
	- propose an algorithm to evaluate news/events related to aapl stock using information from the Yahoo finance website and the Google trend website.
	- regress the changes in weekly stock prices on the values of the news at the beginning of the week

2. Literature Review

- The basic theory regarding stock price forecasting is the [Efficient Market Hypothesis (EMH)](https://www.investopedia.com/terms/e/efficientmarkethypothesis.asp)
	- which asserts that the price of a stock reflects all information available and everyone has some degree of access to the information. 
	- The implication of EMH is that the market reacts instantaneously to news and no one can outperform the market in the long run.
	- basic [ARIMA](https://www.investopedia.com/terms/a/autoregressive-integrated-moving-average-arima.asp) model modification
		- clustering time series from ARMA models with clipped data
		- fuzzy neural network approach
		- support vector machines model
	- use textual information in public media to evaluate news
		- AZFin text system5
		- a matrix form text mining system
		- named entities representation scheme
3. Data
- The news is then assigned a value of +1 or -1 accordingly. If the influence of the news is highly controversial or ambiguous, then the news is assigned a zero value. The starting point of the Yahoo finance news data is set one month earlier than the starting point of the stock price data.
- Google trends: It shows how often a specific search term is entered relative to the total search volume on Google Search. It is possible to refine the request by geographical region and time domain. Google Trend provides a very rough measure of how much people talk about a certain topic at any point of time. 


4. [台灣加權指數TAIEX Taiwan Capitalization Weighted Stock Index](https://wiki.mbalib.com/zh-tw/台湾证券交易所发行量加权股价指数)
	- techqnical analysis:
		- [investing.com](https://hk.investing.com/indices/taiwan-weighted)
		- [Yahoo](https://tw.stock.yahoo.com/t/idx.php): market data 
		- [Google](https://www.google.com/search?tbm=fin&sxsrf=ACYBGNRbxR-7_R6N3f9hSUsKGYdW8JZEcw:1570031120914&q=TPE:+TAIEX&stick=H4sIAAAAAAAAAONgecRozC3w8sc9YSmtSWtOXmNU4eIKzsgvd80rySypFBLjYoOyeKS4uDj0c_UNkosKLXkWsXKFBLhaKYQ4erpGAAAu-w0uRQAAAA&biw=1366&bih=733#scso=_FcaUXaTpGaaEhbIP7fy_CA7:0)
		- This data set contains the open, high, low, close and adjusted close prices of TAIEX stock on every Monday throughout these five years. It also include trading volume values.

	- fundamental analysis:
		- news
			- reuters: [CN](https://cn.reuters.com/news/archive/topic-tw-stocks), [US](https://www.reuters.com/search/news?blob=taiwan+stock+market), [UK](https://uk.reuters.com/search/news?blob=Taiwan+stock), US,UK 14th August
			- Yahoo
				- https://tw.money.yahoo.com/marketindex/%5ETWII
				- https://tw.news.yahoo.com/search?p=%E5%8F%B0%E7%81%A3%E5%8A%A0%E6%AC%8A%E6%8C%87%E6%95%B8&fr=
				- https://tw.news.yahoo.com/stock
				- https://tw.news.yahoo.com/politics
		- [google trend](https://trends.google.com/trends/explore?q=taiwan%20stock)

## Listening to Chaotic Whispers: A Deep Learning Framework for News-oriented Stock Trend Prediction
brief introduction
- quality of news are low quality or even 
	- three principles to solve: sequential context dependency, divese influnce, and effective and efficient learning
	- techniqual analysis and foundamental analysis
	- deep learning framework based on the three principles

1. introduction
- motivation: maxmized profits
- challenges: highly volatile and non-stationary nature of the market
- Method: technical analysis(prices and volumes) and foundemental analysis(ecnomical trend and contents)
	- new trend: content from the online media
	- challenges: quality, trustworthiness and comprehensiveness is vary drastically and most of the news are bad quality
	- Three principles to deal with chaotic online news
		- Sequential Context Dependency: consider a sequence of related recent news as a unified context (HAN and RNN)
		- Diverse Influence: discriminate differnet news accroding to the importance (HAN and RNN)
		- Effective and Efficient Learning: Not all news can provide inforamtice indication (SPL)

2. related Work
	- technical analysis: deal with time-series historic market data to find the trading patterns that can be leveraged for future prediction.
		- Model: recurrent neural networks (RNN)
		limitations: cant reveal the dynamics of the market beyond the price data
	- foudamental analysis: seek information outside market-historic-data, such as geopolitics, business principles
		- method: multi-layer dimension reduction algorithm with semantics and sentiment to predict intra-day directional-movements of a currency-pair in the foreign exchange market. 
		- method2: incorporating an outside knowledge graph into the learning process for event embeddings. 
		- method3: text regression task to predict the volatility of stock prices
		- method4: novel tree representa- tion, and use it to train predictive models with tree kernels using support vector machines
		- method5:  extract a large scale of expressive features to represent the unstructured text data and employs a robust feature selection to enhance the stock prediction
	- analyze sentiments from public news and social media
		- method1: implements a generic stock price prediction framework using sentiment analysis
		- method2: They conduct a thorough study over 10 million stock-relevant tweets from Weibo, and find five attributes that stock market in China can be com- petently predicted by various online emotions
		- method3: consider the topics relating to the target stocks, and ex- tracting topics and related sentiments from social media to make prediction.

3. Empirical analysis
	- Sequential Context Dependency: integrate and interpret each news in a sequential temporal context
	- Diverse Influence: distinguish the news with more intensive and influence
	- Effective and Efficient Learning: follow a similar process which particular conducts learning on more informative news at the easlier stage and further optimized to tackle harder samples

4. DEEP LEARNING FRAMEWORK FOR NEWS-ORIENTED TREND PREDICTION
	- **problem**:
		> Rise_Percent(t) = [Open_Price(t+1)-Open_price(t)]/Open_Price(t) (t is given date and given stock s)
		- stock are classfied into: DOWN(significant dropping), UP(significant rising), PRESERVE(steady stock)
		- Tasks: use the news corpus sequence from time t-N to t-1 denoted as [Ct-N, Ct-N+1,...Ct-1] to predict the classs of Rise_Percent(t) N: length of a time sequence, s: stock, t: date, 
	- **Hybrid Attention Networks**:
		>
	- **Self-paced Learning Mechanism**:



	









































