# 📈 Stock Screener v3.0 — Definitive Trading Guide

> **Built using verified Screener.in ratio names only. All filters confirmed available.**

---

## 🔧 v2.0 Errors Fixed in v3.0

| v2.0 (Wrong Name) | v3.0 (Correct Name) | Status |
|---|---|---|
| `Current ratio > 1` | `Quick ratio > 0.8` | ✅ Fixed — Current ratio not available |
| `PE < 80` | `Price to Earning < 80` | ✅ Fixed — exact name required |
| `Quarter sales growth > 10` | `YOY Quarterly sales growth > 10` | ✅ Fixed |
| `Quarter profit growth > 10` | `YOY Quarterly profit growth > 10` | ✅ Fixed |
| ATR volatility filter | ❌ Removed — not available in Screener.in | Removed |

---

# 📅 MONTHLY SCREENER — Core Query (33 filters)

> **Timeframe:** 2–8 weeks. Run every Monday morning.

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
Cash from operations last year > 0 AND
Free cash flow last year > 0 AND
Pledged percentage < 10 AND
Promoter holding > 30 AND
Quick ratio > 0.8 AND
Price to Earning < 80 AND
YOY Quarterly sales growth > 10 AND
YOY Quarterly profit growth > 10
```

---

# 📅 MONTHLY SCREENER — Power Query (39 filters)

> Use this when market is in strong bull phase. Stricter — returns fewer but higher quality stocks.

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
Volume 1month average * Current price > 10000000 AND
Current price > High price * 0.85 AND
Profit after tax > 0 AND
Return on capital employed > 15 AND
Return on equity > 12 AND
Return on invested capital > 12 AND
Debt to equity < 1 AND
Piotroski score > 5 AND
G Factor > 4 AND
Sales growth 3Years > 8 AND
Profit growth 3Years > 5 AND
EPS growth 3Years > 5 AND
OPM last year > 10 AND
Cash from operations last year > 0 AND
Free cash flow last year > 0 AND
Pledged percentage < 10 AND
Promoter holding > 30 AND
Change in promoter holding > -2 AND
Quick ratio > 0.8 AND
Price to Earning < 80 AND
YOY Quarterly sales growth > 10 AND
YOY Quarterly profit growth > 10
```

---

# 📆 WEEKLY SCREENER — Core Query (33 filters)

