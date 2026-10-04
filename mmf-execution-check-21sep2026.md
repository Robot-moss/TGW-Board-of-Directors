# MMF EXECUTION CHECK — RAISED 21 SEPTEMBER 2026, CLOSED 1 OCTOBER 2026

**Board seat:** COO (execution) | **Trigger:** scheduled task, one-off
**Status:** ✅ **EXECUTED.** ₦5,000,000 deposited into the Coronation Money Market Fund, confirmed by David 1 October 2026.
**Elapsed:** 13 days from decision to execution. Seventeen days inside the thirty-day sprint window.
**Downstream:** this check produced the Rule 1 v1 → v2 rewrite. See §4 and `MEMORY-CORE-tier1.md` §4.

---

## 1. RESULT

| Field | Confirmed |
|---|---|
| Fund | **Coronation Money Market Fund** (Coronation Asset Management Ltd) |
| Amount | **₦5,000,000 — the full committed amount** |
| Source | Piggyvest (₦8,000,000 balance → ₦3,000,000 residual) |
| Confirmed | 1 October 2026, by David |
| Yield at decision | 20.54% YTD (Q3 2026) |
| Management fee | 1.50% |
| Redemption | 24–48 hours, no penalty |

**Reconciliation baseline — the board's original ask was wrong and is corrected here.**

The board asked for unit price / NAV at purchase. **No such figure exists.** This is a constant-price fund: returns arrive as income credited, not as a rising unit price, so there is no purchase NAV to anchor on. The board was applying an equity-fund reconciliation to a cash-fund product.

The board also asked for the client ID. **That request is withdrawn.** It is an access identifier and has no business sitting in a project document.

**The correct method:** opening balance and date (held) against income credited per statement period. Realised yield = income ÷ average balance, annualised, compared to the 20.54% quoted. **Outstanding: the first statement.** That is the only item still needed.

---

## 2. WHAT THE DEPOSIT BOUGHT — AND WHAT IT DID NOT

**Yield: ₦527,000/year.** Piggyvest at ~10% against 15.91% inflation is roughly −6% real. Coronation at 20.54% is roughly +4.6%.

**Runway: unchanged.** ₦5m at 48 hours plus ₦3m in Piggyvest is still ₦8m inside two business days — 6.4 months. The board's own Part A argument, that an MMF is not meaningfully less liquid than Piggyvest, is what made this a free improvement rather than a trade-off.

**Concentration: unchanged, by 0.00pp.** Odion was 70.8% of ₦113.0m of financial assets before and is 70.8% of ₦113.0m after. A reallocation between two **non-Odion** assets leaves both numerator and denominator untouched.

**Board error recorded (B2).** The board presented that third point as a correction, on the assumption David had mistaken a yield win for a risk win. He had not. His stated objective was capital efficiency — *"making better financial decisions as the options open up to me"* — not de-concentration, and he had never claimed otherwise. The board graded the decision against an objective he had not invoked, and spent his attention explaining a point he already held. The standing correction is in `MEMORY-CORE-tier1.md` §3b.

What survives, as a finding rather than a lesson: **the sweeps and the Lokoja sale are now the entire active de-concentration engine.** That is why the ₦500,000 question below mattered more than its size.

---

## 3. THE COLLISION FLAGGED ON 21 SEPTEMBER — CLOSED BETTER THAN PROPOSED

The board flagged that the ₦5m transfer and the Dangote IPO's second ₦500,000 tranche both drew on the same ₦8m Piggyvest balance, leaving ₦2.5m against a stated ₦3m buffer, immediately before the December–March rent gap. The board assumed the resolution would be accepting the smaller buffer.

**David resolved it differently and better:** he changed the tranche's funding source to the monthly Odion returns and left the ₦3m buffer whole — intact at exactly the figure he set, going into the quarter when it is most needed.

Recorded as **E1** in the cognitive profile. One observation, not a pattern. Counterweight recorded alongside it: the chosen source re-routed the cost into Rule 1 rather than removing it, which is the subject of §4.

---

## 4. RULE 1 v1 → v2 — THE REWRITE THIS CHECK PRODUCED

### 4a. There is only one surplus stream

Odion income ₦2,100,000 + rent ₦91,666 − burn ₦1,250,000 = **~₦941,666/month.**

The Odion return *is* the water that becomes the surplus. "From Odion returns" and "from the monthly surplus" are the same money by a different route. The distinction was real and it protected the buffer — but it did not create money outside Rule 1's claim. The month the tranche goes in, the sweep is **~₦440,000 instead of ~₦940,000.**

### 4b. Why v1 was retired rather than patched

