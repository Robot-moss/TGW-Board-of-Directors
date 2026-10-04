# AVA cBOT — CRO VERDICT
**Date:** 4 October 2026 | **Board seat:** Chief Risk Officer
**Submission:** *Asian Acceptance (AVA): approval to build and forward-test the gold cBot*, 3 Oct 2026, 20 pages
**Request:** build the cBot · 6-month Pepperstone Razor demo at 67% size · the §8 promotion and stop criteria
**Capital at risk in this request:** **NIL**

---

## 1. VERDICT

**APPROVED.** Build it, run the demo, adopt the §8 criteria — with five conditions in §5.

The request asks for no capital. The only resource at stake is his time, and the plan's own stop rules cap even that. **There is no rational basis to refuse a no-capital forward test of a pre-registered, holdout-validated rule.** The Red Team's job here is not to block it but to make sure the demo can actually fail.

### On the quality of the submission

This is the most rigorous piece of research the board has received, and that includes the discretionary work. Specifically: **pre-registration** of every test before its data was examined; a **one-time holdout** read once; **5,000-path Monte Carlo in 20-day blocks** so losing streaks stay clustered; a **neighbouring-settings plateau** (all 54 profitable in both halves); **pessimistic costs at ~2× measured, then doubled again** as a stress case; **multiple-testing correction**; a **random-entry control**; and an **audited null market**. Most funds do not work to this standard. It is recorded, and it is why the verdict is short.

---

## 2. WHAT THE EVIDENCE SUPPORTS

| Measure | Path 2, taken trades, pessimistic costs |
|---|---|
| Result per trade | **+0.32R** (+0.17 to +0.47), p < 0.001 |
| Trades | 687 over 12.6 years |
| Win rate | 33% |
| Average win / loss | +2.89R / −0.95R |
| Profit factor | 1.50 |
| First half / second half | +0.23R (p 0.03) / +0.38R (p 0.001) |
| Holdout, 125 unseen trades | **+0.30R**, PF 1.48, 8 of 13 months positive |
| Costs doubled again | **+0.18R**, p 0.01 — still positive |

