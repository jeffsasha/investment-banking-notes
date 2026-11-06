# 27 | Valuing Banks and Financial Institutions: Why P/E Breaks and P/B Works

*Every valuation tool you have learned so far — DCF, comps, precedent transactions — was built for companies that make things, sell things, or provide services. Then you meet your first bank, and the whole toolkit starts misfiring. Debt is not leverage here; it is the raw material. Free cash flow is not measurable. And the multiple every banker reaches for first is not P/E but P/B. This article explains why banks are different, and how to value them anyway.*

> **Learning goals.** After this article you can: (1) explain why enterprise value, EV/EBITDA, and free cash flow to the firm break down for banks; (2) value a bank with a two-stage dividend discount model, including the terminal price-to-book step; (3) compute a bank's excess capital from its CET1 ratio and explain why it matters for valuation; (4) derive the justified P/B formula from the Gordon growth model and use it to judge whether a bank's market P/B is high or low; (5) run a simple cross-sectional P/B–ROE regression and know what it can and cannot tell you.
>
> **Prerequisites.** Article 03 (enterprise value vs equity value) for why EV exists at all, article 04 (trading multiples) for how P/E and P/B normally behave, article 06 (DCF I) for WACC and free cash flow, article 07 (DCF II) for terminal value, and article 13 (restructuring) for what happens when a leveraged balance sheet goes wrong. Damodaran (2013) is the backbone of sections 2–4; Wilcox (1984) underpins section 5.

## 1. A Bank Is Not a Company That Happens to Borrow a Lot

Start with the most natural mistake. You open a bank's balance sheet and it looks like a normal company, except the debt is enormous — often ten times equity or more. Your first instinct, trained by articles 03 and 06, is to compute enterprise value: market cap plus debt minus cash. Stop. For a bank, that number is meaningless, and the reason is simple once you see it: **for a bank, debt is not funding, it is inventory.**

A manufacturer borrows money to build a factory, then uses the factory to make products. Debt is a financing choice layered on top of the business. A bank takes deposits and borrows in wholesale markets, then lends that money out at a higher rate. The deposits *are* the business — they are the raw material that gets transformed into loans.

The same logic kills EV/EBITDA. EBITDA — earnings before interest, taxes, depreciation, and amortisation — exists to strip out financing decisions and show operating performance. But for a bank, interest is not a financing cost sitting below the operating line. Net interest income — interest earned on loans minus interest paid on deposits — *is* the operating line. It is the bank's gross margin, the equivalent of a retailer's revenue minus cost of goods sold. Stripping out interest from a bank's earnings is like stripping out the cost of goods sold from a retailer's earnings and calling the result operating profit. You have removed the business itself.

Free cash flow to the firm breaks for a related reason. FCFF needs three ingredients: operating cash flow, capital expenditure, and working capital. For a bank, none of the three is well defined. What is a bank's capital expenditure? A new branch is capex; a new loan is also an investment of cash, but it shows up as an asset on the balance sheet, not as capex. What is working capital? Deposits are technically liabilities, but treating a growing deposit base as a working-capital outflow — the way you would treat a manufacturer piling up inventory — would make a healthy, growing bank look cash-flow negative. The definitions that make a DCF work for an industrial company simply do not map onto a balance sheet whose assets and liabilities are both financial contracts. This is the starting point of Damodaran's argument in his paper on valuing financial service firms: the cash flows to a financial service firm cannot be easily estimated, because capital expenditure, working capital, and debt are not clearly defined for them (Damodaran, 2013).

So the first rule of bank valuation is a negative one: **do not value the firm. Value the equity, directly.** Everything in this article follows from that.

## 2. The Equity-Only Rule: Dividends, Not Free Cash Flow

If you cannot value the whole firm, value the shareholders' slice. There are three standard ways to do that, and for banks they collapse into one family:

- **Dividend discount model (DDM).** Value the shares as the present value of the dividends they will pay. This is the workhorse, and it is the model this article builds in full.
- **Free cash flow to equity (FCFE).** Value the cash the bank *could* pay out — actual or potential dividends. For a bank, "potential dividends" is the interesting phrase, because a bank can only pay what regulators let it pay. Section 4 is about exactly that constraint.
- **Residual income (excess return) model.** Value book equity today plus the present value of future earnings above the cost of equity. It is mathematically the same answer as the DDM if you are consistent, and it is often the cleaner way to think about a bank, because a bank's book value is meaningful in a way a manufacturer's often is not. A bank's assets are mostly loans and securities marked — at least approximately — to market.

