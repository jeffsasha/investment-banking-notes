# 07 | DCF Valuation II: Terminal Value and Sanity Checks

*Last article we built the engine — the five-year cash flow forecast and the discount rate — and it valued Alder & Grove's first five years at $270 million. Nice. Except the company doesn't shut down in year five. Everything it earns from year six to forever is still unpriced, and that tail is about to turn out to be three-quarters of the whole answer. This is the article about the part of the DCF bankers trust the least and rely on the most.*

> **Learning goals.** After this article you can: (1) explain why the terminal value typically dominates a DCF and what that implies; (2) derive the Gordon growth formula and state the conditions under which it is valid; (3) compute a terminal value with the exit-multiple method and cross-check it against the Gordon result; (4) run the sensitivity and sanity checks bankers actually use before showing a DCF to anyone senior.
>
> **Prerequisites.** Article 06 (UFCF and WACC — we continue the Alder & Grove example from there) and article 04 (trading multiples, which the exit-multiple method leans on).

## 1. Why the tail eats the dog

Here is the uncomfortable arithmetic of every DCF you've ever seen. Last article, Alder & Grove's first five years of cash flow discounted to **$269.8m**. A reasonable estimate of that company's total enterprise value will land somewhere around **$1.1 billion**. Which means the five years we modeled in loving detail — the revenue build, the margins, the capex schedule, the working capital — account for barely a quarter of the answer. The other three quarters come from a single line item: the *terminal value*, our one-line guess about "everything after year five."

This isn't a bug in our example. It's the standard outcome. In most banker DCFs the terminal value is 60–80% of total enterprise value, because five years of cash discounted at 8–10% simply can't compete with *infinity* of cash discounted at the same rate. The forecast period is the part you understand; the terminal value is the part that matters. Sit with that asymmetry for a moment, because it explains the entire culture of suspicion around the DCF: you're spending 90% of your modeling effort on 25% of the value.

Two honest reactions follow. The first is to dismiss the DCF as a game where the answer is whatever you want — pick your terminal growth rate and back into any valuation you like. The second is to treat the terminal value as a precision instrument — compute it to four decimals and defend it like physics. Both are wrong. The terminal value is neither a joke nor a fact. It's a disciplined way to bound your ignorance: you compress everything you can't forecast into a small number of assumptions, and then you stress-test those assumptions until you know exactly where the model breaks. This article is about building that discipline.

## 2. The Gordon growth model: pricing infinity in one line

The most common terminal value method is the **Gordon growth model** (also called the perpetuity growth method). The idea: after year $n$, the company's free cash flow grows at a constant rate $g$ forever. Then the value at year $n$ of all cash flows from year $n+1$ onward is:

```math
TV_n = \frac{UFCF_{n+1}}{WACC - g} = \frac{UFCF_n \times (1 + g)}{WACC - g}
```

This isn't a definition — it's a geometric series summed in closed form. Let's derive it, because the derivation is where the constraints come from:

```math
TV_n = \frac{UFCF_{n+1}}{(1+WACC)} + \frac{UFCF_{n+1}(1+g)}{(1+WACC)^2} + \frac{UFCF_{n+1}(1+g)^2}{(1+WACC)^3} + \cdots
```

Factor out the first term. Each subsequent term multiplies the previous one by $\frac{1+g}{1+WACC}$. That's a geometric series with ratio $q = \frac{1+g}{1+WACC}$:

```math
TV_n = \frac{UFCF_{n+1}}{1+WACC} \times \left(1 + q + q^2 + \cdots \right) = \frac{UFCF_{n+1}}{1+WACC} \times \frac{1}{1 - q}
```

And $1 - q = 1 - \frac{1+g}{1+WACC} = \frac{WACC - g}{1+WACC}$, so the $(1+WACC)$ terms cancel and you're left with $\frac{UFCF_{n+1}}{WACC - g}$. Clean. But notice what the derivation demanded: the geometric series only converges if $q < 1$, i.e., **$g < WACC$**. Strictly. If $g \geq WACC$, the series diverges and the formula produces nonsense — a negative denominator or an infinite value. That's the first hard constraint: terminal growth must be below the discount rate, with a comfortable spread, not a rounding error of one.

The second constraint comes from economics, not math. A company cannot grow faster than the economy forever, or it eventually *becomes* the economy and then keeps going past it. Terminal growth is therefore capped by long-run **nominal** growth — real GDP growth plus inflation — typically 3–5% for the U.S. in bankers' models, and most practitioners use 2–3% to be safe. Note the word *nominal*: your cash flows are nominal, your WACC is nominal, so $g$ must be nominal too. Mixing real growth with a nominal discount rate is a quiet, common error.

