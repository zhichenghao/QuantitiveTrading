# Quantitive Analysis

Stock market model
![image](historicalSystem.png)

### Question

```mark
1. efficient market hypthesis
2. Fama-French 三因子模型
3. fundamental analysis 基本面分析与 techqnical analysis 技术面分析, 将基本面中的信息放入量化投资的框架中进行研究
4. Modern portfolio theory
5. Capital Asset Pricing Mode
6. Factor Model
7. arbitrage and arbitrage pricing theory
8. 投资策略：数据+量化模型
9. introduction to stock market
10. how to apply process mining in stock market
11. 三大法人的走势和大盘走势的对比
12. What should I need to know about "自变量" and "因变量"
13. input: activities (what does activities include? if we use one specific stock, which features do i need? such as P/E, MA5, and Risk free rate the machine learning can be used such as regression or classification?)
how to quantify the information whcih has big influnce on the stock market, such as news, social media information
14. goal: predict the trend of whole stock market or specific stock or trust?
15. output: a process model
16. 如果股价低于近20日平均价10%，则用全部可用资金买入， 如果股价高于近20日平均价10%，则卖出全部所持的该股票， 但是多低叫显著低于，多高叫显著高于，
17. **找到一个三家具体的人或基金的具体动作，从而了解买卖，散户跟风，有可能盲目跟风，**
为什么要分开自营商， 陆资有可能是dirty data受外部因素的影响，不只是市场，可能是受政治或者随机的因素的影响
```
## Quantitive Trading System
a complext area of quant finance, MATLAB, R, Python, **C/C++** 

The **skills** required by a sophisticated quantitative trading researcher are diverse. An extensive background in mathematics, probability and statistical testing provide the quantitative base on which to build. An understanding of the components of quantitative trading is essential, including forecasting, signal generation, backtesting, data cleansing, portfolio management and execution methods. More advanced knowledge is required for time series analysis, statistical/machine learning (including non-linear methods), optimisation and exchange/market microstructure. Coupled with this is a good knowledge of programming, including how to take academic models and implement them rapidly.
## Taiwan Stock三大法人
### 自营商：是指在股票买卖中，是自己买卖股票而不是代理他人买卖的公司或者个人。
1. Dealers (Proprietary) 自营商（自行买卖）
2. Dealers (Hedge) 自营商（避险)

### 投信
1. Securities Investment Trust Companies 投信

### 外資
1. Foreign Investors include Mainland Area Investors (Foreign Dealers excluded) 外资及陆资不包含外资自营商
2. Foreign Dealers 外资自营商

