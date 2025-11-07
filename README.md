# reddit-sentiment-sp500

# Reddit Sentiment vs. S&P 500 — Quantifying Market Emotion

##  Motivation
In early 2021, the GameStop (GME) “meme-stock” event revealed something new about modern markets:  
collective **retail investor emotion**, coordinated through online platforms like Reddit, could move prices in measurable ways.  

This project revisits that idea in a post-meme era — asking whether **Reddit sentiment still leaves a statistical footprint** on broad market indices like the **S&P 500**.  
It also explores a broader question: *as AI-generated content spreads online, how “human” is the sentiment that still drives markets?*

---

## Project Overview
This repository contains an end-to-end analysis pipeline to:
1. **Collect Reddit posts** from investing communities (`r/wallstreetbets`, `r/stocks`, `r/investing`) using the [Pushshift API](https://github.com/pushshift/api).
2. **Compute daily sentiment** using the VADER NLP model (tuned for social-media tone and emojis).
3. **Fetch financial data** for the S&P 500 index via the [`yfinance`](https://pypi.org/project/yfinance/) API.
4. **Align and compare time-series** to test correlations, lag relationships, and potential predictive power of sentiment.
5. **Visualize results** — interactive plots of sentiment vs. daily returns, volatility, and event spikes.

---

## Methods & Tools
| Category | Tools / Libraries |
|-----------|------------------|
| Data Collection | `requests`, Pushshift API |
| NLP / Sentiment | `nltk`, `vaderSentiment` |
| Market Data | `yfinance`, `pandas` |
| Statistical Analysis | `numpy`, `statsmodels`, `scikit-learn` |
| Visualization | `matplotlib` |
| Environment | `conda`, `python-dotenv`, Jupyter Notebooks |

---

## Example Questions Explored
- Does positive Reddit sentiment lead to short-term market optimism (1-day lag correlation)?
- Are sentiment spikes associated with higher volatility periods?
- Has linguistic “authenticity” changed from 2021 → 2025 (hinting at AI-generated posts)?
- What happens when synthetic sentiment competes with organic retail emotion?

---

## Setup
Clone and recreate the environment:
```bash
git clone https://github.com/<your-username>/reddit-sentiment-sp500.git
cd reddit-sentiment-sp500
conda env create -f environment.yml
conda activate rsent
