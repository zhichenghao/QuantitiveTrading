# Twitter mood predicts the stock market

## Abstract
- Invesitager whether  measurements of collective mood states derived from large-scale Twitter deeds are correlated to the valued of the Dow Jones Industrial Average (DJIA) over time.

- analyze text content of daily Twitter dees by tow mood tracking tools: OpinionFinder (measure positive vs. negative mood) and Mood States (GPOMS, measure mood in 6 dimensions: calm, alert, sure, vital, kind and happy)

- cross-validate the resulting mood time series 

## 1. Introduction
- Effient Market Hypothesis (EMH): stock market prices are largely driven by new information. i.e. news, rather than present and past prices
- critically examined EMH: Socionomic Theory of Finance (STF), behavioral economics and behavioral finance. These theory show staock market can some degree be predicted
- News maybe unpredictable but very early indicators can be extracted from online social media to predict changes in various economic and commercial indivators.
- news, public mood states, sentiment
- difficut to investigate large scale public mood and time-consuming
- Twitter has large-scale tweets which can provide an accurate representation of public mood and sentiment
- OpinionFindder: analyze positive or negative
- GPOMS: analyze text content of tweets to generate six-dimensional dailuy time series of public moode to provide a more detailed view of changes in pubilc along a variety of different mood dimensions.
- result correlated with Dow Jones Industrial Average  

## 2. Results

### 2.1 Data and methods overview
- Time period: February 28 to December 19th 2008
- Number: 
	- 9853498 tweets posted by approximately 2.7M users
	- Identification: tweet identiier and the date-time of the submission
	- only take into account tweets that contain explicit statements of their authors' mood states, e.g. I feel, i am feeling...
	- filter out tweets taht match regular expressions http:" or "www"
- ***Three Phases***:
	- first phases: subject collection of daily tweets to 2 mood assessment tools: opinionFinder and GPOMS
		- result: 7 public mood time series (one by OpinionFinder and 6 by GPOMS) and DJIA closing-values from Yahoo! Finance
	- Second Phases: investigate the hypothesis that public mood as measured by GPOMS and OpinionFinder is predictive of Future DJIA values.
		- use Granger causality analysis which correlate DJIA values to GPOMS and OF values of the past n days.
	- Third phases: deploy a self-organizing Fuzzy Neural Network model to test the hypothesis: to assess the effects of including public mood information on the accuracy of the prediction model.

### 2.2 Generating public mood time series: OpinionFinder and GPOMS (need to find the z-score normalization???)
- OpinionFinder is a software package for sentiment analysis that can be applied to determine sentence-level subjectivity, e.g. identify the emotional polarity of sentences
- select positive and negtive words that are marked as "weak" and "strong" from2718 positve and 4912 negative words
- GPOMS captured additional dimensions of public mood: calm, alert, sure, vital, kind and happy.
-method: Normalize OF and GPOMS to z-scores on the basis of a lcoal mean and standard deviation within a sliding window of k days before and after the particular date.
- z-score normalization is intended to provide a common scale for comparisons of the OF and GPOMS time series.

### 2.3 Cross-validating OF and GPOMS time series against large socio-cultural events (linear regression result ???)
- validate the ablility of OF and GPOMS to capture various aspects of public mood
	- Choose time peirod form Octorber 5, 2008 to December 5 2008, because it includes serveral social cultural events (US presidential election and thanksgiving) that may have complex, uniques, significant effect on public mood.

### 2.4 Bivariate Granger causality analysis of mood vs.DJIA prices
- Explore that whether other vairabtion of the public's mood state correlate with changes in the stock market, in particular DJIA closing values
- apply Granger causality analysis: Granger causality analysis rests on the assumption that if a variable X causes Y then changes in X will systematically occur before changes in Y. 
- reject the null hypothesi that the mood time series do not predict DJIA values

### 2.5 Non-linear models for emotion-based stock prediction
- relation between public mood and stock market values is almost non-linear: use Self-organizing Fuzzy Neural Network(SOFNN) model
	- input 1: the past 3 days of DJIA values
	- input 2: the same combined with various permutations of our mood time series
	- evaluate SOFNN model's ability to predict daily DJIA prices
	
### 3. Discussion
- Changes in public mood state cna indeed be tracked from the content of large-scale Twitter feeds by means of rather simple text processing techqniues
- The calmness of the public (measured by GPOMS) is thus predictive of the DJIA rather than general levels of positive sentiment as measured by OpinionFinder.
- Limitations:
	- First: we note that our analysis is not designed to be limited to any par- ticular geographical location nor subset of the world’s population.
	- Second, although we have cross-validated the results of 2 different tools to assess public mood states, we have no knowledge of the “ground truth” for public mood states nor in fact for the particular subsample of the population repre- sented by the community of Twitter.com users.
	- these results are strongly indicative of a predictive correlation between measurements of the public mood states from Twitter feeds, but offer no information on the causative mecha- nisms that may connect online public mood states with DJIA values.






































