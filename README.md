# financial-news-stock-analysis
Predicting Stock Price Moves with Financial News Sentiment
Executive Summary

Financial markets are influenced not only by company performance and historical price patterns but also by investor perception and market news. This project analyzes the relationship between financial news sentiment and stock price movements using Natural Language Processing (NLP), technical indicators, and statistical correlation analysis.

The goal of this analysis is to determine whether news sentiment can provide useful signals for predicting short-term stock movements.

The project combines two major datasets:

Financial news headlines with publication information and stock symbols
Historical stock price data containing Open, High, Low, Close, and Volume values

The analysis pipeline includes:

Exploratory Data Analysis (EDA)
News sentiment extraction
Technical indicator calculation using TA-Lib
Daily return calculation
Sentiment-price correlation analysis

The results show that news sentiment has a measurable relationship with stock returns, suggesting that financial headlines can provide useful information when combined with traditional market indicators.

1. Introduction

Financial news is published continuously and can influence investor decisions. Positive announcements may increase buying pressure, while negative news may cause selling activity.

However, not every headline affects the market. Therefore, this project focuses on separating useful information from noise by analyzing:

The emotional tone of financial news
The relationship between sentiment and stock performance

The analysis was conducted as part of Nova Financial Solutions' effort to improve data-driven investment insights.

2. Dataset Description

Two datasets were used.

Financial News Dataset

The news dataset contains:

Column	Description
headline	News article title
url	Article link
publisher	News source
date	Publication timestamp
stock	Related stock symbol

The dataset was cleaned by:

Converting dates into proper datetime format
Handling timezone differences
Removing invalid records
Creating text-based features

Additional features created:

Headline length
Word count
Sentiment score
Sentiment category
Stock Price Dataset

Historical price data contains:

Column	Description
Open	Opening price
High	Highest price
Low	Lowest price
Close	Closing price
Volume	Trading volume

Daily returns were calculated using:

DailyReturn=
Close
t−1
	​

Close
t
	​

−Close
t−1
	​

	​

×100
3. Exploratory Data Analysis
News Volume Analysis

The publication frequency of financial news was analyzed over time.

The analysis showed periods where news activity increased significantly, suggesting possible relationships with important market events.

Publisher Analysis

The most active publishers were identified.

This analysis helps understand which sources contribute the largest amount of financial information.

Headline Analysis

Headline length and word count were analyzed to understand the structure of financial news.

Most headlines were concise and focused on:

Earnings announcements
Price movements
Analyst recommendations
Market events
4. Sentiment Analysis
Methodology

Sentiment analysis was performed on financial headlines using a natural language processing approach.

Each headline received a sentiment score:

Positive → optimistic market tone
Neutral → no strong emotional signal
Negative → pessimistic market tone

The sentiment score was converted into three categories:

Category	Meaning
Positive	Strong positive signal
Neutral	No clear direction
Negative	Negative market sentiment
Sentiment Distribution

The analysis found:

Positive news: 442,936 articles
Neutral news: 739,332 articles
Negative news: 225,060 articles

Most financial headlines were neutral, which is expected because many market reports are informational rather than emotional.

5. Technical Analysis

Technical indicators were calculated using TA-Lib.

Moving Averages

The following indicators were created:

Simple Moving Average (SMA)
SMA 20
SMA 50
Exponential Moving Average (EMA)
EMA 20
EMA 50

Moving averages help identify market trends.

A shorter moving average crossing above a longer moving average may indicate bullish momentum.

RSI Indicator

Relative Strength Index (RSI) was calculated to identify overbought and oversold conditions.

Interpretation:

RSI above 70 → possible overbought condition
RSI below 30 → possible oversold condition
MACD Indicator

MACD was calculated to analyze momentum changes.

Interpretation:

MACD above signal line → increasing bullish momentum
MACD below signal line → possible bearish momentum
6. Correlation Analysis

To measure the relationship between news sentiment and stock movement:

News dates were aligned with trading dates
Daily sentiment was averaged
Stock returns were merged with sentiment values
Pearson correlation was calculated

The calculated correlation:

Pearson correlation = 0.124

This indicates a weak positive relationship between sentiment and daily returns.

A positive sentiment score was generally associated with slightly higher returns.

7. Sentiment Impact on Returns

Average daily returns by sentiment category:

Sentiment	Average Return
Negative	-0.856%
Neutral	0.325%
Positive	0.921%

The results show:

Positive news days produced higher average returns
Negative news days produced negative average returns

This suggests that news sentiment can provide additional information for short-term market analysis.

8. Investment Strategy Recommendation

Based on the findings:

Strategy 1: Sentiment-Based Screening

Investors could monitor highly positive news sentiment stocks and investigate possible upward price movement.

Strategy 2: Combine Sentiment with Technical Indicators

News sentiment alone is not enough.

A stronger strategy combines:

Positive sentiment
Increasing moving averages
Strong momentum indicators
Strategy 3: Risk Management

Because correlation is not extremely strong, investors should avoid relying only on news sentiment.

Other factors such as:

Company fundamentals
Market conditions
Economic events

should also be considered.

9. Limitations

This analysis has several limitations:

Correlation does not prove causation
News impact may happen with delays
Some headlines may contain noise
Market movements depend on many external factors

Future improvements could include:

Using advanced NLP models
Adding more companies
Testing prediction models
Including news publication time effects
10. Conclusion

This project demonstrates how financial news and stock market data can be combined to generate useful market insights.

The analysis showed that sentiment extracted from financial headlines has a relationship with stock returns. When combined with technical indicators such as moving averages, RSI, and MACD, sentiment analysis can become a valuable tool for financial decision-making.

The results support the idea that market narratives influence investor behavior and can contribute to predictive analytics systems.
