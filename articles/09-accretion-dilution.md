# 09 | Accretion/Dilution and Merger Models

*Every deal announcement is followed by the same conference call ritual. Management talks about strategy, vision, the bright combined future — and within five minutes, the first analyst asks the only question that actually matters to the stock price that day: "Is it accretive?" This article is about that question. What it means, how the math actually works, and why the most dangerous thing in M&A is a deal that is accretive and terrible.*

> **Learning goals.** After this article you can: (1) define accretion and dilution precisely and explain why the market cares; (2) build a pro forma income statement — combining two companies plus synergies, financing costs, and purchase-accounting adjustments; (3) derive the shortcut rules for when an all-stock or all-cash deal is accretive; (4) explain why accretion is not the same as value creation, with real examples of the confusion.
>
> **Prerequisites.** Articles 02–03 (financial statements, enterprise vs. equity value) and 04 (multiples — P/E does a lot of work here). No DCF needed; the merger model is accounting, not forecasting infinity.

## 1. The question underneath every deal headline

When a company announces an acquisition, its shareholders immediately want to know one thing: **will my slice of earnings per share get bigger or smaller?** If pro forma EPS (the combined company's EPS after the deal) is higher than the acquirer's standalone EPS, the deal is *accretive* — each existing share now claims more earnings. If it's lower, the deal is *dilutive* — each share claims less.

This is not a subtle concept, but its importance is easy to underestimate. Three reasons bankers and investors obsess over it:

**First, it's the deal's first impression.** The announcement-day stock reaction is driven more by the accretion/dilution math than by the strategic story. A deal announced as "20% accretive in year one" gets a hearing; a "15% dilutive" deal starts the call in a hole. Management teams know this, which is why the accretion figure is always on slide one of the announcement deck.

**Second, it's the currency politics of stock deals.** In an all-stock merger, the *exchange ratio* — how many acquirer shares each target share receives — is negotiated partly by staring at the accretion math. Target shareholders want a rich ratio; acquirer shareholders want the deal accretive. The merger model is the spreadsheet where that negotiation gets quantified.

**Third, it disciplines the price.** Accretion analysis is the fastest reality check on whether you're overpaying. If you need heroic synergy assumptions to make a deal merely *breakeven* on EPS, the price is probably too high. Bankers compute "breakeven synergies" — the synergy number that gets accretion to exactly zero — as a matter of routine, and it often tells you more than the headline synergy target does.

Now the three levels, per this series' habit. The *intuition* (combining two income statements and dividing by the new share count tells you whether each share earns more) is rock solid. The *strict conclusions* (the algebraic conditions for accretion in pure stock or pure cash deals — derived below) are non-negotiable. The *judgment calls* (whether the synergies are real, whether "adjusted" EPS is the right denominator of truth) are where deals are won, lost, and occasionally misrepresented.

## 2. The pro forma income statement: stitching two companies together

A **merger model** is, at its core, a pro forma income statement: what the combined company's P&L looks like after the deal closes. Building it is mechanical. There are five steps, and every one of them is just careful bookkeeping.

**Step 1: Add the two standalone income statements.** Acquirer net income plus target net income. This is your baseline — the "nothing changes" world.

**Step 2: Add synergies.** The extra earnings the combination creates: cost savings (closing duplicate headquarters, combined purchasing) and revenue synergies (cross-selling, pricing power). Synergies phase in over time — bankers model a *realization schedule* (say, 50% in year one, 100% by year two), because no synergy arrives on closing day.

**Step 3: Subtract the cost of paying.** This is where the consideration mix matters:
- *Cash funded by debt:* new interest expense, after tax.
- *Cash from the balance sheet:* foregone interest income on the cash you spent, after tax. (Spending $300m of cash that earned 3% costs you $9m of pre-tax income. People forget this one constantly.)
- *Stock:* no P&L cost at all — but the share count goes up, which is where the dilution shows up instead.

**Step 4: Subtract purchase-accounting adjustments.** When you buy a company for more than the book value of its assets, accountants make you allocate the premium. Identifiable intangible assets (customer relationships, patents, trademarks) get written up and then *amortized* — a new annual D&A charge that depresses reported earnings for years. PP&E gets stepped up to fair value and depreciated faster. (Goodwill — the leftover premium — is *not* amortized under US GAAP; it's tested for impairment. A common exam-trap distinction.) These charges are non-cash, but they hit GAAP EPS, so they hit the accretion math.

**Step 5: Divide by the new share count.** Acquirer shares plus any shares issued to target shareholders. Compare the result to the acquirer's standalone EPS.

That last step is the whole reveal. Let's see it in action.

## 3. A full worked example: Crestfield buys Northline

Meet the players — both fictional, both deliberately ordinary, because merger math is clearest on boring companies.

**Crestfield Holdings** (the acquirer), an industrial distributor:
- Revenue $2,000m, EBITDA $300m (15% margin)
- D&A $60m → EBIT $240m
- Interest $20m → EBT $220m; tax at 25% = $55m
- **Net income: $165m**
- 55 million shares at $60 → market cap $3,300m, **EPS $3.00**, P/E 20.0x

**Northline Industrial** (the target), a smaller rival distributor:
- Revenue $800m, EBITDA $120m (15% margin)
- D&A $30m → EBIT $90m
- Interest $6m → EBT $84m; tax at 25% = $21m
- **Net income: $63m**
- 42 million shares at $18 → equity value $756m (P/E 12.0x)

**Deal terms.** Crestfield offers **$20 per share** — an 11.1% premium. Equity value: 42m × $20 = **$840m**. Target net debt is $60m, so enterprise value = $900m (7.5x EBITDA — reasonable for the sector).

**Consideration: 60% stock / 40% cash.**
- Stock portion: 60% × $840m = $504m. At Crestfield's $60 share price, that's 8.4m new shares — or **0.20 shares per target share** (each target shareholder gets 0.20 Crestfield shares plus cash).
- Cash portion: 40% × $840m = $336m — **$8.00 cash per target share** — funded entirely with new debt at 7%.

**Synergies.** Run-rate by end of year two: $30m of cost savings (one distribution center closed, combined procurement) plus $12m of revenue synergies at a 40% incremental margin ($4.8m of EBITDA). Total run-rate synergy EBITDA: **$34.8m**. Year-one realization: 50% of cost savings ($15m) and 40% of revenue synergies ($1.92m) → **$16.92m** of year-one synergy EBITDA.

**Purchase accounting.** Identifiable intangibles written up by $240m, amortized straight-line over 12 years → $20m/year. PP&E stepped up $50m, depreciated over 5 years → $10m/year. Total **D&A step-up: $30m/year** (non-cash, but it hits EPS).

**Transaction fees:** $18m, one-time. After tax: $13.5m.

Now the year-one pro forma:

| Pro forma build, year 1 | $m |
|---|---|
| Crestfield standalone net income | 165.00 |
| + Northline standalone net income | 63.00 |
| + Synergies, after tax: $16.92m × (1 − 25%) | 12.69 |
| − New interest, after tax: $336m × 7% × (1 − 25%) | (17.64) |
| − D&A step-up, after tax: $30m × (1 − 25%) | (22.50) |
| **= Pro forma net income (adjusted, excl. one-time fees)** | **200.55** |
| − Transaction fees, after tax | (13.50) |
| = Pro forma net income (GAAP) | 187.05 |
| ÷ Pro forma shares: 55.0m + 8.4m | 63.4m |
| **Pro forma adjusted EPS** | **$3.16** |
| Pro forma GAAP EPS | $2.95 |

Against Crestfield's standalone $3.00:

- **Adjusted basis: +5.5% accretive.** ($3.16 vs. $3.00)
- **GAAP basis: −1.7% dilutive.** ($2.95 vs. $3.00)

Read that twice, because it's the single most useful lesson in this article: **the same deal is accretive and dilutive at the same time**, depending on whether you count one-time fees. This is why every announcement deck says "accretive" with an asterisk, and why the asterisk deserves your full attention. Bankers and management almost always present *adjusted* (or "cash") EPS — excluding one-time fees and sometimes excluding the D&A step-up too — while GAAP EPS tells the unvarnished story. Neither is lying; they're answering different questions. Your job is to know which question is being answered.

The intuition for *why* this deal is structurally accretive (before the fees) is worth isolating, because it generalizes. Northline's earnings yield on the purchase price is $63m / $840m = **7.5%**. The two things Crestfield "pays" with both cost less than that: the stock portion costs the acquirer's earnings yield ($165m / $3,300m = **5.0%**), and the cash portion costs the after-tax borrowing rate (7% × 0.75 = **5.25%**). When you buy earnings at a 7.5% yield using currency that costs you 5.0–5.25%, each share ends up owning more earnings. The D&A step-up ($22.5m after tax) is a drag, but the synergies ($12.69m) and the yield spread cover it with room to spare.

That logic compresses into two clean rules — the shortcut math of section 4.

## 4. The shortcut math: two rules that explain most deals

You don't always need the full model. For pure-consideration deals with no synergies, accretion reduces to a comparison of two yields.

**Rule 1 — all-stock deal.** The deal is accretive if and only if the *target's P/E is lower than the acquirer's P/E* (equivalently, the target's earnings yield exceeds the acquirer's). Here's why, in one derivation:

```math
EPS_{pro\ forma} = \frac{NI_A + NI_T}{S_A + S_{new}} > \frac{NI_A}{S_A} = EPS_A
```

New shares issued: $S_{new} = \frac{m_T \cdot NI_T}{P_A}$, where $m_T$ is the P/E paid for the target and $P_A$ the acquirer's share price. Cross-multiplying (everything positive):

```math
(NI_A + NI_T) \cdot S_A > NI_A \cdot \left(S_A + \frac{m_T \cdot NI_T}{P_A}\right)
```

```math
NI_T \cdot S_A > NI_A \cdot \frac{m_T \cdot NI_T}{P_A} \quad \Rightarrow \quad \frac{P_A \cdot S_A}{NI_A} > m_T
```

The left side is the acquirer's P/E ($m_A$). So: **accretive ⟺ $m_A > m_T$**. You're paying for the target's earnings with shares priced at a richer multiple than the multiple you're paying — buying earnings at 13.3x with currency valued at 20x. Check our example: Crestfield at 20.0x buys Northline at $840m/$63m = 13.3x. 20 > 13.3, so the stock portion is accretive — consistent with the full model.

**Rule 2 — all-cash deal funded with debt.** Accretive if and only if the *target's earnings yield exceeds the after-tax cost of debt*:

```math
EPS_{pf} = \frac{NI_A + NI_T - r(1-t) \cdot V_T}{S_A} > \frac{NI_A}{S_A}
\iff \frac{NI_T}{V_T} > r(1-t)
```

You're borrowing at rate $r$ to buy an earnings stream yielding $NI_T/V_T$. If the earnings yield beats the borrowing cost, EPS rises. In our example: 7.5% > 5.25% ✓.

**Mixed deals blend the two.** Think of the consideration as a portfolio: each dollar of target earnings bought with stock "costs" the acquirer's earnings yield; each dollar bought with debt costs the after-tax interest rate. The weighted-average cost of the consideration, versus the target's earnings yield, determines accretion before synergies and accounting adjustments.

And **synergies shift the boundary**. The standard question — *breakeven synergies* — asks how much synergy is needed for exactly zero accretion. In our example, without any synergies, adjusted pro forma EPS would be $(165 + 63 − 17.64 − 22.50)/63.4 = \$2.96$ — about 1.2% dilutive. Closing a 4-cent gap on 63.4m shares needs just $2.3m of after-tax earnings, i.e. roughly **$3.1m of pre-tax synergies**. That's a trivial hurdle against a $30m cost-synergy plan, which tells you this deal is *structurally* accretive — it doesn't depend on heroic synergy assumptions. When you see a deal whose breakeven synergies are 80% of the announced target, you're looking at a deal priced for perfection.

## 5. Why accretion gets gamed — and why "accretive" is not "good"

Here is the uncomfortable truth the conference call never mentions: **accretion measures accounting, not value.** A deal can be accretive and destroy shareholder value, and a deal can be dilutive and create it. The merger model answers "does EPS go up?" — but shareholders should be asking "did we buy these earnings for less than they're worth?"

Four ways the confusion plays out in practice:

**The P/E arbitrage illusion.** A company trading at 30x earnings buys a slower-growing company at 12x. By Rule 1, the deal is massively accretive — reported EPS jumps. But nothing real happened: the acquirer just stapled a lower-multiple earnings stream onto its own. If the market was pricing the acquirer's 30x multiple on *its* growth profile, and the combined company now grows more slowly, the multiple compresses and shareholders lose — despite the "accretive" headline. Accretion from multiple arbitrage is financial engineering wearing a strategy costume.

**The leverage trick.** Debt is cheap, especially when rates are low. By Rule 2, almost any cash deal funded with cheap debt is accretive — you're buying a 7% earnings yield with 3% after-tax money. But leverage adds risk that EPS doesn't show: the interest is fixed, the earnings aren't. An accretive levered deal can still be a bad deal if the target's earnings are cyclical and the debt can't flex. EPS counts the return; it never counts the risk.

**The timing game.** Accretion is usually quoted for *year one*. But synergies are back-ended, integration costs are front-ended, and the D&A step-up lingers for a decade. A deal can be dilutive in year one, accretive by year three — or the reverse, if year-one accretion was manufactured by excluding every inconvenient charge as "one-time." Always ask: accretive *when*, and on *whose definition* of earnings?

**Growth vs. yield.** A dilutive deal can be excellent: buying a fast-growing target at a high P/E is dilutive today (Rule 1 — high $m_T$), but if the target's earnings compound at 25%, the dilution reverses within a couple of years and the NPV is strongly positive. Conversely, buying a declining business at 6x is accretive forever and value-destructive forever. EPS is a one-year snapshot; value is a lifetime.

The academic evidence backs the skepticism. Loughran, T. & Vijh, A. (1997), "Do Long-Term Shareholders Benefit from Corporate Acquisitions?", *Journal of Finance* — studying 947 acquisitions — found that over the five years after closing, acquirers in **stock mergers earned excess returns of −25.0%**, while acquirers in **cash tender offers earned +61.7%**. The market's long-run verdict on stock-financed deals — the ones most engineered for headline accretion — is brutal. (One reading, consistent with Myers & Majluf (1984) from our reading list: paying with stock signals that management thinks its own shares are overvalued — expensive currency for a reason.)

And Moeller, S., Schlingemann, F. & Stulz, R. (2004), "Firm size and the gains from acquisitions", *Journal of Financial Economics*, showed that acquirer announcement returns **fall with acquirer size** — small acquirers gain, large acquirers' shareholders systematically lose. The deals with the most elaborate accretion presentations tend to come from the largest acquirers, where empire-building incentives are strongest. When the deck has forty pages of accretion analysis and two pages of strategy, notice the ratio.

The honest use of accretion analysis is narrower and more useful: it's a **pricing discipline tool**. Compute the deal's accretion with *zero* synergies, with *management's* synergies, and the breakeven synergy number. If the deal needs the full synergy plan just to break even on EPS, the price leaves no margin for error — and synergy plans, as every integration team will tell you, are where optimism goes to be audited.

## 6. Common Misconceptions

**"Accretive means the deal creates value."** No. Accretion is an EPS comparison; value creation is an NPV comparison (price paid vs. present value of incremental cash flows, per articles 06–07). They often disagree, and when they do, NPV is the one that matters.

**"Stock deals are always dilutive."** Only if the target's P/E exceeds the acquirer's (Rule 1). High-multiple acquirers routinely do accretive stock deals — which is exactly the P/E arbitrage trap described above.

**"Cash deals are always accretive."** Only if the target's earnings yield beats the after-tax funding cost (Rule 2). Pay 25x earnings with 8% debt and the deal is dilutive on day one.

**"Synergies are basically guaranteed — management committed to them."** Synergy realization rates are the most lied-about number in M&A. Cost synergies (cutting overlap) realize at high rates; *revenue* synergies (cross-selling, "one plus one equals three") realize far less often, because they require customers to cooperate. Discount revenue synergies heavily, and never let a deal's accretion depend on them.

**"Purchase accounting doesn't matter — it's non-cash."** It doesn't affect cash flow, but it affects reported EPS, debt covenants tied to accounting ratios, and management compensation tied to EPS. That's why "cash EPS" (adding back the D&A step-up) exists as a separate disclosure — useful, but also a convenient place to bury the cost of overpaying.

**"Year-one accretion is the number that matters."** Bankers show a two-to-three-year accretion profile for a reason: the *crossover year* (when a dilutive deal turns accretive) and the *steady-state* accretion tell you whether the dilution is a timing artifact or a structural overpay.

## 7. Test Yourself

**Q1.** In our example, suppose Crestfield instead funds the *entire* $840m equity purchase with new debt at 7% (no stock issued). No synergies, no D&A step-up, ignore fees. Is the deal accretive or dilutive, and by how much?

*Answer.* Pro forma NI = 165 + 63 − 840 × 7% × (1 − 25%) = 165 + 63 − 44.10 = $183.90m. Shares stay 55m. EPS = 183.90/55 = **$3.34**, vs. $3.00 standalone → **+11.5% accretive**. Check with Rule 2: target earnings yield = 63/840 = 7.5% > after-tax debt cost 5.25% ✓. (Notice: more accretive than the actual mixed deal — because replacing 5.0%-yield stock currency with 5.25%-cost debt *raised* the blended cost slightly? No — wait. The all-debt deal is *more* accretive here because there's no share-count increase at all. The stock portion of the real deal added 8.4m shares; avoiding that dilution outweighs the slightly higher cost of debt. Good illustration that the share count is half the story.)

**Q2.** Now suppose it's an *all-stock* deal at the same $20/share offer price, no synergies, no adjustments. Accretive or dilutive?

*Answer.* New shares = 840/60 = 14.0m; total 69.0m. EPS = (165 + 63)/69.0 = **$3.30** → **+10.1% accretive**. Check with Rule 1: acquirer P/E 20.0 > target P/E 13.3 ✓. Both pure structures are accretive here — this target is simply cheap relative to both of Crestfield's currencies.

**Q3.** Back to the actual mixed deal (with the $30m D&A step-up and $16.92m year-one synergies, adjusted basis). Management's synergy plan slips: only $8m of pre-tax synergies materialize in year one. Still accretive?

*Answer.* After-tax synergy contribution: 8 × 0.75 = $6.0m. Pro forma NI = 165 + 63 + 6.0 − 17.64 − 22.50 = $193.86m. EPS = 193.86/63.4 = **$3.06** → still **+1.9% accretive**, but the margin for error is nearly gone — consistent with the breakeven-synergy calculation (~$3.1m pre-tax) from section 4. This is the number the board should have stared at before approving the price.

**Q4.** A CEO boasts: "This acquisition is 15% accretive to EPS in year one." Give two reasons a shareholder might still vote against the deal.

*Answer.* Any two of: (1) the accretion comes from P/E arbitrage — stapling a low-multiple, low-growth business onto a high-multiple one, which may compress the combined multiple; (2) it's funded with debt, adding financial risk EPS doesn't capture; (3) the 15% is on *adjusted* EPS that excludes the D&A step-up and "one-time" integration costs — GAAP accretion may be far lower or negative; (4) year-one accretion says nothing about NPV — if the price exceeded the present value of incremental cash flows (articles 06–07 test), value was destroyed regardless; (5) the long-run evidence (Loughran & Vijh 1997) says stock-financed acquirers underperform badly over five years.

---

*Next up: article 10, The Football Field and Fairness Opinions — how bankers lay every valuation method side by side into one picture, triangulate a range, and what a fairness opinion actually promises (less than you'd think).*