### example
1. percentage of 三大法人 (16th Aug 2019): [三大法人买卖金额统计表](https://www.twse.com.tw/zh/page/trading/fund/BFI82U.html)


| 16/08        | 买进金额        | 卖出金额        |
| :--         |     :---:      |          ---: |
| 自营商         | 5,436,677,911(15.1%)     | 5,159,068,904(11.2%)    |
| 投信          | 1,415,994,587(3.9%)       | 1,529,144,400(3.3%)      |
| 外资           | 29,214,513,306(81.0%)       | 39,547,867,502(85.5%)      |
| 合计                  | 36,062,400,444	       | 46,228,432,636      |


| 16/08        | 买进金额        | 卖出金额        |
| :------          |     :---:        |          ---: |
| 自營商(自行買賣) | 1,245,015,007(3.5%)  | 1,305,505,016(2.8%)|
| 自營商(避險)     | 4,191,662,904(11.6%)| 3,853,563,888(8.4%)|
| 投信            |1,415,994,587(3.9%)| 1,529,144,400(3.3%)  |
| 外資及陸資(不含外資自營商)| 29,209,727,946(81.0%)|39,540,219,332(85.5%)    |
| 外資自營商       | 4,785,360(0.01%)       | 7,648,170(0.01%)|
| 合计            | 36,062,400,444	| 46,228,432,636      |

2. [外資及陸資持股比例前20](https://www.twse.com.tw/zh/page/trading/fund/MI_QFIIS_sort_20.html)
- [2923 鼎固-KY](https://tw.stock.yahoo.com/q/ts?s=2923)
- [006203 元大MSCI台灣](https://tw.stock.yahoo.com/q/ta?s=006203)
- [6415 矽力-KY](https://tw.stock.yahoo.com/q/bc?s=6415)
- [8482 商億-KY](https://tw.stock.yahoo.com/q/bc?s=8482)
- [2936 客思達-KY](https://tw.stock.yahoo.com/q/bc?s=2936)

3. Article“Data mining investigation of co-movements on the Taiwan and China stockmarkets for future investment portfolio”

- [Stock Prices index](https://wiki.mbalib.com/wiki/%E8%82%A1%E7%A5%A8%E4%BB%B7%E6%A0%BC%E6%8C%87%E6%95%B0)
	- computed from the prices of selected stocks
	- describe the market (The samples are chosen based on their representation in the market as a whole and are adjusted every year by considering profitability, oper- ational efficiency and trading liquidity of the shares, so that the indi- ces can mirror the market trends)
	- criteria: investable and transparent
	- Taiwan stock exchange capitalization weighted stock index [TAIEX 100](https://zh.wikipedia.org/wiki/%E5%8A%A0%E6%AC%8A%E8%82%A1%E5%83%B9%E6%8C%87%E6%95%B8)
	- include sectors: non-Finance Sub-Index, Non-Electronics Sub-Index, and Non-Finance Non-Electronics Sub-Index
		- industril sub-indices: Cement/ Glass/Ceramics, Textiles, Foods, Plastics/Chemicals/Rubber, Electric Machinery/Electric Appliance/Cable/Electronics, Paper/Pulp, Con- struction, and Finance
		- Industrial Price Average Index
		- Composite Price Average Index
	- source: Reuters, Bridge, Quick, Bloomberg (https://www.bloomberg.com/quote/TWSE:IND), Primark




PS:

- [KD,J](http://www.zqt888.cn/html/cgxt/4966.html)：是以最高价、最低价及收盘价为基本数据进行计算，得出的K值、D值和J值分别在指标的坐标上形成的一个点，连接无数个这样的点位，就形成一个完整的、能反映价格波动趋势的KDJ指标.
- [MACD](http://www.zqt888.cn/html/cgxt/4965.html): 称为指数平滑移动平均线，是由两线一柱组合起来形成，快速线为DIF，慢速线为DEA，柱状图为MACD.
- [RSI](http://www.zqt888.cn/html/cgxt/4967.html): 相对强弱指数RSI，是衡量证券自身内在相对强度的指标，是根据一定时期内上涨和下跌幅度之和的比率制作出的一种技术曲线，能够反映出市场在一定时期内的景气程度。相对强弱指标RSI是用以计测市场供需关系和买卖力道的方法及指标。
- [乖离率](https://www.zcaijing.com/bias/79981.html):又称偏离率，简称Y值，是通过计算市场指数或收盘价与某条移动平均线之间的差距百分比，以反映一定时期内价格与其MA偏离程度的指标，从而得出价格在剧烈波动时因偏离移动平均趋势而造成回档或反弹的可能性，以及价格在正常波动范围内移动而形成继续原有势的可信度.
- [威廉指标](https://www.zcaijing.com/dxbzmmd/208581.html): W&R指标应用摆动原理来研判股市是否处于超买或超卖的现象，即可以测量股市同期循环内的高点或低点，而提出有效的买卖讯号
- [多空指标](https://www.zcaijing.com/kxianjishuzhibiao/1275.html)：是通过将不同天数价格移动平均后再用加权平均方法计算而得出的一条移动平均线的综合指标
- [DMI](http://www.zqt888.cn/html/cgxt/1579.html): 动向指标意在探求股价在上涨和下跌过程中，买卖双方力量的均衡点，以及价格在双方的互动下波动循环的一种技术分析指标。其最大的特点就是能够较为准确的告知我们行情未来的变化趋势.
- [P/E Price-to-Earning Ratio:](https://zh.wikipedia.org/wiki/市盈率) 指每股市价除以每股盈余
- MA 5: N日MA=(C1+C2+C3+C4+C5+....+Cn)/n, C为收盘价，n 为移动平均周期数，N日MA即N日收盘价的算术平均数
- [指數系列](https://www.twse.com.tw/zh/page/products/indices/series.html)





























