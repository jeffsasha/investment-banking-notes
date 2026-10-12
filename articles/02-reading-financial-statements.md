# 02 | Reading Financial Statements Like a Banker

*Open any 10-K and you'll drown in two hundred pages of numbers. Bankers don't read all of it. They read three statements as one machine, pull five numbers, and know within minutes whether the business is healthy — or held together with accounting tape. This article builds that machine from scratch, with every number tied out by hand.*

> **Learning goals.** After this article you can: (1) explain how the income statement, balance sheet, and cash flow statement link into one system; (2) trace any transaction through all three statements; (3) build a cash flow statement from the other two with the indirect method; (4) name the five numbers a banker pulls first and why; (5) spot the three most common earnings-quality red flags.
>
> **Prerequisites.** Article 01. Basic vocabulary: revenue, expense, asset, liability. No modeling experience needed.

## 1. One Machine, Three Views

Intuition first. A company is a machine that turns inputs (cash, materials, labor) into outputs (products, services) and back into cash. The three financial statements are three views of the same machine:

- The **income statement** (P&L) answers: *did the machine make money this period?*
- The **balance sheet** answers: *what does the machine own and owe right now?*
- The **cash flow statement** answers: *where did the cash actually go?*

One equation governs all of accounting — the **accounting identity**:

```math
\text{Assets} = \text{Liabilities} + \text{Equity}
```

Read it as: everything the company owns (assets) was paid for either by borrowing (liabilities) or by its owners (equity). There is no third source of funding. Every transaction keeps this equation balanced, because every transaction is recorded in at least two places at once — the **double-entry** idea. Buy a machine with cash: cash falls, equipment rises, both sides still equal.

Two linkages weld the three statements into one system, and bankers check them the way a pilot checks fuel gauges — first, and without thinking:

1. **Net income flows into retained earnings.** $\text{Ending retained earnings} = \text{Beginning} + \text{Net income} - \text{Dividends}.$ Profit that isn't paid out stays inside the company and shows up on the balance sheet.
2. **Ending cash ties to the cash flow statement.** $\text{Ending cash} = \text{Beginning cash} + \text{net change in cash}.$ If the cash flow statement says cash rose by $\$770$ but the balance sheet disagrees, something is broken — full stop.

Keep those two in your head. Everything below is just detail.

## 2. The Income Statement: Profit on Paper

The income statement measures performance over a *period* — a quarter, a year — using **accrual accounting**: revenue is recorded when it is *earned*, expenses when they are *incurred*, regardless of when cash changes hands. Sell $\$900$ of goods on credit in December and collect the cash in January? December shows the revenue. This is the **revenue recognition** principle, paired with the **matching principle**: record the cost of those goods (COGS, cost of goods sold) in the *same* period as the revenue they produced, so each period's profit reflects the economics of what actually happened.

Meet our teaching company — **Apex Industrial Co.**, founded this year, selling one product. Its Year 1 events:

1. The founder puts in $\$1{,}000$ cash for shares.
2. Apex buys equipment for $\$600$ cash (useful life: 6 years).
3. Apex buys $\$500$ of raw materials **on credit** — the supplier gets paid later.
4. Apex sells $\$900$ of product: $\$700$ collected in cash, $\$200$ on credit (customers pay later). The goods sold cost $\$450$ to make.
5. Apex incurs $\$200$ of **SG&A** (selling, general & administrative — salaries, rent): $\$160$ paid in cash, $\$40$ owed at year-end.
6. **Depreciation**: the $\$600$ equipment is "used up" evenly over 6 years → $\$600/6 = \$100$ per year of depreciation. This is a **non-cash expense**: no cash leaves the building, but the asset's book value falls.
7. Apex borrows $\$200$ at 10% interest → $\$20$ of interest, paid in cash.
8. Apex pays suppliers $\$350$ of the $\$500$ owed.
9. Income tax at 25% — accrued (owed at year-end, not yet paid).

Apex's income statement:

| Line | \$ | Why |
|---|---|---|
| Revenue | 900 | earned in Year 1 (even the \$200 not yet collected) |
| − COGS | (450) | matched to the units actually sold |
| **Gross profit** | **450** | 50% gross margin ($450/900$) |
| − SG&A | (200) | operating costs of the period |
| **EBITDA** | **250** | before interest, tax, depreciation |
| − Depreciation | (100) | non-cash: equipment "used up" |
| **EBIT** | **150** | operating profit |
| − Interest | (20) | cost of the debt |
| **EBT** | **130** | earnings before tax |
| − Tax @ 25% | (32.5) | accrued, not paid |
| **Net income** | **97.5** | left for shareholders |

Definitions, since this series defines every term on first use:

- **EBITDA** (earnings before interest, taxes, depreciation & amortization): a rough proxy for the cash the operations throw off before financing decisions and accounting choices. Bankers live on this number — comps, DCF, and LBO models all start here.
- **EBIT** (operating profit): what the business earned from operations after recognizing that its assets wear out.
- **Net income** ("the bottom line"): what's left for shareholders after everyone else — suppliers, employees, lenders, the tax authority — has been paid.

Now notice the tension that drives this entire article: net income is $\$97.5$, yet the company collected $\$700$ in cash from customers and spent far more than that. Profit and cash are different things — the next two sections exist because of that gap.

## 3. The Balance Sheet: Who Owns What, Right Now

If the income statement is a movie (a period of time), the balance sheet is a photograph (a point in time): what the company owns and owes *at year-end*. Apex's:

**Assets** — what it owns:

| Asset | \$ | |
|---|---|---|
| Cash | 770 | $1{,}000 - 600 + 700 - 160 + 200 - 20 - 350$ |
| Accounts receivable (AR) | 200 | customers who owe us |
| Inventory | 50 | bought \$500, used \$450 in COGS |
| PP&E, net | 500 | equipment \$600 minus \$100 depreciation |
| **Total assets** | **1,520** | |

**Liabilities** — what it owes:

| Liability | \$ | |
|---|---|---|
| Accounts payable (AP) | 150 | bought \$500 of materials, paid \$350 |
| Accrued liabilities | 40 | SG&A owed but not yet paid |
| Debt | 200 | the loan |
| Taxes payable | 32.5 | tax accrued, not yet paid |
| **Total liabilities** | **422.5** | |

**Equity** — what's left for the owners:

| Equity | \$ | |
|---|---|---|
| Share capital | 1,000 | the founder's investment |
| Retained earnings | 97.5 | this year's net income, kept in the business |
| **Total equity** | **1,097.5** | |

Tie-out: $\$422.5 + \$1{,}097.5 = \$1{,}520$ ✓. The identity holds.

Three things a banker sees in this photograph that a beginner misses:

1. **Book value is not market value.** Equity on the books is $\$1{,}097.5$, but no buyer would pay exactly that — market value reflects *future* cash flows, which is what articles 04–07 teach you to estimate. The balance sheet records history at cost, not value.
2. **Net debt matters more than debt.** $\text{Net debt} = \text{debt} - \text{cash} = 200 - 770 = -\$570.$ Negative net debt means a **net cash** position: Apex could repay every dollar of debt tomorrow and still hold cash. Bankers always net the cash — enterprise value (article 03) is built on exactly this move.
3. **Working capital is cash trapped in operations.** $\text{AR} + \text{inventory} - \text{AP} = 200 + 50 - 150 = \$100$ is tied up funding customers and stock. Growing companies routinely show rising profits alongside *falling* cash because working capital eats it — and the cash flow statement is where that shows up.

## 4. The Cash Flow Statement: Follow the Money

Accrual accounting is useful, but it can lie by omission: it tells you profit, not cash. The cash flow statement reconciles the two, sorting every cash movement into three buckets:

- **Operating (CFO)** — cash from running the business day to day.
- **Investing (CFI)** — cash spent on or earned from long-term assets: equipment, acquisitions, asset sales.
- **Financing (CFF)** — cash between the company and its funders: issuing shares, borrowing, repaying debt, paying dividends.

The **indirect method** — the one bankers actually use — starts from net income and undoes every accrual:

```math
\text{CFO} = \text{Net income} + \text{non-cash expenses} - \Delta\text{operating assets} + \Delta\text{operating liabilities}
```

Why those signs? Depreciation was *subtracted* to reach net income, but no cash left — so add it back. AR *rose* by $\$200$: we booked $\$200$ of revenue without collecting a dollar — subtract it. AP *rose* by $\$150$: we booked $\$500$ of materials but paid only $\$350$ — add it back. The rule of thumb: **a rise in an operating asset uses cash; a rise in an operating liability provides cash** (and vice versa). Tattoo it on your brain — you'll use it daily.

Apex's cash flow statement:

| | \$ |
|---|---|
| Net income | 97.5 |
| + Depreciation (non-cash) | 100.0 |
| − Increase in AR | (200.0) |
| − Increase in inventory | (50.0) |
| + Increase in AP | 150.0 |
| + Increase in accrued liabilities | 40.0 |
| + Increase in taxes payable | 32.5 |
| **Cash flow from operations** | **170.0** |
| Purchase of equipment | (600.0) |
| **Cash flow from investing** | **(600.0)** |
| Equity issued | 1,000.0 |
| Debt borrowed | 200.0 |
| **Cash flow from financing** | **1,200.0** |
| **Net change in cash** | **770.0** |
| Beginning cash | 0.0 |
| **Ending cash** | **770.0** |

