## newsArticle1
**Analysis of Stock Price Movement Following
Financial News Article Release**

1. Abstraction
	- measure the abnormal return
	- articles through different sources of news will cause positive or negative return
	- certain times of the day had abnormally price movements associated with them

2. Introduction
 - the use of news analytics to supplement trade decision making
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
6. Experimental Result and Analysis
7. Conclusions and Future Directions