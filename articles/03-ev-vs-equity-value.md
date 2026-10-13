# 03 | Enterprise Value vs Equity Value: The Bridge

*Ask anyone on the street what a company is worth and they'll quote the share price times the share count. Ask a banker and you'll get a different number — bigger, stranger, and more honest. This article is about why.*

> **Learning goals.** After this article you can: (1) define enterprise value and equity value and explain what each one is the value *of*; (2) build the bridge between them, component by component; (3) run a treasury-stock-method dilution calculation for options; (4) explain why valuation multiples must use enterprise value for EBITDA and equity value for net income; (5) run the bridge in reverse, from an enterprise value down to a per-share price.
>
> **Prerequisites.** Article 02 (how the three statements connect, what EBITDA approximates). Comfort with basic algebra.

## 1. Why Market Cap Answers the Wrong Question

**Market capitalization** — share price × shares outstanding — is the value of the *equity*, i.e., what the shareholders' slice is worth. It is not the value of the *company*.

Here's the intuition. Imagine you buy a house for $500,000, and it comes with a $300,000 mortgage you have to take on. How much did the house cost you? One answer: $500,000 — that's what you paid the seller. Another answer: the house itself, as an asset, is what you're really acquiring, and its value doesn't depend on how the seller happened to finance it. If the seller had owned it free and clear, you'd have paid $500,000 for $500,000 of house. If the seller had borrowed $490,000 against it, you'd still be getting $500,000 of house — just with a lot more debt attached.

Companies work the same way. When a buyer acquires a company, it pays the shareholders the **equity value** — but it *inherits the debt*. The lenders don't go away; someone still owes them. So the value of the whole operating asset, independent of how it happens to be financed today, is a different number: the **enterprise value (EV)**.

This distinction is the single most-used idea in valuation. DCF models produce enterprise value. Comparable-company multiples like EV/EBITDA are expressed in enterprise value. Deal prices get quoted in enterprise value. Every valuation road in this series crosses this bridge, in both directions.

The formal relationship, in its short form:

```math
\text{Enterprise Value} = \text{Equity Value} + \text{Total Debt} - \text{Cash \& Equivalents}
```

That one line is the bridge. The rest of this article is understanding *why each piece is there*, so you never apply it mechanically.

## 2. The Bridge, Component by Component

First, definitions, because bankers are sloppy with these words in conversation and precise about them in models:

- **Equity value** (sometimes just "equity") = the value belonging to common shareholders. What market cap measures.
- **Enterprise value** = the value of the firm's *operating assets* — the business itself — available to *all* capital providers: shareholders, lenders, and anyone else with a senior claim.

The full bridge used in practice:

```math
EV = \text{Equity Value} + \text{Debt} + \text{Noncontrolling Interest} + \text{Preferred Stock} - \text{Cash}
```

Each component, with the reason it sits where it does:

| Component | What it is | Why it's added (+) or subtracted (−) |
|---|---|---|
| **+ Total debt** (loans, bonds, drawn revolvers) | Money the company owes lenders | A buyer inherits it — it's part of what the whole asset "costs" to own. Debt holders have a claim on the operating asset, so their claim belongs inside EV. |
| **+ Noncontrolling (minority) interest** | The portion of consolidated subsidiaries owned by *other* investors | EBITDA (the usual EV denominator) includes 100% of a subsidiary's earnings, so EV must include 100% of its value — including the slice that belongs to minority holders. |
| **+ Preferred stock** | A hybrid security, senior to common equity | Preferred holders get paid before common shareholders, like lenders. Their claim sits above equity, so it belongs inside EV. |
| **− Cash & equivalents** | Cash the company holds | A buyer can use the target's own cash to repay the target's debt the day after closing — so cash *offsets* the debt the buyer inherits. Subtracting it keeps EV focused on the operating asset, not the treasury balance. |

The cash subtraction deserves a pause, because it confuses everyone the first time. Subtracting cash does *not* mean cash is worthless or that the buyer gets it for free. It means this: suppose two identical businesses, one holding $100m of cash and one holding none. The cash-rich one has $100m *more* equity value (its shareholders own that cash). But its EV is the *same* — because EV = equity + debt − cash, and the extra $100m of equity is exactly cancelled by the extra $100m subtracted. The operating asset didn't change; only where the value sits changed. Hold that thought — it becomes the most important insight of this article (Section 8).

A note on language you'll hear on desks: "net debt" = total debt − cash. So the short bridge is often written as **EV = Equity Value + Net Debt**. Same thing, fewer words.

