# Tomato Market Price Trend Analysis
## Maharashtra APMC Markets | Jan 2025 – Aug 2026

**Author:** Aasif  
**Data Source:** Agmarknet, Government of India  
**Dataset:** 3,093 records | 6 markets | 20 months | Zero missing values

---

## The Core Argument

The Indian government has four systems to fight tomato price volatility —
PSF, MIS, Operation Greens, and the Tomato Grand Challenge.
All of them are either reactive (act after the crisis) or structural (slow to deploy).

**None of them is predictive.**

Our analysis of 20 months of daily APMC data from Maharashtra identifies
a single, measurable, publicly available signal that precedes every major
price event in the state — and proposes using existing government
infrastructure to act on it before the crisis lands.

---

## 1. What We Analysed

| Detail | Value |
|--------|-------|
| Commodity | Tomato |
| State | Maharashtra |
| Markets | 6 APMC markets |
| Period | Jan 2025 – Aug 2026 |
| Records | 3,093 daily observations |
| Missing values | Zero |

**Markets covered:**

| Market | District | Role |
|--------|----------|------|
| Pimpalgaon Baswant APMC | Nashik | Primary Production Hub |
| Nasik APMC | Nashik | Secondary Production Hub |
| Mumbai APMC | Mumbai | Consumption |
| Pune APMC | Pune | Consumption |
| Pune Manjri APMC | Pune | Secondary Consumption |
| Nagpur APMC | Nagpur | Inland Distribution |

---

## 2. What Existing Systems Do (And Where They Stop)

| System | What It Does | When It Acts | The Gap |
|--------|-------------|-------------|---------|
| PSF (Price Stabilisation Fund) | Buys from surplus states, sells at ₹35–45/kg to consumers | After spike is visible | Reactive |
| MIS (Market Intervention Scheme) | Reimburses 100% transport to move surplus out of crashing markets | After crash has begun | Reactive |
| Operation Greens | 50% subsidy on cold storage and transport infrastructure | Always active | Structural but slow |
| Tomato Grand Challenge | Funds 28 startups for forecasting apps and processing | In progress | No live trigger yet |

**The gap:** Every system waits for the crisis to show up in retail prices 
before activating. By then farmers have already made irreversible decisions —
they have planted, harvested, and sent trucks to market.
The damage is done before the intervention begins.

---

## 3. Key Findings From Our Data

### Finding 1 — The Swing Is Predictable, Not Random
**Evidence: Chart 04 (Seasonality) + Chart 13 (Decomposition)**

Price ranged from ₹200 to ₹10,500/quintal across 20 months — a 52x spread.
This looks like chaos but our seasonal decomposition proves it is not.
A recurring semi-annual pattern with an amplitude of ₹600–900/quintal
appears consistently — independent of weather or policy.
The swing is violent but it has a calendar.
**You can see it coming.**

### Finding 2 — Farmers Are Trapped in a Self-Defeating Cycle
**Evidence: Chart 08 (Year-over-Year Comparison)**

Jan–Apr 2026 prices crashed 30–50% versus the same months in 2025.
The reason: high 2025 prices motivated excess planting across Maharashtra
and Karnataka. That bumper Rabi 2026 crop hit markets simultaneously
and collapsed prices. The farmers who planted because prices were high
got hurt because they planted.
MIS was triggered after the crash. It could not undo sowing decisions
made three months earlier.

### Finding 3 — Arrival Quantity Alone Explains Almost Nothing
**Evidence: Chart 06 (Scatter) + Regression R²**

Linear regression across all 6 markets shows a statistically significant
negative relationship between arrivals and price (p < 0.05) —
more supply does push prices down. But R² is low across every market.
Arrival quantity alone explains only 5–15% of daily price movement.
The remaining 85–95% is weather, transport availability, inter-state
demand, and trader behaviour.
This is why blanket forecasting apps struggle — and why a 
**single-market leading indicator** is more valuable than a complex model.

### Finding 4 — One District Controls the Entire State
**Evidence: Chart 11 (Market Share)**

