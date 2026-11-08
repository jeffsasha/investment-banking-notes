# 28 | Valuing Real Estate Companies: NAV, FFO, and Cap Rates

*Article 27 taught you that a bank breaks every valuation tool because its debt is its raw material. Real estate breaks the toolkit in the opposite direction: here the debt is ordinary, the assets are buildings you can walk through, and the earnings number on the income statement is designed to mislead you. A real estate company reports depreciation on buildings that usually go up in value, and the industry had to invent its own earnings metric to fix it. This article is about that fix, and the three numbers every real estate analyst lives by: NOI, the cap rate, and NAV.*

> **Learning goals.** After this article you can: (1) build net operating income (NOI) from a rent roll and explain what it includes and excludes; (2) derive the cap rate from the Gordon growth model and use it to value a single property; (3) value a REIT property by property with net asset value (NAV) and explain the premium or discount to NAV; (4) compute funds from operations (FFO) and adjusted funds from operations (AFFO) from GAAP net income and explain why both exist; (5) compute a REIT's implied cap rate from its market value and compare it with private-market cap rates.
>
> **Prerequisites.** Article 02 (financial statements) for how depreciation flows through the income statement, article 03 (enterprise value) for the bridge between equity value and firm value, article 06 (DCF I) for the Gordon growth model and WACC, and article 07 (DCF II) for terminal value. NAREIT (1991) is the backbone of section 5; Geltner (1991) underpins the warning about appraisals in section 4.

## 1. A Building Is Not a Factory

Start with the instinct you have built up over the last 27 articles: to value a company, you look at its earnings, you apply a multiple or discount its cash flows, and you adjust for debt. Then you open the accounts of a real estate investment trust — a REIT — and the first number you meet is net income, and net income is wrong. Not slightly wrong. Structurally wrong, by design.

The reason is depreciation. Under GAAP, a company that owns a building must depreciate it over its useful life — typically 27.5 years for residential property and 39 years for commercial property in the US. Each year, a slice of the building's historical cost is charged against earnings as if the building were wearing out. For a factory machine, that is roughly fair: machines do wear out. For a well-maintained office tower in a growing city, it is fiction. The building's market value usually rises while its book value falls. A REIT can report falling net income year after year while its properties get more valuable and its rents go up. If you value it on P/E, you are pricing a fiction.

There is a second difference, the mirror image of the bank problem in article 27. For a bank, enterprise value was meaningless because debt is inventory. For a property company, enterprise value works fine — debt is ordinary financing — but the operating line is different from anything you have seen. A property company's revenue is rent, its operating cost is the cost of keeping the building running, and the difference is called **net operating income**, or **NOI** — the single most important number in real estate:

```math
\text{NOI} = \text{effective gross income} - \text{operating expenses}
```

Note what is missing. NOI excludes interest, taxes on the company's income, depreciation, amortisation, and capital expenditure. It is the cash the property throws off before financing and before accounting conventions get involved. A building collects rent and pays to keep the lights on. The difference is NOI.

One more thing to get straight before we build anything. Real estate is valued in two different markets at the same time, and they do not always agree: the **private market**, where buildings change hands in negotiated deals and values come from appraisals, and the **public market**, where REIT shares trade every second. A REIT can trade at a discount to the value of its own buildings, and often does — and that gap is itself one of the most useful signals in the sector. Section 4 explains how to measure it.

## 2. The Cap Rate: One Number That Prices a Building

If NOI is the income a building produces, the **capitalisation rate** — the cap rate — is the price of that income. It is the yield a buyer demands on a property, and it converts NOI into value with a single division:

```math
\text{Value} = \frac{\text{NOI}}{\text{cap rate}}
```

That is direct capitalisation — how most commercial property is actually priced: one year's NOI and one market cap rate, not a ten-year DCF. For a stabilised building, the cap rate *is* the DCF, compressed into one number. Here is why.

Take the Gordon growth model from article 06: the value of a perpetually growing cash flow is next year's cash flow divided by the discount rate minus the growth rate. Apply it to a building, with NOI as the cash flow:

```math
V_0 = \frac{\text{NOI}_1}{r - g}
```

Compare that with the direct capitalisation formula. The cap rate must be:

```math
\text{cap rate} = r - g
```