## 3. Worked Example: Northgate Foods

Let's run a complete bridge on a fictional company, Northgate Foods, a regional packaged-foods business. Every number below is invented; the mechanics are exactly what you'd do on a real one.

**Step 1 — Equity value, fully diluted.**

The share price is $45.00 and there are 20.0 million basic shares outstanding. But there are also 1.2 million employee stock options outstanding, all in the money, with a weighted-average exercise price of $30.00. If those options get exercised, new shares appear — so equity value should count them. The standard method is the **treasury stock method (TSM)**:

- Option holders pay the company to exercise: proceeds = $1.2\text{m} \times \$30.00 = \$36.0\text{m}$
- The company uses that cash to buy back its own shares at the market price: shares repurchased = $\$36.0\text{m} / \$45.00 = 0.8\text{m}$
- Net new shares = $1.2\text{m} - 0.8\text{m} = 0.4\text{m}$

(The intuition: the option holders bring $36m of cash *into* the company when they exercise, which offsets part of the dilution — you don't just add all 1.2m shares.)

```math
\text{Fully diluted shares} = 20.0\text{m} + 0.4\text{m} = 20.4\text{m}
```

```math
\text{Equity Value} = 20.4\text{m} \times \$45.00 = \$918.0\text{m}
```

Note what just happened: market cap (basic) would have been $900.0m, but equity value is $918.0m. **Equity value ≥ market cap** whenever there are dilutive securities outstanding. On a real deal, you'd also fold in RSUs and convertible notes; the principle is the same — count every claim that converts into common shares.

**Step 2 — The bridge.**

Northgate's balance sheet shows:

| Item | $m |
|---|---|
| Term loan | 320.0 |
| Revolver drawn | 60.0 |
| Senior bonds | 180.0 |
| **Total debt** | **560.0** |
| Noncontrolling interest | 40.0 |
| Preferred stock | 25.0 |
| Cash & equivalents (unrestricted) | 95.0 |

```math
\begin{align}
EV &= 918.0 + 560.0 + 40.0 + 25.0 - 95.0 \\
   &= \$1{,}448.0\text{m}
\end{align}
```

So: the shareholders' slice is worth $918m, but the whole business — the asset a buyer is actually acquiring — is valued at **$1,448m**. The $530m difference is the debt and senior claims the buyer inherits, net of the cash it can use against them.

**Step 3 — Sanity check with multiples.**

Northgate's LTM EBITDA is $190.0m and its LTM net income is $110.0m:

```math
EV/EBITDA = 1{,}448.0 / 190.0 = 7.6\times
```

```math
P/E = 918.0 / 110.0 = 8.3\times
```

Both multiples are reasonable for a stable food business — nothing in the bridge produced an absurd result, which is always worth checking. (A bridge that implies 25× EBITDA for a commodity food company means you mis-added something.)

## 4. Why EV Owns the Multiples: The Matching Principle

Here is the rule that governs every valuation multiple you'll ever build:

> **The numerator's claimants must match the denominator's claimants.**

EBITDA — earnings *before interest* — is the cash the operating asset generates for **all** capital providers: lenders get paid their interest out of it, shareholders get what's left. So the numerator must be the value of the claim *all* of them hold together: enterprise value. That's why the multiple is **EV/EBITDA**, never "Price/EBITDA."

Net income, by contrast, is what's left *after* interest — it belongs to shareholders alone. So the numerator is the shareholders' value: **P/E**, price over earnings. Same logic: **EV/Revenue** (revenue belongs to the whole firm, before anyone gets paid) and **EV/EBIT**.

This is why the bridge matters mechanically, not just philosophically. When you pull a "5.0× EBITDA" multiple from comparable companies in Article 04, that 5.0× is multiplying into an *enterprise* value. To get from there to what the shares are worth — the number anyone actually pays — you must run the bridge in reverse: subtract net debt, minority interest, and preferred, then divide by diluted shares. Skip the bridge and you've valued the wrong thing.

One more consequence: because EV includes debt, **EV multiples are comparable across companies with different capital structures**, while equity multiples are not. Two identical businesses, one debt-free and one heavily levered, have the same EV/EBITDA but wildly different P/E ratios — the levered one's equity is a smaller, riskier slice, so its P/E looks "cheaper" or "richer" for reasons that have nothing to do with the business. Bankers prefer EV multiples precisely because they strip out financing noise. (This is also why LBO analysis in Article 08 lives or dies on getting EV right.)

## 5. Running the Bridge in Reverse

In practice you'll cross the bridge both ways:

- **Equity → EV** (this section's example): you observe a share price and need the whole-firm value — the starting point for comps.
- **EV → Equity**: your DCF or your comps output gives you an *enterprise* value, and you need the per-share price — the number that goes in the pitch book.

Let's do the reverse on Northgate. Suppose your DCF says the enterprise is worth $1,448.0m:

```math
\begin{align}
\text{Equity Value} &= EV - \text{Net Debt} - \text{NCI} - \text{Preferred} \\
&= 1{,}448.0 - (560.0 - 95.0) - 40.0 - 25.0 \\
&= 1{,}448.0 - 465.0 - 65.0 \\
&= \$918.0\text{m}
\end{align}
```

```math
\text{Value per share} = 918.0 / 20.4 = \$45.00
```

It round-trips exactly to the market price — as it should, since we built the example from it. On a real valuation the DCF-implied EV won't equal the market-implied EV, and the gap between the implied per-share value and the actual share price is the entire point of the exercise: that's your upside (or downside).

Watch the share count on the reverse trip: always divide by **fully diluted** shares. Dividing an equity value that already reflects option dilution by *basic* shares double-counts the dilution benefit and overstates the per-share value. It's one of the most common junior errors, and it always flatters the valuation — which is exactly why you should be suspicious when you see it.

## 6. The Extended Bridge: What Else Gets Added

The four-component bridge covers most situations. The extended version adds the debt-like items that show up on real balance sheets:

| Item | Treatment | Why |
|---|---|---|
| **Operating lease liabilities** | Add to debt | A lease is a financing obligation in disguise — the company must pay it like debt. (Under ASC 842 / IFRS 16 these sit on the balance sheet; add the liability.) |
| **Pension / OPEB deficit** | Add to debt | An underfunded pension is money the company owes its retirees — a senior, debt-like claim. Add the *deficit* (liability minus plan assets), not the gross liability. |
| **Convertible notes** | Judgment call | Split treatment is common: the straight-debt portion in debt, the conversion option in diluted shares. In quick math, many bankers put the full face value in debt *and* include converts in dilution — pick one lane and be consistent. |
| **Restricted cash** | Do **not** subtract | If the cash is pledged as collateral or trapped offshore with real repatriation cost, the buyer can't freely use it to repay debt. Only subtract cash that's actually available. |
| **Deferred compensation / minority puts** | Add | Anything the company is contractually obliged to pay out behaves like debt. |

In our Northgate example these were immaterial, so the short bridge was the right tool. The extended bridge earns its keep on airlines (leases), old industrials (pensions), and acquisitive roll-ups (minority puts) — exactly the companies where a lazy EV calc goes wrong.

## 7. Judgment Calls Worth Knowing Early

Three things bankers argue about that you should at least recognize:

**Operating cash vs. excess cash.** A business needs *some* cash in the tills to operate — you can't sweep every dollar to repay debt without breaking the business. Sophisticated bridges subtract only *excess* cash (often estimated as cash above ~2% of revenue, or a fixed minimum). For most exercises, subtracting all unrestricted cash is fine; just know the refinement exists.

**Gross debt vs. net debt in multiples.** You'll sometimes see "net debt / EBITDA" as a leverage ratio — that's debt *minus* cash, and it's the right measure of burden because cash offsets debt. But when bridging to EV, keep the components visible (debt added, cash subtracted separately) rather than netting early; it makes errors easier to spot.

**Negative EV.** If cash exceeds equity value plus debt, EV goes negative. This occasionally happens with distressed companies whose equity has collapsed toward zero while they still hold cash. It does *not* mean the company is free — the debt still has to be repaid, and the equity is usually pricing in bankruptcy. A negative EV is a flag that says "look closer," not a bargain sticker.

## 8. The Invariance Insight: Only the Slices Move

Now the payoff for the intuition from Section 2. Suppose Northgate borrows $200m and uses it to buy back shares. Debt rises $200m; equity value falls $200m (fewer shares, same price per share in a frictionless world). What happens to EV?

```math
EV = (\text{Equity} - 200) + (\text{Debt} + 200) - \text{Cash} = \text{unchanged}
```

Nothing. The pie is the same size; only the slices moved. Same with the cash example from Section 2: accumulate $100m of cash and equity rises $100m, but the subtraction rises $100m too, and EV doesn't budge.

This is the practical shadow of one of the most famous results in finance: Modigliani and Miller's proposition that, under idealized conditions (no taxes, no bankruptcy costs, frictionless markets), a firm's total value is independent of its capital structure — it depends on the earning power of the underlying assets, not on how the claims on those assets are sliced up. (Modigliani, F. & Miller, M.H. (1958). "The Cost of Capital, Corporation Finance and the Theory of Investment." *American Economic Review*, 48(3), 261–297 — verified.)

Be careful about what this does and doesn't say — this is exactly the intuition/rigor line this series tries to keep clean:

- **Intuition (true and useful):** EV is the financing-independent measure of the business. That's why it's the anchor of every valuation method.
- **Rigorous result:** the independence holds *under the paper's assumptions*.
- **Needs verification in practice:** real markets have taxes (interest is tax-deductible, which genuinely favors debt), distress costs, and agency frictions — so capital structure *does* affect value in the real world, just second-order relative to the operating asset. Article 06 (WACC) will show you exactly where the tax shield enters the math.

Bankers live in the middle: they use EV as the clean, financing-neutral measure for comparing businesses, while knowing that in any specific deal, the financing structure changes what the equity is worth and what a buyer can pay.

---

## Common Misconceptions

- **"Enterprise value is what the acquirer pays."** Close, but no. The acquirer pays the *equity value* (plus a control premium) to shareholders, *assumes or refinances* the debt, and pays fees on top. EV is the value of the asset changing hands — the starting point for the price, not the price. Deal announcements quote EV because it's the financing-neutral measure of deal size.
- **"More debt means a more valuable company, since debt is added."** Only if you forget the other side of the bridge: adding debt without changing the business reduces equity value dollar-for-dollar (Section 8). EV is unchanged. Anyone who tells you leverage "creates" enterprise value is confusing the slice with the pie.
- **"A cash-rich company has a higher EV."** No — shown in Section 2. The extra cash raises equity value by exactly the amount subtracted. Cash changes the *composition* of value, not its total. (What cash does change: the company's flexibility, and the net debt a buyer inherits.)
- **"Always subtract 100% of cash."** Restricted or trapped cash can't be used to repay debt, so it stays out of the subtraction. And some bankers subtract only *excess* cash above operating needs. Read the footnotes before you net.
- **"EV/EBITDA and P/E tell the same story."** They can tell opposite stories for levered companies. A highly levered firm can show a "cheap" P/E (small equity base) alongside a full EV/EBITDA. If you only look at P/E, leverage can disguise an expensive business as a cheap stock.

## Test Yourself

**Q1.** A company has a $600m market cap, no options outstanding, $250m of debt, and $80m of cash. What is its enterprise value? If it then uses $80m of cash to repay $80m of debt, what is the new EV?
*A1. EV = 600 + 250 − 80 = $770m. After repaying: equity is unchanged at $600m (using cash to repay debt doesn't change equity value — assets fall $80m and liabilities fall $80m), debt is $170m, cash is $0. New EV = 600 + 170 − 0 = $770m. Unchanged — the pie didn't move, only its composition did.*

**Q2.** Why is EV/EBITDA the standard multiple but "Price/EBITDA" is never used? What goes wrong if you mix them?
*A2. Matching principle: EBITDA is earnings before interest — it belongs to all capital providers, so the numerator must be the all-claimants value (EV). Price is the shareholders-only value. "Price/EBITDA" mismatches claimants: for two identical businesses with different leverage it gives different multiples for the same asset, which defeats the purpose of comparing.*

**Q3.** A founder says: "My company has $50m in the bank, so it's worth at least $50m more than an identical company with no cash." What's right and wrong about this?
*A3. Right: the founder's *equity* is worth $50m more — shareholders own that cash. Wrong: the *enterprise value* is identical. EV = equity + debt − cash rises $50m on the equity side and falls $50m on the cash side. The operating business is worth the same; the treasury balance isn't the business.*

**Q4.** Your DCF produces an enterprise value of $2.0bn. Net debt is $700m, noncontrolling interest is $100m, no preferred stock, and fully diluted shares are 40m (basic shares are 37m). What is the implied per-share value, and what mistake would dividing by basic shares cause?
*A4. Equity value = 2,000 − 700 − 100 = $1,200m. Per share = 1,200 / 40 = $30.00. Dividing by basic shares (1,200 / 37 = $32.43) overstates value by ~8% — it counts the option/RSU dilution in the equity value (via TSM) but then pretends those shares don't exist in the denominator.*

---

*Next up — **04 | Comparable Company Analysis: Trading Multiples**: picking real peers, spreading their multiples, and turning "the market pays 8× EBITDA for businesses like this" into a valuation range.*
