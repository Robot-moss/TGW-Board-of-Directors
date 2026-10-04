# TRADING STATE — VERIFIED ANALYSIS
**Date:** 23 September 2026 | **Board seat:** Chief Risk Officer
**Source:** TradingView paper-trading export, 105 closed trades, 9 Jun – 21 Sep 2026, XAUUSD, Pepperstone feed, ~$1,078,000 notional account, 100x leverage available
**Status:** FIRST POSITIVE-EXPECTANCY SAMPLE ON RECORD

---

## 1. HEADLINE METRICS

| Metric | Live (Dec 25–May 26) | **Demo (Jun–Sep 26)** |
|---|---:|---:|
| Trades | 190 | 105 |
| Win rate | 7.4% | **26.67%** |
| Profit factor | <1 | **1.450** |
| Expectancy | negative | **+$798.62** |
| Avg win / avg loss | — | $9,642.79 / −$2,417.45 |
| Realised R:R | 4.33 | 3.99 |
| Net | −$16,085 | **+$83,854.69** |
| **Max drawdown** | — | **−$41,027 (−3.81%)** |

Break-even win rate at ~4R is ~20%. **26.67% clears it.**

---

## 2. THE CENTRAL FINDING — CONVICTION SIZING IS THE EDGE

Trades split into quartiles by position notional:

| Quartile | n | Median notional | Win rate | Net P&L | Exp/trade |
|---|---:|---:|---:|---:|---:|
| Q1 smallest | 26 | $860,367 | **19.2%** | **−$11,750** | −$452 |
| Q2 | 26 | $1,623,331 | 23.1% | **−$24,546** | −$944 |
| Q3 | 26 | $2,513,273 | 30.8% | +$31,802 | +$1,223 |
| Q4 largest | 27 | $5,023,798 | **33.3%** | **+$88,349** | +$3,272 |

**Win rate rises monotonically with position size: 19.2% → 23.1% → 30.8% → 33.3%.**
Top 10 largest positions: **5/10 winners (50%)** versus 26.67% overall.

**Flat-size counterfactual:** normalising every trade to the median notional produces **−$14,155, PF 0.909**. Actual result with dynamic sizing: **+$83,855, PF 1.450.**

> **Dynamic conviction sizing added $98,010 versus trading flat size. It is not noise — it is the edge.**

**Corollary: Q1 + Q2 combined lose $36,296 over 52 trades.** Trading only Q3/Q4-conviction setups would have produced **+$120,151 on 53 trades** instead of +$83,855 on 105 — a better result on half the volume and half the commission.

### Board correction on record
A prior session computed Pearson r(size, P&L) = +0.195 and concluded sizing was uncorrelated with outcome. **That statistic was the wrong tool** — a linear correlation on a heavy-tailed P&L distribution is dominated by outliers and cannot detect a monotonic relationship in hit rate. The rank/quartile test is the correct instrument and it reverses the finding.

---

## 3. THE LOSING-STREAK FIGURE WAS A MEASUREMENT ARTIFACT

The live dataset separately classified **32 breakeven trades**, which broke up losing runs. The demo export carries **no breakeven flag**, so a naive script counts every scratch as a loss.

| Breakeven band | Scratch trades identified | Longest TRUE losing streak |
|---|---:|---:|
| ±$0 (naive) | 0 | **22** |
| ±$200 | 7 | 18 |
| **±$500 (~0.05% of account)** | **16** | **9** |
| ±$1,000 | 26 | 8 |

**True comparable streak: ~9, versus 13 in the live record.** The streak got *shorter* as execution improved, exactly as theory predicts.

**Expected longest losing run:**
- At 7.4% win rate over 190 trades: **~34**
- At 26.67% win rate over 105 trades: **~10.7**

Observed 9 is **normal and slightly better than expected.**

