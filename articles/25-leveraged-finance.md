# 25 | Leveraged Finance: The Debt Behind the Deal

*Article 08 showed you an LBO from the buyer's side: borrow a lot, buy the company, and let its cash flows pay the debt down. But that article skipped the most interesting question — who actually lends that money, on what terms, and why do they agree? This one answers it. If the LBO is the deal, leveraged finance is the market that makes the deal possible.*

> **Learning goals.** After this article you can: (1) name the layers of a leveraged capital structure, in order of seniority, and explain what each layer gets in return for its risk; (2) size leverage as a multiple of EBITDA and test it with interest coverage and covenant math; (3) price a floating-rate loan from SOFR, spread, floor, and OID, and compare it honestly with a fixed-rate bond; (4) describe how a loan syndication works, including price flex in both directions; (5) explain why the same borrower can look safe to one lender and reckless to another.
>
> **Prerequisites.** Article 06 (DCF I) for the cost of debt, article 08 (LBO) for sources and uses, article 13 (restructuring) for what seniority means when things go wrong, and article 20 (debt capital markets) for how bonds are sold. Article 24 (private credit) is the natural companion piece: this article covers the syndicated, broadly distributed side of the same market.

## 1. The Product Group Behind the LBO

Inside an investment bank, **leveraged finance** — often shortened to LevFin — is the product group that arranges debt for borrowers that are too leveraged for the ordinary investment-grade bond market. Its clients are of two kinds: private equity sponsors doing buyouts, and companies that are already leveraged, whether by a past buyout, an acquisition, or a refinancing.

That definition needs unpacking, because "leveraged" is doing a lot of work. A borrower is not leveraged because it has debt in absolute dollars. It is leveraged because its debt is large relative to its cash flow. The standard yardstick, which you met in article 08, is:

```math
\text{Total leverage} = \frac{\text{Total funded debt}}{\text{EBITDA}}
```

**EBITDA** — earnings before interest, taxes, depreciation, and amortisation — is used here not because it is a perfect measure of cash flow (it is not; it ignores capital expenditure, working capital, and cash taxes), but because it is a rough, comparable proxy for the cash a business throws off before paying its lenders. **Funded debt** means debt that is actually drawn and owed — term loans and bonds — as opposed to a revolving credit facility that is committed but undrawn. A company with $1 billion of debt and $500 million of EBITDA is at 2.0x leverage. The same $1 billion against $150 million of EBITDA is 6.7x, and that is a very different credit.

LevFin sits between two neighbours you already know. On one side is Debt Capital Markets (article 20), which sells bonds for investment-grade companies that lenders compete to fund. On the other side is the LBO team and the sponsor coverage bankers, who bring the deal. LevFin is the group that structures the debt stack, talks to the lenders, and — crucially — commits to the financing before it knows for certain that the lenders will buy it. That commitment is what lets a sponsor bid with confidence, and it is why LevFin bankers get paid: they are selling certainty, and certainty has a price.

A useful mental model: the sponsor decides how much the company is worth and how much equity it will contribute. LevFin decides, with the market, how much debt the company's cash flows can carry, in what form, and at what price. If those two answers do not add up to the purchase price, the deal does not happen — or it happens at a lower price. This is the mechanism behind a finding you should keep in mind throughout this article: in a large sample of 1,157 buyouts from 1980 to 2008, Axelson, Jenkinson, Strömberg, and Weisbach (2013) found that buyout leverage was driven mainly by economy-wide credit conditions, not by the characteristics of the individual company, and that higher leverage went with higher purchase prices and lower subsequent fund returns. When credit is easy, buyers pay more. That is not a coincidence; it is the LevFin market doing its work, for better and for worse.

## 2. The Capital Structure, Layer by Layer

Think of a leveraged company's debt as a stack of claims on the same cash flows, ordered by who gets paid first. The order matters enormously, because in a restructuring (article 13) it decides who recovers money and who does not. From top — safest — to bottom — riskiest — a typical stack looks like this:

| Layer | What it is | Typical size | Secured? | Pricing style |
|---|---|---|---|---|
| Revolving credit facility ("revolver") | A credit line the company draws and repays as needed, like a corporate overdraft with a limit | Often $50–150 million of commitments, usually undrawn at close | Yes, first lien | Floating, lowest spread |
| First-lien term loan (TLB) | A funded loan, repaid over 5–7 years, sold to institutional investors | 3.0–4.0x EBITDA | Yes, first lien on substantially all assets | Floating: SOFR + spread |
| Second-lien term loan | A funded loan ranking behind the first lien on the same collateral | 0.5–1.5x EBITDA | Yes, but second in line | Floating, wider spread |
| Senior unsecured notes (high-yield bonds) | Bonds with no claim on specific assets | 1.0–2.0x EBITDA | No | Fixed coupon |
| Mezzanine / PIK notes | The riskiest debt, sometimes paying interest in additional debt rather than cash | 0.5–1.0x EBITDA | No, subordinated | Highest coupon, often part PIK |

