# 📈 Stock Screener — Complete Trading Guide

> **27 filters | 17 strict technicals | 4 timeframe momentum | Must Go Up**

---

# � MONTHLY SCREENER

> **Timeframe:** Hold for **2-8 weeks**. Run once a week. Best for **swing trading / positional trading.**

## 🔍 Monthly Query

Copy-paste this into [Screener.in](https://www.screener.in/screens/) → Create New Screen:

```
Is not SME AND
Market Capitalization > 500 AND
Return over 1month > 0 AND
Return over 1week > 0 AND
Return over 1day > 0 AND
Return over 3months > 0 AND
Current price > DMA 50 AND
Current price > DMA 200 AND
DMA 50 > DMA 200 AND
DMA 50 > DMA 50 previous day AND
DMA 200 > DMA 200 previous day AND
RSI > 52 AND
RSI < 68 AND
MACD > MACD Signal AND
MACD > 0 AND
MACD > MACD Previous Day AND
MACD Signal > MACD Signal Previous Day AND
Volume > Volume 1month average AND
Current price > High price * 0.85 AND
Profit after tax > 0 AND
Return on capital employed > 15 AND
Return on equity > 12 AND
Debt to equity < 1 AND
Piotroski score > 5 AND
Sales growth 3Years > 8 AND
Profit growth 3Years > 5 AND
Cash from operations last year > 0
```

### 📅 When to Run Monthly Screener
| When | Why |
|------|-----|
| **Monday morning** (9:00–9:15 AM) | Weekend gives clean data. Plan the week |
| **1st trading day of the month** | Monthly return resets, fresh signals |
| **After a 2-3 day pullback that bounces** | Strongest stocks survive dips |

### 📅 Monthly Hold Period
| Action | Timeline |
|--------|----------|
| **Enter** | Over 2-3 days (split buys) |
| **Hold** | 2-8 weeks minimum |
| **Review** | Every Monday — re-run screener to confirm stock still passes |
| **Exit** | When sell signals trigger (see Sell Rules below) |

---

# 📆 WEEKLY SCREENER

> **Timeframe:** Hold for **3-10 days**. Run daily or every 2 days. Best for **short-term swing trading.**

## 🔍 Weekly Query

Copy-paste this into [Screener.in](https://www.screener.in/screens/) → Create New Screen:

```
Is not SME AND
Market Capitalization > 500 AND
Return over 1week > 2 AND
Return over 1day > 0 AND
Return over 1month > 0 AND
Current price > DMA 50 AND
Current price > DMA 200 AND
DMA 50 > DMA 200 AND
DMA 50 > DMA 50 previous day AND
DMA 200 > DMA 200 previous day AND
RSI > 52 AND
RSI < 68 AND
MACD > MACD Signal AND
MACD > 0 AND
MACD > MACD Previous Day AND
MACD Signal > MACD Signal Previous Day AND
Volume > Volume 1month average AND
Current price > High price * 0.85 AND
Profit after tax > 0 AND
Return on capital employed > 15 AND
Return on equity > 12 AND
Debt to equity < 1 AND
Piotroski score > 5 AND
Sales growth 3Years > 8 AND
Profit growth 3Years > 5 AND
Cash from operations last year > 0
```

### 📆 When to Run Weekly Screener
| When | Why |
|------|-----|
| **Every morning** (9:00–9:15 AM) | Fresh daily data for short-term trades |
| **Tuesday-Wednesday** | Best days — Monday gaps are settled, Friday selling hasn't started |
| **After a sharp 1-day dip that recovers** | Stocks that bounce back fast = strongest short-term momentum |

### 📆 Weekly Hold Period
| Action | Timeline |
|--------|----------|
| **Enter** | Same day or next day (faster than monthly) |
| **Hold** | 3-10 trading days |
| **Review** | Daily — check RSI, MACD, DMA 50 on chart |
| **Exit** | Faster exits than monthly (see Sell Rules below) |

---

# 🔑 KEY DIFFERENCE: Monthly vs Weekly

| | Monthly 📅 | Weekly 📆 |
|---|---|---|
| **Primary trigger** | `Return over 1month > 0` | `Return over 1week > 2` |
| **Momentum check** | 1day + 1week + 1month + 3months | 1day + 1week + 1month |
| **Hold time** | 2-8 weeks | 3-10 days |
| **Run frequency** | Once a week (Monday) | Daily or every 2 days |
| **Entry speed** | Split over 2-3 days | Same day or next day |
| **Stop-loss** | 8-10% or below DMA 50 | 5-7% or below DMA 50 |
| **Profit target** | 15-20% partial, trail rest | 8-12% partial, trail rest |
| **Best for** | Positional / swing trading | Short-term swing trading |

---

# 🧠 Filter Breakdown — Why Each Filter Exists

### Layer 1: Quality Gate (2 filters)

| # | Filter | Purpose |
|---|--------|---------|
| 1 | `Is not SME` | SME stocks are illiquid, widely manipulated, and have poor price discovery. Removing them eliminates an entire class of risky stocks |
| 2 | `Market Capitalization > 500` | Stocks above ₹500 Cr market cap have institutional interest, better governance, and are much harder to manipulate with fake volume |

### Layer 2: Multi-Timeframe Momentum (4 filters)

This is the **"must go up"** layer. The stock must be rising across **every** timeframe.

| # | Filter | Monthly Version | Weekly Version |
|---|--------|----------------|----------------|
| 3 | **Primary** | `Return over 1month > 0` | `Return over 1week > 2` |
| 4 | **Short-term** | `Return over 1week > 0` | `Return over 1day > 0` |
| 5 | **Immediate** | `Return over 1day > 0` | `Return over 1day > 0` |
| 6 | **Medium-term** | `Return over 3months > 0` | `Return over 1month > 0` |

> **Combined effect:** A stock passing all 4 is rising across every meaningful timeframe. Probability of immediate reversal is extremely low when all timeframes align.

### Layer 3: Strict Technical Analysis (13 filters)

#### Moving Averages (5 filters)

| # | Filter | Purpose |
|---|--------|---------|
| 7 | `Current price > DMA 50` | Price above 50-day moving average — **short-term uptrend** |
| 8 | `Current price > DMA 200` | Price above 200-day moving average — **long-term uptrend** |
| 9 | `DMA 50 > DMA 200` | **Golden Crossover** — the single most powerful bullish signal in technical analysis |
| 10 | `DMA 50 > DMA 50 previous day` | 50-DMA itself is **rising daily** — trend accelerating |
| 11 | `DMA 200 > DMA 200 previous day` | 200-DMA is **rising daily** — macro uptrend deeply established |

> **Combined:** Price above both DMAs + Golden Crossover + both rising = strongest possible DMA configuration.

#### RSI (2 filters)

| # | Filter | Purpose |
|---|--------|---------|
| 12 | `RSI > 52` | Confirms **bullish momentum** — above the neutral 50 line |
| 13 | `RSI < 68` | **Not overbought** — room to run. Above 70 = crash risk |

> **Sweet spot 52-68:** Strong momentum with room to grow. Not exhausted.

#### MACD (4 filters)

| # | Filter | Purpose |
|---|--------|---------|
| 14 | `MACD > MACD Signal` | **Bullish crossover active** — classic buy signal |
| 15 | `MACD > 0` | In **bull territory** — not a fake crossover in a downtrend |
| 16 | `MACD > MACD Previous Day` | MACD is **increasing** — momentum accelerating |
| 17 | `MACD Signal > MACD Signal Previous Day` | Signal line **also rising** — double momentum confirmation |

> **Combined:** All 4 MACD conditions green = momentum firing on all cylinders.

#### Volume & Price Position (2 filters)

| # | Filter | Purpose |
|---|--------|---------|
| 18 | `Volume > Volume 1month average` | Above-average volume — **real money** behind the move |
| 19 | `Current price > High price * 0.85` | Within 15% of 52-week high — **strong trend**, not a collapsed stock bouncing |

### Layer 4: Fundamental Floor (8 filters)

| # | Filter | Purpose |
|---|--------|---------|
| 20 | `Profit after tax > 0` | Company is **actually profitable** |
| 21 | `ROCE > 15` | Good returns on capital invested |
| 22 | `ROE > 12` | Decent equity returns for shareholders |
| 23 | `Debt to equity < 1` | **Not over-leveraged** — safe balance sheet |
| 24 | `Piotroski score > 5` | Passes 6+ of 9 **academic financial health checks** |
| 25 | `Sales growth 3Years > 8` | Revenue growing consistently |
| 26 | `Profit growth 3Years > 5` | Earnings growing consistently |
| 27 | `Cash from operations > 0` | Profits are **real cash**, not accounting tricks |

---

# 🟢 When to Buy

### Step 1 — Run the screener and get your list

### Step 2 — Verify each stock before buying

- [ ] Open chart on **TradingView / Chartink**
- [ ] Visually confirm price is **above DMA 50 & DMA 200**
- [ ] Confirm **MACD histogram is green** and growing
- [ ] No major **news event** coming (earnings, AGM, bonus)
- [ ] **NIFTY/SENSEX** is not in free-fall

### Step 3 — Entry Timing

| Entry Type | How | Risk |
|------------|-----|------|
| 🎯 **Pullback Buy** (safest) | Price dips 1-2% but stays above DMA 50. RSI ~52-55 | Low |
| 🎯 **Breakout Buy** | Closes at new weekly high with volume > 1.5x average | Medium |
| 🎯 **Ideal Entry** | Price near DMA 50 (support) + RSI 52-55 + MACD just crossed bullish | Lowest |

### ⚠️ Do NOT Buy

| Mistake | Why |
|---------|-----|
| Stock already up **5%+** today | You're **chasing** — wait for pullback |
| RSI **above 70** | **Overbought** — wait for dip |
| Volume **very low** | No conviction — could be fake move |
| Buying **all at once** | Split into **2-3 buys** over 3-5 days |

---

# 🔴 When to Sell

### 🛑 Stop-Loss (Non-Negotiable)

| Rule | Monthly 📅 | Weekly 📆 |
|------|-----------|-----------|
| Price closes **below DMA 50** | **EXIT** | **EXIT** |
| Down from buy price | **EXIT at 8-10%** | **EXIT at 5-7%** |

> Set **GTT order** the SAME DAY you buy. No exceptions.

### 📈 Profit Targets

| Milestone | Monthly 📅 | Weekly 📆 |
|-----------|-----------|-----------|
| **Partial profit** | Sell 30-40% at **15-20%** gain | Sell 40-50% at **8-12%** gain |
| **Trailing stop** | After 20%+ → trail **8-10%** below peak | After 12%+ → trail **5-7%** below peak |
| **Big winner** | At 50%+ → sell another 25-30% | At 25%+ → sell another 25-30% |

### 🔴 Technical Exit Signals

| Signal | Action |
|--------|--------|
| RSI goes **above 80** | **Book profits** — extremely overbought |
| MACD crosses **below Signal** | **EXIT** — momentum has died |
| DMA 50 crosses **below DMA 200** | **EXIT everything** — Death Cross |
| Price closes **below DMA 200** | **Full exit** — long-term trend broken |
| Volume spike + **big red candle** | **Exit** — smart money is leaving |

### 🔄 Re-Entry Rules

1. Wait **2-3 days** to confirm signal is real
2. Must pass **all 27 filters** again
3. Enter at **pullback near DMA 50**, not at the top
4. Use **tighter stop-loss** (5-7%) for re-entries

---

# 📋 Quick Checklist

### 🔍 Search
- [ ] Right time (Monday AM for monthly / daily AM for weekly)
- [ ] NIFTY not crashing
- [ ] Copy-paste correct query (monthly vs weekly)

### 🟢 Buy
- [ ] Stock passes all 27 filters
- [ ] Chart confirms visually
- [ ] Entry on pullback / red candle day
- [ ] RSI in 52-60 zone
- [ ] Position split into 2-3 buys
- [ ] GTT stop-loss set immediately
- [ ] No major news event coming

### 🔴 Sell
- [ ] Closes below DMA 50 → **EXIT**
- [ ] Down 8-10% monthly / 5-7% weekly → **EXIT**
- [ ] Hit profit target → **Book partial**
- [ ] RSI > 80 → **Book all profits**
- [ ] MACD < Signal → **EXIT**
- [ ] DMA 50 < DMA 200 → **EXIT everything**

---

# ⚠️ If Screener Returns 0 Results

Remove these filters **one at a time** (in this order):

| Priority | Remove This | Why It's Safe to Remove |
|----------|-------------|------------------------|
| 1st | `Return over 1day > 0` | One bad day can kill this |
| 2nd | `DMA 200 > DMA 200 previous day` | 200-DMA moves slowly, often flat |
| 3rd | `MACD Signal > MACD Signal Previous Day` | Signal line rises slowly |
| 4th | `DMA 50 > DMA 50 previous day` | DMAs lag in choppy markets |
| 5th | `Return over 3months > 0` | In corrections, 3-month returns go negative market-wide |
