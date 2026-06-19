# Predicting Stock Price Moves with News Sentiment

## Overview

This project investigates the relationship between financial news sentiment and stock market performance. By combining Natural Language Processing (NLP) techniques with technical stock analysis, the project aims to determine whether news headlines can provide useful signals for predicting stock price movements.

The analysis was completed as part of the Nova Financial Solutions Financial News Sentiment Analysis Challenge.

---

## Business Objective

Financial news influences investor decisions and market behavior. The objective of this project is to:

* Analyze financial news headlines and extract sentiment scores.
* Calculate technical indicators from historical stock price data.
* Measure the statistical relationship between news sentiment and stock returns.
* Provide data-driven investment insights based on the findings.

---

## Dataset

### Financial News Dataset

The dataset contains:

* Headline
* URL
* Publisher
* Publication Date
* Stock Symbol

### Historical Stock Price Dataset

The stock market dataset contains:

* Date
* Open
* High
* Low
* Close
* Volume

Stock data was obtained using Yahoo Finance (YFinance).

---

## Project Structure

```text
financial-news-stock-analysis/

├── .github/
├── .vscode/
├── data/
│   └── raw/
├── notebooks/
├── scripts/
├── src/
├── tests/
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Task 1: Exploratory Data Analysis (EDA)

### Completed Analysis

* Data loading and cleaning
* Missing value analysis
* Headline length analysis
* Publisher activity analysis
* Publication trend analysis
* Keyword and topic exploration
* News volume visualization

### Key Findings

* Most financial headlines are relatively short and information-focused.
* A small number of publishers contribute a large portion of the articles.
* News publication volume varies significantly across time.

---

## Task 2: Quantitative Analysis

Technical indicators were computed using TA-Lib.

### Indicators Calculated

#### Moving Averages

* SMA 20
* SMA 50
* EMA 20
* EMA 50

#### Relative Strength Index (RSI)

Used to identify overbought and oversold market conditions.

#### MACD

Used to identify momentum shifts and trend reversals.

### Visualizations

* Closing Price vs Moving Averages
* RSI Indicator
* MACD Indicator

---

## Task 3: Sentiment and Correlation Analysis

### Sentiment Analysis

Financial news headlines were analyzed using sentiment scoring techniques.

Each article was classified as:

* Positive
* Neutral
* Negative

### Date Alignment

News publication dates were aligned with stock trading dates to ensure accurate comparison between sentiment and market performance.

### Daily Returns

Daily stock returns were calculated using:

```python
Daily_Return = Close.pct_change() * 100
```

### Correlation Analysis

Average daily sentiment scores were compared with daily stock returns using Pearson Correlation.

### Results

Pearson Correlation:

```text
0.124
```

Interpretation:

* The relationship is positive but relatively weak.
* Positive sentiment tends to be associated with higher daily returns.
* Negative sentiment tends to be associated with lower daily returns.

### Average Daily Returns by Sentiment

| Sentiment | Average Return (%) |
| --------- | ------------------ |
| Negative  | -0.856             |
| Neutral   | 0.325              |
| Positive  | 0.921              |

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* TA-Lib
* NLTK / NLP Tools
* Git
* GitHub Actions
* Jupyter Notebook

---

## Installation

Clone the repository:

```bash
git clone <repository-url>
```

Create and activate a virtual environment:

```bash
python -m venv .venv
```

Windows:

```bash
.venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Key Insights

* News sentiment has a measurable relationship with stock returns.
* Positive news generally corresponds to higher average returns.
* Technical indicators help confirm trends identified through sentiment analysis.
* Combining sentiment analysis with technical analysis may improve investment decision-making.

---

## Limitations

* Correlation does not imply causation.
* Market movements are influenced by many external factors.
* Some headlines may not contain strong sentiment signals.
* News impact may occur with time delays.

---

## Future Improvements

* Apply advanced transformer-based sentiment models.
* Analyze additional stocks.
* Build predictive machine learning models.
* Investigate lagged effects of news sentiment on stock returns.

---

## Author

Helina Leul

Financial News Sentiment Analysis Project – Nova Financial Solutions Challenge
