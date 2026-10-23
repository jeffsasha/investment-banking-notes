# 13 | Restructuring 101: Distress and Chapter 11

*Every valuation method in this series assumed a healthy company arguing about its price. This article is about what happens when the argument changes to a simpler, harsher question: the company can't pay its debts — so who gets paid, and in what order?*

> **Learning goals.** After this article you can: (1) distinguish financial from economic distress (and insolvency from illiquidity); (2) read the early-warning signs — liquidity, covenants, maturities, and the Altman Z-score; (3) explain what happens inside a Chapter 11 case from petition to plan confirmation; (4) run a recovery waterfall — the restructuring banker's core calculation — and see why the valuation math "inverts" in distress.
>
> **Prerequisites.** Articles 01–12, especially the DCF (06–07) and the merger math (09). Restructuring reuses every tool we've built, but pointed in the opposite direction.

## 1. The Question Changes

Everything so far answered one question: what is the company worth? Restructuring answers a different one: **there isn't enough money to go around — so who gets paid first?**

This is why restructuring bankers describe their job as "valuation in reverse." In a healthy M&A deal, the equity value is the headline number and debt is a subtraction (articles 03, 06). In distress, the enterprise value is a *fixed pie*, and the analyst's real job is slicing it: debt tranche by debt tranche, from the top of the capital structure down, until the pie runs out. Everyone below the cut line gets zero. The valuation (how big is the pie) still matters enormously — it determines exactly where the cut line falls — but the drama is in the slicing.

Two distinctions matter before anything else.

**Illiquidity vs. insolvency.** *Illiquidity* means you can't pay *today*: cash is short, a maturity is coming, the revolver is drawn to the max. *Insolvency* means you can't pay *ever, in full*: liabilities exceed assets (balance-sheet insolvency) or you cannot meet obligations as they come due (cash-flow insolvency). Illiquidity is often fixable with bridge financing. Insolvency requires someone to take a loss — and the entire restructuring business is about deciding who.

**Financial vs. economic distress.** *Financial distress* = the business works, the balance sheet doesn't. Cash flows are positive but debt service eats everything; fix the capital structure and the company lives. *Economic distress* = the business itself is broken: declining demand, obsolete product, costs that can't be cut. No amount of debt forgiveness saves a company nobody wants to buy from. Andrade and Kaplan (1998) studied highly-leveraged 1980s buyouts that became distressed and found that when distress was purely financial — the operations were sound — the *cost of the distress itself* was 10–20% of firm value: real money, but the underlying value was mostly preserved. That's an empirical finding, not a law of nature, but it frames the banker's first diagnostic: is this a balance-sheet problem or a business problem? The answer determines whether you restructure the debt or sell the assets.

## 2. How Companies Get Into Trouble: The Early Warnings

Companies rarely collapse overnight. The signals pile up in a predictable order:

1. **Liquidity erosion.** Cash balances shrink, the revolving credit facility (revolver) gets drawn down, payables stretch. Bankers watch the *liquidity runway*: cash plus available revolver, divided by monthly cash burn. Under 6–9 months of runway with a maturity inside it, the CFO is already calling bankers.
2. **Covenant breaches.** Leveraged loans and bonds carry covenants — promises like "leverage must stay below 5.0×" or "interest coverage above 2.5×." Breach one and the lenders can accelerate the debt (demand it all *now*). Companies then beg for *waivers* or *amend-and-extend* deals: higher interest, tighter terms, in exchange for more time.
3. **Maturity walls.** Debt that all comes due in the same year. A healthy company refinances; a distressed one finds the market closed to it, and each maturity becomes a cliff.
4. **Ratings downgrades and widening spreads.** The bond market prices distress long before the lawyers arrive. When a company's bonds trade at 60¢ on the dollar, the market is already doing recovery analysis — pricing its own guess about the waterfall in section 5.

The classic academic attempt to quantify all this is the **Altman Z-score** (Altman, 1968): a formula that combines five financial ratios into a single distress-prediction number, built with a statistical technique called *multiple discriminant analysis* (MDA — roughly, finding the weighted combination of ratios that best separated bankrupt from non-bankrupt firms in the data).

