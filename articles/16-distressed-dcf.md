# 16 | Distressed DCF: Valuing a Company That Might Not Survive

*Every valuation method in this series so far has quietly assumed the company will still be around in ten years, arguing about its price. This article drops that assumption. When a company might not survive, the honest question is not "what are the cash flows?" but "what are the cash flows in each possible future — and how likely is each one?"*

> **Learning goals.** After this article you can: (1) explain why a standard DCF breaks down for a distressed company; (2) build a probability-weighted, scenario-based DCF; (3) reconcile that value to a going-concern DCF by showing exactly how much value distress destroys; (4) run the resulting enterprise value through a recovery waterfall; and (5) read a distressed bond price as a rough market estimate of default probability.
>
> **Prerequisites.** Articles 03 (enterprise value versus equity value), 06–07 (DCF and terminal value), and 13 (restructuring and the recovery waterfall). If you have not read 13 yet, read it first — this article is its valuation companion.

## 1. Why the Ordinary DCF Breaks in Distress

A standard DCF — the one we built in articles 06 and 07 — rests on three quiet assumptions. For a healthy company they are harmless. For a distressed company each one fails, and each failure pushes the answer in a different direction, which is why a naive DCF on a troubled company can be wrong by hundreds of millions without any arithmetic error.

**Assumption one: the company is a going concern.** A DCF discounts cash flows into the indefinite future and then adds a terminal value, which is usually the largest single number in the whole model. That is a bet that the company survives long enough to reach stable growth. A company with a maturity wall next year, a drawn revolver, and suppliers demanding cash on delivery may not get there. If it does not, the terminal value is not merely uncertain — it is zero in the liquidation branch of the world, and the model has no branch for that world.

**Assumption two: the discount rate is stable and knowable.** The weighted average cost of capital, or WACC, blends the cost of equity and the after-tax cost of debt according to the company's capital structure. In distress, every input wobbles. The cost of debt is no longer a yield on a healthy bond; it is a distressed yield that already embeds a large probability of default. The cost of equity, usually estimated with the capital asset pricing model (CAPM — the idea that a stock's expected return rises with its sensitivity to the market, its beta), becomes unreliable because beta for a near-bankrupt stock is noisy, leverage is extreme, and the market value of equity — the weight in the WACC — is collapsing as you watch. Worst of all, if you raise the discount rate to reflect distress *and* you also haircut the cash flows for distress, you count the same risk twice. We will come back to this trap, because it is the single most common error in distressed valuation.

