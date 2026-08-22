# 🍅 Tomato Market Price Trend Analysis — Maharashtra

> *The government has the tools to prevent tomato price crashes.  
> What's missing is a data-driven trigger — and the will to use it early.*

Analysis of 3,093 daily APMC records across 6 Maharashtra markets
from January 2025 to August 2026 — identifying where the supply
signal exists, where it doesn't, and what existing schemes should
do differently.

---

## The Finding in One Paragraph

India's four intervention systems (PSF, MIS, Operation Greens,
Tomato Grand Challenge) all activate after the crisis is visible
in retail prices. Our regression analysis identifies that
**Nasik APMC daily arrivals** are the only statistically proven
supply-price signal in Maharashtra's tomato network
(R²=17%, p<0.001, slope -₹3.12/MT) — updated daily on Agmarknet,
free to access, and currently unmonitored as a trigger.
Separately, Pimpalgaon's seasonal supply surge
(129,000 MT in a single month, causing a 66% within-season price crash)
points to cold storage as the structural fix —
and Operation Greens already funds it.

---

## Dataset

| Detail | Value |
|--------|-------|
| Source | Agmarknet — Government of India |
| Commodity | Tomato |
| Markets | 6 Maharashtra APMC markets |
| Period | Jan 2025 – Aug 2026 (20 months) |
| Records | 3,093 daily observations |
| Missing values | Zero |

---

## Key Numbers (Verified from Data)

| Metric | Value |
|--------|-------|
| Price range | ₹200 – ₹10,500/quintal |
| Mean price | ₹1,677 | Median | ₹1,400 |
| Most expensive market | Nagpur (₹2,188 avg) |
| Cheapest market | Nasik (₹1,084 avg) |
| Nashik-Nagpur supply chain gap | ₹1,104/quintal |
| Most volatile market | Pimpalgaon (CV 66%) |
| Most stable market | Pune Manjri (CV 46.5%) |
| Nashik district supply share | 61.1% of state total |
| Seasonal amplitude | ₹1,194/quintal (decomposition) |
| Seasonal peak | June | Trough | March |
| Only proven supply-price signal | Nasik (R²=17%, p<0.001) |

---

## Six Findings

**1 — Price range is extreme but seasonal**
₹200–₹10,500 over 20 months. Seasonal decomposition confirms
a recurring ₹1,194 amplitude tied to the agricultural calendar —
not random volatility.

**2 — The Pimpalgaon within-season crash**
Pimpalgaon produces near-zero supply Jan–Jul, then floods the market
Aug–Nov. Sep 2025: 129,171 MT arrived in one month → price fell
from ₹3,221 to ₹1,083 within 8 weeks. Farmers dump simultaneously
because there is no cold storage to stagger sales.

**3 — Supply predicts price only at Nasik**
Regression across all 6 markets. Only Nasik is statistically
significant (R²=17%, p<0.001). All other markets including
Pimpalgaon show R²<1% and p>0.40. Simple arrival monitoring
at Nasik outperforms complex multi-market models.

**4 — One district, 61% of state supply**
Pimpalgaon (48.7%) + Nasik (12.4%) = 61.1% of all Maharashtra
tomato arrivals from Nashik district alone. Single point of failure
with no systematic monitoring attached to intervention triggers.

**5 — The ₹1,104 supply chain cost**
Nasik avg ₹1,084 vs Nagpur avg ₹2,188. Same tomato, 500km apart.
The gap is transport, absent cold chain, middlemen, and market fees.
Operation Greens' 50% transport subsidy exists to address this
but is claimed reactively, not triggered by arrival data.

**6 — 2026 prices were higher than 2025 same months**
Jan 2025 avg ₹1,041 vs Jan 2026 avg ₹1,856 (+78%). 2025 started
at historically depressed levels — not a normal baseline year.
YoY comparison requires this context to interpret correctly.

---

## The Recommendation

**Nasik as early warning lever:**
When Nasik monthly arrivals rise >50% above prior 3-month average,
prices will fall predictably (proven, R²=17%). MIS procurement
should trigger then — at the supply peak — not after downstream
retail prices spike weeks later.

**Cold storage at Pimpalgaon:**
129,000 MT arriving in one month with no storage = guaranteed crash.
Operation Greens already funds 50% cold storage subsidy.
Priority allocation to Pimpalgaon specifically would let farmers
stagger sales and avoid the 66% within-season price collapse.

No new scheme. No new budget. Same tools — used on the right signal,
at the right time.

---

## Project Structure

```
tomato-market-analysis/
├── data/                           → Raw dataset (never modified)
├── notebooks/
│   ├── 01_data_exploration.ipynb   → Data profiling and quality check
│   ├── 02_analysis.ipynb           → Decomposition, regression, summary
│   └── 03_visualizations.ipynb     → 14 charts with interpretations
├── charts/                         → All generated visualisations
├── report/
│   ├── findings.md                 → Full written analysis
│   └── market_summary.csv          → Master stats table
└── webpage/                        → Interactive showcase
```

## Run It

```bash
git clone https://github.com/Aasifshaikh-00000/tomato-market-analysis.git
cd tomato-market-analysis
pip install -r requirements.txt
# Run notebooks in order: 01 → 02 → 03
```

---

*Aasif | BSc Data Science | SK College, Nerul | August 2026*