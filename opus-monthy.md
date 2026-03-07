# 📈 Stock Screener — Maximum Conviction Monthly Strategy

> **27 filters | 17 strict technicals | 4 timeframe momentum | Must Go Up**

---

## 🔍 Screener Query

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

---

## 🧠 Filter Breakdown — Why Each Filter Exists

### Layer 1: Quality Gate (2 filters)

| # | Filter | Purpose |
|---|--------|---------|
| 1 | `Is not SME` | SME stocks are illiquid, widely manipulated, and have poor price discovery. Removing them eliminates an entire class of risky stocks |
| 2 | `Market Capitalization > 500` | Stocks above ₹500 Cr market cap have institutional interest, better governance, and are much harder to manipulate with fake volume |

### Layer 2: 4-Timeframe Momentum (4 filters)

This is the **"must go up"** layer. The stock must be rising across **every** timeframe — today, this week, this month, and the last 3 months. If even one timeframe is negative, the stock is rejected.

| # | Filter | Purpose |
|---|--------|---------|
| 3 | `Return over 1day > 0` | **Today is green.** Ensures you're entering on a day the stock is actively moving up, not on a down day |
| 4 | `Return over 1week > 0` | **This week is positive.** Short-term momentum is intact — not just a one-day bounce |
| 5 | `Return over 1month > 0` | **This month is positive.** The primary trend for the month is upward — this is the core "must go up for the month" requirement |
| 6 | `Return over 3months > 0` | **3-month trend is positive.** Confirms this isn't a dead cat bounce — the medium-term trend supports the move |

> **Combined effect:** A stock passing all 4 is rising across every meaningful timeframe. The probability of immediate reversal is extremely low when all timeframes align.

### Layer 3: Strict Technical Analysis (13 filters)

These are **non-negotiable** technical conditions. Every single one must be green.

#### Moving Averages (5 filters)

| # | Filter | Purpose |
|---|--------|---------|
| 7 | `Current price > DMA 50` | Price is above the 50-day moving average. The stock is in a **short-term uptrend**. DMA 50 acts as dynamic support |
| 8 | `Current price > DMA 200` | Price is above the 200-day moving average. The stock is in a **long-term uptrend**. Institutional investors watch this level closely |
| 9 | `DMA 50 > DMA 200` | **Golden Crossover** — the single most powerful bullish signal in technical analysis. When the 50-DMA crosses above the 200-DMA, it signals a major trend reversal. Historically, stocks stay bullish for months after this signal |
| 10 | `DMA 50 > DMA 50 previous day` | The 50-DMA itself is **rising daily**. Not just above the 200-DMA, but actively accelerating upward. This eliminates flat/stalling crossovers |
| 11 | `DMA 200 > DMA 200 previous day` | Even the 200-DMA is **rising daily**. When both moving averages are rising, the uptrend is powerful and deeply established. This is the strongest possible DMA configuration |

> **Combined DMA effect:** Price above both DMAs + Golden Crossover + both DMAs rising = the stock is in the most bullish technical position possible.

#### RSI — Relative Strength Index (2 filters)

| # | Filter | Purpose |
|---|--------|---------|
| 12 | `RSI > 52` | RSI above 52 confirms **bullish momentum**. Below 50 = bearish, 50-52 = neutral. We want confirmed bullish, not borderline |
| 13 | `RSI < 68` | RSI below 68 means the stock is **not yet overbought**. Above 70 = overbought (high crash risk). The 52-68 range is the **sweet spot** — strong momentum with room to run |

> **RSI sweet spot (52-68):** The stock has enough momentum to continue rising, but hasn't reached the danger zone where profit-booking causes sharp drops.

#### MACD — Moving Average Convergence Divergence (4 filters)

| # | Filter | Purpose |
|---|--------|---------|
| 14 | `MACD > MACD Signal` | **Bullish crossover is active.** MACD line above the signal line is a classic buy signal used by traders worldwide |
| 15 | `MACD > 0` | MACD is above the **zero line**. This confirms the stock is in bull territory — not just a temporary crossover in a downtrend |
| 16 | `MACD > MACD Previous Day` | MACD is **increasing daily**. The momentum is not just bullish — it's **growing**. This catches stocks where the move is accelerating |
| 17 | `MACD Signal > MACD Signal Previous Day` | Even the **signal line itself is rising**. This is the strongest MACD configuration — both lines moving up together means momentum is building, not fading |

> **Combined MACD effect:** Bullish crossover + above zero + MACD rising + Signal rising = momentum is firing on all cylinders with zero signs of weakening.

