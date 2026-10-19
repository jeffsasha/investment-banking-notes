# 08 | LBO Analysis: Sources, Uses, and Returns

*Every banker learns the DCF as "what this company is worth to anyone." The LBO answers a narrower, more personal question: what is this company worth to* me *— a buyer who borrows most of the purchase price, uses the company's own cash flows to repay that debt, and sells what's left in five years? Same company, different animal. The returns can be spectacular. They can also be a massacre. This article is about why both are true.*

> **Learning goals.** After this article you can: (1) explain the LBO intuition — buying a company largely with its own future cash flows; (2) build a sources-and-uses table and a simple debt schedule with interest, amortization, and a cash sweep; (3) identify what makes a good LBO candidate, and why boring beats exciting; (4) compute equity returns — IRR and MOIC — from a five-year model, and decompose them into EBITDA growth, debt paydown, and multiple expansion.
>
> **Prerequisites.** Articles 02–03 (financial statements, enterprise vs. equity value) and 06–07 (the DCF). The LBO is valuation with a different question attached, so the earlier machinery all shows up again.

## 1. The intuition: buy it with its own money

Strip the jargon and a leveraged buyout is almost comically simple. A private equity firm wants to buy a company worth $800 million. It does not have $800 million of its own money lying around for one deal — or rather, it doesn't want to *use* $800 million even if it could. Instead it borrows $400 million from lenders, puts in $400 million of its investors' equity, buys the company, and then spends the next five years directing the company's cash flows at the debt until the debt is mostly gone. Then it sells the company — now nearly debt-free and bigger — and the equity, which started at $400 million, is worth $1 billion.

Three levels to keep straight, per this series' habit. The *intuition* (a stable company can service debt, and repaying debt with the company's own cash transfers value to equity) is solid and centuries old — it's how every mortgaged house purchase works. The *strict conclusions* (debt must be repaid from cash flow, so coverage ratios are the binding constraint; equity is the residual claim and gets wiped first if things go wrong) are non-negotiable. The *estimates* (how much debt the cash flows can support, what the company will be worth at exit) are judgment calls that decide whether the deal makes or loses money.

The reason this works at all — the reason lenders hand over $400 million — is the subject of section 3. The short version: the company being bought is the collateral, the cash cow, and the repayment plan all at once. A house mortgage is secured by a house you then live in; an LBO is secured by a company that then pays for itself.

One more piece of intuition before the machinery: leverage amplifies *everything*, in both directions. If the asset returns 10% and you borrowed half the money at 5%, your equity earns roughly 15% — the spread between the asset's return and the borrowing cost accrues to you. If the asset returns 2% and you borrowed at 5%, your equity earns roughly *negative* 1%. The same debt that juices the upside detonates the downside. Every number in this article's model will demonstrate that symmetry.

The academic backbone of the whole industry is Jensen, M. (1986), "Agency Costs of Free Cash Flow, Corporate Finance, and Takeovers," *American Economic Review*: debt isn't just cheap financing, it's a *discipline device* — mandatory interest payments force managers to stop wasting free cash flow on empire-building. Keep that idea in your pocket; it explains why PE firms love boring, cash-rich companies that public markets find dull.

## 2. Sources and uses: the deal's balance sheet

Every LBO model starts with a one-page accounting of the transaction itself — where the money comes from (*sources*) and where it goes (*uses*). By construction, the two sides balance, like a balance sheet.

Meet our target: **Meridian Industrial**, a fictional maker of industrial fasteners. Steady demand, 40% market share in its niche, EBITDA of **$100 million**, almost no debt. A PE firm — call it Harbor Capital — agrees to buy it.

Deal terms:

- **Purchase enterprise value:** 8.0x LTM EBITDA = **$800m** (a full but not crazy multiple for a stable industrial)
- **Financing:** $400m of debt (4.0x EBITDA) + the rest in equity
- **Fees:** bankers, lawyers, financing fees run ~2% of EV = **$16m** (fees are a *use* — real cash that leaves the table on day one and never comes back)

| Sources | $m | | Uses | $m |
|---|---|---|---|---|
| Term loan (4.0x EBITDA) | 400 | | Purchase EV (8.0x) | 800 |
| Sponsor equity | 416 | | Fees & expenses | 16 |
| **Total sources** | **816** | | **Total uses** | **816** |