The third constraint is the subtlest and the most economic: **in perpetuity, ROIC fades toward WACC.** The intuition is competitive equilibrium — excess returns attract competitors, who bid them away. If your terminal year earns 25% returns on invested capital while its cost of capital is 9%, the model is asserting the company defends a 16-point spread *forever*. Sometimes that's defensible (a genuine moat), but it needs a paragraph of justification, not a shrug. Many bankers enforce the discipline mechanically: assume terminal ROIC equals WACC, which implies the steady-state reinvestment rate is $\frac{g}{ROIC} = \frac{g}{WACC}$ — and then check that the implied capex and working capital in the terminal year are consistent with that reinvestment rate. If your forecast has capex at half of D&A in year five while $g$ assumes 3% perpetual growth, the model's left hand doesn't know what its right hand is doing.

Distinguish the levels, as this series does: the *intuition* (a mature company grows roughly with the economy) is solid; the *strict conclusions* ($g < WACC$; nominal-to-nominal consistency) are non-negotiable; the *estimates* (is 2.5% or 3% right? does the moat survive?) are judgment calls you must be able to defend out loud.

## 3. The exit-multiple method: smuggling the market into the DCF

The second standard method skips the perpetuity entirely. Instead, you assume that at the end of year $n$, the company is sold for what comparable companies trade for:

```math
TV_n = EBITDA_n \times (\text{terminal EV/EBITDA multiple})
```

Then discount that back like any other year-$n$ amount. That's it — no growth rate, no infinite series.

Be clear-eyed about what this method *is*: it's a relative valuation wearing a DCF costume. You're importing the market's pricing (via comps, which was article 04) and pasting it at the end of your intrinsic valuation. There's nothing wrong with that — in practice it's often the method bankers trust more, precisely because it's anchored to observable prices rather than to a growth rate you invented. But it means the "DCF" now contains a comps valuation inside it, and you should say so rather than pretend the whole thing is intrinsic.

The method has its own discipline: the terminal multiple should reflect what the company will look like *at maturity*, not today. A high-growth company trading at 15x EBITDA today might deserve a 9–10x terminal multiple once growth has normalized. Bankers typically pick the terminal multiple at or below current trading multiples, and they always show which comps justify it.

A warning that saves careers: **never compute both methods and average them.** They are not two independent estimates — they're two different assumptions about the same unknowable future, and averaging them produces a number that corresponds to no coherent story. The professional move is to pick one as primary (usually Gordon growth for a stable company, exit multiple when comps are strong) and show the other as a cross-check. If the two methods disagree violently, that's information — it means your growth assumption and your multiple assumption are telling different stories about the company's future, and you need to figure out which one you actually believe.

## 4. Worked example: Alder & Grove, continued

Back to our outdoor-gear company. From article 06: year-5 UFCF is **$76.9m**, WACC is **8.625%**, year-5 EBITDA is **$154.7m** (EBIT $116.0m + D&A $38.7m), the year-5 discount factor is **0.6612**, and the first five years' PV is **$269.8m**.

**Method A — Gordon growth with $g = 2.5\%$.**

```math
UFCF_6 = 76.9 \times 1.025 = 78.8
```

```math
TV_5 = \frac{78.8}{0.08625 - 0.025} = \frac{78.8}{0.06125} = 1,286.9
```

So the terminal value *at year five* is **$1,286.9m**. Discount it back:

```math
PV(TV) = 1,286.9 \times 0.6612 = 850.9
```

Total enterprise value:

```math
EV = 269.8 + 850.9 = 1,120.7
```

About **$1.12 billion** — and the terminal value is $\frac{850.9}{1120.7} = 75.9\%$ of it. There it is: three-quarters of the answer from one growth assumption. Everything in the rest of this article is about earning the right to that number.

**Method B — exit multiple of 8.0x year-5 EBITDA.**

```math
TV_5 = 154.7 \times 8.0 = 1,237.6
```

```math
PV(TV) = 1,237.6 \times 0.6612 = 818.3 \quad \Rightarrow \quad EV = 269.8 + 818.3 = 1,088.1
```

**$1.09 billion** — within 3% of the Gordon result. Now the cross-checks, which are the real product of running both methods:

- *Implied exit multiple from the Gordon TV:* $\frac{1286.9}{154.7} = 8.3x$. Our 8.0x assumption sits just below it — consistent; the market wouldn't obviously call our growth assumption aggressive.
- *Implied perpetual growth from the exit multiple:* rearrange the Gordon formula, $g = WACC - \frac{UFCF_6}{TV_5}$:

```math
g_{\text{implied}} = 0.08625 - \frac{78.8}{1237.6} = 0.08625 - 0.0637 = 2.26\%
```

2.26% against our 2.5% assumption — the two methods are telling the same story. *This* is what a healthy DCF looks like: not two methods averaged, but two methods interrogating each other and agreeing.

One more number for the road: implied EV / year-1 EBITDA is $\frac{1120.7}{127.2} = 8.8x$. If comps trade at 7–9x, our DCF sits inside the market's range rather than floating above it — another quiet confirmation that nothing in the model has come unmoored.

## 5. The sensitivity grid: the table every banker actually shows

Because the terminal value dominates, the honest DCF presentation isn't a single number — it's a grid. Here is Alder & Grove's year-5 terminal value ($m) across plausible WACC and $g$:

| WACC \ $g$ | 1.5% | 2.5% | 3.5% |
|---|---|---|---|
| 7.625% | 1,287 | 1,538 | 1,911 |
| 8.625% | 1,106 | **1,287** | 1,538 |
| 9.625% | 970 | 1,106 | 1,287 |

Read what the grid is saying. Moving WACC down one point *and* $g$ up one point takes the terminal value from $1,287m to $1,911m — up 48%. Moving both the other way takes it to $970m — down 25%. On inputs that would each survive a casual review. The diagonal symmetry is no accident: what matters is the *spread* $(WACC - g)$, and small spreads are leverage. A 6.1-point spread prices the tail at $1.3bn; a 4.1-point spread prices it at $1.9bn. Half the spread, half-again the value.

This is why senior bankers ask about the terminal value first and the forecast second. The five-year build is where analysts spend their weeks; the $(WACC - g)$ spread is where the answer lives. When you present a DCF, lead with the grid, not the headline number. Anyone who has done this before will flip to the sensitivity table before reading your revenue assumptions — meet them there.

Two footnotes for completeness. First, the **mid-year convention** from article 06 applies to the terminal value too: discount $TV_5$ at 4.5 years instead of 5, which at our WACC multiplies its PV by $\sqrt{1.08625} \approx 1.042$ — about +4%, or $36m on our numbers. Refinement, not revolution, but include it when the model is real. Second, the terminal year must be a **normal year**: if year five is the peak of a cycle (margins at all-time highs) or the trough, growing it into perpetuity bakes the cycle in forever. Normalize margins and capex to mid-cycle before applying either method.

## 6. Sanity checks that keep you honest

Run these before any DCF leaves your desk. Each one takes minutes; each one has caught a broken model.

1. **The 80% rule.** If the terminal value exceeds ~80–85% of enterprise value, your forecast period is too short or your terminal assumptions too rich. Ours is 76% — high, typical, acceptable. Above 85%, extend the forecast or defend the tail in writing.
2. **The implied-multiple cross-check.** Convert your Gordon TV into an implied EV/EBITDA multiple and compare it to comps. Ours: 8.3x vs. an 8.0x assumption — clean. If your Gordon math implies 14x in an industry trading at 8x, your $g$ is doing something heroic.
3. **The implied-growth cross-check.** Convert your exit multiple into an implied perpetual growth rate and compare it to your Gordon $g$. Ours: 2.26% vs. 2.5% — the same story. A 5% implied growth rate next to a 2% assumption means the methods disagree and you must pick a side.
4. **The GDP ceiling.** Terminal $g$ must sit below long-run nominal GDP growth. At 2.5% we're comfortably under a ~4% ceiling. Anything above ~4% for a U.S. company needs an extraordinary justification, and above ~5% is indefensible — the company would eventually outweigh the economy.
5. **The ROIC fade.** Check the terminal year's implied return on invested capital against WACC. Perpetual excess returns need a named moat; otherwise assume fade. The mechanical version: steady-state reinvestment $= g / ROIC$ should reconcile with the capex and working capital in your terminal year.
6. **Nominal consistency.** Nominal cash flows, nominal WACC, nominal $g$ — all three, no mixing. If you ever build a real-terms DCF (rare in banking), everything converts together.
7. **The comps reality check.** Your DCF's implied trading multiple (ours: 8.8x year-1 EBITDA) should land within shouting distance of where comps trade. A DCF at 14x in a 7–9x industry isn't "intrinsic insight" until you've written down exactly why this company deserves double the market's multiple.
8. **The Penman test.** Penman, S. H. & Sougiannis, T. (1998), "A Comparison of Dividend, Cash Flow, and Earnings Approaches to Equity Valuation," *Contemporary Accounting Research*, 15(3): 343–383, showed that when you truncate forecasts at finite horizons — which is all we ever do — valuation errors are systematically smaller for accrual-earnings-based techniques than for cash-flow techniques, precisely because the terminal value carries less weight when near-term book values anchor the valuation. And Francis, J., Olsson, P. & Oswald, D. R. (2000), "Comparing the Accuracy and Explainability of Dividend, Free Cash Flow, and Abnormal Earnings Equity Value Estimates," *Journal of Accounting Research*, 38(1): 45–70, confirmed it: in practice, the models are only theoretically equivalent, and free-cash-flow estimates show larger bias than abnormal-earnings estimates. The takeaway isn't to abandon the DCF — it's humility about what the DCF is: the theoretically cleanest method and, in finite-horizon practice, the one most exposed to terminal-value error. Which is exactly why checks 1–7 exist.