Verify it three independent ways, because bankers never trust a single tie-out:

1. **Balance sheet tie** — ending cash $\$770$ matches the balance sheet ✓.
2. **Direct count** — cash in: $\$700$ (customers) $+ \$1{,}000$ (founder) $+ \$200$ (loan) $= \$1{,}900$; cash out: $\$600$ (equipment) $+ \$160$ (SG&A) $+ \$20$ (interest) $+ \$350$ (suppliers) $= \$1{,}130$; net $\$770$ ✓.
3. **The story reads right** — operations generated $\$170$, the equipment cost $\$600$, and the founder plus the lender funded the gap.

Now the punchline of this whole article: **net income was $\$97.5$, but cash rose $\$770$** — and neither number alone tells the story. Profit understates cash here (depreciation is non-cash, and financing cash isn't profit). In a fast-growing company the reverse is the classic trap: profits climbing while cash *falls*, because working capital and capex devour it. The cash flow statement is the lie detector for the income statement.

## 5. The Four Linkages (Your Tie-Out Checklist)

When a banker opens a model — yours, a client's, anyone's — they verify four links before trusting a single output:

1. **Net income → retained earnings.** Ending RE $=$ beginning RE $+$ net income $-$ dividends. Here: $\$0 + \$97.5 - \$0 = \$97.5$ ✓.
2. **Non-cash expenses add back.** Depreciation of $\$100$ reduced net income but not cash — CFO adds it back ✓.
3. **Capex lives in investing, not in profit.** The $\$600$ equipment never touched this year's income statement (only its $\$100$ of depreciation did) — it sits in CFI ✓. Confusing capex with an expense is the classic beginner error, and it breaks every valuation built on top.
4. **ΔCash ties to the balance sheet.** $\text{CFO} + \text{CFI} + \text{CFF} = 170 - 600 + 1{,}200 = 770$, which equals ending cash ✓.

Memorize these. In interviews, "walk me through the three statements" is really asking you to prove you own these four links — usually with a twist. The favorite: *depreciation rises by $\$10$; what happens?* Net income falls $\$7.5$ after 25% tax; then CFO $= -\$7.5$ (NI) $+ \$10$ (add-back) $- \$2.5$ (smaller rise in taxes payable, since the tax bill itself shrank) $=$ **unchanged**. Note the subtlety: the famous "depreciation tax shield" only becomes *cash* when the tax is actually paid in cash — here the tax was merely accrued, so the shield just shrinks a payable. (Test Yourself Q1 makes you prove it.)

## 6. The Five Numbers Bankers Pull First

A banker opening any company's statements doesn't read top to bottom. They pull five numbers:

**1. Revenue growth.** Is the top line growing — and is the growth real (more volume, better pricing) or bought (acquisitions)? One year tells you nothing; bankers want three to five years of trend.

**2. EBITDA and EBITDA margin.** Apex: EBITDA $= \$250$, margin $= 250/900 \approx 27.8\%$. The *trend* in margin matters more than the level: a margin sliding from 30% to 22% over three years screams pricing pressure or cost creep, even while revenue grows.

**3. Free cash flow.** The cash the business generates after keeping itself running — the single number every DCF discounts (articles 06–07):

```math
\text{UFCF} = \text{EBIT}(1-t) + \text{D\&A} - \text{CapEx} - \Delta\text{NWC}
```

For Apex: $\$150 \times 0.75 + \$100 - \$600 - \$27.5$. Here $\Delta\text{NWC} = \Delta(\text{AR} + \text{inventory} - \text{AP} - \text{accrued} - \text{taxes payable}) = 200 + 50 - 150 - 40 - 32.5 = 27.5$. So $\text{UFCF} = 112.5 + 100 - 600 - 27.5 = -\mathbf{\$415}$. Negative — but look at *why*: a one-time $\$600$ equipment purchase in year one. A banker doesn't panic at a negative; they ask what *normalized* capex looks like. Cross-check via the CFO bridge: $\text{CFO} - \text{CapEx} + \text{interest}(1-t) = 170 - 600 + 20 \times 0.75 = -415$ ✓. Two routes, same answer — that's how you know the arithmetic is honest.

**4. Net debt and leverage.** Net debt $= 200 - 770 = -\$570$ (net cash — Apex is unlevered). Two ratios decide how much debt any deal can support, and the entire LBO article (08) is built on them: **leverage** $=$ net debt $/$ EBITDA, and **interest coverage** $=$ EBIT $/$ interest $= 150/20 = 7.5\times$.

**5. Cash conversion.** How much of EBITDA actually becomes cash? Roughly $(\text{CFO} - \text{maintenance capex}) / \text{EBITDA}$. Apex's CFO of $\$170$ versus EBITDA of $\$250$ — the gap is working capital build ($\$200$ AR $+$ $\$50$ inventory, partly offset by $\$150$ AP). The banker's question: is that a one-time build as the business scales, or are customers paying slower every year (rising **DSO**, days sales outstanding)? Only the trend answers it.

## 7. Reading Like a Banker: Earnings Quality

Two companies can report identical net income with very different honesty. Three red flags:

1. **Accruals growing faster than cash.** Net income climbing year after year while CFO stagnates or falls means profits are being manufactured — through receivables games, aggressive revenue recognition, or under-reserved expenses. The cash flow statement is the detector. This is precisely why it exists.
2. **Capitalizing what should be expensed.** Moving a cost off the income statement and onto the balance sheet (calling it an "asset") boosts today's profit at the expense of tomorrow's. Software development costs, "prepaid" expenses that never reverse, and a permanently growing "other assets" line all deserve skepticism.
3. **EBITDA adjustments that never end.** "Adjusted EBITDA" that adds back "one-time" restructuring charges *every single year* isn't adjusting — it's marketing. Bankers do normalize earnings, but they heavily discount adjustments that recur.

The through-line: **trust cash first, profit second, and always ask what had to be assumed** to produce each number. Useful lives, tax rates, bad-debt reserves — every one is a judgment call, and judgment calls lean optimistic when bonuses depend on them.

---

## Common Misconceptions

- **"Profit equals cash."** The most expensive sentence in finance. Profit follows accrual rules; cash follows the bank account. Apex earned $\$97.5$ while its cash rose $\$770$ — same company, same year, two different questions answered.
- **"The balance sheet shows what the company is worth."** It shows historical cost minus depreciation, not value. A brand, a customer list, a great engineering team often appear nowhere on it — yet buyers pay billions for exactly those. Articles 04–07 explain how.
- **"Depreciation is meaningless because it's non-cash."** It's non-cash *today*, but it measures a real economic cost: the equipment will need replacing. Ignore it forever and you can "profitably" run a company into the ground — which is why UFCF subtracts capex.
- **"More debt is always bad."** Debt is a tool: it funds growth, and its interest is tax-deductible — Apex's $\$20$ of interest saved $\$5$ in tax ($20 \times 25\%$). The question is never "debt or no debt" but "can the cash flows service it" — coverage and leverage ratios, section 6.

## Test Yourself

**Q1.** Apex's depreciation increases by $\$10$ (tax rate 25%, all else equal — and the tax bill is still *accrued*, not paid). What happens to net income, CFO, and ending cash? Then: how would the answer change if taxes were paid in cash?
*A1. EBT falls $\$10$ → the tax accrual falls $\$2.5$ → net income falls $\$7.5$ (to $\$90$). CFO $= -\$7.5$ (NI) $+ \$10$ (D&A add-back) $- \$2.5$ (smaller rise in taxes payable) $= \$0$ change — CFO stays $\$170$, and ending cash stays $\$770$, because no cash tax was ever paid: the "shield" merely shrinks a payable. Balance-sheet check: PP&E $-\$10$, taxes payable $-\$2.5$, retained earnings $-\$7.5$ → $-\$10 = -\$10$ ✓. If taxes were paid in cash instead, the $\$2.5$ lower tax bill would mean $\$2.5$ less cash out the door — CFO and ending cash would both rise $\$2.5$. That's the textbook "depreciation tax shield" version.*

**Q2.** A company reports net income of $\$50$m growing 20% a year, but CFO has been flat at $\$10$m for three years. Name two specific things you'd investigate first.
*A2. (1) Receivables and revenue recognition — is AR growing faster than revenue (channel stuffing, looser payment terms to book sales early)? (2) Capitalized costs or working-capital games — expenses parked on the balance sheet instead of the P&L, or payables stretched to flatter CFO temporarily. Either way: profits without cash always need an explanation.*

**Q3.** Compute Apex's UFCF starting from CFO instead of EBIT, and confirm it matches $-\$415$.
*A3. $\text{UFCF} = \text{CFO} - \text{CapEx} + \text{interest}\times(1-t) = 170 - 600 + 20 \times 0.75 = 170 - 600 + 15 = -\mathbf{\$415}$ ✓ — same as $\text{EBIT}(1-t) + \text{D\&A} - \text{CapEx} - \Delta\text{NWC}$.*

**Q4.** Why does a banker subtract cash to get net debt instead of just looking at total debt?
*A4. Because cash can repay debt tomorrow — what matters for risk and valuation is debt net of immediately available repayment capacity. Enterprise value (article 03) values the operations; netting cash cleanly separates operating value from the cash sitting on the balance sheet.*

---

*Next up — **03 | Enterprise Value vs Equity Value: The Bridge**: why bankers value the whole firm instead of just the shares, and the bridge that connects the two.*