```math
Z = 1.2X_1 + 1.4X_2 + 3.3X_3 + 0.6X_4 + 1.0X_5
```

where $X_1$ = working capital / total assets, $X_2$ = retained earnings / total assets, $X_3$ = EBIT / total assets, $X_4$ = market value of equity / book value of total debt, and $X_5$ = sales / total assets. The cutoffs: $Z > 2.99$ is the "safe" zone, $Z < 1.81$ is the distress zone, and in between is the grey zone — where the model declines to judge. Altman reported roughly 90% accuracy one year before bankruptcy on his original sample of manufacturers; accuracy decays fast at longer horizons.

Worked example — fictional Meridian Packaging Corp.:

| Input | Computation | Ratio |
|---|---|---|
| Working capital: CA $180m − CL $150m = $30m; total assets $800m | $X_1 = 30/800$ | 0.0375 |
| Retained earnings $120m | $X_2 = 120/800$ | 0.1500 |
| EBIT $90m | $X_3 = 90/800$ | 0.1125 |
| Market cap $250m; total debt $500m | $X_4 = 250/500$ | 0.5000 |
| Sales $960m | $X_5 = 960/800$ | 1.2000 |

```math
Z = 1.2(0.0375) + 1.4(0.1500) + 3.3(0.1125) + 0.6(0.5000) + 1.0(1.2000)
  = 0.045 + 0.210 + 0.371 + 0.300 + 1.200 = 2.13
```

$Z = 2.13$: the grey zone, drifting toward trouble. Now fast-forward two bad quarters — EBIT halves to $45m, the market cap falls to $150m, retained earnings drop to $80m, sales slip to $900m, working capital compresses to $10m:

```math
Z = 1.2(0.0125) + 1.4(0.1000) + 3.3(0.0563) + 0.6(0.3000) + 1.0(1.1250)
  = 0.015 + 0.140 + 0.186 + 0.180 + 1.125 = 1.65
```

$Z = 1.65 < 1.81$: the distress zone. Nobody files for bankruptcy *because* a formula said so — but every restructuring banker has run this arithmetic, and a sub-1.81 score is when the phone calls start.