The practical point: for a bank, the dividend discount model is not a textbook curiosity you learn and then abandon, the way it is for industrial companies. It is the primary tool. Damodaran's conclusion is blunt: financial service firms are best valued using equity valuation models rather than enterprise valuation models, and with actual or potential dividends rather than free cash flow to equity (Damodaran, 2013).

One thing to get straight before we build the model: the discount rate is the **cost of equity**, not WACC. WACC blends the cost of debt and equity, and we just established that a bank's debt is not financing — it is inventory. There is no meaningful WACC for a bank. The cost of equity, usually estimated from CAPM — risk-free rate plus beta times the equity risk premium — is the only discount rate in play. A typical large US bank's cost of equity sits around 9–11%. We will use 10% in the worked example.

## 3. The Dividend Discount Model, Worked End to End

Let us value a fictional bank, Meridian Bancorp. The numbers are invented, but the structure is exactly what a FIG (financial institutions group) analyst runs in Excel.

**The facts.** Meridian has 500 million shares outstanding. Book value of equity is $10,000 million, so book value per share (BVPS) is $20.00. Net income is $1,500 million, so return on equity (ROE) is 15%. The cost of equity is 10%. Meridian pays out 40% of earnings as dividends and retains 60%.

**Stage 1: five years of high growth.** When a bank retains earnings, its book value grows, and if ROE holds steady, earnings grow at the same rate. This is the sustainable growth formula you met in article 06:

```math
g = ROE \times \text{retention ratio}
```

Here g = 15% × 60% = 9% per year. Earnings per share start at $3.00 (15% × $20.00) and grow at 9%; dividends are 40% of earnings each year.

| Year | EPS | DPS (40% payout) | BVPS (end of year) |
|:----:|----:|-----------------:|-------------------:|
| 0 | $3.00 | — | $20.00 |
| 1 | $3.27 | $1.308 | $21.80 |
| 2 | $3.56 | $1.426 | $23.76 |
| 3 | $3.89 | $1.554 | $25.90 |
| 4 | $4.23 | $1.694 | $28.23 |
| 5 | $4.62 | $1.846 | $30.77 |

Check the arithmetic on one row so you trust the table: EPS in year 1 is $3.00 × 1.09 = $3.27; DPS is $3.27 × 40% = $1.308; BVPS grows by retained earnings, $20.00 × 1.09 = $21.80. The rest of the table is the same machinery, year after year.

**Stage 2: terminal value via P/B.** After year 5 we assume Meridian matures: ROE fades to 12%, growth fades to 3%, and the cost of equity stays at 10%. Instead of projecting dividends forever, we value the bank at the end of year 5 using the justified P/B formula that section 5 derives in full. For now, take it as given:

```math
\frac{P}{B} = \frac{ROE - g}{k_e - g} = \frac{0.12 - 0.03}{0.10 - 0.03} = \frac{0.09}{0.07} = 1.29\times
```

Terminal price at the end of year 5 = 1.29 × BVPS at year 5 = 1.29 × $30.77 = $39.56.

**Discount everything at 10%.** The present values of the five dividends:

| Year | DPS | Discount factor | PV of dividend |
|:----:|----:|----------------:|---------------:|
| 1 | $1.308 | 0.9091 | $1.19 |
| 2 | $1.426 | 0.8264 | $1.18 |
| 3 | $1.554 | 0.7513 | $1.17 |
| 4 | $1.694 | 0.6830 | $1.16 |
| 5 | $1.846 | 0.6209 | $1.15 |

The five dividends are worth $5.84 in today's money. The terminal price is worth $39.56 × 0.6209 = $24.57. Add them:

```math
\text{Value per share} = \$5.84 + \$24.57 = \$30.40
```

Meridian's intrinsic value is about **$30.40 per share**, or 1.52× its current book value of $20.00. If the market price is $36, the model says the market is paying 1.8× book for a bank whose fundamentals justify 1.52× — either the market expects a higher ROE than 12% in maturity, a lower cost of equity than 10%, or the stock is expensive. That is the whole game: the model does not give you a price, it gives you a way to interrogate the market's price.