A few definitions, because the jargon hides simple ideas. A **lien** is a legal claim on assets: a first-lien lender gets the proceeds of selling the collateral before a second-lien lender sees a dollar. **Senior** means paid first; **subordinated** means paid later. **Secured** means backed by specific collateral; **unsecured** means backed only by the company's general promise to pay. A **term loan B** (TLB) is simply the institutional version of a term loan: it is sold to funds and collateralised loan obligation (CLO) vehicles rather than held by the company's relationship banks, it usually amortises very slowly (often just 1% of principal per year, with the rest due as a bullet at maturity), and it is lightly covenanted — a point we return to in section 5.

Why stack debt this way instead of borrowing it all in one loan? Because different investors want different things. A CLO wants a floating-rate, secured, first-lien loan. A high-yield bond fund wants a fixed coupon and accepts being unsecured if the yield compensates it. A mezzanine fund wants equity-like upside and will accept payment-in-kind (PIK) interest — interest added to principal rather than paid in cash — for a much higher return. The stack matches each dollar of borrowing to the investor most willing to fund it; the banker's job is to know, tranche by tranche, what the market will bear this month, because the answer changes with credit conditions.

Notice what is *not* in the stack: equity. The sponsor's equity sits below all of this debt. It gets nothing until every lender is paid, and it is wiped out first if the company fails. That is the discipline of leverage from article 08, and it is also why lenders are willing to lend at all — there is a cushion of equity beneath them, and the sponsor loses its money before they lose theirs.

## 3. Sizing the Debt: How Much Is Too Much?

Lenders do not size debt by gut feeling. They start with EBITDA, adjust it, and then apply two tests: a leverage test and a coverage test.

**Adjusted EBITDA.** The EBITDA in a financing is rarely the EBITDA in the audited accounts. Sponsors present "adjusted EBITDA," which adds back one-off costs, adds expected cost savings from the deal ("synergies"), and sometimes adds the annualised effect of acquisitions. Some of these adjustments are legitimate — a genuinely one-off legal bill should not count against borrowing capacity. Some are heroic. Experienced lenders haircut the adjustments: they may accept half the claimed synergies, or none of them until they are actually delivered. A good habit when you read any LBO case: always ask what EBITDA would be *without* the adjustments, and re-run the leverage math on that number. The difference between headline leverage and unadjusted leverage is often the whole story of a deal that later struggles.

**The leverage test** is the multiple itself. Total debt divided by EBITDA, and senior-secured debt divided by EBITDA, are the two numbers every lender watches. In a typical large buyout in a normal credit market, total leverage might land around 5.0–6.0x EBITDA, with 3.5–4.5x of it senior secured. Those are not laws of nature; they are market conventions that tighten when lenders are nervous and loosen when they are competing for deals. That looseness is precisely the Axelson et al. (2013) finding in action: leverage is set by the credit cycle as much as by the company.

**The coverage test** asks whether the cash flow covers the interest bill with room to spare:

```math
\text{Interest coverage} = \frac{\text{EBITDA}}{\text{Cash interest expense}}
```

A coverage ratio of 2.0x means EBITDA is twice the interest bill: the company could lose half its EBITDA and still pay its lenders. A ratio of 1.2x means almost no margin for error. Lenders also look at a stricter version, sometimes called fixed-charge coverage, which puts mandatory debt amortisation and capital expenditure in the denominator alongside interest — because a company that can pay its interest but cannot fund its factories or repay its scheduled principal is still in trouble, just more slowly.

Both tests are backward-looking if you only use last year's EBITDA, and lenders know it. So the real sizing conversation is forward-looking: what does EBITDA look like in a bad year? LevFin bankers build a downside case — revenue down, margins compressed — and check that the company still covers its interest and does not breach its covenants in that case. If it does not, the debt stack is too big, whatever the headline multiple says. This is the single most useful discipline in leveraged finance: size the debt for the downside, not the pitch deck.

## 4. Pricing the Debt: SOFR, Spread, Floor, and OID

This is where the arithmetic lives, so let us do it carefully with one borrower carried through the whole article.