**Assumption three: cash flows mean-revert to something sensible.** Healthy-company DCFs assume margins recover, working capital normalises, and capital expenditure settles into a maintenance rhythm. A distressed company often does the opposite: it sells assets to raise cash (so today's cash flow looks better than the business really is), stretches payables (so working capital looks like a source of cash right up until suppliers stop shipping), and cuts maintenance capital expenditure (so free cash flow is flattered while the asset base quietly rots). Projecting those flattered numbers forward as if they were sustainable is how a dying retailer gets valued like a healthy one.

None of this means DCF is useless in distress. It means a single-path DCF is the wrong tool. The fix is not a cleverer discount rate. The fix is to model more than one future.

## 2. The Fix: Value Scenarios, Not a Single Future

The core idea is disarmingly simple, and it is the same idea Aswath Damodaran develops for declining and distressed companies: value the company in each plausible future, then weight those values by how likely each future is.

```math
Expected\ Enterprise\ Value = \sum_{scenarios} (Probability_i \times Value_i)
```

In practice, three scenarios are usually enough to be honest without pretending to a precision nobody has:

1. **Survival as a going concern.** The company fixes its balance sheet — a refinancing, an out-of-court workout, a debt-for-equity swap — and keeps operating. Value it with a normal DCF, but a DCF *conditional on survival*: cash flows and a discount rate that describe the company if it makes it.
2. **Restructuring as a smaller company.** The company survives in some form but loses assets, contracts, or divisions along the way. Value it at what the slimmed-down business is worth — often estimated from asset sales, a sale of the business to a buyer, or a DCF of the smaller footprint.
3. **Liquidation.** The company does not survive. Value it at what the assets fetch in a forced sale, net of the costs of shutting down — usually much less than book value, because a fire sale is a buyer's market and intangible value like brand and customer relationships largely evaporates.

Two disciplines make this more than hand-waving. First, the probabilities must sum to 100%. Every percentage point you add to survival must come from somewhere else, which forces you to say what you actually believe. Second, each scenario value must be a *present* value, computed as of today. You do not discount the weighted average a second time — the discounting already happened inside each scenario's valuation. Weighting present values gives you a present expected value directly.

Where do the probabilities come from? There is no single right source, and a good banker triangulates:

- **Bond ratings and historical default rates.** Rating agencies publish how often bonds of each rating defaulted over various horizons. A CCC-rated issuer's historical default rate is a reasonable starting point — not a prediction, but a base rate that stops you from inventing a number from thin air.
- **Bond prices.** A bond trading at 60 cents on the dollar is the market's own recovery analysis, expressed as a price. Section 5 shows how to back out a rough default probability from that price.
- **Accounting distress models.** The Altman Z-score from article 13 sorts companies into safe, grey, and distress zones. It is a screening tool, not a probability machine, but a company deep in the distress zone should not be carrying a 90% survival probability in your model without a very good story.
- **The maturity schedule itself.** If $300 million comes due in nine months and the company has $40 million of liquidity, the survival probability is not an abstract statistical question — it is a refinancing question, and your probability should reflect your judgement about whether that refinancing happens.

A final warning before the numbers: do not double-count distress. If your discount rate already includes a large default premium, your cash flows should not also be probability-weighted for default, and vice versa. The clean approach in this article is to put the distress risk in the *probabilities and scenario values*, and to discount the survival scenario at a rate that reflects the risk of the surviving company — elevated, because a recently distressed survivor is still risky, but not a rate that also prices in the chance of death. Pick one place for the risk to live, and be able to say where it lives.

## 3. The Worked Example, Part 1: A Going-Concern DCF, Conditional on Survival

Meet Northfield Retail Group, a fictional mid-sized retailer. It has $550 million of debt (we will meet its tranches in section 5), declining sales, and a refinancing due in eighteen months. Management has a credible turnaround plan — close the worst stores, renegotiate leases, rebuild the brand — but only if the refinancing succeeds. Our job: what is this company worth today, given that it might not make it?

**Step one: the survival DCF.** Conditional on survival, we forecast unlevered free cash flow (UFCF — the cash the whole firm generates for all its capital providers, before interest payments, as defined in article 06) as follows, in $ millions: Year 1: 40; Year 2: 48; Year 3: 56; Year 4: 64; Year 5: 70. These are not heroic numbers — they assume the turnaround works slowly, not miraculously. We discount at 11%: higher than a healthy retailer's roughly 9%, reflecting the survivor's leverage and execution risk, but not a distressed yield, because we have deliberately put the risk of death in the probabilities instead.

```math
PV = \frac{40}{1.11} + \frac{48}{1.11^2} + \frac{56}{1.11^3} + \frac{64}{1.11^4} + \frac{70}{1.11^5}
```

| Year | UFCF ($m) | Discount factor at 11% | Present value ($m) |
|---:|---:|---:|---:|
| 1 | 40 | 0.9009 | 36.04 |
| 2 | 48 | 0.8116 | 38.96 |
| 3 | 56 | 0.7312 | 40.95 |
| 4 | 64 | 0.6587 | 42.16 |
| 5 | 70 | 0.5935 | 41.54 |
| **Total, Years 1–5** | | | **199.64** |

**Step two: the terminal value.** In Year 6, UFCF grows 2% to $71.4 million, and the terminal value — the value of all cash flows after Year 5, using the Gordon growth formula from article 07 — is:

```math
Terminal\ Value = \frac{71.4}{0.11 - 0.02} = \$793.3\ million
```

Discounted back five years at 11%, that is $793.3 × 0.5935 = $470.8 million. Add the two pieces:

```math
Going\text{-}concern\ Enterprise\ Value = 199.6 + 470.8 = \$670.4\ million
```

Pause on that number, because it contains a warning. The terminal value is $470.8 million of the $670.4 million total — about 70%. In a healthy-company DCF that is normal. Here it means 70% of the "survival" value depends on the company living long enough to reach stable growth — the very thing in doubt. A banker who reports $670 million for Northfield without that caveat is not lying, but is not telling the whole truth either. That $670 million is a *conditional* value: what the company is worth *if* it survives. The next step removes the condition.

## 4. Part 2: Probability-Weighting, and the Reconciliation That Proves It

Now assign the scenarios. Based on the maturity schedule, the bond price, and the Z-score zone, we judge: 55% survival as a going concern, 30% restructuring as a smaller company (valued at $210 million — roughly what the better stores and the brand would fetch from a buyer), and 15% liquidation (valued at $90 million — the fire-sale value of inventory, leases, and owned property, net of shutdown costs).

| Scenario | Probability | Scenario value ($m) | Contribution ($m) |
|---|---:|---:|---:|
| Survival (going concern) | 55% | 670.4 | 368.7 |
| Restructuring (smaller company) | 30% | 210.0 | 63.0 |
| Liquidation | 15% | 90.0 | 13.5 |
| **Expected enterprise value** | **100%** | | **445.3** |

The probability-weighted enterprise value is **$445 million**, not $670 million. The $225 million gap is not a fudge factor — it is the expected value that distress destroys, and it reconciles exactly:

```math
Expected\ loss = 0.30 \times (670.4 - 210.0) + 0.15 \times (670.4 - 90.0) = 138.1 + 87.1 = \$225.2\ million
```

In words: there is a 30% chance of losing $460 million of value relative to survival, and a 15% chance of losing $580 million. Expected loss: $225 million. Going-concern value ($670 million) minus expected loss ($225 million) equals expected value ($445 million). If your scenario model does not reconcile this way, something is wrong — usually a probability that does not sum to 100%, or a scenario value that was discounted twice.

**Sensitivity: the answer lives and dies on the survival probability.** If survival is 45% instead of 55% (with the other two scenarios scaled proportionally), expected value falls to about $395 million. If survival is 65%, it rises to about $495 million. Every 10 percentage points of survival probability is worth roughly $50 million here — because the gap between the survival value and the average bad outcome is about $500 million, and 10% of $500 million is $50 million. That is the single most useful sentence in this article for a negotiation: when someone argues about Northfield's value, they are almost always really arguing about the survival probability, even if they think they are arguing about the discount rate. Force the argument into the open by asking, "What survival probability does your price imply?" — and then ask what evidence supports it.

## 5. Part 3: The Waterfall, the Bond Market's Vote, and Equity as an Option

An enterprise value of $445 million is only half the story. Article 13 taught us that in distress, the slicing matters as much as the pie. Northfield's $550 million of debt is layered: $200 million secured (backed by specific assets), $250 million senior unsecured, and $100 million subordinated. Under absolute priority — the rule that senior claims are paid in full before junior claims receive anything — the waterfall at a $445.3 million enterprise value runs:

| Claim | Amount owed ($m) | Recovery ($m) | Recovery rate |
|---|---:|---:|---:|
| Secured debt | 200 | 200.0 | 100% |
| Senior unsecured debt | 250 | 245.3 | 98.1% |
| Subordinated debt | 100 | 0.0 | 0% |
| Equity | — | 0.0 | 0% |

Read that table like a restructuring banker. The secured lenders are whole. The senior unsecured lenders are nearly whole — they lose less than 2 cents on the dollar, which means they have little incentive to force a liquidation and every incentive to support a deal that preserves value. The subordinated lenders and the equity holders get nothing *in a liquidation at today's expected value*. That is why, in real restructurings, the fight is usually between the fulcrum security — the most senior class that is not fully covered, here arguably the senior unsecured holders, who will likely end up owning the reorganised company — and everyone below it. Gilson, John, and Lang (1990) found, in a sample of 169 distressed firms, that about half managed to restructure their debt privately, outside Chapter 11 — and that private workouts were more likely when firms had more intangible assets, owed more of their debt to banks, and faced fewer lenders. Fewer cooks, easier deal. Northfield, with a concentrated senior lender group, fits the profile of a company that might avoid court.

**The bond market's cross-check.** Suppose Northfield's senior unsecured bonds, face value $100, trade at $62. As a rough, back-of-the-envelope exercise, assume a recovery of $40 if the company defaults within the year, and ignore risk premiums and coupons. Then the price should equal the probability-weighted payoff:

```math
62 = (1 - p) \times 100 + p \times 40
```

Solving: $100 - 60p = 62$, so $p = 38 / 60 = 63.3\%$. That is a *risk-neutral* implied default probability — it bakes in investors' risk aversion, so it overstates the true statistical probability — and it assumes a one-year horizon and a guessed recovery. Treat it as a sanity check, not a measurement: if your model says survival is 55% (implying a 45% chance of some bad outcome) while the bond market implies a 63% one-year default probability, the market is more pessimistic than you are, and you owe an explanation for the gap. Maybe the market is pricing a liquidity crisis your scenario weights underplay. Maybe the recovery assumption is wrong. Either way, the disagreement is the interesting part.

**Why equity can still trade above zero.** The waterfall says equity gets nothing — so why does the stock of a company like Northfield still change hands at a positive price? Because equity in a levered, distressed company behaves like a call option on the firm's assets, with the strike price equal to the face value of the debt. If the asset value recovers above $550 million before the debt matures, equity holders capture the upside; if it does not, their loss is capped at what they already paid, because limited liability means they cannot lose more than their investment. The waterfall values the company *today*, at one point in time. The stock price values the *chance* that tomorrow is better. Both can be right at once — and a banker who tells you the equity is "worthless because the waterfall says so" is confusing a liquidation snapshot with an option on the future. The option value is usually small when distress is deep, but it is not zero, and it explains why distressed equities can rally violently on good news: a small rise in asset value, or a fall in uncertainty, can multiply a small option value many times over.

## 6. What Happens to the Other Methods in Distress?

A distressed company breaks the other valuation tools too, and knowing how is part of the job:

- **Trading multiples (article 04)** mislead twice over. Earnings-based multiples are meaningless when earnings are negative, and enterprise-value-to-sales multiples from healthy peers ignore the distress discount entirely. If you must use multiples, use distressed peers — companies in the same trouble — or adjust the healthy-peer multiple explicitly for the probability of distress, exactly as in section 2. Damodaran's work on distressed companies makes this adjustment the centrepiece, not a footnote.
- **Precedent transactions (article 05)** need a distress filter. A healthy-company takeover premium is the wrong benchmark for a forced sale; distressed asset sales transact at discounts, not premiums, and the "precedents" that matter are other fire sales and 363 sales (asset sales inside Chapter 11), not strategic mergers.
- **LBO analysis (article 08)** usually stops working altogether. An LBO buyer needs new debt, and nobody lends new debt to a company that cannot service its old debt — unless the buyer is buying the debt itself, at a discount, which is a different trade (distressed-debt investing) with a different return calculation.
- **Sum-of-the-parts (article 15)** becomes *more* useful, not less. When the whole is worth less than the market thinks, valuing each division or asset separately — and asking which pieces a buyer would actually pay for — is often the fastest route to a credible restructuring or liquidation value. That is why the $210 million restructuring scenario in our example was framed as "what a buyer pays for the good pieces," not as a DCF of a shrunken company nobody has modelled.

The through-line: in distress, every method needs a scenario adjustment, a distressed peer set, or both. A valuation that does not mention distress explicitly is not a valuation of a distressed company — it is a valuation of a different, healthier company that happens to share its name.

---

## Common Misconceptions

- **"Just raise the discount rate to reflect distress."** A higher discount rate is a blunt instrument: it shrinks near-term and distant cash flows alike, it hides the actual judgement (how likely is default?) inside an opaque number, and it invites double-counting if you also haircut the cash flows. Put distress in the scenarios and probabilities, where it can be argued about, and keep the discount rate for the risk of the surviving company.
- **"A negative equity value means the equity is worthless and the model is broken."** A DCF that subtracts $550 million of debt from a $445 million enterprise value gives equity of negative $105 million — but equity cannot be worth less than zero, because of limited liability. The negative number is not a valuation; it is a diagnostic. It tells you the equity's value, if any, comes entirely from optionality (section 5), not from the current asset value covering the debt.
- **"The bond price tells you the true default probability."** It tells you a risk-neutral probability under assumed recovery, horizon, and coupons. Change the assumed recovery from $40 to $55 and the implied probability in our example falls from 63% to 44%. The bond price is evidence, not a measurement — use it to challenge your probabilities, not to replace them.
- **"Distressed valuation is just pessimistic valuation."** It is *branching* valuation. The survival branch in our example is genuinely optimistic — $670 million, with a full turnaround. The discipline is not pessimism; it is refusing to present the optimistic branch as if it were the only branch.
- **"If the company files Chapter 11, the analysis is over."** Chapter 11 is usually the middle of the story, not the end. The valuation questions — what is the reorganised company worth, who is the fulcrum security, what does the new capital structure look like — are exactly the questions this article trains you to ask, with the court as an additional (and slow) negotiating party.

## Test Yourself

**Q1.** A distressed company has a going-concern value of $800 million, a 40% chance of restructuring at $300 million, and a 10% chance of liquidation at $100 million. What is its probability-weighted enterprise value, and what survival probability is implied? (Assume the three scenarios exhaust the possibilities.)
*A1. Survival probability = 100% − 40% − 10% = 50%. Expected value = 0.50 × 800 + 0.40 × 300 + 0.10 × 100 = 400 + 120 + 10 = $530 million.*

**Q2.** In the Northfield example, why is it wrong to discount the survival cash flows at a distressed yield of, say, 20%, and then also probability-weight the result with a 55% survival chance?
*A2. Because the 20% yield already charges for the risk of default — investors demand it precisely because the company might not pay. Probability-weighting then charges for the same risk a second time, understating value. Put the distress risk in one place: here, the probabilities.*

**Q3.** Northfield's expected enterprise value is $445.3 million and its secured debt is $200 million, senior unsecured $250 million, subordinated $100 million. A new appraisal argues the liquidation value should be $140 million, not $90 million, with all other inputs unchanged. What is the new expected enterprise value, and who benefits?
*A3. New expected value = 368.7 + 63.0 + 0.15 × 140 = 368.7 + 63.0 + 21.0 = $452.7 million. The waterfall now pays secured $200 million in full, senior unsecured $250 million in full (252.7 available after secured), and subordinated lenders $2.7 million — a 2.7% recovery instead of zero. Equity still gets nothing. Small changes at the bottom of the waterfall only help the fulcrum and below.*

**Q4.** A distressed bond with face value $100 trades at $70. Assuming a recovery of $50 on default, a one-year horizon, and no coupons or risk premium, what default probability does the price imply? Why should you distrust that number as a statistical forecast?
*A4. 70 = (1 − p) × 100 + p × 50, so 100 − 50p = 70, giving p = 60%. Distrust it as a forecast because it is risk-neutral (it includes investors' risk aversion), it depends entirely on the assumed $50 recovery, and it ignores coupons, maturity, and the possibility of a restructuring that is neither full payment nor the assumed recovery.*

## Further reading

- Damodaran, A. (2009). *Valuing Declining and Distressed Companies.* SSRN. — The scenario-weighting framework used in this article, including how to estimate distress probabilities from ratings, bond prices, and statistical models.
- Gilson, S. C., John, K., & Lang, L. H. P. (1990). *Troubled Debt Restructurings: An Empirical Study of Private Reorganization of Firms in Default.* Journal of Financial Economics, 27, 315–353. — When private workouts succeed, and why fewer lenders and more bank debt help.
- Altman, E. I. (1968). *Financial Ratios, Discriminant Analysis and the Prediction of Corporate Bankruptcy.* Journal of Finance, 23, 589–609. — The original Z-score model, introduced in article 13 and used here as a probability input.

Next up: 13F Filings and Activist Investing: Reading What the Smart Money Owns