> **Timeframe:** 3–10 days. Run daily or every 2 days.

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
Cash from operations last year > 0 AND
Free cash flow last year > 0 AND
Pledged percentage < 10 AND
Promoter holding > 30 AND
Quick ratio > 0.8 AND
Price to Earning < 80 AND
YOY Quarterly sales growth > 10 AND
YOY Quarterly profit growth > 10
```

---

# ⚡ DAILY SCREENER (18 filters)

> **Timeframe:** 1–3 days. Run 9:00–9:30 AM only.

```
Is not SME AND
Market Capitalization > 500 AND
Return over 1day > 1.5 AND
Return over 1week > 0 AND
Current price > DMA 50 AND
Current price > DMA 200 AND
DMA 50 > DMA 200 AND
RSI > 55 AND
RSI < 72 AND
MACD > MACD Signal AND
MACD > 0 AND
Volume > Volume 1month average * 1.5 AND
Current price > High price * 0.90 AND
Profit after tax > 0 AND
Debt to equity < 1 AND
Pledged percentage < 10 AND
Promoter holding > 30 AND
Price to Earning < 80
```

---

# 🧪 NEW FILTERS EXPLAINED (Added in v3.0)

### Free Cash Flow (replaces/adds to Cash from Operations)

| Filter | Ratio Name | Purpose |
|--------|-----------|---------|
| `Free cash flow last year > 0` | Cash Flow → Recent | Cash from operations minus capex. Stronger proof profits are real |

> **Why better:** A company can have positive operating cash flow but still be burning cash on capex. FCF > 0 means it's truly self-funding.

### Liquidity Gate (New)

| Filter | Ratio Name | Purpose |
|--------|-----------|---------|
| `Volume 1month average * Current price > 10000000` | Price × Price | Ensures ₹1 crore/day minimum traded value — you can exit without slippage |

> **Why critical:** A ₹800 Cr market cap stock trading ₹5 lakh/day will trap you on exit. This filter catches it.

### EPS Growth (New)

| Filter | Ratio Name | Purpose |
|--------|-----------|---------|
| `EPS growth 3Years > 5` | Annual Historical | Earnings per share growing = shareholder value being created |

### Operating Margin (New)

| Filter | Ratio Name | Purpose |
|--------|-----------|---------|
| `OPM last year > 10` | Annual P&L Recent | Operating margin > 10% = business has pricing power |

### Promoter Behaviour (New)

| Filter | Ratio Name | Purpose |
|--------|-----------|---------|
| `Change in promoter holding > -2` | Annual P&L Recent | Promoter hasn't sold more than 2% recently — no insider exit |

### Quality Scores (Power Query only)

| Filter | Ratio Name | Purpose |
|--------|-----------|---------|
| `G Factor > 4` | Ratios Recent | Greenblatt-style quality score — earns above cost of capital |
| `Return on invested capital > 12` | Ratios Recent | Better than ROCE — includes all invested capital |

---

# 🔑 Complete Comparison Table

| | Monthly Core | Monthly Power | Weekly | Daily |
|---|---|---|---|---|
| **Filters** | 34 | 40 | 34 | 18 |
| **Hold time** | 2–8 weeks | 2–8 weeks | 3–10 days | 1–3 days |
| **RSI range** | 52–68 | 52–68 | 52–68 | 55–72 |
| **Volume** | > 1M avg | > 1M avg + ₹1Cr/day | > 1M avg | > 1.5x avg |
| **Fundamentals** | Full | Full + ROIC, G Factor, OPM | Full | Light |
| **Promoter check** | Holding > 30 | Holding > 30 + Change > -2 | Holding > 30 | Holding > 30 |
| **Stop-loss** | 8–10% / below DMA 50 | 8–10% / below DMA 50 | 5–7% / below DMA 50 | 3–4% hard |
| **Target** | 15–20% partial | 15–20% partial | 8–12% partial | 4–6% full exit |
| **Dead money** | Exit if < 5% in 3 weeks | Exit if < 5% in 3 weeks | Exit if < 3% in 5 days | Exit if < 2% in 2 days |

---

# 🧠 Complete Filter Reference (All 40 Filters)

### Layer 1 — Quality Gate (2)
| # | Filter | Ratio Section | Purpose |
|---|--------|--------------|---------|
| 1 | `Is not SME` | Price | Removes illiquid, manipulated SME stocks |
| 2 | `Market Capitalization > 500` | Ratios Recent | Institutional interest threshold — ₹500 Cr+ |

### Layer 2 — Multi-Timeframe Momentum (4)
| # | Filter | Ratio Section | Purpose |
|---|--------|--------------|---------|
| 3 | `Return over 1month > 0` | Price Recent | Medium-term momentum positive |
| 4 | `Return over 1week > 0` | Price Recent | Short-term momentum positive |
| 5 | `Return over 1day > 0` | Price Recent | Immediate momentum positive |
| 6 | `Return over 3months > 0` | Price Recent | Trend established over quarter |

### Layer 3 — Technicals (13)
| # | Filter | Ratio Section | Purpose |
|---|--------|--------------|---------|
| 7 | `Current price > DMA 50` | Price Recent | Short-term uptrend |
| 8 | `Current price > DMA 200` | Price Recent | Long-term uptrend |
| 9 | `DMA 50 > DMA 200` | Price Recent | Golden Cross — strongest DMA signal |
| 10 | `DMA 50 > DMA 50 previous day` | Price Recent | 50-DMA accelerating |
| 11 | `DMA 200 > DMA 200 previous day` | Price Recent | Macro trend deepening |
| 12 | `RSI > 52` | Price Recent | Bullish momentum confirmed |
| 13 | `RSI < 68` | Price Recent | Not overbought — room to run |
| 14 | `MACD > MACD Signal` | Price Recent | Bullish crossover active |
| 15 | `MACD > 0` | Price Recent | Bull territory — not a fake crossover |
| 16 | `MACD > MACD Previous Day` | Price Recent | MACD accelerating |
| 17 | `MACD Signal > MACD Signal Previous Day` | Price Recent | Signal also accelerating |
| 18 | `Volume > Volume 1month average` | Price Recent | Real money behind the move |
| 19 | `Current price > High price * 0.85` | Price Recent | Within 15% of 52-week high |

### Layer 4 — Fundamental Floor (8)
| # | Filter | Ratio Section | Purpose |
|---|--------|--------------|---------|
| 20 | `Profit after tax > 0` | Annual P&L Recent | Actually profitable |
| 21 | `Return on capital employed > 15` | Annual P&L Recent | Good capital efficiency |
| 22 | `Return on equity > 12` | Ratios Recent | Good shareholder returns |
| 23 | `Debt to equity < 1` | Ratios Recent | Not overleveraged |
| 24 | `Piotroski score > 5` | Ratios Recent | 6/9 financial health checks passed |
| 25 | `Sales growth 3Years > 8` | Annual Historical | Revenue growing consistently |
| 26 | `Profit growth 3Years > 5` | Annual Historical | Earnings growing consistently |
| 27 | `Cash from operations last year > 0` | Cash Flow Recent | Profits are real cash |

### Layer 5 — Safety Gate (6 — added v2.0)
| # | Filter | Ratio Section | Purpose |
|---|--------|--------------|---------|
| 28 | `Pledged percentage < 10` | Ratios Recent | No margin call blowup risk |
| 29 | `Promoter holding > 30` | Ratios Recent | Promoter has skin in game |
| 30 | `Quick ratio > 0.8` | Ratios Recent | Can pay short-term debts |
| 31 | `Price to Earning < 80` | Ratios Recent | Valuation sanity |
| 32 | `YOY Quarterly sales growth > 10` | Quarter P&L Recent | Recent revenue momentum |
| 33 | `YOY Quarterly profit growth > 10` | Quarter P&L Recent | Recent earnings momentum |

### Layer 6 — Quality Boost (7 — added v3.0)
| # | Filter | Ratio Section | Purpose |
|---|--------|--------------|---------|
| 34 | `Free cash flow last year > 0` | Cash Flow Recent | Profits are real after capex |
| 35 | `Volume 1month average * Current price > 10000000` | Computed | ₹1 Cr/day minimum liquidity |
| 36 | `EPS growth 3Years > 5` | Annual Historical | Per-share earnings growing |
| 37 | `OPM last year > 10` | Annual P&L Recent | Business has pricing power |
| 38 | `Change in promoter holding > -2` | Annual P&L Recent | Insiders not selling |
| 39 | `G Factor > 4` | Ratios Recent | Quality-adjusted earnings power |
| 40 | `Return on invested capital > 12` | Ratios Recent | Superior capital allocation |

---

# 🟢 When to Buy

### Step 1 — Run the screener
Use **Core Query** for normal markets. Use **Power Query** in strong bull phase.

### Step 2 — Manual Verification Checklist
- [ ] Chart on TradingView — price above both DMAs visually
- [ ] MACD histogram green and growing
- [ ] Pledged % confirmed on Screener.in company page
- [ ] No earnings, AGM, bonus announcement in next 2 weeks
- [ ] NIFTY 50 is **above its own DMA 200** (manual check — see Market Regime rules below)

### Step 3 — Entry Type
| Type | Condition | Risk |
|------|-----------|------|
| 🎯 Pullback Buy (safest) | Dips 1–2% but holds DMA 50. RSI ~52–55 | Low |
| 🎯 Breakout Buy | Closes at new weekly high, volume > 1.5x avg | Medium |
| 🎯 Ideal Entry | Price near DMA 50 + RSI 52–55 + MACD just crossed bullish | Lowest |

### Step 4 — Risk:Reward Check *(New)* 🆕
> **Only enter if:** Potential target ÷ stop-loss distance ≥ 2

| Screener | Target | Stop | Minimum R:R |
|----------|--------|------|-------------|
| Monthly | 15–20% | 8–10% | 2:1 or better |
| Weekly | 8–12% | 5–7% | 2:1 or better |
| Daily | 4–6% | 3–4% | 1.5:1 or better |

**Example:** Stock at ₹100. DMA 50 at ₹92 → stop = 8%. Target = ₹120 → upside = 20%. R:R = 2.5:1 ✅

### Portfolio Construction Rules
| Rule | Value | Why |
|------|-------|-----|
| Max positions | 6–10 | Manageable + diversified |
| Capital per trade | 5–10% | Single stock can't destroy portfolio |
| Sector cap | Max 2 stocks/sector | Avoids correlated crash |
| Cash buffer | Keep 20% always | For new entries + averaging |

### ⚠️ Do NOT Buy If
- Stock up 5%+ today → chasing, wait for pullback
- RSI above 70 → overbought
- Volume very low → no conviction
- Pledged % above 10 → blowup risk
- Change in promoter holding very negative → insiders exiting
- NIFTY is below its DMA 200 → reduce all position sizes by 50%

---

# 🔴 When to Sell

### 🛑 Stop-Loss (Non-Negotiable)
| Rule | Monthly | Weekly | Daily |
|------|---------|--------|-------|
| Below DMA 50 close | EXIT | EXIT | EXIT |
| Fixed % from buy | 8–10% | 5–7% | 3–4% |
> Set GTT order the SAME DAY you buy.

### ⏳ Dead Money Exit
| Screener | Rule |
|----------|------|
| Monthly | No +5% move after 3 weeks → exit, redeploy |
| Weekly | No +3% move after 5 trading days → exit |
| Daily | No +2% move by end of Day 2 → exit |

### 📈 Profit Targets
| Milestone | Monthly | Weekly | Daily |
|-----------|---------|--------|-------|
| Partial exit | 30–40% at 15–20% gain | 40–50% at 8–12% gain | Full exit at 4–6% |
| Trailing stop | After 20%+ → trail 8–10% below peak | After 12%+ → trail 5–7% | N/A |
| Big winner | At 50%+ → sell another 25–30% | At 25%+ → sell 25–30% | N/A |

### 🔴 Technical Exit Signals
| Signal | Action |
|--------|--------|
| RSI > 80 | Book profits — extremely overbought |
| MACD crosses below Signal | EXIT — momentum dead |
| DMA 50 crosses below DMA 200 | EXIT everything — Death Cross |
| Price closes below DMA 200 | Full exit — long-term trend broken |
| Volume spike + big red candle | Exit — smart money leaving |
| Pledged % suddenly spikes | Exit immediately |
| Change in promoter holding sharply negative | Exit — insider selling |

### 🔄 Re-Entry Rules
1. Wait 2–3 days to confirm signal is real
2. Must pass ALL filters for that screener again
3. Enter at pullback near DMA 50, not at top
4. Use tighter stop-loss (5–7%) for re-entries

---

# 🌐 Market Regime Rules *(New — Manual Check)* 🆕

> Screener.in doesn't provide NIFTY data in filters. Do this **manually before running any screener.**

| NIFTY Condition | What to Do |
|-----------------|-----------|
| NIFTY above DMA 200 + DMA 50 > DMA 200 | ✅ Full position sizes. Run all screeners |
| NIFTY above DMA 200 but DMA 50 < DMA 200 | ⚠️ Reduce position size by 30%. Monthly screener only |
| NIFTY below DMA 200 | 🔴 Reduce position size by 50%. Monthly only. No new weekly/daily |
| NIFTY falling 3%+ per day | 🔴🔴 Stop all entries. Move to 80%+ cash |

**How to check:** Open NIFTY 50 chart on TradingView → enable DMA 50 + DMA 200 overlays → visual check before opening Screener.in.

---

# 💰 India Tax Guide for Traders *(New)* 🆕

| Hold Period | Tax Type | Rate | Applies To |
|-------------|----------|------|-----------|
| < 1 year | Short Term Capital Gains (STCG) | **20%** | All weekly + daily trades, most monthly |
| > 1 year | Long Term Capital Gains (LTCG) | **12.5%** above ₹1.25L/year | Only if monthly trade becomes a long hold |

**Practical impact on targets:**

| Net Target | Pre-tax Needed (STCG @ 20%) | Pre-tax Needed (LTCG @ 12.5%) |
|------------|-----------------------------|---------------------------------|
| 10% net | 12.5% gross | 11.4% gross |
| 15% net | 18.75% gross | 17.1% gross |
| 20% net | 25% gross | 22.8% gross |

> **Rule of thumb:** Add ~25% to your target to account for tax. If you want 10% net, aim for 12.5% gross on monthly screener trades.

---

# ⚠️ If Screener Returns 0 Results

Remove in this exact order — **never remove safety filters** (marked 🔒):

| Priority | Remove This | Why Safe |
|----------|-------------|---------|
| 1st | `Return over 1day > 0` | One bad day kills this |
| 2nd | `DMA 200 > DMA 200 previous day` | 200-DMA moves very slowly |
| 3rd | `MACD Signal > MACD Signal Previous Day` | Signal line lags |
| 4th | `DMA 50 > DMA 50 previous day` | DMAs lag in choppy markets |
| 5th | `Return over 3months > 0` | Market-wide corrections kill this |
| 6th | `YOY Quarterly profit growth > 10` | Relax to `> 5` first, then remove |
| 7th | `YOY Quarterly sales growth > 10` | Same as above |
| 8th | `EPS growth 3Years > 5` | Power filter — safe to remove |
| 9th | `OPM last year > 10` | Power filter — safe to remove |
| Never 🔒 | `Pledged percentage < 10` | Blowup risk |
| Never 🔒 | `Profit after tax > 0` | Must be profitable |
| Never 🔒 | `Debt to equity < 1` | Balance sheet safety |
| Never 🔒 | `Promoter holding > 30` | Alignment filter |
| Never 🔒 | `Free cash flow last year > 0` | Real cash filter |

---

# 📋 Master Checklist

### 🌐 Before Running Screener
- [ ] Check NIFTY vs DMA 200 manually on TradingView
- [ ] Confirm which regime you're in (see Market Regime table)
- [ ] Right time of day (Monday 9 AM monthly / daily 9–9:30 AM weekly+daily)

### 🟢 Buy
- [ ] Passes all filters for selected screener
- [ ] Chart confirms visually (DMAs, MACD, RSI)
- [ ] R:R check passes (minimum 2:1 for monthly/weekly)
- [ ] Pledged % confirmed low on company page
- [ ] Entry on pullback / RSI in 52–60 range
- [ ] Position sized correctly (5–10% of portfolio)
- [ ] Sector cap not breached (max 2 stocks/sector)
- [ ] GTT stop-loss set immediately after buying
- [ ] No earnings/AGM/news event within 2 weeks

### 🔴 Sell
- [ ] Closes below DMA 50 → EXIT
- [ ] Fixed % stop hit → EXIT
- [ ] Dead money threshold reached → EXIT
- [ ] Hit profit target → Book partial (or full for daily)
- [ ] RSI > 80 → Book all profits
- [ ] MACD < Signal → EXIT
- [ ] Death Cross (DMA 50 < DMA 200) → EXIT everything
- [ ] Pledged % spiked or promoter selling aggressively → EXIT

---

# 📊 Version History

| Version | Total Filters | Key Additions |
|---------|--------------|---------------|
| v1.0 | 27 | Original monthly + weekly screener |
| v2.0 | 33 | Safety filters, daily screener, portfolio rules, dead money exits |
| v3.0 | 40 | Correct ratio names, FCF, liquidity gate, EPS growth, OPM, promoter behaviour, G Factor, ROIC, market regime rules, R:R framework, tax guide |
