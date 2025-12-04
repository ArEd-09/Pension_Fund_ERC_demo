# Pension Fund ERC Optimization Model

**https://erc-portfolio-creator.streamlit.app/** | **Authors:** Edward Arion, Lucas Jaccard, Audrey Champion, Rihem Rhaiem, Arda Budak

## Project Overview
As part of the Quantitative Asset & Risk Management II course, this project implements a quantitative asset allocation tool based on the **Equal Risk Contribution (ERC)** approach. Designed for a theoretical USD Pension Fund mandate, the web app aims to deliver a tool for testing multiple portfolio allocations where each asset contributes equally to the total portfolio risk.

Using the Compustat database since 2000, we selected 1000 North American companies and 1500 International companies based on their market cap, as well as 44 ETFs in order to integrate multiple asset classes and to allow for the possibility of a global exposition. All values have been converted to USD. By doing so, the returns are indeed for an USD-based investor.

**WARNING**: An AI chatbot has been integrated to the app, which was trained on our data and methodology. Unfortunately, it was integrated only for the purpose of the project, and will no longer be available due to the expiry of the free-plan. The country exposure graph has a variable called "unknown". It is actually the ETFs exposure.

## 🔑 Key Features
* **ERC Optimization Engine:** Uses a 36-month wolling window to compute the matrix of covariance and adjust weights over time. If certain assets are not available in the                                   database at a selected date, they integrate the portfolio later, once they become available.
* **Monte Carlo Simulation:** Uses the historical distribution of the selected assets and does NOT assume Normal distribution (Historical Bootstrap).
* **Backtesting Framework:** Compares the ERC strategy against benchmarks (equally-weighted & S&P500) over the selected period.
* **Risk-Free Rate:** All returns computed are in excess of the risk-free rate (Fama-French 1-month treasury bill).
* **Interactive Dashboard:** Real-time parameter adjustment (selected assets, selected period, rebalancing frequency) using Streamlit.

## 🛠️ Technology Stack
* **Python 3.9+**
* **Core Libraries:** `pandas`, `numpy`, `scipy`, `matplotlib`/`plotly`
* **Frontend:** `Streamlit`

## ⚙️ Installation & Usage

### 1. Clone the repository
```bash
git clone [https://github.com/EdwardArion/](https://github.com/EdwardArion/)[Nom-Du-Repo].git
cd [Nom-Du-Repo]