Pimpalgaon APMC alone handles 49% of all Maharashtra tomato arrivals.
Add Nasik APMC and the Nashik district accounts for ~70% of total supply.
Every market in the state — Mumbai, Pune, Nagpur — is dependent on 
trucks leaving this one district.
One crop disease, one highway closure, one bad monsoon in Nashik,
and every retail price in Maharashtra moves within 48 hours.
This is a systemic single-point-of-failure that no existing scheme addresses.

### Finding 5 — The ₹1,100 Gap Is the Supply Chain Cost
**Evidence: Chart 10 (Price Range) + Chart 09 (Correlation)**

The average price difference between Nasik (₹1,084) and Nagpur (₹2,188)
is ₹1,104/quintal. This is not profit — it is transport cost, 
cold chain absence, market fees, and middlemen margins embedded in every
quintal that crosses the state. During supply shocks this gap widens further.
Operation Greens' 50% transport subsidy directly targets this gap —
but uptake depends on farmers and traders applying. 
The subsidy exists. The awareness and timing to use it does not.

### Finding 6 — Nagpur Is the Most Exposed Market
**Evidence: Chart 07 (Volatility) + Chart 03 (Heatmap)**

Nagpur is simultaneously the most expensive (₹2,188 avg) and 
most volatile market (CV 62%) despite having zero local production.
It absorbs every supply shock from Nashik with no buffer.
A cold wave in Nashik or a truck strike on NH-48 hits Nagpur
before any intervention can reach it.

---

## 4. The Recommendation — The Pimpalgaon Signal

The government does not need a new scheme, a new agency, or new money.
It needs a data-driven trigger that fires PSF and MIS 
**before** the crisis is visible in retail prices.

Our data identifies that trigger.

**The signal:**
> When Pimpalgaon Baswant APMC monthly arrival volumes exceed
> 150% of their 20-month rolling average for two or more
> consecutive months — a state-wide price crash will follow
> within 60–90 days.

**What existing systems should do when signal fires:**

| Action | Agency | Using Existing Tool |
|--------|--------|-------------------|
| Pre-position NCCF trucks for inter-state redistribution | NCCF / NAFED | MIS infrastructure |
| SMS alert to farmers in Nashik via PM-KISAN network — reduce new planting | Ministry of Agriculture | PM-KISAN database |
| Begin procurement from Pimpalgaon before crash lands | PSF | Price Stabilisation Fund |
| Trigger Operation Greens transport subsidy proactively | MoFPI | Operation Greens |

**Why this is different from what exists:**
- The data (Agmarknet) is already public and updated daily — no new sensors needed
- The infrastructure (PSF, MIS, NCCF) already exists — no new budget needed
- The trigger threshold is objective and data-driven — removes political delay
- It acts 60–90 days earlier than current interventions

**The one thing missing is the monitoring and the will to act on the signal.**

---

## 5. Summary Statistics

| Metric | Value |
|--------|-------|
| Price range | ₹200 – ₹10,500/quintal |
| Mean price | ₹1,677/quintal |
| Median price | ₹1,300/quintal |
| Most expensive market | Nagpur (₹2,188 avg) |
| Cheapest market | Nasik (₹1,084 avg) |
| Most volatile | Pimpalgaon (CV 66%) |
| Most stable | Pune Manjri (CV 47%) |
| Highest volume | Pimpalgaon (49% of all arrivals) |
| Seasonal amplitude | ₹600–900/quintal per cycle |
| YoY price change Jan–Apr | −30% to −50% (2025 → 2026) |

---

## 6. Methodology

| Step | Tool |
|------|------|
| Data loading and profiling | pandas, numpy |
| Visualisation (14 charts) | matplotlib, seaborn |
| Seasonal decomposition | statsmodels (period=6) |
| Regression analysis | scipy.stats.linregress |
| Volatility measurement | Rolling CV% (30-day window) |

*Full reproducible code: github.com/Aasifshaikh-00000/tomato-market-analysis*