Read this table carefully, because it already contains the whole bet. Harbor is paying $816 million in total but only $416 million of it is *its* money — **51%** of the capital. The other 49% belongs to lenders, who get a fixed 8% return and first claim on everything. Harbor's equity is the residual: it gets whatever is left after the debt is serviced and repaid. If Meridian thrives, the residual is enormous relative to the $416m check. If Meridian stumbles, the residual is what gets destroyed first.

A note on the debt stack, since real deals have more than one loan. The typical structure layers tranches by seniority: a **revolving credit facility** (a credit card for the company, usually undrawn at close), a **term loan** (amortizing, secured, cheapest), then **high-yield bonds** or **mezzanine** debt (unsecured, more expensive, sometimes with warrants). Our model collapses all of it into one $400m term loan at 8% — a simplification, but the mechanics of interest, amortization, and repayment are the same.

Two ratios bankers watch from this table onward. **Leverage** = Debt / EBITDA: ours is 4.0x at entry — aggressive but standard for a stable business in a normal credit market. **Interest coverage** = EBITDA / Interest: ours is $100m / $32m = 3.1x — the company earns more than three times its interest bill, which is what lets everyone sleep at night.

## 3. What makes a good LBO target: boring is beautiful

Not every company can be bought this way. The debt has to be repaid from the company's cash flows, which imposes a brutal filter. The classic LBO candidate checklist:

1. **Stable, predictable cash flows.** This is the whole game. Lenders underwrite the downside, not the dream — they need to believe EBITDA will still be there in a recession. Fasteners, food distribution, waste management, enterprise software maintenance: boring industries with recurring revenue. A biotech with binary trial outcomes need not apply.
2. **Low capital intensity and modest working capital needs.** Every dollar of capex or working capital is a dollar that can't repay debt. Asset-light businesses with maintenance capex well below D&A are ideal.
3. **Strong market position.** A defensible niche means pricing power, which means margins survive downturns. Meridian's 40% share in industrial fasteners is exactly the profile.
4. **Low existing debt.** You're about to load the company with leverage; starting from a clean balance sheet gives you the full debt capacity to work with.
5. **Experienced management (or a plan to install it).** The PE firm typically keeps the management team and gives them a large equity stake — 10–20% of the equity is standard. This is the Jensen (1986) insight made concrete: managers who own a leveraged slice of the company think like owners, because the debt leaves no room for waste.
6. **Assets, optionally.** Factories and inventory help on the margin as collateral, but this is the least important item — lenders size the debt to *cash flow*, not to asset value. A software company with no factories but sticky subscription revenue can support more leverage than a steel mill.

Notice what's missing from the list: growth. Growth is nice, but a no-growth company with rock-solid $100m EBITDA is a better LBO candidate than a fast grower burning cash. The debt doesn't care about your growth story; it cares about next quarter's interest payment. This is the single most counterintuitive thing for people coming from growth-equity or venture thinking: **in an LBO, predictability is worth more than growth.**

## 4. The debt schedule: where the leverage lives

Between entry and exit sits the debt schedule — the engine room of the model. Each year, the company earns EBITDA, pays interest on the debt outstanding at the start of the year, pays taxes, funds capex and working capital, and then *every remaining dollar* goes to repay debt. That last part — the **cash sweep** — is what makes the equity returns work: debt doesn't just sit there, it gets actively destroyed by the company's own cash flow.

Let's build it. Assumptions for Meridian, held constant for simplicity:

- EBITDA grows **8% per year** (solid operational improvement, nothing heroic)
- D&A = $20m/year, capex = $22m/year, increase in working capital = $3m/year
- Interest = **8%** on beginning-of-year debt
- Tax rate = **25%** (interest is tax-deductible — the tax shield saves 25% × $32m = **$8m** in year one alone, real money that partly offsets the cost of debt)

**Levered free cash flow** each year is:

```math
FCF = EBITDA - Interest - Taxes - Capex - \Delta NWC
```

where $Taxes = 25\% \times (EBITDA - D\&A - Interest)$.

Year 1, step by step:

```math
Interest_1 = 8\% \times 400.0 = 32.0
```

```math
EBT_1 = 108.0 - 20.0 - 32.0 = 56.0 \quad\Rightarrow\quad Tax_1 = 25\% \times 56.0 = 14.0
```

```math
FCF_1 = 108.0 - 32.0 - 14.0 - 22.0 - 3.0 = 37.0
```

All $37.0m sweeps to debt: end-of-year-1 debt = $400.0m − $37.0m = **$363.0m**. One year in, leverage is already down from 4.0x to $\frac{363.0}{108.0} = 3.4x$. The company is literally buying itself back from the lenders.

Running the same machinery for five years:

| Year | 0 | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|---|
| EBITDA | 100.0 | 108.0 | 116.6 | 126.0 | 136.0 | 146.9 |
| Interest (8%) | — | 32.0 | 29.0 | 25.4 | 20.9 | 15.6 |
| EBT | — | 56.0 | 67.6 | 80.6 | 95.1 | 111.3 |
| Taxes (25%) | — | 14.0 | 16.9 | 20.1 | 23.8 | 27.8 |
| Levered FCF | — | 37.0 | 45.7 | 55.4 | 66.3 | 78.5 |
| Debt, beginning | 400.0 | 400.0 | 363.0 | 317.3 | 261.9 | 195.5 |
| Debt, end | — | 363.0 | 317.3 | 261.9 | 195.5 | 117.1 |
| Leverage (Debt/EBITDA) | 4.0x | 3.4x | 2.7x | 2.1x | 1.4x | 0.8x |

Study the dynamics. Interest *falls* every year because the balance shrinks, which *raises* free cash flow, which *accelerates* paydown — a virtuous circle. Total debt repaid: $400.0m − $117.1m = **$282.9m**, paid entirely from the company's own earnings. Nobody injected another dollar. This is the sentence that explains private equity to your skeptical friends: *the company paid for 70% of its own acquisition debt, and the equity holders kept all of it.*

Bankers also track **covenants** — tripwires in the loan agreement, typically a maximum leverage ratio and a minimum interest coverage ratio, tested quarterly. Breach one and the lenders can demand immediate repayment, which is how a fundamentally okay company dies. Our model's leverage glides from 4.0x to 0.8x and coverage rises throughout, so covenants are never threatened — but in a downside case (section 7) they are exactly where the trouble starts.

## 5. The exit: turning deleveraging into dollars