#### Volume & Price Position (2 filters)

| # | Filter | Purpose |
|---|--------|---------|
| 18 | `Volume > Volume 1month average` | Today's volume is **above the monthly average**. High volume confirms that real money is behind the move — not a low-volume fake breakout. Smart money leaves volume footprints |
| 19 | `Current price > High price * 0.85` | Price is **within 15% of the 52-week high**. Stocks near their highs tend to continue higher (momentum effect). Stocks far from their highs are in downtrends being bounced |

### Layer 4: Fundamental Floor (8 filters)

These are **intentionally balanced** — strict enough to filter out junk, but loose enough to let good momentum stocks through.

| # | Filter | Purpose |
|---|--------|---------|
| 20 | `Profit after tax > 0` | Company is **actually making money**. Filters out loss-making companies that might be going up on speculation alone |
| 21 | `ROCE > 15` | Return on Capital Employed above 15% means the business **generates good returns** on the capital invested. Below 15% = mediocre capital allocation |
| 22 | `ROE > 12` | Return on Equity above 12% means **shareholders** are getting decent returns. Confirms the company is efficient at converting equity into profits |
| 23 | `Debt to equity < 1` | Debt is less than equity — the company is **not over-leveraged**. High-debt companies collapse faster in downturns. Low debt = financial safety |
| 24 | `Piotroski score > 5` | Passes **6+ of 9 academic financial health checks** (profitability, leverage, operating efficiency). Developed by Professor Joseph Piotroski — research proves high Piotroski stocks outperform |
| 25 | `Sales growth 3Years > 8` | Revenue has grown **8%+ annually for 3 years**. Confirms the business is genuinely expanding, not stagnating |
| 26 | `Profit growth 3Years > 5` | Profits have grown **5%+ annually for 3 years**. Growth is translating to the bottom line |
| 27 | `Cash from operations > 0` | The company generates **real cash** from its operations. This catches companies that show accounting profits but burn cash — if cash flow is positive, the profits are real |

---

## 📅 When to Search

### ✅ Best Times to Run

| When | Why |
|------|-----|
| **Monday morning** (9:00–9:15 AM, before market opens) | Weekend gives clean end-of-week data with no intraday noise. Plan the entire week's trades in advance |
| **1st trading day of the month** | Monthly return data resets. Fresh momentum signals emerge. Best time to find new monthly uptrend entries |
| **After a 2-3 day market pullback that bounces** | Stocks that survive a dip and **still** pass all 27 filters are the strongest in the market. These are the ones that truly "must go up" |

### ❌ Do NOT Run

| When | Why |
|------|-----|
| During market hours | Intraday data keeps changing — DMA, RSI, MACD all fluctuate. Decisions based on incomplete data lead to bad entries |
| Budget day / RBI policy day | Extreme volatility creates false breakouts and fake crossovers that reverse by next week |
| NIFTY down 3%+ in a single day | Panic selling distorts every indicator. Even great stocks show false sell signals during panic |

---

## 🟢 When to Buy

### Step 1 — Run the screener and get your list

### Step 2 — Verify each stock before buying

- [ ] Open the stock's chart on **TradingView** or **Chartink**
- [ ] Visually confirm price is **above DMA 50 & DMA 200**
- [ ] Confirm **MACD histogram is green** and bars are growing
- [ ] Check no major **news event** is coming (earnings, AGM, bonus, split)
- [ ] Verify **NIFTY/SENSEX** is not in free-fall (overall market context)

### Step 3 — Entry Timing

| Entry Type | How to Execute | Risk Level |
|------------|----------------|------------|
| 🎯 **Pullback Buy** (safest) | Wait for a 1-2% intraday dip where price touches or nears DMA 50 but stays above it. RSI should be around 52-55. This gives you the best entry price in an uptrend | Low |
| 🎯 **Breakout Buy** | Buy when stock closes at a new **weekly high** with volume > 1.5x average. The breakout confirms new strength | Medium |
| 🎯 **Ideal Entry** | Price is near DMA 50 (acting as support) + RSI in the 52-55 zone + MACD just crossed above Signal. This is the textbook pullback entry | Lowest |

### ⚠️ Do NOT Buy

| Mistake | Why It's Dangerous |
|---------|-------------------|
| Stock already up **5%+** today | You're **chasing**. Enter on pullbacks, not after the move has already happened |
| RSI is **above 70** | **Overbought** territory. The stock needs to cool off. Buy the dip after RSI pulls back to 55-60 |
| Volume is **very low** | Low volume = no conviction. The move could be fake and easily reversed |
| Buying **all at once** | Split into **2-3 buys** over 3-5 days. If the stock dips after your first buy, you can average at a better price |