The cap rate is the discount rate minus the expected growth rate of NOI. That one line explains almost everything about how cap rates behave. When interest rates rise, the discount rate rises, and cap rates rise — which means values fall. When a market's rents are expected to grow fast, the cap rate is lower, and values are higher. A warehouse in a booming logistics market might trade at a 5% cap rate; a struggling suburban office park might trade at 9%. The difference is not that one building is "better" — it is that the market demands a higher yield to hold the riskier, slower-growing asset.

Let us price a building. A mid-rise office building in Houston — call it the Travis Tower — has next-twelve-months NOI of $4.8 million, and comparable office buildings in the market are trading at a 6.0% cap rate. Its value is:

```math
V = \frac{\$4.8\text{ million}}{0.06} = \$80.0\text{ million}
```

Now watch how sensitive that number is. If interest rates rise and the market cap rate moves from 6.0% to 6.5%, the same building is suddenly worth $4.8 / 0.065 = \$73.8$ million — down 7.7%. If cap rates compress to 5.5%, it is worth $4.8 / 0.055 = \$87.3$ million — up 9.1%. Half a percentage point of cap rate moves the value by roughly 8%. That is why real estate people talk about cap rates the way bond people talk about yields.

## 3. NOI: Building It from the Rent Roll

The cap rate formula looks trivial, which means all the real work — and all the ways to get fooled — lives inside NOI. Here is how you build it.

Start at the top with **gross potential rent**: what the building would collect if every square foot were leased at market rent. Say the tower has 200,000 square feet at $50 per square foot per year: gross potential rent of $10.0 million.

Then subtract **vacancy and collection loss**. No building is ever 100% occupied, and some tenants do not pay. At 5% vacancy, that is $0.5 million, leaving **effective gross income** of $9.5 million.

Then subtract **operating expenses** — everything it costs to run the building:

| Expense | Amount |
|:--------|-------:|
| Property taxes | $1.5m |
| Insurance | $0.5m |
| Maintenance and repairs | $1.0m |
| Property management | $0.6m |
| Utilities | $1.1m |
| **Total operating expenses** | **$4.7m** |

```math
\text{NOI} = \$9.5\text{m} - \$4.7\text{m} = \$4.8\text{m}
```

There it is — the $4.8 million from section 2. But three details in this table are where analysts earn their keep.

**First, above- and below-market rents.** The rent roll shows what tenants are *contractually* paying, not what the space would fetch today. If a tenant signed a ten-year lease in 2019 at $62 per square foot and market rent is now $50, that tenant is overpaying — and when their lease expires, the rent falls. A seller who capitalises today's NOI without adjusting for that is selling you a shrinking income stream. The mirror image is below-market rent, which is upside waiting for the lease to roll. Always ask when each lease expires, and how far contract rent sits from market rent?

**Second, capital expenditure is not in NOI, but it is real.** The roof, the elevators, the lobby renovation — none of that appears in operating expenses. Two buildings with the same NOI can have wildly different capex needs, and the buyer who ignores that overpays. This is exactly why the industry invented AFFO in section 5: to put the capex back in.

**Third, the expense ratio is a smell test.** Operating expenses of $4.7 million on effective gross income of $9.5 million is an expense ratio of about 49%. For an office building, 40–55% is normal; for an industrial warehouse it might be 15–25%, because the tenant pays most costs directly. If a seller shows you an office building with a 30% expense ratio, they have probably left something out.

## 4. NAV: Valuing a REIT Property by Property

A single building is priced by direct capitalisation. A REIT — a company that owns dozens or hundreds of buildings — is priced the same way, one building at a time, and the sum is called **net asset value**, or NAV: the real estate analyst's sum-of-the-parts (article 15), with properties as the parts and the cap rate as the method.

Let us value a fictional REIT, Bayou Realty Trust, a Houston-based landlord with three properties:

| Property | NOI | Market cap rate | Value |
|:---------|----:|----------------:|------:|
| Downtown office tower | $12.0m | 6.5% | $184.6m |
| Industrial warehouse | $6.0m | 5.5% | $109.1m |
| Retail strip centre | $4.0m | 7.0% | $57.1m |
| **Total gross asset value** | **$22.0m** | | **$350.8m** |

Check one row: the office tower at $12.0 million of NOI divided by a 6.5% cap rate is $12.0 / 0.065 = \$184.6$ million. Notice the cap rates differ by property type — industrial lowest (strongest expected rent growth, lowest risk), retail highest. That is the market's judgement, embedded in three numbers.