Notice one thing about the numbers: the five years of dividends contribute less than a fifth of the value. The terminal value does the heavy lifting, exactly as it did in the industrial DCF of article 07. The sensitivity is brutal — raise the terminal ROE from 12% to 13% and the terminal P/B becomes (0.13 − 0.03)/(0.10 − 0.03) = 1.43×, terminal price $43.97, and value per share rises to about $33.13. One percentage point of long-run ROE is worth roughly $2.70 a share. That is why bank analysts obsess over whether a bank's ROE is sustainable or a cyclical peak.

## 4. Excess Capital: The Dividend a Bank *Could* Pay

The DDM above uses actual dividends. But banks are special in a second way: they are not free to pay whatever they can afford. Regulators require them to hold minimum capital, and that constraint shapes value. This is where the concept of **excess capital** comes in.

The key regulatory ratio is the **Common Equity Tier 1 (CET1) ratio**:

```math
\text{CET1 ratio} = \frac{\text{Common Equity Tier 1 capital}}{\text{Risk-weighted assets (RWA)}}
```

Risk-weighted assets are the bank's assets weighted by how risky the regulator thinks they are — a Treasury bond counts for almost nothing, a subprime loan counts heavily. Under the Basel framework, large banks typically must hold CET1 of at least 7% of RWA (the 4.5% minimum plus the 2.5% capital conservation buffer), and systemically important banks face surcharges on top. In practice, most large banks target 10–12%.

Suppose Meridian has risk-weighted assets of $80,000 million and CET1 capital of $10,000 million — a CET1 ratio of 12.5%. If its effective requirement, including buffers and its own target, is 10%, it needs $8,000 million of CET1 and holds **$2,000 million of excess capital** — $4.00 per share. That $4.00 is, in principle, distributable: the bank could pay it out as a special dividend or buy back shares without breaching its requirement, subject to the annual regulatory stress test.

Why does this matter for valuation? Because a bank that is over-capitalised is sitting on cash that earns almost nothing, and the market will not pay a full multiple for trapped capital. A bank with a 15% ROE on its *required* capital but only 10% on its *total* capital, because a third of its equity is idle excess, is a different investment from a bank earning 15% on all of it. When you see a bank trading below book value, the first question to ask is whether it is over-capitalised — and whether management has a credible plan to return the excess. Conversely, a bank trading above book value with a thin CET1 ratio is fragile: one bad stress-test result and the dividend gets cut.

The honest version of the DDM for a bank therefore values *potential* dividends — actual dividends plus the distribution of excess capital over time — not just the dividend the bank happens to pay today. A bank paying a 40% payout ratio while sitting on $2 billion of excess capital is under-distributing, and a careful analyst adds the eventual release of that capital into the model.

## 5. P/B and ROE: The One Relationship That Matters

If there is a single chart a bank analyst lives by, it is P/B against ROE. The intuition is simple: a bank that earns more than its cost of equity creates value on every dollar of book equity, so the market pays more than a dollar for each dollar of book. A bank that earns less than its cost of equity destroys value, so the market pays less than a dollar. The Gordon growth model makes this precise.

Start with the Gordon formula for a bank in steady state: price equals next year's dividend divided by the cost of equity minus growth. Next year's dividend is next year's earnings times the payout ratio, and earnings are ROE times book value. The payout ratio, in steady state, is whatever is left after retaining enough to fund growth: payout = 1 − g/ROE. Put it together:

```math
P_0 = \frac{D_1}{k_e - g} = \frac{ROE \times B_0 \times (1 - g / ROE)}{k_e - g}
```

Simplify, and the dividend and the earnings both disappear:

```math
\frac{P_0}{B_0} = \frac{ROE - g}{k_e - g}
```

This is the **justified P/B formula**. It says a bank's fair price-to-book depends on exactly three things: its ROE, its growth rate, and its cost of equity. Test it on Meridian's steady state: ROE 15%, growth 5%, cost of equity 10%.

```math
\frac{P}{B} = \frac{0.15 - 0.05}{0.10 - 0.05} = \frac{0.10}{0.05} = 2.0\times
```

Price = 2.0 × $20.00 = $40.00. And you can verify it through the dividend route: EPS is $3.00, the payout ratio is 1 − 5%/15% = 66.7%, so DPS is $2.00, and $2.00 / (10% − 5%) = $40.00. Same answer, two paths. If the formulas ever disagree, you have made an arithmetic error — the two derivations are the same statement.

Now test the formula on a weak bank. Same $20.00 book value, but ROE of 8% against a 10% cost of equity, growing at 3%:

```math
\frac{P}{B} = \frac{0.08 - 0.03}{0.10 - 0.03} = \frac{0.05}{0.07} = 0.71\times
```