---

## 🔴 When to Sell

### 🛑 Stop-Loss Rules (Non-Negotiable)

**Set these the SAME DAY you buy. Use GTT (Good Till Triggered) orders on your broker.**

| Rule | Action | Why |
|------|--------|-----|
| Price **closes below DMA 50** | **EXIT immediately** | The short-term trend has broken. If DMA 50 fails as support, the next support is DMA 200 — and you don't want to ride that drop |
| Down **8-10%** from your buy price | **EXIT immediately** | Capital protection first. No indicator, no fundamental analysis overrides this rule. Losing 8% is recoverable. Losing 30% is not |

> **Golden rule:** Never risk more than 2-3% of your total portfolio on a single trade. If stop-loss is 8%, position size should be max 25-35% of portfolio.

### 📈 Profit Targets

| Milestone | Action | What Happens Next |
|-----------|--------|-------------------|
| Stock up **15-20%** | Sell **30-40%** of your position | Book partial profit. Move stop-loss to your **buy price** — now the remaining position is **risk-free** |
| Stock up **20%+** | Switch to **trailing stop** | Trail your stop **8-10% below the highest price** reached. If it keeps going up, you ride it. When it reverses 8-10% from peak, you exit with profit |
| Stock up **50%+** | Sell another **25-30%** | At this point, you've likely booked 60-70% of position. Let the final 30% ride with the trailing stop for potential multi-bagger returns |

### 🔴 Technical Exit Signals

Exit even if your stop-loss or target hasn't been hit:

| Signal | Action | Why |
|--------|--------|-----|
| RSI goes **above 80** | **Book profits** | Extremely overbought. A correction is very likely. Don't be greedy |
| MACD crosses **below Signal** | **EXIT** | Bullish momentum has died. The trend may be reversing |
| DMA 50 crosses **below DMA 200** | **EXIT everything** | **Death Cross** — the opposite of golden crossover. Major bearish signal. Get out completely |
| Price closes **below DMA 200** | **Full exit** | Long-term trend is broken. This stock has shifted from bull to bear territory |
| Volume spike + **big red candle** | **Exit** | This is **distribution** — smart money is selling large quantities. Don't be the last one holding |

### 🔄 Re-Entry Rules

If you sold a stock and it shows up in the screener again:

1. **Wait 2-3 days** to confirm the signal is genuine and not a false bounce
2. Only re-enter if it passes **all 27 filters** again
3. Enter at a **pullback near DMA 50**, never at the top of the new move
4. Use a **tighter stop-loss** (5-7%) since this is a re-entry into a previously failed position

---

## 📋 Quick Checklist

### 🔍 Search
- [ ] Monday morning (before 9:15 AM)
- [ ] 1st trading day of month
- [ ] After a bounce from a 2-3 day dip
- [ ] NIFTY is not crashing today

### 🟢 Buy
- [ ] Stock is in screener results (passes all 27 filters)
- [ ] Chart visually confirms uptrend (TradingView/Chartink)
- [ ] Entry is on a red candle / pullback day (not chasing)
- [ ] RSI is in 52-60 zone (not overbought)
- [ ] Position split into 2-3 buys over 3-5 days
- [ ] GTT stop-loss set immediately after buying
- [ ] No major news event coming for this stock

### 🔴 Sell
- [ ] Closes below DMA 50 → **EXIT**
- [ ] Down 8-10% from buy price → **EXIT** (stop-loss hit)
- [ ] Up 15-20% → **Sell 30-40%**, move stop to buy price
- [ ] Up 20%+ → **Trailing stop** 8-10% below peak
- [ ] RSI > 80 → **Book all profits**
- [ ] MACD crosses below Signal → **EXIT**
- [ ] DMA 50 crosses below DMA 200 → **EXIT everything**

---

## ⚠️ If Screener Returns 0 Results

Remove these filters **one at a time** (in this order) until results appear:

| Priority | Remove This | Why |
|----------|-------------|-----|
| 1st | `Return over 1day > 0` | One bad day can kill this — most volatile filter |
| 2nd | `DMA 200 > DMA 200 previous day` | 200-DMA moves very slowly, often flat in sideways markets |
| 3rd | `MACD Signal > MACD Signal Previous Day` | Signal line is smoothed — rises slowly |
| 4th | `DMA 50 > DMA 50 previous day` | DMAs lag in choppy markets |
| 5th | `Return over 3months > 0` | In a broad correction, 3-month returns go negative market-wide |