Now build the NAV. Gross asset value is $350.8 million. Subtract the debt of $200.0 million and other liabilities of $10.0 million, add back cash of $5.0 million:

```math
\text{NAV} = \$350.8\text{m} - \$200.0\text{m} - \$10.0\text{m} + \$5.0\text{m} = \$145.8\text{m}
```

Bayou has 10 million shares outstanding, so NAV per share is \$145.8 / 10 = **\$14.58**. If Bayou's shares trade at $13.00, the REIT trades at a **discount to NAV** of:

```math
\frac{\$13.00 - \$14.58}{\$14.58} = -10.8\%
```

Is that a buying opportunity? Sometimes — REITs trading at wide discounts to NAV have historically been where activists and acquirers go shopping (article 17's playbook applies here too). But the discount can also be the market's verdict: the appraised cap rates may be stale, the office tower's tenants may be about to leave, or management may have a record of overpaying. A discount to NAV is a question, not an answer.

And here is the uncomfortable part: NAV itself rests on appraisals, and appraisals are slow. An appraiser values a building partly by looking at what similar buildings sold for and partly by looking at the last appraisal — a process the literature calls smoothing. Geltner (1991) showed that appraisal-based returns understate true volatility because appraisers anchor on past estimates, and Cannon and Cole (2011), studying 25 years of NCREIF data, found appraisals on average more than 12% above or below the eventual sale price, lagging the market in both directions — too low in hot markets, too high in cold ones. When the market turns, appraised NAV is the last number to know.

## 5. FFO and AFFO: Why Net Income Lies for REITs

NAV values the properties. But a REIT is also an operating company, and investors need an earnings number to put a multiple on. GAAP net income is the wrong number, for the depreciation reason in section 1. So in 1991 the industry association NAREIT created its own metric — **funds from operations**, or FFO — and it has been the headline REIT earnings number ever since:

```math
\text{FFO} = \text{net income} + \text{real estate depreciation} - \text{gains on property sales}
```

Three adjustments, each with a logic. Add back real estate depreciation, because buildings do not wear out the way the accounting assumes. Subtract gains on property sales, because selling a building is not operating performance — it is a one-off, and leaving it in would let a REIT manufacture "growth" by selling its best assets. The result is a measure of recurring operating profit from owning and leasing buildings.

Let us compute it for Bayou Realty Trust. Suppose Bayou reports GAAP net income of $8.0 million, real estate depreciation of $9.5 million, and a $2.0 million gain on the sale of a small property:

```math
\text{FFO} = \$8.0\text{m} + \$9.5\text{m} - \$2.0\text{m} = \$15.5\text{m}
```

With 10 million shares, FFO per share is **$1.55**. At a share price of $13.00, Bayou trades at a **P/FFO multiple** of $13.00 / \$1.55 = $8.4\times$. That is the number REIT analysts quote the way other analysts quote P/E — except it is P/FFO, because P/E is meaningless here. A typical large-cap REIT trades at 12–20× FFO; Bayou at 8.4× looks cheap, consistent with its discount to NAV. Both metrics tell the same story.

But FFO has its own flaw: it ignores capital expenditure. A landlord that spends heavily on tenant improvements and leasing commissions — the cost of signing new tenants — can report healthy FFO while bleeding cash. So analysts compute **adjusted funds from operations**, or AFFO, which subtracts recurring capex and straight-line rent adjustments:

```math
\text{AFFO} = \text{FFO} - \text{recurring capex} - \text{straight-line rent adjustments}
```

For Bayou: recurring capex of $3.0 million and straight-line rent adjustments of $1.0 million give AFFO of \$15.5 − \$3.0 − \$1.0 = **\$11.5 million**, or **$1.15 per share**. AFFO is the closest thing to a REIT's true cash earnings, and it is the right denominator for the dividend: Bayou pays a dividend of $0.90 per share, which is an **AFFO payout ratio** of $0.90 / \$1.15 = 78\%$. That is a normal, sustainable ratio for a REIT — most target 70–85%. A REIT paying out more than 100% of AFFO is paying its dividend out of asset sales or new debt, and that cannot go on forever.

One honest caveat: AFFO is not standardised. Unlike FFO, which NAREIT defines, each REIT defines AFFO slightly differently — what counts as "recurring" capex is a judgement call, and management has an incentive to define it narrowly. Always read the reconciliation in the earnings supplement.

## 6. The Implied Cap Rate: What the Stock Market Thinks the Buildings Are Worth

NAV tells you what the appraisers think the buildings are worth. The share price tells you what the stock market thinks. The bridge between them is the **implied cap rate**: the cap rate the market is implicitly applying to the REIT's portfolio.

Take Bayou. Its market capitalisation is 10 million shares × $13.00 = $130.0 million. Add debt of $200.0 million and other liabilities of $10.0 million, subtract cash of $5.0 million, and you get an enterprise value of $335.0 million — the market's price for the whole portfolio. The portfolio produces NOI of $22.0 million. So:

```math
\text{Implied cap rate} = \frac{\$22.0\text{m}}{\$335.0\text{m}} = 6.6\%
```

Now compare: the appraisers' weighted average cap rate on the same portfolio is \$22.0 / \$350.8 = 6.3\%. The stock market applies 6.6% — a higher yield, a lower value. That gap is the same 11% discount to NAV from section 4, expressed in yield terms. It is the cleaner way to compare across REITs, because it strips out leverage: two REITs with the same buildings but different debt levels have different NAV discounts and share prices, but the same implied cap rate if the market values their buildings identically.

The implied cap rate is also how you compare public and private real estate directly. If private-market office buildings trade at a 6.0% cap rate and a listed office REIT implies 7.0%, either the REIT is cheap, or the market expects its NOI to fall, or the private-market transactions are stale. In 2022–2023 that gap blew out across the sector, and the appraisals caught up later. When public and private disagree, the public market is usually early, not wrong.

## 7. What Else Analysts Actually Check

NOI, the cap rate, NAV, FFO, and the implied cap rate are the valuation core. But a real estate analyst's day is mostly spent on the operating details that determine whether the NOI in the model is real:

**Leverage and debt maturity.** Bayou has $200 million of debt against $350.8 million of gross assets — a loan-to-value ratio of 57%, normal for a REIT. But the maturity schedule is what keeps analysts up at night: a REIT might have nothing due for two years, then $80 million maturing in a single quarter, when refinancing is expensive or unavailable. Always look at the maturity ladder, and at what share of the debt is fixed-rate versus floating.

**Lease expiry and WALT.** The weighted average lease term — WALT — is the average time until the REIT's leases expire, weighted by rent. A long WALT (seven-plus years) means income is locked in; a short WALT (two years) means the REIT is constantly re-leasing space, and its NOI is hostage to the rental market.

**Same-store NOI growth.** The cleanest measure of whether a landlord is doing a good job: NOI growth on properties owned in both periods, stripping out acquisitions and sales. If a REIT grows total NOI by 8% but same-store NOI by 1%, it is buying growth, not creating it. Same-store growth of 3–5% is healthy; negative same-store growth is a red flag no acquisition can hide.

## Common Misconceptions

**"A high cap rate means a better investment."** A high cap rate means the market demands a high yield — because the asset is risky, the leases are short, the rents are expected to fall, or the market is illiquid. A 9% cap rate building is not a bargain; it is a building the market has priced for trouble. And a cap rate is not a return: a buyer paying 6% earns 6% of first-year income yield *plus* NOI growth and appreciation — roughly an 8% total return if NOI grows at 2%. The bargain case needs a specific reason the market's judgement is wrong: rents about to rise, a lease about to roll to a better tenant, a neighbourhood about to turn.

**"FFO is a REIT's cash flow."** FFO is an accrual measure, not a cash measure — it starts from GAAP net income and adjusts for depreciation and gains. It ignores recurring capital expenditure entirely, which is real cash going out the door. AFFO is the closer proxy for cash earnings, and even AFFO depends on management's definition of "recurring" capex. Never underwrite a dividend on FFO alone.

**"NAV is what the REIT is worth, full stop."** NAV is an appraisal-based estimate, and appraisals lag the market and smooth volatility — Geltner (1991) and Cannon and Cole (2011) both document it. A REIT trading at a discount to NAV may be cheap, or its NAV may simply be out of date. The discount is a starting point for diligence, not a buy signal.

**"P/FFO and P/E are interchangeable."** They rhyme, but the denominators are different animals. FFO adds back depreciation that P/E leaves in, so a P/FFO of 15× is not "the same as" a P/E of 15×. Comparing a REIT's P/FFO with an industrial company's P/E is comparing two different definitions of earnings. Compare REITs with REITs, on P/FFO and on implied cap rates.

**"Depreciation means the buildings are wearing out, so adding it back is aggressive."** Depreciation is a tax and accounting convention based on historical cost. A well-located, well-maintained building usually appreciates. The honest question is not whether depreciation should be added back — it should — but whether the capex needed to keep the building competitive is being counted. That is what AFFO is for.

## Test Yourself

**1.** A retail property produces NOI of $3.6 million and trades at a 6.0% cap rate. What is its value? If rising rates push the market cap rate to 6.75%, what is the new value, and by what percentage has it fallen?

*Answer: Value = \$3.6m / 0.06 = \$60.0 million. At a 6.75% cap rate, value = \$3.6m / 0.0675 = \$53.3 million — a fall of (\$53.3 − \$60.0) / \$60.0 = −11.1%. Half a point of cap rate costs more than a tenth of the value.*

**2.** A REIT reports GAAP net income of $20.0 million, real estate depreciation of $18.0 million, and a $4.0 million gain on a property sale. It has 20 million shares outstanding. Recurring capex is $6.0 million and straight-line rent adjustments are $2.0 million. The share price is $25.50 and the dividend is $1.00 per share. Compute FFO per share, AFFO per share, the P/FFO multiple, and the AFFO payout ratio.

*Answer: FFO = \$20.0m + \$18.0m − \$4.0m = \$34.0m, or \$1.70 per share. AFFO = \$34.0m − \$6.0m − \$2.0m = \$26.0m, or \$1.30 per share. P/FFO = \$25.50 / \$1.70 = 15.0×. AFFO payout ratio = \$1.00 / \$1.30 = 76.9% — a sustainable dividend.*

**3.** A REIT has an enterprise value of $500 million and portfolio NOI of $30 million. What is its implied cap rate? If comparable private-market properties trade at a 5.5% cap rate, what would the portfolio be worth at that rate, and is the REIT trading at a discount or a premium to private-market value?

*Answer: Implied cap rate = \$30m / \$500m = 6.0%. At a 5.5% private-market cap rate the portfolio would be worth \$30m / 0.055 = \$545.5 million. The REIT's enterprise value of \$500 million is about 8.3% below that — it trades at a discount to private-market value, assuming the NOI and the cap rate comparison are both honest.*

**4.** A REIT's FFO per share rises 10% in a year, but its AFFO per share falls 5%. Give two plausible explanations, and say what you would check first.

*Answer: First, recurring capex may have jumped — heavy tenant improvements and leasing commissions to sign new tenants. FFO ignores capex, so it rises while the cash cost of generating that income eats AFFO. Second, straight-line rent adjustments may have grown — free-rent periods or step-up leases that flatter FFO without producing cash yet. Check the earnings supplement's AFFO reconciliation first: the capex and straight-line lines will tell you which one it is, and whether it is a one-year bulge or a structural cost of the portfolio.*

## References

- NAREIT (1991). *White Paper on Funds From Operations* (clarified 1995). — The industry definition of FFO: net income excluding gains on property sales, plus real estate depreciation and amortisation. The starting point for all REIT earnings analysis.
- Geltner, D. (1991). *Smoothing in Appraisal-Based Returns.* Journal of Real Estate Finance and Economics, 4(3), 327–345. — Why appraisal-based values understate true volatility: appraisers anchor on past estimates.
- Cannon, S. E. & Cole, R. A. (2011). *How Accurate are Commercial Real Estate Appraisals? Evidence from 25 Years of NCREIF Sales Data.* Journal of Portfolio Management, 37(5), 68–88. — Appraisals are on average more than 12% above or below subsequent sale prices, and lag the market in both directions.
- Gore, R. & Stott, D. (1999). *Toward a More Informative Measure of Operating Performance in the REIT Industry: Net Income vs. Funds from Operations.* SSRN working paper. — Evidence that FFO is more closely associated with REIT stock returns than GAAP net income.

*Next up: Real Estate Debt: CMBS, Mezzanine, and the Capital Stack — how a building's debt is sliced, sold, and priced, and why the bottom of the stack takes the first loss.*
