# 🍅 Tomato Market Price Trend Analysis — Maharashtra

> *The government has the tools to fix tomato price volatility.  
> What's missing is the trigger.*

A data analysis study of daily tomato prices across **6 Maharashtra APMC markets**
from **January 2025 to August 2026** — identifying a leading market signal
that precedes every major price event in the state.

---

## The Finding in One Paragraph

India's four major price intervention systems (PSF, MIS, Operation Greens,
Tomato Grand Challenge) are either reactive or structural — they activate
after the crisis is already visible. Our analysis of 3,093 daily market
observations identifies a single publicly available signal —
**Pimpalgaon Baswant APMC arrival volumes** — that precedes state-wide
price crashes by 60–90 days. Using this signal with existing government
infrastructure could prevent the boom-bust cycle without any new scheme or budget.

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

## Project Structure
## 🗂️ Project Structure

```text
tomato-market-analysis/
├── data/       → Raw dataset (CSV)
├── notebooks/  → Python analysis scripts
├── charts/     → Generated visualizations
├── report/     → Written findings and insights
└── webpage/    → Showcase website
```


## Key Findings

1. **The swing is predictable** — seasonal decomposition confirms a
   recurring ₹600–900/quintal annual amplitude. Not chaos. A calendar.

2. **Farmers are in a self-defeating cycle** — high prices trigger
   excess planting which triggers the very crash that hurts them.
   MIS activates after the damage is done.

3. **Supply quantity explains very little** — R² < 15% across all markets.
   A single upstream signal is more reliable than complex forecasting models.

4. **One district controls the state** — Nashik supplies 70% of
   Maharashtra's tomato volume. Single-point-of-failure with no monitoring.

5. **The ₹1,100 gap** — the Nashik-to-Nagpur price difference is the
   cost of an absent cold chain. Operation Greens addresses this
   structurally but not in real-time.

6. **Nagpur is most vulnerable** — highest price, highest volatility,
   zero local production, no buffer.

---

## The Recommendation

Monitor Pimpalgaon Baswant APMC arrivals daily on Agmarknet.
When volumes exceed 150% of the 20-month average for 2+ months —
pre-position NCCF trucks, alert farmers via PM-KISAN, and begin
PSF procurement. Use existing tools. Just 60 days earlier.

---

## Run It

```bash
git clone https://github.com/Aasifshaikh-00000/tomato-market-analysis.git
cd tomato-market-analysis
pip install -r requirements.txt
# Run notebooks in order: 01 → 02 → 03
```

---

*Built by Aasif | BSc Data Science | August 2026*