### Depth, not length, was always the risk
The 22-trade "run" (trades #58–#79, 7–18 Aug) cost **−$36,136 — just 3.35% of account**, averaging −$1,643 per trade. Max peak-to-trough drawdown across all 105 trades: **−$41,027 (−3.81%)**, against a gross return of +7.8%. That is a respectable return-to-drawdown profile.

---

## 4. TRAJECTORY

| Segment | Period | Win rate | Net |
|---|---|---:|---:|
| First 35 | 9–30 Jun | 25.71% | +$53,514 |
| Middle 35 | 30 Jun – 17 Aug | 22.86% | +$9,186 |
| Last 35 | 17 Aug – 21 Sep | **31.43%** | +$21,154 |

Win rate is highest in the most recent third. Consistent with continued improvement; sample far too small to confirm a trend.

---

## 5. WHAT REMAINS UNPROVEN

1. **Sample size.** 105 trades. Confidence interval on a 26.67% win rate is roughly 18–36%. Target: **300+ trades**.
2. **Ranks are unlogged.** Position size is a *proxy* for conviction, not a record of it. The Readiness Gate requires ranks that predict results — size predicts results, but the A+/A/B/C label was never recorded. **Log rank at entry from the next sample onward.**
3. **Demo conditions.** No real-money emotional load, idealised fills, no slippage realism.
4. **Realised-R vs planned-R gap.** The user's own diagnosis: the leak has moved from entry timing to trade management. Documented instance — trade #104 (21 Sep): short 4347.95, target 4334.29 (13.66 pts), stopped at 4345.57 for 2.38 pts. **+$664.69 against roughly $3,800 planned.**
5. **The stall-reduction behaviour.** The user reduces risk when price stalls before breakeven conditions are met, and suspects it works against him but has no statistics. **Untested and testable.**

---

## 6. RULE ADHERENCE (context: this sample was execution-focused, not rules-focused)

8 of 29 trading days breached the self-imposed trade cap. Five were all-loss days exceeding the stop-at-3 rule:

| Date | Trades | Net |
|---|---:|---:|
| 19 Jun | 4, all losses | −$15,143 |
| 10 Aug | 5, all losses | −$8,168 |
| 7 Aug | 5, all losses | −$7,122 |
| 4 Sep | 6, all losses | −$5,485 |
| 17 Aug | 4, all losses | −$4,501 |
| **Total** | | **−$40,419** |

Holding the rule would have produced roughly **$124,274** instead of $83,855 — about **48% better**, with no change to system or edge.

---

## 7. HRT ACCOUNT — AGREED STRUCTURE

- Separate high-leverage account, isolated from prop and personal accounts
- Funded **once per year**, **$1,000** initially; never refunded within the year
- Aggressive dynamic sizing on **A+ setups only**
- **Risk capped at 20% per trade**, not 30% (see below)
- Maximum **3 HRT trades per month** — forces genuine A+ selection
- **60–70% of profits withdrawn quarterly** to personal account
- Deployment gated on: RSFE statistical validation + logged ranks + prop income. **Target: Q1 2027.**

**Survival math at the corrected 9-loss streak:**

| Risk/trade | 9 consecutive losses |
|---|---:|
| 10% | −61.3% |
| **20%** | **−86.6%** |
| 30% | −96.0% |

The 30% tier converts a survivable drawdown into a terminal one without a corresponding increase in edge. **Cap at 20%.**

**Scaling cap:** the user's stated ceiling is $100,000. The board's position is that HRT should be capped at **2–3% of liquid net worth**, not an absolute figure. At current net worth (~₦350m ≈ $262,000) that is roughly **$5,250**. A $100,000 HRT account requires a liquid net worth of **$3.3m–$5m**. The phrase "willing to lose it all" is a true statement about $1,000 and an untested one about $100,000.

**Refund discipline requires architecture, not willpower.** The user has stated he will likely buckle. Recommended: fund HRT on a single fixed calendar date from the money market fund, with a standing rule that no MMF withdrawal for HRT occurs at any other time, and disclose the rule to a third party (Sarah).

---

## 8. OPEN ITEM FOR THE RED TEAM SESSION

**The order-flow source has changed and the rank definition has not.** The RSFE playbook states that spot CFD volume is "fictional" and that GC futures (Bookmap) is "the trustworthy, centralized tape." A+ rank requires "textbook GC order-flow confirmation." The user now reports using the TradingView footprint chart, which is spot-based.

Given that Section 2 establishes conviction sizing as the edge, and A+ rank is what drives conviction, **a silent change in the order-flow input is a change to the thing that generates the returns.** Either the rank definition is updated to reflect spot footprint, or the A+ tier is capped in its absence. To be resolved before HRT funding.
