# 04 | Comparable Company Analysis: Trading Multiples

*The fastest valuation in banking takes about twenty minutes: find five companies that look like yours, see what the market pays for each dollar of their earnings, and apply that price to your company. It sounds almost too simple to be real work. It is real work — the simplicity is the point, and the judgment calls hiding inside it are where analysts earn their keep.*

> **Learning goals.** After this article you can: (1) explain the logic of relative valuation and where it breaks down; (2) choose a peer set and defend the choices; (3) build a comps table — market cap, enterprise value, LTM and forward multiples; (4) convert a multiple range into an enterprise value and a per-share price; (5) name the adjustments (calendarization, non-recurring items, growth) that separate a serious comps table from a decorative one.
>
> **Prerequisites.** Articles 02 (EBITDA and the three statements) and 03 (the EV bridge, the matching principle). Comfort with division.

## 1. Valuation by Analogy

Suppose you want to know what your house is worth. You could hire an engineer to estimate the replacement cost of every brick (that's the DCF approach — build it up from fundamentals, article 06). Or you could look at what three similar houses on your street sold for last month and scale by square footage. The second method is **comparable company analysis** — "comps" — and it is the first valuation method bankers reach for, for a simple reason: it answers the question clients actually ask, which is not "what is this company worth in a perfect world" but "what would the market pay for it *right now*."

The logic has three steps:

1. **Find peers** — public companies similar to the one you're valuing.
2. **Observe their prices** — the market has already valued them; read the price tags via multiples.
3. **Apply** — multiply your company's earnings by the peers' multiples.

A **multiple** is just a ratio of value to some financial metric: EV/EBITDA, P/E, EV/Revenue. It says "the market pays X dollars for each dollar of Y." If packaging companies trade at 7.6× EBITDA and your packaging company earns $85m of EBITDA, the market's implied price for the whole firm is about $646m. That is the entire method. Everything else in this article is about doing those three steps *honestly*.

Two honesties matter. First, comps is **relative valuation**: it tells you what your company is worth *relative to how the market prices its peers*, not what it's worth in any absolute sense. If the whole sector is overvalued, comps will happily tell you your overvalued company is fairly priced. Second, no two companies are truly identical, so every comps table is an argument — "these companies are similar *enough*, in the dimensions that matter" — and a good analyst can defend that argument out loud.

## 2. What Makes a Company "Comparable"

When bankers say "comparable," they mean similar along the dimensions that drive what investors pay. Five matter most:

1. **Business model.** What the company actually does and how it makes money. A rigid plastic packaging maker and a paperboard mill both say "packaging," but their cost structures, customers, and cycles differ. Product mix, customer concentration, and geography all count.
2. **Growth.** A company growing EBITDA at 12% a year deserves a higher multiple than one growing at 2% — investors pay for growth. Comparing a high-growth peer to a no-growth target without adjusting is the most common comps sin.
3. **Margins.** Two companies with the same revenue but different margins are different businesses to an investor. This is why EV/Revenue is a blunt tool and EV/EBITDA is sharper — EBITDA already reflects profitability.
4. **Risk.** Leverage, cyclicality, customer concentration, regulatory exposure. A highly levered peer's equity multiple will look odd next to an unlevered target's (the matching principle from article 03 is doing quiet work here).
5. **Size.** Larger companies often trade at higher multiples — deeper liquidity, more diversified, lower perceived risk. A $10bn peer is a stretch comp for a $400m target; note the gap rather than pretending it isn't there.

In practice a peer set is **5 to 10 companies**: enough to see a pattern, few enough that each one was chosen deliberately. Bankers start from industry classifications and screening tools, then apply judgment — cutting the conglomerate whose packaging division is 15% of revenue, keeping the pure-play even if it's smaller. And here's a piece of desk honesty worth knowing early: there is always temptation to **cherry-pick** peers that give the answer your pitch book wants. Everyone in the room knows this. The defense is transparency — show the full set, show the median, and let the ugly peer stay in the table.

## 3. Spreading the Comps: Building the Table

"Spreading comps" is the mechanical part, and analysts do it constantly. For each peer you need:

- **Share price × fully diluted shares** = market cap (equity value).
- **The EV bridge** (article 03): EV = market cap + net debt + NCI + preferred − cash. Every EV multiple starts from this number.
- **Financials**: revenue, EBITDA, EBIT, net income — for the **last twelve months (LTM)** and, usually, the **next twelve months (NTM)** estimated.

**LTM** deserves a definition because you'll compute it weekly as an analyst. Companies report annually and quarterly, on different fiscal year-ends. To compare a December year-end peer with a March year-end peer as of today, you build a trailing twelve months for each:

```math
\text{LTM} = \text{last fiscal year} + \text{stub quarters this year} - \text{same quarters last year}
```

Example: a peer's fiscal 2025 EBITDA was $100m, Q1 2026 EBITDA was $30m, and Q1 2025 EBITDA was $22m. LTM EBITDA through March 2026 is:

```math
100 + 30 - 22 = \$108\text{m}
```

This **calendarization** — restating every peer to the same twelve-month window — is unglamorous and essential. Skip it and you're comparing one company's good quarter against another company's bad one.

**NTM** (next twelve months) figures come from equity research consensus estimates — what analysts expect. LTM tells you what the company *did*; NTM tells you what the market *expects*. Bankers show both, because the market prices expectations, not history. There's real evidence behind that habit: Liu, Nissim, and Thomas (2002) tested a battery of multiples against actual stock prices and found that **forward-earnings multiples explain prices remarkably well** — pricing errors within 15% of the stock price for about half their sample — and that forward earnings beat historical earnings, cash flow, book value, and (dead last) sales as valuation drivers. (Liu, J., Nissim, D. & Thomas, J. (2002). "Equity Valuation Using Multiples." *Journal of Accounting Research*, 40(1), 135–172 — verified.) When a banker insists on showing NTM multiples next to LTM ones, this paper is the quiet academic backing.

## 4. The Multiples Menu

Not all multiples are interchangeable. The matching principle from article 03 — *the numerator's claimants must match the denominator's* — picks the right one for each job:

| Multiple | Numerator → denominator | Best for | Watch out for |
|---|---|---|---|
| **EV/Revenue** | Whole firm → whole firm | Early-stage / negative-earnings companies; top-line comparisons | Ignores margins completely — a 5%-margin business at 2× revenue is a very different deal than a 25%-margin one |
| **EV/EBITDA** | Whole firm → all capital providers | The workhorse: capital-structure-neutral, pre-accounting-choice-ish | Ignores capex intensity and working capital — two companies with the same EBITDA can have very different cash flows |
| **EV/EBIT** | Whole firm → all capital providers | Capital-intensive industries where depreciation is a real economic cost | Depreciation policies differ across companies |
| **P/E** | Equity → shareholders | Quick equity-level gut check; what most civilians quote | Distorted by leverage — useless for comparing levered vs. unlevered peers |
| **EV/FCF** | Whole firm → cash to all providers | Cash-generative businesses; closest multiple to DCF thinking | Lumpy year to year; needs averaging |
| **PEG** | P/E ÷ earnings growth rate | Growth-adjusting the P/E: "how much am I paying per unit of growth" | Growth estimates are guesses wearing suits |

Two conventions to internalize. First, **EV multiples for operating metrics, equity multiples for bottom-line metrics** — EV/EBITDA and EV/Revenue are fine; "Price/EBITDA" is a matching-principle violation, and P/E is only meaningful when leverage is similar across the set. Second, **forward multiples are usually lower than LTM multiples** for growing companies (the denominator grows while the price already reflects it). If you see an NTM multiple *above* the LTM multiple, the market expects earnings to shrink — worth a raised eyebrow.

## 5. Worked Example, Part 1: Spreading Bluepeak Packaging

Let's value a fictional company, **Bluepeak Packaging** — a mid-sized North American maker of rigid plastic containers. LTM revenue $520m, LTM EBITDA $85m, LTM EBIT $58m, LTM net income $30m. Current share price $13.10, fully diluted shares 32.0m (market cap $419.2m). Net debt $180m (debt $240m, cash $60m).

Five peers, spread as of the same date. (Every number is invented; the mechanics are the real ones.)

| Peer | Price | Dil. sh. (m) | Mkt cap ($m) | Net debt ($m) | EV ($m) | LTM rev ($m) | LTM EBITDA ($m) | LTM NI ($m) |
|---|---|---|---|---|---|---|---|---|
| Crestline Containers | $52.00 | 24.0 | 1,248.0 | 420 | 1,668.0 | 1,050 | 210 | 95 |
| Northfield Packaging | $38.50 | 25.5 | 981.8 | 310 | 1,291.8 | 900 | 172 | 72 |
| Summit Paper & Board | $64.00 | 32.8 | 2,099.2 | 900 | 2,999.2 | 1,900 | 340 | 150 |
| Lakeside Fiber | $29.75 | 21.5 | 639.6 | 180 | 819.6 | 620 | 118 | 48 |
| Beacon Flexible Pkg | $41.00 | 21.2 | 869.2 | 260 | 1,129.2 | 760 | 148 | 62 |

Check one row so the arithmetic is visible — Northfield: $38.50 × 25.5m = $981.8m market cap; EV = 981.8 + 310 = $1,291.8m (no NCI or preferred in this simplified set).

Now the multiples:

| Peer | EV/EBITDA | EV/Revenue | P/E |
|---|---|---|---|
| Crestline Containers | 1,668.0 / 210 = **7.9×** | 1,668.0 / 1,050 = **1.6×** | 1,248.0 / 95 = **13.1×** |
| Northfield Packaging | 1,291.8 / 172 = **7.5×** | 1,291.8 / 900 = **1.4×** | 981.8 / 72 = **13.6×** |
| Summit Paper & Board | 2,999.2 / 340 = **8.8×** | 2,999.2 / 1,900 = **1.6×** | 2,099.2 / 150 = **14.0×** |
| Lakeside Fiber | 819.6 / 118 = **6.9×** | 819.6 / 620 = **1.3×** | 639.6 / 48 = **13.3×** |
| Beacon Flexible Pkg | 1,129.2 / 148 = **7.6×** | 1,129.2 / 760 = **1.5×** | 869.2 / 62 = **14.0×** |
| **Median** | **7.6×** | **1.5×** | **13.6×** |
| Mean | 7.7× | 1.5× | 13.6× |

A note on **median vs. mean**: bankers default to the median, because one weird peer shouldn't move the valuation. Here Summit (8.8× — it's the biggest, most diversified peer) pulls the mean up to 7.7× while the median stays at 7.6×. When a peer is a genuine outlier, the median shrugs; the mean doesn't. If you ever see a comps page showing only the mean with one 15× peer in the set, you're looking at advocacy, not analysis.

