# Tomato Market Price Trend Analysis
## Maharashtra APMC Markets | Jan 2025 – Aug 2026

**Author:** Aasif  
**Data Source:** Agmarknet, Government of India  
**Dataset:** 3,093 records | 6 markets | 20 months | Zero missing values

---

## 1. Overview

This report analyses daily tomato modal prices and arrival volumes across
6 major APMC markets in Maharashtra from January 2025 to August 2026.
The analysis covers price trends, seasonal patterns, market-level volatility,
supply-price relationships, and year-over-year comparison.

---

## 2. Market Profiles

| Market | District | Role | Avg Price | CV% |
|--------|----------|------|-----------|-----|
| Nagpur APMC | Nagpur | Distribution Hub | ₹2,188 | 62.1% |
| Mumbai APMC | Mumbai | Consumption | ₹1,847 | 51.3% |
| Pune APMC | Pune | Consumption | ₹1,724 | 54.2% |
| Pune Manjri APMC | Pune | Secondary Consumption | ₹1,612 | 46.8% |
| Pimpalgaon APMC | Nashik | Primary Production Hub | ₹1,156 | 66.4% |
| Nasik APMC | Nashik | Secondary Production Hub | ₹1,084 | 48.9% |

> CV% = Coefficient of Variation. Higher means more price unpredictability.

---

## 3. Key Findings

### 3.1 Price Range and Extremes
- Overall price range: **₹200 – ₹10,500 per quintal** (52x spread)
- Overall mean: **₹1,677/quintal** | Median: **₹1,300/quintal**
- Mean > Median confirms right-skewed distribution — extreme spikes 
  pull the average up
- 95% of all trading days saw prices below ₹3,900 — anything above 
  is a true outlier event

### 3.2 Seasonality
- Tomato prices follow a clear **bi-annual cycle** in Maharashtra
- **Peak months:** July–August (monsoon disrupts road transport from Nashik)
  and November–December (post-kharif supply gap + festival demand)
- **Low months:** February–March (Rabi harvest floods the market)
- Seasonal decomposition confirms a **semi-annual amplitude of ~₹600–900/quintal**
  — meaning the time of year alone shifts prices by this much,
  independent of any other factor

### 3.3 Production vs Consumption Market Gap
- Nashik district (Pimpalgaon + Nasik) supplies ~70% of Maharashtra's 
  total tomato volume
- Price gap between Nashik (₹1,084 avg) and Nagpur (₹2,188 avg) = 
  **~₹1,100/quintal** → this is the transport cost + trader margin 
  embedded in every quintal that travels across the state
- During supply shocks this gap widens further — Nagpur absorbs the 
  most pain because it's furthest from the source

### 3.4 Supply-Price Relationship
- Regression confirms a **statistically significant negative relationship** 
  between arrivals and price at most markets (p < 0.05)
- However, **R² is low across all markets** — arrival quantity alone 
  explains only a small share of price movement
- Remaining variation = weather, transport conditions, demand shocks, 
  trader behaviour, and inter-state supply from Karnataka and Andhra Pradesh
- Pimpalgaon shows the strongest supply-price link (production market economics)
- Nagpur shows the weakest (price driven by availability, not volume)

### 3.5 Year-over-Year Comparison
- **Jan–Apr 2026 prices dropped 30–50%** vs same period in 2025
- Cause: high 2025 prices motivated excess tomato planting →
  bumper 2026 Rabi crop → oversupply → price crash
- Prices recovered from May 2026 onward as supply normalised
- This is the classic agricultural **boom-bust cycle** — 
  well documented across Indian vegetable markets

### 3.6 Volatility Analysis
- Pimpalgaon (CV 66%) and Nagpur (CV 62%) are the most volatile markets
- Counter-intuitive: Pimpalgaon is volatile because its prices are 
  directly tied to harvest size — bumper crop days see massive price drops
- Nagpur is volatile because supply disruptions hit it hardest and fastest
- Pune Manjri (CV 47%) is the most stable — smaller, localised market 
  with more consistent demand

---

## 4. Notable Price Events

| Event | Date | Market | Price | Cause |
|-------|------|--------|-------|-------|
| Extreme Spike | Jan 2025 | Pune | ₹10,500 | Cold wave + supply disruption |
| Summer Peak | Jul–Aug 2025 | All | ₹2,800–3,200 | Monsoon transport disruption |
| Winter Peak | Nov–Dec 2025 | All | ₹2,500–3,000 | Post-kharif supply gap |
| Price Crash | Jan–Apr 2026 | All | ₹200–800 | Oversupply from bumper Rabi crop |
| Recovery | May–Aug 2026 | All | ₹1,200–2,200 | Supply normalisation |

---

## 5. Implications

**For Farmers:**
Prices are predictably seasonal. Planting decisions made during high-price 
periods lead to oversupply the following season — the boom-bust trap. 
Storage infrastructure and futures market access could help smooth income.

**For Traders:**
Nagpur offers the highest margins but carries the highest risk.
Nashik markets offer stability but thin margins. 
The Jul–Aug and Nov–Dec windows are historically the best for selling.

**For Policy:**
70% of Maharashtra's tomato supply comes from one district (Nashik).
Any weather event, road disruption, or crop disease there cascades 
across the entire state. Supply chain diversification and price 
stabilisation funds (like PM-AASHA) are critical intervention points.

---

## 6. Data & Methodology

- **Source:** Agmarknet (data.gov.in) — Government of India agricultural markets portal
- **Coverage:** Daily modal price and arrival quantity for 6 Maharashtra APMC markets
- **Tools:** Python (pandas, numpy, matplotlib, seaborn, scipy, statsmodels)
- **Analysis:** Descriptive statistics, seasonal decomposition (period=6), 
  linear regression (scipy.stats.linregress), rolling volatility (CV%)
- **Charts:** 14 visualisations generated programmatically and reproducible

---

*Full code available at: github.com/Aasifshaikh-00000/tomato-market-analysis*