Price = 0.71 × $20.00 = $14.29 — a 29% discount to book. The bank earns less than its cost of equity, so each dollar of book value is worth less than a dollar. This is not a market inefficiency. It is the market correctly saying that capital trapped in a sub-cost-of-equity business is worth less than the capital itself. The formal version of this idea goes back to Wilcox (1984), whose P/B–ROE model in the *Financial Analysts Journal* showed that price-to-book is fundamentally a function of return on equity, growth, and the required return — the same three variables in the formula above.

Three corollaries worth remembering. First, **growth is only valuable if ROE exceeds the cost of equity**. Raise growth from 5% to 7% for the strong bank and P/B rises from 2.0× to (0.15 − 0.07)/(0.10 − 0.07) = 2.67×. Do the same for the weak bank — growth 3% to 5% — and P/B *falls* from 0.71× to (0.08 − 0.05)/(0.10 − 0.05) = 0.60×. Growing a value-destroying business faster destroys more value. Second, **P/B of 1.0× is not "cheap" by itself**. It is the price for a bank earning exactly its cost of equity in steady state (set ROE = k_e in the formula and P/B = 1). Third, **book value is only as good as the balance sheet**. If the loans are overstated — if provisions for bad loans are too low — book value is a fiction, and P/B is a trap. The 2008 crisis was, among other things, a mass discovery that bank book values were overstated.

## 6. A P/B–ROE Regression Across Peers

The formula tells you what P/B *should* be, given ROE. A regression tells you what the market *actually* pays. Bankers run both and compare them. Take four illustrative US regional banks:

| Bank | ROE | P/B |
|:-----|----:|----:|
| Cascade Bancorp | 8% | 0.7× |
| Harbor Financial | 12% | 1.4× |
| Meridian Bancorp | 15% | 2.0× |
| Summit Bank | 18% | 2.4× |

A simple linear regression through these points gives roughly:

```math
\frac{P}{B} \approx -0.66 + 17 \times ROE
```

For a bank earning 13% ROE, the market line predicts P/B of about −0.66 + 17 × 0.13 = 1.55×. If that bank actually trades at 1.9×, it is expensive relative to its peers' ROE — unless there is a reason: a better deposit franchise, a cleaner loan book, a faster-growing wealth business. The regression is a screening tool, not a verdict. It tells you where to look, not what to conclude.

And be careful what goes into the regression. A proper version controls for growth expectations and risk (beta, or the cost of equity) as well as ROE, because the justified-P/B formula says all three matter. A regression on ROE alone will flatter a high-ROE bank that is taking wild risks to get there. Also, never mix banks with different business models in one regression: a custody bank, a credit-card lender, and a mortgage bank have different ROEs for structural reasons, and the market knows it.

## 7. What Else Bankers Actually Check

P/B and the DDM are the valuation core, but a bank analyst's day is mostly spent on the operating details that determine whether the ROE in the model is real. Four things matter most:

**Net interest margin (NIM).** Net interest income divided by average earning assets — the spread between what the bank earns on loans and pays on deposits, and the single biggest driver of earnings. The deposit franchise — how cheaply and how stickily a bank funds itself — is the moat. Banks with sticky, low-cost deposits (checking accounts that pay almost nothing) lend at the same rate as everyone else and keep more of it.

**The efficiency ratio.** Non-interest expense divided by total revenue (net interest income plus fees). Lower is better; 50–60% is normal for a large bank, below 50% is excellent. It is the bank's cost discipline in one number, and it is where management credibility shows up fastest.

**Asset quality.** Non-performing loans as a percentage of total loans, and the provision for credit losses. A bank can report a wonderful ROE for years by under-provisioning — booking too little for loans that will go bad — and then the losses arrive all at once. If loan growth is much faster than the economy and provisions are falling, be suspicious. This is the lesson of every banking crisis, and the reason book value cannot be taken on trust.

## Common Misconceptions

**"A bank trading below book value is a bargain."** Sometimes — if the discount reflects temporary fear and the ROE is about to recover above the cost of equity. But the justified-P/B formula says a bank earning below its cost of equity *should* trade below book. The discount is the market's verdict, not a pricing error. The bargain case needs a specific reason the ROE will rise: a cost-cutting programme, a rate environment that widens NIM, a release of excess capital. "It is below book" is not, by itself, a reason.