## 6. Worked Example, Part 2: From Multiples to a Price

Apply the median EV/EBITDA multiple to Bluepeak's $85.0m of LTM EBITDA:

```math
\text{Implied EV} = 85.0 \times 7.6 = \$646.0\text{m}
```

The observed peer range gives a valuation band: low end 6.9× → $586.5m, high end 8.8× → $748.0m. Now run the bridge in reverse (article 03) to get to the shares:

```math
\begin{align}
\text{Implied Equity Value} &= EV - \text{Net Debt} \\
&= 646.0 - 180.0 \\
&= \$466.0\text{m}
\end{align}
```

```math
\text{Implied price per share} = 466.0 / 32.0 = \$14.56
```

Against the actual $13.10 share price, that's about **11% implied upside** — the comps are saying the market prices Bluepeak a touch cheaply versus its peers. (Or the peers are a touch expensive. Comps can't tell you which — Section 8.)

Now triangulate with the other multiples, because a serious comps page never rests on one:

- **EV/Revenue:** median 1.5× × $520m revenue = **$780m EV** → equity $600m → **$18.75/share**.
- **P/E:** median 13.6× × $30m net income = **$408m equity** → **$12.75/share**.

Three multiples, three answers: $14.56, $18.75, $12.75. This spread is *normal* and it's the point of the exercise — each multiple sees the company through a different lens. The revenue multiple ignores Bluepeak's margin problem (its 16.3% EBITDA margin trails every peer, which range from ~18% to 20%), so it overstates. The P/E is weighed down by Bluepeak's leverage and interest burden. The EV/EBITDA answer sits in the middle and gets the most weight on a real comps page — it's the multiple least distorted by financing and accounting choices. A banker would present something like: "trading comps imply $13–$17 per share, centered on $14.50" — a range, with a view on which end is better supported.

