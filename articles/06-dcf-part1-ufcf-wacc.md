# 06 | DCF Valuation I: UFCF and WACC

*Comps tell you what the market thinks. Precedent transactions tell you what buyers paid. The DCF is the one method that asks the company itself: how much cash are you actually going to produce, and what is that worth today? It is also the one method where every single assumption is yours — which is both its power and its danger.*

> **Learning goals.** After this article you can: (1) explain the DCF intuition — why a company is worth the present value of its future cash flows; (2) build unlevered free cash flow (UFCF) from EBIT, line by line; (3) compute WACC from its three ingredients — cost of equity, after-tax cost of debt, and market-value weights; (4) discount a five-year forecast into a present value by hand; (5) spot the classic DCF mistakes before they cost you credibility.
>
> **Prerequisites.** Article 02 (the three statements as one machine) and article 03 (enterprise value vs. equity value). Basic algebra; nothing fancier.

## 1. The intuition: a company is a cash machine

Strip away the branding, the strategy decks, and the org chart, and a company is a machine that takes in capital and spits out cash — unevenly, unpredictably, but cash. If you bought the entire company today, locked the doors, and simply collected whatever cash it produced for the rest of its life, what you collected is what you bought. The DCF (discounted cash flow) just puts a price on that collection.

Two ideas do all the work:

**A dollar today beats a dollar tomorrow.** Not because of inflation alone, but because a dollar today can be invested — lent out, put in the market, used to avoid borrowing. This is the *time value of money*, and it is the least controversial idea in finance. If you can earn 8% a year elsewhere at comparable risk, then $108 arriving a year from now is worth exactly $100 to you today. Run that logic in reverse — dividing instead of multiplying — and you get *discounting*.

**Risk demands compensation.** A promised dollar from the U.S. Treasury is not the same as a hoped-for dollar from a startup. The riskier the cash flow, the higher the return you demand for waiting, and the harder you discount it. The discount rate is therefore doing double duty: it prices *time* and it prices *risk*.

Put them together and the DCF philosophy fits in one sentence: *a company's enterprise value is the present value of the cash its business will generate in the future, discounted at a rate that reflects the risk of those cash flows.* Everything else in this article is machinery for making that sentence operational: which cash flows, which discount rate.

## 2. The one formula that runs everything

If cash flow $CF_t$ arrives in year $t$ and your required return is $r$, its value today is:

```math
PV = \frac{CF_1}{(1+r)} + \frac{CF_2}{(1+r)^2} + \cdots + \frac{CF_n}{(1+r)^n}
```

This is not a definition handed down from nowhere — it is compounding run backwards. If $100 invested at $r$ becomes $100 \times (1+r)$ in one year, then a claim on $100 \times (1+r)$ a year from now must be worth $100$ today, or an arbitrage exists: buy the cheap one, sell the dear one, pocket the difference. Each term in the sum is one future year's cash, pulled back to today at the compound rate. Add them up and you have priced the whole stream.

A practical note on timing that bankers actually argue about: the formula above assumes cash arrives on December 31st. Real businesses generate cash throughout the year, so many models use a *mid-year convention* — discounting year $t$ by $(1+r)^{t-0.5}$ instead of $(1+r)^t$ — which raises the value slightly. It is a refinement, not a revolution; this article sticks with year-end discounting to keep the arithmetic transparent, and part 2 will show where the mid-year adjustment lives.

## 3. UFCF: the cash that belongs to everyone

Here is the first genuinely consequential choice in any DCF: *which* cash flow do you discount? The answer bankers standardize on is **unlevered free cash flow (UFCF)** — the cash the business generates for *all* of its capital providers, debt holders and equity holders alike, before any financing decisions muddy the picture.