After five years, Harbor sells Meridian. Assume a conservative exit — the same 8.0x EV/EBITDA multiple it paid, i.e., **no multiple expansion** (we'll see in section 6 what expansion would add):

```math
EV_{exit} = 146.9 \times 8.0 = 1{,}175.5
```

```math
Equity_{exit} = EV_{exit} - Debt_{exit} = 1{,}175.5 - 117.1 = 1{,}058.4
```

Harbor's $416m check is now worth **$1,058.4m**. Two return metrics, and you need both:

- **MOIC** (multiple on invested capital, "the multiple"): $\frac{1058.4}{416} = 2.54x$ — "we made two-and-a-half times our money."
- **IRR** (internal rate of return): $2.544^{1/5} - 1 = 20.5\%$ per year.

MOIC tells you *how much*; IRR tells you *how fast*. A 2.5x return over five years (20.5% IRR) beats a 3.0x return over ten years (11.6% IRR) — which is why PE firms are obsessed with hold periods and sometimes sell early. Quick mental math worth memorizing: **2x in 5 years ≈ 15% IRR; 3x in 5 years ≈ 25% IRR; 2x in 3 years ≈ 26% IRR.**

For perspective on what the leverage actually did, consider the counterfactual: Harbor buys Meridian with *no* debt — $816m of pure equity — and exits at the same $1,175.5m EV. MOIC = $\frac{1175.5}{816} = 1.44x$, IRR = 7.6%. The same company, the same operational performance — but leverage took the return from 7.6% to 20.5%. That gap is the entire economic argument for the LBO, and the entire source of its risk.

## 6. Where the returns come from: three buckets

Total equity value created: $1,058.4m − $416.0m = **$642.4m**. Bankers decompose this into three buckets — the standard attribution every PE investment memo contains:

1. **EBITDA growth** (operational improvement): $(146.9 - 100.0) \times 8.0 = \$375.5m$ — the company got bigger and more profitable, valued at the entry multiple.
2. **Debt paydown** (deleveraging): $400.0 - 117.1 = \$282.9m$ — the company's cash flows retired debt, and every repaid dollar transferred straight to equity.
3. **Multiple expansion** (buy low, sell high on the multiple): $(8.0 - 8.0) \times 146.9 = \$0m$ — we assumed none.

Check: $375.5 + 282.9 + 0 = 658.4$, which is $16m more than the $642.4m actually created. The missing $16m is the **fees** paid on day one — the silent fourth bucket, always negative, which is why bankers obsess over fee discipline. So the true attribution: growth **58%**, deleveraging **44%**, fees **−2%**, multiple expansion 0%.

Two lessons. First, in a typical deal with no multiple expansion, *deleveraging is nearly half the return* — the "financial engineering" people sneer at is really just the arithmetic of a company paying down its own debt. Second, multiple expansion is the bucket bankers are most skeptical of in underwriting, because it requires the *next* buyer to pay more per dollar of EBITDA than you did. When you see an investment memo leaning on expansion from 8x to 10x, that's hope, not a plan. The discipline is to underwrite the deal so it works at *flat* multiples — as ours does, at 20.5% — and treat any expansion as upside. (For reference: one turn of expansion, exiting at 9x instead of 8x, would take exit equity to $1,205.3m and IRR to 23.7% — about 3 points per turn. Nice when it happens; never counted on.)

## 7. The other edge: leverage cuts both ways

Now the massacre. Same deal, but Meridian's end markets soften and EBITDA *declines* 10% per year instead of growing 8%. The debt schedule doesn't care about your thesis — interest is still due:

| Year | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|
| EBITDA | 90.0 | 81.0 | 72.9 | 65.6 | 59.0 |
| Interest | 32.0 | 30.1 | 28.7 | 27.6 | 26.9 |
| Levered FCF | 23.5 | 18.2 | 13.2 | 8.5 | 4.1 |
| Debt, end | 376.5 | 358.3 | 345.2 | 336.7 | 332.6 |

The virtuous circle runs in reverse: shrinking EBITDA leaves less cash after interest, paydown stalls, interest stays high. At exit, EV = $59.0m × 8.0 = **$472.4m** against debt of **$332.6m**, leaving equity of just **$139.8m**. MOIC = 0.34x — a **−66%** loss — and IRR = −19.6%. The company is still operating, still generating cash, still worth nearly half a billion dollars. The equity is still destroyed, because debt is senior and the residual absorbs everything first.

This is why section 3's checklist exists, and why lenders obsess over downside cases rather than base cases. A 10%-per-year decline is not an exotic disaster — it's one bad cycle in an industrial business.

Which brings us to the variable PE partners actually fight about: the **entry price**. Hold everything else in the base case fixed and vary only the purchase multiple (debt stays 4.0x EBITDA, so the debt schedule is unchanged — only the equity check moves):

| Entry multiple | Equity check | MOIC | IRR |
|---|---|---|---|
| 7.0x | $314m | 3.37x | 27.5% |
| 8.0x | $416m | 2.54x | 20.5% |
| 9.0x | $518m | 2.04x | 15.4% |

Each additional turn of entry multiple costs roughly **5–6 points of IRR**. The debt, the operations, the exit — all identical. The only difference is what you paid on day one. This table is why PE firms walk away from auctions: at 9x, a perfectly executed deal earns 15.4%, below most funds' 20%+ hurdle, so there is no price at which the deal works and the discipline is to *not do it*. "You make your money when you buy" is the industry's oldest cliché, and the math above is why it's true.

One honest caveat, from Kaplan, S. N. & Strömberg, P. (2009), "Leveraged Buyouts and Private Equity," *Journal of Economic Perspectives*, 23(1), 121–146: across 17,171 buyouts from 1970 to 2007, only about **6% ended in bankruptcy or reorganization** — an annual default rate of roughly 1.2%, *below* the 1.6% average for all U.S. corporate bond issuers over a similar period. The downside case above is real, but the caricature of PE as systematic corporate strip-mining doesn't survive the data: most levered companies service their debt and survive. Leverage raises the stakes; it doesn't predetermine the outcome.

## 8. IRR vs. MOIC: how bankers keep score

You'll hear both numbers in every PE conversation, and they can disagree. IRR rewards *speed*: returning capital fast — through a quick sale or a **dividend recapitalization** (borrowing against the company to pay yourself a dividend mid-hold) — juices IRR even if total profit barely moves. MOIC rewards *scale*: total dollars returned per dollar invested, regardless of timing. A 2.0x in two years (41% IRR) and a 2.0x in five years (15% IRR) are the same MOIC and very different IRRs.

This creates well-known games. Funds can inflate IRR by selling winners early and holding losers (the "quick flip"), or by calling capital late. Sophisticated investors (limited partners) therefore look at both, plus **DPI** — distributions actually paid out in cash, the "show me the money" metric — because IRR and MOIC on paper mean nothing until cash returns. The professional stance: underwrite on MOIC with a required IRR hurdle (often ~20%), report both honestly, and distrust any track record shown on IRR alone.

And a final piece of context on where the LBO sits in this series: it's the third valuation lens after comps (what the market pays), precedent transactions (what buyers paid), and the DCF (what the cash flows are worth). The LBO answers "what can a *leveraged* buyer pay while still hitting its return hurdle" — which is why bankers run one in every sale process: it sets the floor price a PE bidder can afford, and tells the sell-side exactly how far the bidding can go.

## Common Misconceptions

- **"LBO returns come from financial engineering, not the business."** In our base case, 58% of the value created was plain EBITDA growth — the company getting better. Deleveraging (44%) looks like engineering, but it's the company's own cash flows doing the work. And the downside case proves the negative: no business performance, no return, no matter how clever the structure.
- **"More leverage always means higher returns."** Up to a point, yes — then interest consumes the cash flow, covenants start binding, and the equity becomes a lottery ticket. Our downside case at 4.0x entry leverage lost two-thirds of the equity on a mere 10%/yr EBITDA decline. There is an optimal leverage point, and it's set by cash flow stability, not by ambition.
- **"IRR is all that matters."** IRR can be gamed with timing; MOIC can be gamed with patience. Professionals underwrite with both plus a hurdle rate, and LPs ultimately care about DPI — cash actually returned. Any single metric in isolation is a story someone chose to tell you.
- **"Good LBO targets are asset-heavy companies you can borrow against."** Lenders size debt to *cash flow coverage*, not to asset appraisals. A factory with volatile earnings supports less debt than a software company with sticky subscriptions. Collateral helps at the margin; predictability is the actual constraint.
- **"The entry multiple doesn't matter much if you grow the business."** The sensitivity table says otherwise: 7x → 27.5% IRR, 9x → 15.4% IRR, identical operations. Overpaying by two turns of EBITDA nearly halves the return. Price discipline *is* the job.
- **"Private equity just loads companies with debt and strips them."** The data disagrees with the caricature: Kaplan & Strömberg (2009) find ~6% of 17,171 buyouts ended in bankruptcy, a lower annual default rate than the broad corporate bond market. The model *requires* a living, cash-generating company — a stripped carcass can't service debt. (That doesn't make every deal virtuous; it makes the strip-mining story statistically rare.)