Meet **Meridian Packaging** (fictional). It makes industrial packaging, generates EBITDA of $200 million, and is being bought for an enterprise value of $1,600 million — 8.0x EBITDA. The financing, at close, is:

| Tranche | Amount | Leverage | Pricing |
|---|---|---|---|
| First-lien TLB | $600 million | 3.0x | SOFR + 375 bps, 4.00% SOFR floor, OID 99.5 |
| Second-lien loan | $200 million | 1.0x | SOFR + 700 bps, 4.00% SOFR floor |
| Senior unsecured notes | $300 million | 1.5x | 9.50% fixed coupon |
| **Total funded debt** | **$1,100 million** | **5.5x** | |
| Sponsor equity (plus rollover) | $500 million | | |
| **Total sources** | **$1,600 million** | | |

First, the vocabulary. **SOFR** (Secured Overnight Financing Rate) is the benchmark floating rate for dollar loans, replacing LIBOR. It moves with central-bank policy and money-market conditions. A **basis point** (bp) is one hundredth of a percentage point: 375 bps = 3.75%. The **spread** is the lender's margin over SOFR, set by the borrower's risk. A **SOFR floor** is a minimum value for SOFR in the pricing formula: if SOFR falls below the floor, the floor is used instead, protecting the lender's return when rates fall. **OID** (original issue discount) means the loan is sold for less than its face value — an OID of 99.5 means lenders pay $99.50 for every $100 of principal — which is an extra, upfront return to the lender and an extra cost to the borrower.

Now the annual cash interest, assuming SOFR is 4.30% — above the 4.00% floor, so the floor does not bind:

```math
\begin{aligned}
\text{TLB interest} &= \$600\text{m} \times (4.30\% + 3.75\%) = \$600\text{m} \times 8.05\% = \$48.3\text{m} \\
\text{Second-lien interest} &= \$200\text{m} \times (4.30\% + 7.00\%) = \$200\text{m} \times 11.30\% = \$22.6\text{m} \\
\text{Notes interest} &= \$300\text{m} \times 9.50\% = \$28.5\text{m} \\
\text{Total cash interest} &= \$48.3\text{m} + \$22.6\text{m} + \$28.5\text{m} = \$99.4\text{m}
\end{aligned}
```

Check the coverage and the blended cost:

```math
\text{Interest coverage} = \frac{\$200\text{m}}{\$99.4\text{m}} = 2.01\text{x}
```

```math
\text{Blended cash rate} = \frac{\$99.4\text{m}}{\$1,100\text{m}} = 9.04\%
```

So Meridian pays about 9% on average for its debt, and its EBITDA covers interest just over twice. That is a workable but not comfortable position — a normal outcome for a 5.5x deal, and a useful benchmark to hold in your head.

Two refinements that trip people up. First, the **floor**. Suppose SOFR falls to 3.00%. A naive calculation gives the TLB rate as 3.00% + 3.75% = 6.75%. The correct rate is 4.00% + 3.75% = 7.75%, because the floor replaces SOFR. Floors are worth real money to lenders when rates fall, and they are one reason floating-rate borrowers do not benefit one-for-one from rate cuts. Always check the floor before you price a loan.

Second, the **OID**. Meridian's TLB is issued at 99.5, so lenders pay $597 million for $600 million of principal. The $3 million discount is, in effect, extra interest spread over the loan's life. Over a 7-year loan, a rough straight-line amortisation gives about $0.43 million per year of additional cost, lifting the TLB's all-in rate from 8.05% to roughly 8.12%. That is an approximation — the exact yield depends on the repayment schedule and fees — but the direction matters: the headline spread is never the whole cost. Fees, OID, and the floor all belong in the true price, and a banker who quotes only the spread is either careless or selling something.

One more comparison, because it shows how the stack is optimised. Suppose Meridian replaced the second-lien loan and the notes ($500 million at a blended cash cost of $51.1 million, or 10.22%) with a single **unitranche** facility of $500 million at SOFR + 575 bps = 10.05%, costing $50.25 million a year. That saves about $0.85 million a year and replaces two documents, two lender groups, and two sets of negotiations with one. Article 24 explained why borrowers often pay *more* for a unitranche despite that saving: here the saving is small, and the borrower gives up the flexibility of refinancing one tranche without touching the other, and the ability to play lender groups against each other. Whether the trade is worth it depends on how much the borrower values simplicity and certainty — which, as article 24 showed, is often a lot. The numbers alone never settle it.

## 5. Covenants: The Lender's Early-Warning System

Lenders do not just set a price and hope. They write **covenants** — promises the borrower makes, tested regularly — into the loan documents. There are two families, and confusing them is a classic error.