**"P/E is the right multiple for banks because earnings are what matter."** Earnings matter, but P/E for a bank is hostage to the provisioning cycle and to leverage. Two banks with the same P/E can have very different ROEs and very different capital levels, because P/E ignores the balance sheet entirely. P/B forces you to confront the balance sheet: how much capital is behind those earnings, and what return that capital earns. That is why FIG bankers lead with P/B and use P/E as a cross-check, not the other way round.

**"Higher growth is always better for a bank's valuation."** Only if ROE exceeds the cost of equity. Section 5 showed the arithmetic: growing a sub-cost-of-equity bank faster *lowers* its justified P/B. Loan growth that chases volume at thin spreads, or an acquisition that dilutes ROE, destroys value even while the bank gets bigger. Bankers who brag about loan growth without mentioning the ROE on that growth are selling you something.

**"The dividend discount model is too simple for a real bank."** It is simple in structure and ferociously sensitive in practice — one point of terminal ROE moved our valuation by 9%. That sensitivity is not a flaw in the model; it is the truth about banks. A bank's value genuinely does hinge on whether it can sustainably earn above its cost of equity. The model's job is to make that hinge visible and to force you to state your assumption, not to hide it behind complexity.

## Test Yourself

**1.** A bank has book value per share of $50, ROE of 14%, a cost of equity of 11%, and steady-state growth of 4%. What is its justified P/B, and what is the implied share price? Verify the price through the dividend route.

*Answer: Justified P/B = (0.14 − 0.04)/(0.11 − 0.04) = 0.10/0.07 = 1.43×. Implied price = 1.43 × $50 = $71.43. Check: EPS = 14% × $50 = $7.00; payout = 1 − 4%/14% = 71.4%; DPS = $7.00 × 71.4% = $5.00; price = $5.00/(0.11 − 0.04) = $71.43. The two routes agree.*

**2.** Meridian Bancorp from section 3 trades at $36.00. Using the two-stage model (value $30.40), is it overvalued or undervalued — and what single assumption change would most plausibly justify the market price?

*Answer: Overvalued by about 18% on the model's assumptions ($36.00 vs $30.40). The most plausible justification is a higher terminal ROE: the market may expect Meridian to sustain more than 12% ROE in maturity. A terminal ROE of roughly 14% would lift the terminal P/B to (0.14 − 0.03)/(0.10 − 0.03) = 1.57×, terminal price to about $48.36, and value per share to roughly $35.87 — essentially the market price. Alternatively the market may be pricing a lower cost of equity or the release of excess capital that the model ignores.*

**3.** A bank has risk-weighted assets of $120,000 million, CET1 capital of $13,200 million, and an effective CET1 requirement of 10%. How much excess capital does it hold, and what is the value per share if it has 600 million shares outstanding?

*Answer: CET1 ratio = $13,200/$120,000 = 11.0%. Required CET1 = 10% × $120,000 = $12,000 million. Excess capital = $13,200 − $12,000 = $1,200 million, or $2.00 per share — distributable in principle, subject to the stress test and board approval.*

**4.** Two banks both grow book value at 6% a year. Bank A earns 16% ROE with a 10% cost of equity; Bank B earns 9% ROE with a 10% cost of equity. Which bank benefits from growing faster, and by how much does each bank's justified P/B move if growth rises to 8%?

*Answer: Only Bank A benefits. Bank A: P/B at 6% growth = (0.16 − 0.06)/(0.10 − 0.06) = 2.50×; at 8% growth = (0.16 − 0.08)/(0.10 − 0.08) = 4.00× — growth adds value because ROE exceeds the cost of equity. Bank B: P/B at 6% = (0.09 − 0.06)/(0.10 − 0.06) = 0.75×; at 8% = (0.09 − 0.08)/(0.10 − 0.08) = 0.50× — faster growth destroys value, because every new dollar of book earns 9% against a 10% cost.*

## References

- Damodaran, A. (2013). *Valuing Financial Service Firms.* Journal of Financial Perspectives, 1(1), 59–74. — The case for equity models and actual or potential dividends over enterprise valuation and FCFF for banks, insurers, and investment banks. (Working paper version, April 2009.)
- Wilcox, J. W. (1984). *The P/B–ROE Valuation Model.* Financial Analysts Journal, 40(1), 58–66. — The formal link between price-to-book, return on equity, growth, and the required return.

*Next up: Valuing Real Estate Companies: NAV, FFO, and Cap Rates — how to value the companies that own the buildings, a toolkit that will feel familiar if you have ever underwritten a property.*