**The edge survives every stress the author applied to it.** The separation from the random-entry baseline (+0.08R on gold before costs, against the rule's +0.31R) is the single most persuasive number in the report: the acceptance signal, not gold's general intraday tendency, carries the result.

---

## 3. THE FOUR FINDINGS

### 3.1 Path 2 has no holdout protection. The researched setting does.

§12 states it plainly: *"Path 2 was chosen from neighbouring settings **after** the holdout was read."* So the +0.30R holdout validates the **researched** setting; Path 2's +0.32R does not inherit that protection, and its advantage is unproven at p 0.16.

The author already handles this — Path 1 runs in shadow — but the plan does not say what *forces* a revert. **Condition 2 makes it explicit.**

### 3.2 The market-selection multiple-comparison problem

Eleven other markets were tested; gold passed at p 0.007. A Bonferroni correction across twelve markets puts that at **p ≈ 0.084 — outside 5%.**

**The holdout is the defence and it is a good one** — a frozen rule read once on unseen data is immune to selection across markets. But it defends the *researched* setting only, which reinforces 3.1. Noted, not disqualifying.

Related: the EURGBP control was designed to show no edge and returned **+0.15R before costs** (+0.04R after, p 0.30). It washes out after costs, and the author audited it and disclosed it. The honest read is that there is a small baseline drift in the engine or in intraday FX generally; the rule's excess over the random-entry baseline is ~+0.23R rather than the headline +0.31R. **Still a real edge. Just smaller than the top-line number.**

### 3.3 The flat spells collide with the relocation window

| Plan | Longest under water, history | Monte Carlo bad case (1 in 10) |
|---|---|---|
| 67% demo | 18 months | **46 months** |
| 100% full | 18 months | **47 months** |
| Floor plan | 46 months | **68 months** |

**A 46-month flat spell spans the entire Phase A relocation window.** And flat is harder to hold than down — a drawdown feels like an event, four years of nothing feels like being wrong.

This is not an argument against the system. It is an argument for **never letting this bot be the thing that has to work by a date.** The §8 band already judges results against a 5th-percentile band rather than against zero, which is the correct instrument. Keep it.

### 3.4 The question the report does not ask: what is this bot *for*?

The report evaluates AVA as a standalone system. The board has to evaluate it as an income instrument, and the arithmetic is decisive.

**Burn is ₦1,250,000/mo = $937/mo = $11,244/yr at ₦1,334.**

| Deployment | Annual return | Net to him | vs burn |
|---|---|---|---|
| His own liquid USD (~$16,000, ~$10k committed) at 19.4% | $3,104 | $3,104 | **28% of burn** |
| Capital required to cover burn at 19.4% | — | — | **~$58,000** |
| Capital required at 12.9% (demo size) | — | — | **~$87,000** |
| Passed $100k prop, floor plan 8.7%, 80% split | $8,700 | $6,960 | **62% of burn** |
| Passed $100k prop, demo size 12.9%, 80% split | $12,900 | $10,320 | **92% of burn — short** |
| Passed $100k prop, **full size 19.4%, 80% split** | $19,400 | **$15,520** | **138% of burn — COVERS** |

**Three conclusions:**

1. **AVA cannot cover burn on his own capital.** It needs ~$58,000; he has ~$16,000 with ~$10,000 committed. As a personal-capital instrument it is a compounding engine, not an income source.
2. **AVA covers burn on one passed $100k prop account at full size, with 38% headroom.** That is the business case, and it is a sound one.
3. **But full size is ~13 months away at best** — Stage 1 demo (6 months), then Stage 2 live at demo size, then 60 taken trades before promotion. At ~55 taken trades a year, **60 trades is itself about 13 months.** The honest earliest date for burn coverage via AVA is **late 2027 to early 2028**, and that assumes a prop account is passed in the meantime.

**For the 2027 wedding gate this matters:** AVA is not a 2027 income stream. It may well be a 2028 one. The gate's dependence on the IOA's first mandate is unchanged by this submission.

---

## 4. THE $94k FTMO ACCOUNT — THIS SUBMISSION SETTLES THE OPEN RED TEAM ITEM

The standing question: is the $94k account a live opportunity or an impaired one? AVA's own drawdown statistics answer it.

**The account's parameters:** target $110,000 = **+17.0%** from $94,000. Floor $90,000 = **−4.26%** of rope.

| AVA sizing plan | CAGR | Max DD, history | MC median | MC 1-in-20 | Fits in 4.26%? |
|---|---|---|---|---|---|
| 67% demo size | 12.9% | 10.0% | 12.1% | 18.1% | **NO** |
| Full size | 19.4% | 14.7% | 17.7% | 26.0% | **NO** |
| Floor plan, 10% floor | 8.7% | 8.0% | 7.9% | 9.1% | **NO** |
| Floor plan, 5% floor | 4.3% | 4.0% | 3.9% | **4.5%** | **MARGINAL — the 1-in-20 case breaches** |

**The only sizing that even approaches fitting is the 5% floor plan, whose 1-in-20 drawdown still breaches the account — and at 4.3% a year it would take roughly 3.7 years to make +17%.**

> **FINDING: the $94k FTMO account cannot be recovered by this system under any sizing plan the report offers. Treat it as impaired. Reset, rebuy, or leave it — do not trade it.**

**By contrast, the untouched $100k FTMO account:** 10% of rope against a 10% target. The **floor plan (8.0% max DD, 9.1% at 1-in-20, 8.7% CAGR)** fits inside the rope and reaches +10% in roughly **14 months**. The 67% demo plan at 10.0% historical max DD sits exactly on the limit and its 1-in-20 case of 18.1% destroys the account.

> **The report says it itself — *"the floor plan suits prop-firm accounts with hard loss limits"* — and the arithmetic confirms it. If AVA is ever pointed at an FTMO challenge, it runs the floor plan, not the base plan.**

---

## 5. CONDITIONS OF APPROVAL

| # | Condition |
|---|---|
| **1** | **The parity check is a gate, not a report.** The cBot's own cTrader backtest must reproduce the research engine's trades on Pepperstone data *before* the demo starts. Already planned — this makes it blocking. |
| **2** | **Explicit revert rule for Path 2.** Path 2 lost its holdout protection when it was selected post-hoc. If at 60 taken trades Path 2 has not outperformed the researched setting running in shadow, **revert to the researched setting.** Without a stated revert, the shadow column is decoration. |
| **3** | **Confirm a minimum stop-distance floor.** The stop sits at the previous day's POC — a variable distance — and position size is risk ÷ stop distance. A day where the acceptance level sits close to the POC produces a maximum-size position with maximum gap exposure. The 2% risk cap and max lot size blunt this but do not target it. A floor of ~0.5 × ATR15 is the cleaner instrument. **Is there one? If not, add it.** |
| **4** | **Log MFE (maximum favourable excursion) on every trade from day one.** It costs nothing now and is expensive to retrofit. It is also the measurement that settles the discretionary realised-R-vs-planned-R question, so one field serves both books. |
| **5** | **Decide the $94k account before any live step.** §4 above gives the arithmetic; the decision is his. It should not still be open when Stage 2 is requested. |

**Minor, not conditions:** the event calendar's 60-day expiry warning falls back to first-Friday NFP dates, but CPI and FOMC have no simple rule — note the renewal as a recurring diary item. And the top tier (+1.11R over 112 in-sample trades) correctly runs in shadow; 112 trades is a small subset and its error bars are wide.

---

## 6. WHAT THE DEMO MUST BE ALLOWED TO DO

The §8 band is well built and the board adopts it without change:

| After | 5th percentile | Median | 95th percentile |
|---|---|---|---|
| 27 trades (~6 months) | −10R | +8R | +31R |
| 60 trades (~13 months) | −10R | +18R | +51R |
| 110 trades (~2 years) | −4R | +34R | +78R |

*"Even with the edge intact, about one forward test in seven is negative after 60 trades. So the test is judged against the band, not against zero."*

**That sentence is the single most important risk-management line in the submission.** A negative six months does not falsify this system, and a positive six months does not validate it. The band is the instrument. Judge against it.

**Stop rules adopted as written:** halt and review below the 5th percentile at any monthly review or on any critical execution failure; de-risk and review on a tripwire alarm; review if the daily loss guard triggers twice in a month or the backtest twin disagrees on more than 5% of days.

---

## 7. STANDING RECORD

- **Submitted:** 3 Oct 2026. **Approved:** 4 Oct 2026, conditions §5.
- **Live capital:** not requested, not granted. A separate CRO approval is required for Stage 2.
- **Next CRO checkpoint:** Stage 1 review after 6 months of demo and at least 27 taken trades.
- **Standing finding:** AVA is not a 2027 income stream. Earliest realistic burn coverage is late 2027 to early 2028, and only via a passed $100k prop account at full size. The 2027 wedding gate remains dependent on the IOA's first mandate.
- **Open item closed:** the $94k FTMO account is **impaired**. No sizing plan in this report can recover it inside its remaining rope.