**Maintenance covenants** are tested every quarter, whether or not the borrower does anything. The classic example is a maximum total leverage ratio: Meridian's TLB might require total leverage below 6.0x, stepping down to 5.5x over time. If EBITDA falls to $160 million while debt is still $1,100 million, leverage becomes $1,100 / $160 = 6.875x, and Meridian breaches the covenant even though it has paid every interest bill on time. The breach gives lenders the right to accelerate the loan, renegotiate, or extract fees and concessions — which is why a covenant breach is often the first public sign of distress, well before any missed payment.

**Incurrence covenants**, typical of high-yield bonds, are tested only when the borrower *does* something: incur new debt, pay a dividend, sell assets. A bond might say Meridian cannot incur additional debt if, after giving effect to it, total leverage would exceed 6.0x. If Meridian never incurs new debt, the test never bites, no matter how bad EBITDA gets. That is why bonds are often described as "covenant-lite" by comparison — not because they have no protections, but because their protections are triggered by actions rather than by the passage of time.

The market's drift toward **covenant-lite** (or "cov-lite") term loans — loans with incurrence-style tests or no financial maintenance tests at all — is one of the defining features of modern leveraged finance. Borrowers love cov-lite: it removes the tripwire that hands lenders leverage at the first sign of trouble. Lenders accept it when they are competing for deals, and regret it when the cycle turns, because without a maintenance test they may discover a problem only when the borrower actually runs out of cash. Kaplan and Strömberg (2009), surveying the buyout market, note the same cyclical pattern in a broader form: the terms of buyout financing — leverage, pricing, and protections — loosen in good credit markets and tighten in bad ones, and the loosening itself helps inflate the prices sponsors pay. Cov-lite is not a technical footnote. It is the credit cycle, written into legal documents.

## 6. Syndication: Selling the Loan

Meridian's TLB is not lent by one bank. It is **syndicated**: the arranging bank (or banks) underwrites the loan, then sells pieces of it to institutional investors — CLOs, loan mutual funds, hedge funds, and other asset managers. The process has a rhythm worth knowing, because it explains why loan pricing moves in the days after a deal is announced.

First comes **launch**: the arranger circulates a confidential information memorandum with the company's financials, the proposed structure, and "price talk" — a range for the spread and OID, say SOFR + 350–375 bps at 99.5. Investors indicate how much they want at what price. Then comes **allocation and flex**: if demand is weak, the arranger "flexes" the price up — the spread widens to, say, SOFR + 400 bps, or the OID drops to 99.0 — to attract buyers. If demand is strong, the arranger may "reverse flex" the price down, saving the borrower money. In a fully underwritten deal, the arranger has committed to fund the loan even if syndication fails, and flex is how it protects itself: the flex provisions cap how far the price can move before the arranger, not the borrower, bears the difference. That is the sense in which LevFin bankers sell certainty — they absorb the syndication risk, up to a negotiated limit, so the sponsor can sign a purchase agreement knowing the money will be there.

Syndication also explains a quirk of the loan market: loans trade after close, and their secondary prices reveal what the market thinks of the borrower in real time. A TLB at 98 cents on the dollar is not necessarily in trouble, but one sliding toward 80 is the market pricing in real distress risk, often months before any covenant breach or missed payment.

## 7. What Goes Wrong: The Refinancing Wall

Meridian's structure has a quiet vulnerability built into it: the TLB amortises at only 1% per year, so after seven years Meridian still owes about $558 million on that tranche alone ($600 million minus seven years of $6 million amortisation), plus the full $200 million second lien and $300 million of notes, unless it has used free cash flow to prepay. Its cash flow after interest, mandatory amortisation, capital expenditure, and cash taxes illustrates the point. Start from EBITDA of $200 million, subtract cash interest of $99.4 million and mandatory TLB amortisation of $6 million, leaving $94.6 million; subtract, say, $25 million of capital expenditure and $15 million of cash taxes, and about $54.6 million remains for optional prepayment, acquisitions, or dividends. That is a healthy number — *if* EBITDA holds. If EBITDA falls to $160 million, the same arithmetic leaves only about $14.6 million. The company is not yet in default, but its ability to reduce debt has almost vanished, and the maturity wall is still coming.

That wall is the central risk of leveraged finance. Most leveraged debt is not repaid out of operating cash flow; it is **refinanced** at maturity, on the strength of the company's then-current cash flows and the then-current credit market. If either has deteriorated, refinancing may be expensive, partial, or impossible — and a company that could service its interest perfectly well can still default because nobody will lend it the principal back. So always ask two questions: can it pay the interest, and can it repay or refinance the principal? The first is arithmetic. The second is a judgement about the future credit market, and it is where most leveraged-finance mistakes are made.