One more lens — **forward multiples**. Suppose consensus NTM EBITDA for Bluepeak is $94m and the peers' median NTM EV/EBITDA is 7.1× (lower than the 7.6× LTM median, as expected for growing companies):

```math
\text{Implied EV (forward)} = 94.0 \times 7.1 = \$667.4\text{m}
```

That lands inside the LTM-based range — a good sign. When the forward-implied value lands far *outside* the LTM range, something interesting is happening: either the market expects a real inflection, or the consensus estimates are fantasy. Either way, that's where the conversation goes next.

## 7. Adjustments That Separate Good Comps From Garbage

A comps table fresh off a data pull is raw material, not analysis. The adjustments:

- **Non-recurring items.** A peer's EBITDA includes a $40m restructuring charge? Add it back — you're valuing the ongoing business, not last year's plant closure. Read the footnotes; "adjusted EBITDA" in a press release is management's version, and management is always generous with itself.
- **Calendarization** (Section 3). Non-negotiable when fiscal year-ends differ.
- **Pro forma for M&A.** If a peer bought a competitor six months ago, its LTM EBITDA only includes half a year of the target. Annualize it, or your multiple understates the earnings base.
- **Growth normalization.** If your target grows at 4% and the median peer at 9%, a straight median multiple overstates value. The quick fix is the **PEG lens**: compare P/E-to-growth across peers rather than raw P/E. The thorough fix is a regression of multiples on growth — overkill for most pitch books, standard in fairness opinions.
- **Size and liquidity discount.** Smaller companies trade cheaper, all else equal. If your target is half the size of the smallest peer, say so and consider shading the multiple down — or at least flag it as a caveat.
- **Accounting consistency.** IFRS vs. US GAAP, lease capitalization, revenue recognition — the big ones mostly wash through EBITDA, but they can bite in asset-heavy or subscription businesses. Know which standard each peer reports under before you compare.