Caveats (the model is a flashlight, not a compass): it was built for *public manufacturing* firms — $X_4$ needs a market value of equity, so private companies use a revised variant (Altman later published a $Z'$ with book equity and different weights). The ratios are backward-looking; they miss fraud, sudden liquidity shocks, and off-balance-sheet risk. And the grey zone is wide on purpose: the model knows what it doesn't know.

## 3. The Three Doors: Work It Out, File Chapter 11, or Liquidate

Once distress is real, there are three doors:

**Door 1: Out-of-court restructuring.** The company negotiates directly with creditors — no judge, no public filing. Tools: covenant waivers, amend-and-extend (push maturities out, pay a higher rate), and *exchange offers* (swap old bonds for new ones with longer maturities or lower face value). Some exchanges are *coercive*: accept the new bonds, or get left holding stripped old bonds after *exit consents* remove the old bonds' protections. Out-of-court is cheaper and quieter, but it needs near-unanimous creditor cooperation — one holdout can block it. That's why the *threat* of Door 2 is what makes Door 1 work.

**Door 2: Chapter 11 reorganization.** The company files a bankruptcy petition and keeps operating while it negotiates a *plan of reorganization*. This is the restructuring banker's home turf — section 4 walks through it.

**Door 3: Chapter 7 liquidation.** A trustee shuts the company down and sells everything, distributing proceeds by priority. (Chapter 13 is the personal-bankruptcy equivalent for individuals — not our world; Chapter 15 handles cross-border cases.) Chapter 7 is the "give up" option, and it's what everyone threatens everyone else with: creditors usually get *less* in liquidation than in reorganization, which is exactly why the threat of Chapter 7 makes Chapter 11 negotiations work. Notice the pattern: each door's credibility comes from the door behind it.

## 4. Inside a Chapter 11: The Machinery

A Chapter 11 case runs on a script. The script is legal, but every step has a financial logic — and a banker is usually standing next to the lawyers at each one.

**The petition and the automatic stay.** Filing the petition triggers the *automatic stay* (Bankruptcy Code §362): creditors must stop collecting — no lawsuits, no seizing collateral, no calling the loan. The stay is what buys the company breathing room. Without it, the fastest creditor would grab the assets and the reorganization would be over before it started.

**First-day motions.** On day one, the company asks the judge for permission to keep the lights on: pay employees, honor customer programs, use *cash collateral* (cash that's technically the lenders' collateral), and — critically — approve **DIP financing**. *DIP* = debtor-in-possession: new loans made *after* the filing, which get *super-priority* — they jump ahead of almost all pre-existing debt. DIP lenders are usually the existing lenders; DIP isn't charity, it's the safest loan in the building, and it's how the company funds itself during the case.

**Exclusivity.** The debtor gets an exclusive window (initially 120 days, extendable up to 18 months) to propose its reorganization plan. Creditors can negotiate against it, but only the debtor can *file* one during exclusivity. This is leverage: the debtor controls the draft, and everyone else reacts.

**The plan, the disclosure statement, and voting.** The *plan of reorganization* says who gets what: which debt is reinstated, which is converted to equity, which is wiped out. Creditors vote by *class* (grouped by similar claims). A class is *impaired* if the plan changes its legal rights — impaired classes get to vote. A class accepts if creditors holding **at least 2/3 in dollar amount** *and* **more than 1/2 in number** of those voting say yes. Then the judge *confirms* the plan.

**Cramdown.** If a class votes no, the judge can still confirm the plan over its objection — *cram down* the dissenters — if the plan is "fair and equitable" toward that class and "does not discriminate unfairly." In practice, "fair and equitable" means the **absolute priority rule** (next section) is respected for the dissenting class: senior classes must be paid in full before junior classes get anything. Cramdown is the nuclear option that makes everyone negotiate seriously: holdouts know they can be overridden, but only if the plan truly respects priority — so the debtor can't use cramdown to steal from seniors either.

**Section 363 sales.** Instead of reorganizing, the company can sell assets (or itself) *free and clear* of liens and claims, through a court-supervised auction with a *stalking-horse* bidder setting the floor price. Many "reorganizations" are really 363 sales in disguise: the assets get a clean title, the buyer gets a fresh company, and the old creditors split the sale proceeds by priority. When you read that a bankrupt retailer "was bought out of bankruptcy," this is usually what happened.

## 5. Who Gets Paid First: Absolute Priority and the Recovery Waterfall

The **absolute priority rule (APR)** is the constitution of distressed finance: **each class of claims must be paid in full before any junior class receives anything.** The order, top to bottom:

1. **Administrative claims** — the costs of the bankruptcy itself: lawyers, bankers, professional fees. (Yes, the advisors get paid first. Everyone in the room notices this.)
2. **DIP financing** — super-priority, as discussed.
3. **Secured debt** — paid from its collateral. If the collateral covers the claim, paid in full; any shortfall becomes a *deficiency claim* that drops down to the unsecured pool.
4. **Unsecured debt** — bonds, trade claims, the deficiency scraps from above. Paid pro rata from whatever's left.
5. **Old equity** — last. Usually zero.

The banker's core deliverable is the **recovery analysis**: estimate the reorganized enterprise value (using the DCF, comps, and precedent tools from articles 04–07 — this is where they all come back), then run it down the waterfall and compute each class's recovery in *cents on the dollar*.

Worked example — Meridian Packaging files, and the bankers conclude the reorganized enterprise value is **$420m** (their DCF said $410m, comps said $430m; the football field from article 10 narrows to a point when the pie must actually be sliced). The capital structure:

| Priority | Claim | Amount |
|---|---|---|
| 1. Administrative / professional fees | advisors, lawyers | $15m |
| 2. DIP loan | post-petition financing | $40m |
| 3. First-lien secured debt | fully covered by collateral | $300m |
| 4. Unsecured notes | — | $250m |
| 5. Old equity | — | (whatever's left) |

Now the waterfall — $420m of value, paid top-down:

| Step | Action | Paid | Remaining value |
|---|---|---|---|
| 1 | Admin fees paid in full | $15m | $405m |
| 2 | DIP paid in full (super-priority) | $40m | $365m |
| 3 | First lien paid in full (collateral covers it) | $300m | $65m |
| 4 | Unsecured notes share the $65m pro rata: $65m / $250m | **26¢ on the dollar** | $0m |
| 5 | Old equity | **$0** | — |

The unsecured bondholders — who lent $250m — recover 26%. The equity holders, who owned the company yesterday, get nothing. And notice the knife's edge: if the bankers' EV estimate had been $500m instead of $420m, the unsecured recovery would be $(500-355)/250 = 58$¢. **An $80m disagreement about enterprise value moves the bond recovery by 32 points.** This is why valuation fights are the actual war in bankruptcy court, and why every tool in this series gets reused here — now with the math pointed at the cut line instead of the headline price.

One more subtlety: the unsecured class won't just accept 26¢ quietly. They'll argue the EV is really $500m. The first-lien lenders will argue it's $380m (they're paid in full either way — they want the case *over*). The negotiation, the expert reports, the dueling DCFs — that *is* the restructuring business. And occasionally the seniors *gift* a small recovery to old equity (a few cents) to buy their votes and avoid a cramdown fight — a negotiated exception to absolute priority, not a violation of it.

## 6. What the Restructuring Banker Actually Does

Restructuring bankers get hired by *both* sides — the debtor (the company) or a creditor group (often the bondholders). The work is the same toolkit as the rest of investment banking, plus three distress specialties:

- **The 13-week cash flow.** A week-by-week liquidity forecast for the next quarter. In distress, cash is measured in weeks, not years — this model decides whether the company survives to the next milestone, and DIP lenders live by it.
- **The recovery analysis.** Section 5's waterfall, run across scenarios: what if EV is $380m? $460m? Each class's recovery under each scenario becomes the negotiation map.
- **Negotiating the RSA.** The *restructuring support agreement*: a contract where key creditors agree to support a specific plan before it's filed. Get enough signatures and the Chapter 11 becomes a *prepackaged* bankruptcy — in and out of court in weeks instead of months. The banker's job is assembling that coalition.

Fees are the industry's worst-kept secret: restructuring bankers often charge monthly retainers *plus* a success fee on emergence — and remember, they're administrative claims, paid first. Distress is one of the few businesses that gets *busier* in a recession, which is why every bulge-bracket bank keeps a restructuring group even though the work is famously unglamorous.

## 7. Common Misconceptions

**"Chapter 11 means the company is going out of business."** That's Chapter 7 (liquidation). Chapter 11 is *reorganization* — the company keeps operating while its debts are restructured. Most large bankruptcies you read about (airlines, retailers, energy companies) are Chapter 11; the business survives, the *capital structure* doesn't. Confusing the two is the single most common error in casual discussion of bankruptcy.

**"Shareholders always get wiped out, no exceptions."** *Almost* always — the waterfall says so, and old equity is last. But "gifting" happens: senior classes sometimes let a sliver of value flow to old equity to secure their votes and avoid a cramdown battle. It's a negotiated price for cooperation, paid out of the seniors' own recovery — not a right of the shareholders. Don't confuse the exception with the rule, and don't buy the bonds of a bankrupt company expecting equity-like upside.

**"Bankruptcy destroys the company's value."** It destroys *some* value — Andrade and Kaplan (1998) put the cost of financial distress at 10–20% of firm value: lawyers, lost customers, suppliers demanding cash up front, managers distracted by the case instead of the business. But that's the cost of the *process*, and it applies when the underlying business is sound. When the business itself is broken (economic distress), the value was already gone before the filing. Blaming the bankruptcy for the loss is blaming the autopsy for the death.

**"DIP lenders are doing the company a favor."** DIP is the *safest* loan in the capital structure — super-priority, short duration, often made by the existing lenders protecting their own position (sometimes via "roll-ups" that elevate their old loans to DIP status). It's good business for the lender, not charity. The favor runs the other way: without DIP, there is no reorganization.

**"Creditors always get paid before shareholders — it's the law."** Absolute priority is the *default* rule, and a judge enforcing a cramdown must respect it. But a plan that *every* impaired class votes for can deviate from strict priority — the rule binds dissenters, not consenters. That's the opening that makes negotiated plans possible, and the reason "fair and equitable" has generated a century of litigation over what, exactly, "full payment" means (cash? new notes? equity in the reorganized company?).

## 8. Test Yourself

**Q1.** A bankrupt company emerges with a reorganized EV of $600m. Claims: $120m first-lien secured debt (collateral value $200m), $500m unsecured bonds, plus $20m in administrative/professional fees and no DIP. Run the waterfall: what does each class recover?

*A1. Admin fees first: $600m − $20m = $580m left. First lien: collateral ($200m) covers the $120m claim, so it's paid in full — $460m left. Unsecured bonds split $460m pro rata: $460m/$500m = 92¢ on the dollar. Old equity: $0. Note how close the unsecured class came to par — at this EV, the fight in court would be about whether EV is really $600m or $540m, because $540m − $140m = $400m → 80¢. Every $10m of EV is 2 points of bond recovery.*

**Q2.** A company's Z-score is 1.5. What does the model say, and what are three reasons a banker wouldn't rely on it alone?

*A2. 1.5 < 1.81: the distress zone — the model flags serious bankruptcy risk. But: (1) it was built for public manufacturing firms, and $X_4$ needs a market value of equity — private or service companies need the revised variant; (2) the ratios are backward-looking — they miss fraud, sudden liquidity shocks, and off-balance-sheet liabilities; (3) the wide grey zone (1.81–2.99) shows the model's own uncertainty — a score of 1.5 is a warning light, not a diagnosis. Bankers pair it with the 13-week cash flow, covenant headroom, and the maturity schedule.*

**Q3.** Why would senior creditors ever agree to give *old equity* a recovery in a plan, when absolute priority says equity gets nothing until seniors are paid in full?

*A3. Votes and speed. Old equity's cooperation — voting yes — can deliver the accepting classes needed to confirm a plan consensually, avoiding the cost, delay, and litigation risk of a cramdown fight. The seniors "gift" a small recovery as the price of that cooperation. It's rational: a few cents to equity that buys a fast, uncontested emergence is cheaper than months of professional fees and uncertainty. The key: the gift comes from the seniors' own recovery, by agreement — it's not equity taking value ahead of anyone.*

**Q4.** Two companies each miss a bond payment. Company A has growing revenue and 25% EBITDA margins but 7× leverage from a buyout. Company B has shrinking revenue, 5% margins, and 2× leverage. Which one is a candidate for balance-sheet restructuring, and which one probably needs to sell assets — and why?

*A4. Company A: financial distress — the business works (growing, profitable), the capital structure doesn't (7× leverage). This is the classic restructuring candidate: fix the balance sheet (debt-for-equity swap, maturity extension) and the company lives — exactly the Andrade & Kaplan (1998) situation, where operations were sound. Company B: economic distress — the business itself is deteriorating; 2× leverage is modest, so the problem isn't the debt, it's the demand. No restructuring of claims fixes shrinking revenue; the answer is an operational turnaround or asset sales (possibly via a 363 sale). The banker's first diagnostic — financial vs. economic distress — points each company at a different door.*

---

*Next up — **14 | Frontier: Recent Research on M&A and Valuation**: what the papers actually say about premiums, returns, and AI in banking.*

**Papers cited in this article** (all verified before writing — title, authors, year, journal):
- Altman, E. I. (1968). *Financial Ratios, Discriminant Analysis and the Prediction of Corporate Bankruptcy.* Journal of Finance, 23, 589–609. — The Z-score: five ratios, one distress number; roughly 90% one-year-ahead accuracy on the original manufacturing sample.
- Andrade, G. & Kaplan, S. N. (1998). *How Costly Is Financial (Not Economic) Distress? Evidence from Highly Leveraged Transactions That Became Distressed.* Journal of Finance, 53, 1443–1494. — When the business is sound, the distress *process* costs 10–20% of firm value; the financial/economic distinction that frames every restructuring diagnosis.