## Common Misconceptions

**"More leverage is always better for equity returns."** Up to a point, leverage magnifies equity returns, because a fixed interest bill leaves more residual cash flow when the business grows. Past that point, it magnifies losses, triggers covenants, and consumes the cash flow that would have funded growth. The optimal leverage is the most debt the downside case can carry, not the most the market will offer in a hot year. Axelson et al.'s (2013) finding — that easy credit leads to higher prices and lower fund returns — is the empirical version of this warning.

**"A floating-rate loan is always cheaper than a fixed-rate bond when rates are low."** Only if you ignore the floor, the OID, and the risk that rates rise. A loan at SOFR + 375 bps with a 4.00% floor costs 7.75% even if SOFR is 3.00%, and it costs more if SOFR rises to 5.50%. A fixed 9.50% bond looks expensive when SOFR is 4.30% and cheap when SOFR is 6.00%. The right comparison is the all-in cost across rate scenarios, not today's headline rate.

**"Covenant-lite means no lender protection."** Cov-lite loans still have incurrence tests, collateral, guarantees, reporting requirements, and events of default. What they lack is the quarterly tripwire. That is a real loss of protection — lenders find out later — but it is not the same as lending unsecured with no documents. Precision here matters: the debate about cov-lite is about *timing* of lender intervention, not about whether lenders have rights at all.

**"Second-lien debt is just more first-lien debt."** No. Second-lien lenders share the same collateral but stand behind the first lien in recovery, and their intercreditor agreement — the contract between lender groups — restricts what they can do in a workout, including when they can enforce against collateral. In a restructuring, that subordination can be worth many points of recovery. Pricing that ignores it is mispricing.

**"If the company can pay interest, it is fine."** Interest is the easy part. Principal is the hard part. A leveraged company lives or dies by its ability to refinance, and refinancing depends on future credit conditions that no one controls. Always check the maturity schedule alongside the coverage ratio.

## Test Yourself

**1.** Meridian's SOFR falls to 3.00% and its TLB has a 4.00% floor and a 375 bp spread. What is the TLB's interest rate, and what would a careless analyst who ignores the floor calculate instead?
*Answer: 4.00% + 3.75% = 7.75%. Ignoring the floor gives 3.00% + 3.75% = 6.75%, understating the rate by a full percentage point — $6 million a year on a $600 million loan.*

**2.** Meridian's EBITDA falls to $160 million with funded debt still at $1,100 million and cash interest still at $99.4 million. What are its total leverage and interest coverage? Does it breach a 6.0x maximum leverage maintenance covenant?
*Answer: Leverage = $1,100 / $160 = 6.875x. Coverage = $160 / $99.4 = 1.61x. Yes, 6.875x exceeds the 6.0x covenant, so it breaches even though it has paid all interest due.*

**3.** A borrower can fund $500 million either as a second-lien loan plus notes costing $51.1 million a year, or as a unitranche at SOFR + 575 bps when SOFR is 4.30%. Which is cheaper in cash interest, and by how much? Name one non-price reason to prefer the more expensive option.
*Answer: Unitranche rate = 4.30% + 5.75% = 10.05%, costing $50.25 million — $0.85 million cheaper per year. A non-price reason to prefer the split structure is refinancing flexibility: one tranche can be refinanced or repaid without touching the other, and separate lender groups can be negotiated with independently.*

**4.** Why might a lender accept a covenant-lite loan in a competitive market, even though it knows it will learn about trouble later? And what does that imply about loan terms over the credit cycle?
*Answer: Because refusing means losing the deal to a competing lender, and the lender judges the fee, spread, and relationship value worth the weaker protection. It implies terms are cyclical: protections loosen when credit is plentiful and competition is fierce, and tighten after losses remind lenders why the protections existed — the same cycle Kaplan and Strömberg (2009) describe for buyout financing generally.*

## References

- Axelson, U., Jenkinson, T., Strömberg, P., & Weisbach, M. S. (2013). Borrow Cheap, Buy High? The Determinants of Leverage and Pricing in Buyouts. *Journal of Finance*, 68(6), 2223–2267.
- Kaplan, S. N., & Strömberg, P. (2009). Leveraged Buyouts and Private Equity. *Journal of Economic Perspectives*, 23(1), 121–146.

*Next up: 26 | Equity Capital Markets Beyond the IPO: Follow-Ons, Blocks, and Buybacks.*