David then established the governing principle, unprompted: **surplus will not always serve de-concentration, because life events and unforeseen circumstances exist.**

That retired v1 rather than amending it. A rule known in advance to be unkeepable does not produce compliance — it trains the habit of quiet breach and takes the credibility of every neighbouring rule with it. Logged as board principle **BP1** at David's instruction: *design rules to be keepable, not aspirational.*

### 4c. The measurement error v1 contained

The de-concentration clock depends on surplus entering the **non-Odion financial asset base**, not on it entering the MMF. ₦500,000 into NGX equities advances the clock exactly as fast as ₦500,000 into Coronation. Only surplus that *leaves* the base slows it.

So v1 was pointed at the wrong variable, and the two cases — opportunities and life events — have genuinely different costs and should never have shared one number.

### 4d. A board error caught on review

The board first offered a Channel A cap of "20% of **monthly** surplus" — ₦188,333 — as the amendment that would accommodate a ₦500,000 tranche. **It would have been breached on first use.** Logged as **B4**: test a proposed rule against the live case before offering it. Opportunities are lumpy; the budget for them must be too. The cap is annual.

### 4e. Rule 1 v2, ratified 1 October 2026

| | |
|---|---|
| **Clause 1 — Odion floor** | ₦0 of surplus to Odion until Odion < 50%. **Absolute.** No channels, no carve-outs. v1's teeth were never "100% to the MMF" — they were "0% to Odion," and the floor never conflicts with a life event. |
| **Clause 2 — Default** | 100% of surplus to the Coronation MMF. |
| **Clause 3 — Channel A** | Up to **20% of annual surplus (~₦2,260,000/yr)** to other non-Odion *financial* assets. **Clock-neutral.** Cost is liquidity and price risk only. |
| **Clause 4 — Channel B** | Life events and unforeseen circumstances **suspend** the sweep, **uncapped**, with a **soft trigger**: any draw above one month's full surplus (₦941,666) is written up *before* the money moves. **Clock-stretching** — ~50 months becomes ~62 at a sustained 20% diversion to spending. |
| **Clause 5 — Review** | Anything over ₦250,000 named in the ledger; Channel A reconciled against the ceiling each December. |

The soft trigger was David's choice over a hard cap, in his words *"that way the rules are not violated easily."* Recorded as **E3**: offered the easier design and the more constraining one, he chose the one that binds him harder, reasoning about his own future compliance rather than his present convenience.

**Recorded dissent (constitution §3.2).** The CRO objects that an uncapped Channel B is unfalsifiable — any diversion can be relabelled a life event. The objection is sound and was not dismissed. The decision goes against it because a capped emergency clause is breached in the first real emergency and takes the rule's credibility with it. The CRO's objection converts into the Clause 4 soft trigger, the Clause 5 logging duty, the December reconciliation, and the written test now held in `MEMORY-CORE-tier1.md` §4 Clause 4 — so the disagreement about *what counts* is pre-settled rather than argued under pressure.

**The Dangote ₦500,000 is no longer an exception.** It is the first Channel A draw — 4.4% of the annual ceiling, ~₦1,760,000 headroom remaining, clock-neutral, still gated on David's own documented conditions and the 13 October offer close.

**Known gap, raised and not yet closed:** the wedding fits neither channel. Not an opportunity, so not Channel A; foreseeable, chosen and dated, so it fails the Channel B test — and it is consumption, so it leaves the asset base. A B1/B2 split (unforeseen vs planned life expenditure, the latter pre-funded via a sinking fund) is proposed and awaiting decision.

---

## 5. SPRINT STATUS — OBJECTIVE 1 CLOSED

| KR | Status |
|---|---|
| KR1.1 Coronation MMF account opened | ✅ Confirmed 1 Oct 2026 |
| KR1.2 ₦5,000,000 transferred | ✅ Transferred. First statement outstanding for reconciliation |
| KR1.3 Standing rule activated | ✅ Rule 1 **v2** ratified and active |

Objective 1 closed 17 days early. Objectives 2 (title chain) and 3 (data gaps) are now the critical path, and Objective 2 gates the Lokoja sale — the highest-value single decision in the file.

**Monitoring now live:** Dangote decision check, one-off 10 Oct 2026 (`trig_01EYVbKjNRJmavFDmgFEcKgf`). Rule 1 monthly sweep confirmation, 5th of each month (`trig_01MTwphNr2zTFWFcH5aUc7gL`). Both run in the cloud with no access to his accounts — they can ask and record, not verify.

*Figures carried from the project docs of 18 September 2026 and David's confirmations of 1 October 2026. The deposit is confirmed by David, not independently verified by the board.*
