## AnalysisOfStockPrice
**Analysis of Stock Price Movement Following
Financial News Article Release**

1. Abstraction
	- measure the abnormal return
	- articles through different sources of news will cause positive or negative return
	- certain times of the day had abnormally price movements associated with them

2. Introduction
 - the use of news analytics to supplement trade decision making
 - [high frequency trading](https://www.investopedia.com/terms/h/high-frequency-trading.asp)
 - [media outlet](https://en.wiktionary.org/wiki/media_outlet), time of release and sentiment of the financial news article
 - Goal: build a system to analyze the factors a corporation could use in conjunction with a financial news articles release to manage their stock prices
 - study the corralation of factors and theorize the determinants of causation to determin what link
 - impacts of news: choice of words, time releases, media outlet choice

3. Literature Review
 - Stock price movement is a natural function of **disclosures**, whether they be numberic, textual, oral or written. 
 	- action based, e.g. unscheduled events: new business deal, change in top level management
 	- trading based, e.g. trading volume, timing, larger investors
 	- information based, e.g. new ecinimic data, new producrt release (quantitative data and textual data)
 - **High Frequency Trading**: intersection of systems and algorithms that can read, process and execute trades within milliseconds.
 - **Abnormal Price Movement**: Foudamental analysis(e.g. fiscal values, the ecnomical environment) and technical analysis(historical values, data patterns and market timing). there is a appratent lage between the introduction of information and when the market corrected itself.
 - **Role of Media**: news can cause significant price change
 - **Sentiment Analysis**: examination of text for opinions and emotions. (positive or negative) tool OpinionFinder

 - **Research Gap**
  - relation between news and stock price
  - the timeframes is restrited, day or longer
  - no much sentiment analysis on financila news

4. System Design
	- use textual financial news article and intraday stock quotes to predict stock prices twenty minutes after an article is released.
	- Data Collection: collection using a web scraper from Yahoo!Finance and content is analyzed using OpinionFinder for sentiment polarity
	- Model Building: using regression window
	- evaluated in slope: is a measure of abnormal price movement folowwing an article release

5. Experimental Design
	- Period: 40days 9:50am-3:40pm
	- Companies: S&P 500
	- Article: one per company
	- times of the day, news, media outlets
	- if the news are creating an abnormal price movement, a statistical different would occur between the two datasets.
	- Measure: ΔSlope and sharpe Ration = (RA-RB)/𝜎𝐴, RA: asset return variable is the stock price at t = 20 minus the price at t=0,RB: average stock price within 20 mins with respect to the article release. 𝜎𝐴: standard deviation of prices over the t = -20 to t=0 period

6. Experimental Result and Analysis
	- **correlation between price and financial article release**
		- news article release did create a statistically significant price movement
	- **Does the media outlet impact stock price?**
		- had statistically significant affect
	- **What effect does article release time have on excess returns**
		- companies that release financial news articles during the 9:50-9:59am time period have the potential of receiving abnormal positive price returns.
	- **What is the role of sentiment in price movement?**
		- negetive
		- positive

7. Conclusions and Future Directions
	- CentralFinance was able to identify a strong correlation between the period following the release of a financial news article and abnormal price movement
	- link between media outlets and price movement.
	- time of news article release and how it relates to abnormal price movement. We found that articles released at market opening had significantly higher SharpeArticle to SharpeRandom (2.58 to 1.32 respectively, p-value < 0.01). We believe that this
	- correlation between article sentiment and abnormal price movement:  negative polarity had the highest SharpeArticle value

8. Author [Dr. Robert P. Schumaker](http://robschumaker.com/pubs/?domain=fintext) ? he did not provide any datasets

9. Research Question:
	- What is the correlation between stock price movement and financial news article release?
		- compare price at certain point?
		- invesitage trends (initial trends is up but going down after artile release)
	- Does the media outlet imapct stock price?
		- compare the influence between different media outlets (e.g. wall street journals, trumps news releases and tweet, Bloomberg news)
	- What effect does article release time have on excess returns?
	- what is the role of sentiment in price movement?
	- ? Do i need to analyze one specific stock by using different media outlets? or one media outlets correspond with one stocks and these means need to analyze differetn stocks. What should i need to do?

10. proposal
	- [Stock Market Reactions to Presidential Social Media
Usage: Evidence from Company-Specific Tweets](https://lamacro.davidson.edu/wp-content/uploads/gravity_forms/1-95b74353d944e7d67926fb1900938dee/2017/05/Ge-Kurov-Wolfe_2017_Stock-Market-Reactions-to-Presidential-Social-Media-Usage.pdf)
	- President Trump has utilized Twitter to target specific companies
in his tweets about industrial policy. 
	- Sentiment analysis can find the positive or negtive of those tweets

11. how to use process mining?





