None of these adjustments is exotic. All of them are the difference between a table that informs a board and a table that decorates a pitch book.

## 8. What Comps Can and Can't Tell You

Comps' greatest strength is also its built-in blind spot: **it assumes the market is right about the peers**. If packaging stocks are in a bubble, comps will value your packaging company at bubble prices and call it rigorous. There is a circularity at the heart of relative valuation — price is explained by price — and no amount of spreadsheet polish removes it. That's not a reason to skip comps; it's a reason to pair them with an intrinsic method. The DCF (articles 06–07) doesn't care what the market thinks — which is exactly why bankers run both and put them side by side on the football field (article 10).

Used properly, comps does three jobs no other method does as well:

1. **Market reality check.** Whatever your DCF says, the comps tell you what buyers and public investors are actually paying today. A DCF that implies 12× EBITDA in a 7× market needs a very good story.
2. **A common language.** "7.6× EBITDA" is how buyers, sellers, and bankers negotiate. Multiples are the industry's unit of account.
3. **Speed.** A credible first-pass valuation in an afternoon. When a client calls asking "what could we get for the division," comps answers before the DCF model has its first tab built.

The honest summary: comps tells you what the market *would* pay, the DCF tells you what the company *should* be worth, and the gap between them is where the interesting questions live.

---

## Common Misconceptions

- **"More peers is always better."** A 20-company comps table with conglomerates, foreign giants, and a fintech that once sold boxes is not more rigorous — it's more diluted. Five genuinely similar peers beat fifteen loose ones. Every peer you add should survive the question "would an investor actually compare these two?"
- **"The highest multiple marks the best company."** Sometimes it marks the most overvalued one, or the one with temporarily depressed earnings (a tiny denominator inflates any ratio). Always look at *why* a multiple is high before admiring it.
- **"P/E works fine for cross-industry or cross-leverage comparisons."** The matching principle says no: P/E mixes an equity numerator with earnings after interest, so leverage contaminates it. Two identical businesses with different debt loads show different P/Es for the same asset. That's what EV multiples are for.
- **"Comps gives the right price."** Comps gives the *market-consistent* price. If you want "right" in an absolute sense, you need an intrinsic method — and even then, humility is warranted.
- **"Always use the mean — it's more scientific."** The median exists precisely because peer sets contain outliers. Using the mean with Summit's 8.8× in the set quietly lets the least comparable peer set the price. Medians are a feature, not a shortcut.

## Test Yourself

**Q1.** Delta Fabrication has LTM EBITDA of $60m, net debt of $95m, and 25.0m fully diluted shares. Its peers' median EV/EBITDA is 8.0×. What is the comps-implied EV, equity value, and per-share value?
*A1. Implied EV = 60 × 8.0 = $480m. Equity value = 480 − 95 = $385m. Per share = 385 / 25.0 = $15.40.*

**Q2.** Your peer set's EV/EBITDA multiples are 6.2×, 6.8×, 7.1×, 7.4×, and 13.5×. The 13.5× peer just sold a division, so its LTM EBITDA is temporarily depressed. Do you use the mean or the median — and what goes wrong with the other choice?
*A2. Use the median (7.1×). The mean is 8.2× — the depressed-earnings peer inflates it by more than a full turn, so the "average" is really just that one broken observation dragging the rest. The median ignores it.*

**Q3.** A junior analyst values a highly levered target by applying the peer median P/E to the target's net income. Name two things wrong with this, referencing the matching principle.
*A3. First, P/E is an equity multiple applied to levered earnings — if the target's leverage differs from the peers', the comparison is contaminated: interest expense shrinks the denominator for reasons unrelated to operating performance. Second, the fix is an EV multiple (EV/EBITDA or EV/EBIT) matched to a pre-interest metric, then the bridge back to equity — exactly the article 03 round trip.*

**Q4.** A peer's fiscal year ends in December. Its FY2025 EBITDA was $100m, Q1 2026 EBITDA was $30m, and Q1 2025 EBITDA was $22m. What is its LTM EBITDA as of March 2026, and what is this restatement called?
*A4. LTM = 100 + 30 − 22 = $108m. This is calendarization — restating every peer to the same trailing twelve-month window so the multiples compare like with like.*

---

*Next up — **05 | Precedent Transactions & Control Premiums**: what buyers actually paid for whole companies, why it's more than the trading price, and how much of that premium is real synergy versus winner's curse.*