## Common Misconceptions

- **"The terminal value is the company's value at the end of the forecast."** No — it's the value *at the end of the forecast* of *everything after the forecast*. Calling it "the year-5 value" invites the error of thinking the company is worth $1,287m in year five. It's worth that *plus* the five years of cash you already counted, and the $1,287m itself still has to be discounted back to today.
- **"Any $g$ below WACC is fine."** Below WACC is necessary, not sufficient. A $g$ of 7% with a WACC of 8% converges mathematically and is still economic nonsense — it implies the firm outgrows the economy forever. The binding constraint is usually the GDP ceiling, not the WACC floor.
- **"I'll run both terminal methods and average them for robustness."** Averaging two methods that embed different stories about the future doesn't make the answer robust — it makes it incoherent. Use one as primary, the other as cross-check, and investigate disagreements instead of smoothing them.
- **"A longer forecast fixes the terminal-value problem."** Extending from 5 to 10 years shrinks the terminal value's share, but it replaces one problem with another: years 6–10 are forecasts you have even less basis for. Bankers use 5 years (sometimes 10 for very long-cycle businesses) precisely because forecast credibility decays faster than terminal-value dominance.
- **"The DCF is objective because the math is exact."** The arithmetic is exact; the inputs are judgment. Four-decimal precision on a terminal value built from a guessed growth rate is theater. Precision in the calculation, humility in the conclusion.
- **"Exit multiple is just the easier DCF method."** It's not a DCF method at all — it's relative valuation imported into the DCF. That's fine, but it means your "intrinsic" valuation now leans on market prices, and its result inherits every limitation of comps (article 04) on top of the DCF's own.

## Test Yourself

**Q1.** A company's year-5 UFCF is $120m, WACC is 9%, and you assume 3% perpetual growth. Compute the terminal value at year 5 and its present value today.
*A1. UFCF₆ = 120 × 1.03 = 123.6. TV₅ = 123.6 / (0.09 − 0.03) = 123.6 / 0.06 = $2,060m. Discount factor at 9% for 5 years: 1/1.09⁵ = 0.6499. PV = 2,060 × 0.6499 = $1,338.9m ≈ $1,339m.*

**Q2.** Your Gordon terminal value is $2,060m and year-5 EBITDA is $240m, but comparable companies trade at 7x EV/EBITDA. What does the cross-check tell you, and what do you do?
*A2. Implied multiple = 2,060/240 = 8.6x, materially above the 7x comps. The market wouldn't pay your growth assumption — either $g$ is too high, WACC too low, or you need a written case for why this company deserves a premium multiple in perpetuity. Most likely: lower $g$.*

**Q3.** An analyst sets terminal growth at 8% with WACC at 9.5%, arguing "the company is a fast grower." Name everything wrong with this.
*A3. (1) 8% exceeds long-run nominal GDP growth — the company would eventually become larger than the economy. (2) The 1.5-point WACC−g spread makes the value hyper-sensitive: tiny input changes swing the answer wildly. (3) It assumes high growth with no ROIC fade, i.e., a permanent, widening moat — asserted, not argued. Fix: cap $g$ near 2–3% or model a fade period.*

**Q4.** Your two terminal methods give $1,287m (Gordon) and $1,238m (exit multiple). Your colleague suggests averaging them to $1,263m "to be safe." Do you agree? What do you do instead?
*A4. No. The methods aren't independent draws — they're different stories about the same future, and the average corresponds to no coherent assumption set. Instead, run the cross-checks: implied multiple (8.3x) vs. assumed (8.0x), implied growth (2.26%) vs. assumed (2.5%). They agree here, so pick one as primary (say Gordon, for a stable company), report the other as a supporting cross-check, and present the sensitivity grid rather than a single averaged number.*

---

*Next up — **08 | LBO Analysis: Sources, Uses, and Returns**: how private equity buyers decide what they can afford to pay, and why debt makes their returns dance.*