## Test Yourself

**Q1.** Meridian's purchase EV is 8.0x $100m EBITDA, fees are 2% of EV, and debt is 4.0x EBITDA. What is the sponsor's equity check, and what percentage of total capital is it?
*A1. Uses = 800 + 16 = $816m. Debt = $400m. Equity = 816 − 400 = **$416m**, which is 416/816 = **51.0%** of total capital.*

**Q2.** In the base case, suppose the exit multiple compresses to 7.0x instead of 8.0x (same year-5 EBITDA of $146.9m, same exit debt of $117.1m). What are exit equity, MOIC, and IRR?
*A2. Exit EV = 146.9 × 7.0 = $1,028.5m. Exit equity = 1,028.5 − 117.1 = **$911.4m**. MOIC = 911.4/416 = **2.19x**. IRR = 2.19^(1/5) − 1 ≈ **17.0%**. One turn of multiple compression costs about 3.5 points of IRR — the mirror image of the expansion math in section 6.*

**Q3.** What is the dollar value of the interest tax shield in year 1 of the base case, and why does it matter for the "is debt cheap?" debate?
*A3. Year-1 interest is $32.0m; at a 25% tax rate the shield is 0.25 × 32.0 = **$8.0m** — the government effectively rebates a quarter of the interest bill. It matters because debt's true cost is the* after-tax *rate (8% × (1 − 0.25) = 6%), which is part of why borrowing can be cheaper than equity — a link back to the WACC discussion in article 06. But the shield only has value if the company is profitable enough to use it; in the downside case, shrinking EBT means less shield exactly when you need it most.*

**Q4.** Two targets, both at 4.0x leverage: (a) a packaging company with EBITDA that has grown 3–5% every year for a decade; (b) a semiconductor equipment maker with EBITDA that swings ±30% with the chip cycle but averages higher. Which is the better LBO candidate, and what single ratio from this article is the deciding factor?
*A4. (a), the packaging company — and it's not close. The deciding factor is the* interest coverage ratio *(EBITDA / Interest) through the trough, not the average. Target (b)'s −30% years would crush coverage toward 1x, trip covenants, and stall the paydown virtuous circle from section 4 — exactly the downside-case dynamics of section 7. In LBOs, predictability beats level: lenders underwrite the worst year, not the average year.*

---

*Next up — **09 | Accretion/Dilution and Merger Models**: when one company buys another, does the deal grow earnings per share or shrink it — and why bankers (and CEOs) care so much about the answer.*