The word "unlevered" means: pretend the company has no debt. Not because debt doesn't matter — it does, and it gets its full accounting in the discount rate — but because we want to value the *business*, and then let each claimant's slice be sorted out afterwards (that sorting was article 03's bridge: enterprise value minus net debt gets you to equity value). If we used cash flows *after* interest payments, we'd be mixing the business's operating performance with its financing choices, and we'd have to unmix them later. Cleaner to keep them separate from the start.

UFCF is built from EBIT, and every line in the build has a reason:

```math
UFCF = EBIT \times (1 - t) + D\&A - capex - \Delta NWC
```

Walk it slowly:

- **Start from EBIT, not net income.** Net income has already subtracted interest — the debt holders' cut. But debt holders are part of "everyone," so we start *above* the interest line. (This is the same instinct as article 03: enterprise value is the value to all claimants, so the cash flow must be too.)
- **Tax it at $(1 - t)$.** We apply the corporate tax rate to EBIT as if the company were all-equity financed. This is a hypothetical tax bill — the actual tax paid is lower when interest is deductible — but the interest tax shield is captured inside WACC instead (section 4). Counting it in both places would double-count it; counting it in neither would undervalue the firm. One home, one counting.
- **Add back D&A.** Depreciation and amortization reduced EBIT but consumed no cash this period. They are accounting's way of spreading past spending, not current spending.
- **Subtract capex.** This is the line people forget, and it is the most honest line in the model. D&A tells you what past investments *cost on paper*; capex tells you what the company *actually spends* to maintain and grow its asset base. A business with $30m of D&A and $45m of capex is bleeding $15m a year more than its income statement admits. Growth is not free, and capex is the receipt.
- **Subtract the change in net working capital ($\Delta NWC$).** Growth eats cash before it produces it: more sales mean more inventory on shelves and more receivables waiting to be collected. Net working capital is (current assets − cash) − (current liabilities − debt); when it *increases*, cash is tied up, so we subtract. When it *decreases* — customers paying faster, suppliers paid slower — cash is released, so a negative $\Delta NWC$ adds to UFCF. Get the sign wrong and you have valued growth backwards.

One useful restatement, because you will see it in real models: since $EBITDA = EBIT + D\&A$,

```math
UFCF = EBITDA \times (1 - t) + t \times D\&A - capex - \Delta NWC
```

(Check: $EBITDA(1-t) + t\cdot D\&A = (EBIT + D\&A)(1-t) + t\cdot D\&A = EBIT(1-t) + D\&A$. Same thing.) The $t \times D\&A$ term has a name — the **depreciation tax shield** — and seeing it written out reminds you that depreciation's only cash benefit is the tax it saves.

Distinguish three levels here, because the series keeps this discipline: the *intuition* (value the business for everyone, before financing) is solid; the *strict conclusion* (UFCF pairs with WACC, never with the cost of equity alone) is non-negotiable; the *estimates* (the tax rate you'll actually face, what counts as maintenance vs. growth capex) are judgment calls you must defend, not facts you can look up.

## 4. WACC: the discount rate must match the cash flow

This is the article's load-bearing principle, so let's state it plainly:

> **The discount rate must price the same claims the cash flow belongs to.**

UFCF belongs to debt holders *and* equity holders. So the discount rate must be the blended required return of debt *and* equity — the **weighted average cost of capital (WACC)**. Discount UFCF at the cost of equity alone and you've demanded equity-level returns for cash that partly belongs to lenders; the value comes out too low, and the error is conceptual, not arithmetic.

WACC has three ingredients:

```math
WACC = \frac{E}{V} \cdot r_e + \frac{D}{V} \cdot r_d \cdot (1 - t), \quad V = E + D
```

**Ingredient 1: cost of equity ($r_e$), via CAPM.** Equity holders bear the most risk, so their required return is the highest. The capital asset pricing model builds it up:

```math
r_e = r_f + \beta \times (E[R_m] - r_f)
```

- $r_f$, the **risk-free rate**: what you earn for taking no risk — in practice, the yield on long-term government bonds (the 10-year Treasury is the market standard for U.S. valuations).
- $(E[R_m] - r_f)$, the **market risk premium**: the extra return investors demand for holding the risky market portfolio instead of Treasuries. Typically estimated at 4–6% for the U.S.; it is an estimate with genuine academic debate behind it, not a constant of nature.
- $\beta$ (**beta**): how much the stock amplifies market moves. $\beta = 1$ moves with the market; $\beta = 1.5$ is 50% more volatile *in a way correlated with the market*. Beta is estimated by regressing the stock's returns on the market's — which means it is backward-looking, noisy, and one of the first things a good analyst stress-tests.

**Ingredient 2: after-tax cost of debt ($r_d(1-t)$).** Two subtleties. First, use the *marginal* cost — the yield the company would pay to borrow *today* — not the coupon on bonds issued five years ago in a different rate environment. Second, multiply by $(1-t)$ because interest is tax-deductible: a 6% loan at a 25% tax rate really costs $6\% \times 0.75 = 4.5\%$ after the government absorbs a quarter of it through lower taxes. This tax shield is exactly why the 1958 Modigliani–Miller paper matters here: Modigliani, F. & Miller, M. (1958), "The Cost of Capital, Corporation Finance and the Theory of Investment," *American Economic Review*, 48(3): 261–297 — the founding argument that a firm's cost of capital is anchored by its assets' risk, with financing choices (and their tax consequences) layered on top.

**Ingredient 3: the weights — market values, not book.** $E$ is share price × shares outstanding; $D$ is the *market* value of debt (practitioners often use book debt as a proxy when it trades near par — flag it as the approximation it is). Book equity is a museum of past accounting decisions; the discount rate must price the claims investors *actually hold at today's prices*. Using book weights quietly assumes the market values the firm at its accounting history, which defeats the purpose of valuing it.

One honest complication, worth naming rather than hiding: the weights need the firm's value, which is what you're trying to compute — a circularity. Practitioners break it with a *target* capital structure (where management says leverage is heading) or by iterating the model until the weights converge. It is not a flaw in the theory; it is a reminder that WACC is a model of the future, not a measurement of the past.

## 5. Worked example: Alder & Grove Outdoor Co.

Let's run the whole machine on a fictional company — Alder & Grove, a maker of outdoor gear — with a five-year forecast. All figures in $ millions.

**Assumptions** (stated up front, because in a real model these are the part you'd argue about):

| Assumption | Value |
|---|---|
| Base-year revenue | 500.0 |
| Revenue growth, years 1–5 | 6%, 6%, 5%, 5%, 4% |
| EBIT margin | 18% of revenue |
| Tax rate | 25% |
| D&A | 6% of revenue |
| Capex | 7% of revenue |
| ΔNWC | 15% of the *change* in revenue |

**Step 1 — build UFCF.** Revenue compounds: 530.0, 561.8, 589.9, 619.4, 644.2. Then:

| ($m) | Y1 | Y2 | Y3 | Y4 | Y5 |
|---|---|---|---|---|---|
| Revenue | 530.0 | 561.8 | 589.9 | 619.4 | 644.2 |
| EBIT (18%) | 95.4 | 101.1 | 106.2 | 111.5 | 116.0 |
| NOPAT = EBIT × 0.75 | 71.6 | 75.8 | 79.6 | 83.6 | 87.0 |
| + D&A (6%) | 31.8 | 33.7 | 35.4 | 37.2 | 38.7 |
| − Capex (7%) | (37.1) | (39.3) | (41.3) | (43.4) | (45.1) |
| − ΔNWC | (4.5) | (4.8) | (4.2) | (4.4) | (3.7) |
| **= UFCF** | **61.8** | **65.4** | **69.5** | **73.0** | **76.9** |

Check year 1 by hand: $71.6 + 31.8 - 37.1 - 4.5 = 61.8$. ✓ Notice how UFCF ($61.8m) sits well below EBIT ($95.4m): taxes, reinvestment, and working capital take their cut before any claimant sees a dollar. That gap is the whole reason we build UFCF instead of capitalizing earnings.

**Step 2 — compute WACC.**

| Input | Value | Source |
|---|---|---|
| Risk-free rate $r_f$ | 4.0% | 10-yr Treasury |
| Market risk premium | 5.0% | long-run U.S. estimate |
| Beta | 1.2 | regression vs. market |
| Cost of equity $r_e = 4.0\% + 1.2 \times 5.0\%$ | **10.0%** | CAPM |
| Pre-tax cost of debt $r_d$ | 6.0% | current borrowing yield |
| After-tax cost of debt | **4.5%** | $6.0\% \times (1 - 0.25)$ |
| Market value of equity $E$ | 900 | share price × shares |
| Market value of debt $D$ | 300 | trades near par |

```math
WACC = \frac{900}{1200} \times 10.0\% + \frac{300}{1200} \times 4.5\% = 7.50\% + 1.125\% = 8.625\%
```

**Step 3 — discount.** Discount factors at 8.625%: $1/1.08625 = 0.9206$ in year 1, compounding each year.

| ($m) | Y1 | Y2 | Y3 | Y4 | Y5 |
|---|---|---|---|---|---|
| UFCF | 61.8 | 65.4 | 69.5 | 73.0 | 76.9 |
| Discount factor | 0.9206 | 0.8475 | 0.7802 | 0.7183 | 0.6612 |
| **Present value** | **56.9** | **55.4** | **54.2** | **52.4** | **50.8** |

Sum: $56.9 + 55.4 + 54.2 + 52.4 + 50.8 = \textbf{269.8}$. So the first five years of cash flows are worth about **$270m** today.

Two things to notice. First, year 5's $76.9m of cash is worth only $50.8m today — discounting at 8.625% has eaten a third of it. Time and risk are expensive. Second — and this is the cliffhanger — Alder & Grove doesn't liquidate at the end of year 5. The company keeps going, and the value of *everything after year 5* typically dwarfs what we just computed. Pricing that tail is the terminal value, and it gets its own article next, because it deserves your full suspicion.

Once the terminal value is added, the bridge from article 03 takes over: enterprise value minus net debt (plus non-operating assets, minus minority interests) lands you at equity value, divided by shares for the per-share price a board can actually vote on.

## 6. What this article deliberately leaves for part 2

A short honesty list, so nothing here gets mistaken for the whole story:

- **The terminal value** (Gordon growth vs. exit multiple) — usually 60–80% of the total DCF value, which is exactly why a whole article is devoted to not letting it quietly decide everything.
- **The mid-year convention** — discounting at $(1+r)^{t-0.5}$ to reflect cash arriving throughout the year.
- **WACC circularity** — target capital structures and iteration, mentioned in section 4.
- **Scenario and sensitivity analysis** — the DCF is never one number; it is a table of numbers under different assumptions, and the football field (article 10) is where those tables go to be compared.

## Common Misconceptions

- **"The DCF gives the true value of the company."** It gives a *disciplined, auditable opinion* — every assumption visible, every step checkable. Change the growth rate by one point or WACC by half a point and the answer moves a lot. Treat the output as the center of a sensitivity table, never as a fact.
- **"I'll just discount the cash flow after interest payments at WACC."** That double-counts debt: WACC already compensates lenders through the debt term, so feeding it cash flows that already paid lenders mixes two different claims. Levered cash flow (after interest) pairs with the *cost of equity*; unlevered cash flow pairs with *WACC*. Mismatching them is the single most common DCF error in student models.
- **"WACC weights come from the balance sheet."** Book values record history at historical cost; the discount rate must price claims at *today's market prices*. A company whose equity has tripled since its IPO has a far lower debt weight than its balance sheet suggests.
- **"Cost of debt is the coupon on our existing bonds."** WACC is forward-looking: it asks what the next dollar of debt costs *today*. And the tax shield is not optional decoration — forgetting the $(1-t)$ overstates the cost of debt and understates value.
- **"EBITDA is basically cash flow, so I can discount that."** EBITDA ignores capex and working capital — the two places growth actually consumes cash. In our example, EBITDA in year 1 was $127.2m while UFCF was $61.8m; more than half the "cash flow" never existed. Adding back D&A does not make capex free.
- **"A 1% change in WACC barely matters."** At 8.625% our five-year PV was $269.8m; at 9.625% it falls to about $263m — and once the terminal value (part 2) enters, a single point of WACC can swing total value by 15–20%. Small inputs, large leverage: that is why the discount rate gets its own section.

## Test Yourself

**Q1.** A company reports EBIT of $120m, a 25% tax rate, D&A of $25m, capex of $40m, and an increase in net working capital of $10m. What is UFCF? Show the steps.
*A1. NOPAT = 120 × 0.75 = 90. UFCF = 90 + 25 − 40 − 10 = $65m. The NWC increase is subtracted because growth tied up $10m of cash.*

**Q2.** A firm has market equity of $800m and market debt of $200m. Cost of equity is 11%, pre-tax cost of debt is 5%, tax rate 25%. Compute WACC.
*A2. Weights: E/V = 0.8, D/V = 0.2. After-tax debt cost = 5% × 0.75 = 3.75%. WACC = 0.8 × 11% + 0.2 × 3.75% = 8.8% + 0.75% = 9.55%.*

**Q3.** Why must WACC use market-value weights rather than book values? What practical problem does this create, and how do bankers handle it?
*A3. The discount rate prices the claims investors actually hold at today's prices; book values are historical accounting artifacts. The problem is circularity — the weights need the firm's value, which is what the DCF is solving for. Bankers use a target capital structure or iterate the model until the weights converge.*

**Q4.** An analyst discounts free cash flow *after* interest payments at WACC. Name the error and state the correct pairing.
*A4. Claim/discount-rate mismatch (double-counting debt). Cash flow after interest belongs to equity holders only, so it must be discounted at the cost of equity. WACC pairs exclusively with unlevered (pre-interest) cash flow.*

---

*Next up — **07 | DCF Valuation II: Terminal Value & Sanity Checks**: the Gordon growth model, exit multiples, and how to stop the terminal value from quietly deciding everything.*
