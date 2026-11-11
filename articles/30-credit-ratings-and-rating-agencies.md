# 30 | Credit Ratings and the Rating Agencies: Who Grades the Debt?

*We have spent twenty-nine articles valuing equity from every angle, and the debt side has been sitting quietly in the corner the whole time. But somebody has to decide what a company's promises are worth — and three private companies, whose letter grades move trillions of dollars of other people's money, do most of the deciding. This article is about those grades: what they measure, who pays for them, and why one notch can cost a company forty million dollars a year.*

> **Learning goals.** After this article you can: (1) explain what a credit rating is — and what it is not — and why the market needs an independent opinion on default risk; (2) read the three agencies' scales notch by notch and explain why the line between BBB- and BB+ matters more than any other; (3) describe how a rating is actually produced, from analyst models to the rating committee, and where the issuer-pays conflict sits; (4) compute what a downgrade costs a borrower, in bond prices and in annual interest; (5) explain fallen angels, forced selling, and rating triggers; (6) explain when ratings lag the market, and how bankers use ratings anyway.
>
> **Prerequisites.** Article 03 (enterprise value) for what debt is being graded, article 06 (DCF I) for discounting, article 20 (debt capital markets) for how a bond deal gets priced, and article 25 (leveraged finance) for the high-yield world below the investment-grade line. Cantor & Packer (1994) is the backbone of sections 2 and 3; Kisgen (2006) underpins the claim in section 6 that firms manage their capital structure around their rating; Kisgen & Strahan (2010) is the source for the regulatory-amplification argument in section 5.

## 1. Why Debt Needs a Grade

A company wants to borrow a billion dollars. Thousands of potential lenders — pension funds, insurers, mutual funds, banks — each have to decide whether this company will pay them back. Each lender could do its own credit analysis, but most lack the time, the staff, or the access, and even the ones that do would each reach a slightly different answer.

That is an information problem, and credit ratings are the market's shortcut through it. A **credit rating** is an opinion — the agencies insist on that word, for legal reasons — about the likelihood that a borrower will repay a particular debt, on time and in full. It compresses everything an analyst knows about a company into a handful of letters: AAA, BBB, B, CCC.

The shortcut works because of a feature of bond markets that equity markets do not share. When you buy a stock, your upside is unlimited; when you buy a bond, your upside is capped — you get your coupons and your principal back, nothing more — and your downside is default. The question is almost entirely about the tail: *how likely is this borrower to fail, and how much do I lose if it does?* That is why a single letter grade can usefully summarise a bond.

There is a second reason ratings matter, and it is less elegant: the law. Pension funds, insurers, and banks are often only *allowed* to hold bonds above a certain rating. So a rating is not just an opinion — it is a license. It determines who is allowed to own the bond, which determines who shows up to buy it, which determines what it costs. The power of a rating comes as much from regulation and mandates as from the quality of the analysis behind it.

## 2. The Scale: 21 Notches and One Cliff

The three agencies that matter — **Moody's**, **S&P Global Ratings**, and **Fitch Ratings** — use nearly identical scales. The top is AAA (Aaa at Moody's), the bottom is D, default. Each category from AA down to CCC is split into three notches, giving 21 steps in all. S&P and Fitch use plus and minus signs (AA+, AA, AA-); Moody's uses numbers (Aa1, Aa2, Aa3).

| S&P / Fitch | Moody's | What it means | Grade |
|---|---|---|---|
| AAA | Aaa | Extremely strong capacity to pay | Investment grade |
| AA+, AA, AA- | Aa1, Aa2, Aa3 | Very strong capacity; very low credit risk | Investment grade |
| A+, A, A- | A1, A2, A3 | Strong, but more exposed to a weak economy | Investment grade |
| BBB+, BBB, BBB- | Baa1, Baa2, Baa3 | Adequate capacity; the lowest rung of safety | Investment grade |
| BB+, BB, BB- | Ba1, Ba2, Ba3 | Major ongoing uncertainties; substantial credit risk | Speculative grade |
| B+, B, B- | B1, B2, B3 | Paying today, but bad conditions would likely impair that | Speculative grade |
| CCC+, CCC, CCC- | Caa1, Caa2, Caa3 | Currently vulnerable; default is a real possibility | Speculative grade |
| CC, C | Ca, C | Default probable, imminent, or under way | Speculative grade |
| D | — | Already in default | Default |

The most important line on the whole table sits between BBB- and BB+ — between Baa3 and Ba1 at Moody's. Above it is **investment grade**; below it is **speculative grade**, better known as high yield, or less politely, junk. One notch, and the world changes: different buyers, different funds, different rules, different price. Bankers call it the cliff.

But is a letter grade actually predictive? The agencies' defence, and it is a fair one, is the historical record. S&P's study of global corporate defaults from 1981 to 2024 reports average cumulative default rates by the rating at the start of each period, and the pattern is exactly what you would hope for: the grades rank default risk correctly, and the risk rises steeply as you go down the scale.

| Rating at start | Defaulted within 5 years | Defaulted within 10 years |
|---|---:|---:|
| AAA | 0.34% | 0.67% |
| AA | 0.33% | 0.83% |
| A | 0.39% | 1.13% |
| BBB | 1.09% | 2.50% |
| BB | 5.05% | 9.33% |
| B | 14.69% | 21.04% |
| CCC/C | 46.53% | 50.43% |

Read the table slowly, because it contains the whole economics of credit. A BBB borrower defaults about once in a hundred over five years; a BB borrower about once in twenty; a B borrower about once in seven. The step from BBB to BB — one notch across the cliff — multiplies the five-year default rate by roughly 4.6 times. The agencies' critics have many valid complaints, which section 6 takes up, but "the grades mean nothing" is not one of them. What the table also shows is what a rating does *not* tell you: it says nothing about how much you lose if default happens. Recovery depends on seniority, collateral, and the bankruptcy process. These are also averages over decades, and averages conceal cycles: in 2009, speculative-grade defaults spiked into double digits. A rating is a through-the-cycle opinion, which is why ratings move slowly and why the market sometimes moves first.

## 3. How a Rating Is Actually Made

The popular picture of a rating is a formula: feed in the leverage ratio, get out a letter. The reality is messier. A rating is produced by analysts who build a model, meet management, write a report, and defend it in front of a **rating committee** — senior analysts who vote on the outcome. The committee exists because no formula captures a company's willingness to pay or the quality of its management, and because a committee is harder to game than a spreadsheet.

What goes into the decision? Two buckets. The quantitative bucket is the one you can check: leverage (debt to EBITDA), coverage (EBITDA to interest), scale, profitability, cash flow conversion, liquidity, and financial policy — the agencies' polite term for "what management actually does with its money." A company that keeps leverage at 2x EBITDA and pays a steady dividend is a different credit from one that keeps leverage at 2x today and announces a debt-funded buyback tomorrow. The agencies grade the policy, not just the numbers.

The qualitative bucket is the one that makes analysts argue: industry risk, competitive position, management quality and governance, country risk, and event risk. A retailer with 3x leverage and a utility with 3x leverage are not the same credit, because the retailer's cash flows swing with the consumer cycle while the utility's are regulated and predictable. The agencies publish detailed criteria for each sector, but the final judgement is exactly that — a judgement, voted on by a committee.

Two mechanics matter for bankers. First, **outlooks and watches**: a rating usually carries an outlook — positive, stable, or negative — and a company can be put on **CreditWatch** (S&P) or review (Moody's) when an event like a merger might change the rating soon. Second, the split between **issuer ratings** and **issue ratings**: the issuer rating grades the company as a whole, while each bond gets its own rating, higher or lower depending on seniority and security. When a banker says "the deal is rated BBB," they usually mean the issue rating.

Now the awkward part: who pays. Since the early 1970s, the dominant model has been **issuer-pays** — the company being rated pays the agency for the rating. Before that, investors paid, through subscriptions; photocopying and then the internet made that model impossible. The conflict is obvious and the agencies do not deny it: the customer paying for the opinion is the same company being graded, and the agency competes with two rivals for that customer's business. If you are too harsh, the issuer takes its fees to your competitor — a practice the industry calls **ratings shopping**. The defence is that reputation is the agencies' only real asset: if investors stop believing the grades, the grades stop mattering, and the fees stop coming. That defence held well for plain corporate bonds and failed badly for structured finance in 2008. Issuer-pays is a conflict that is managed, not solved.

## 4. What a Downgrade Costs: A Worked Example

Ratings move markets because they move yields, and yields move prices. Here is the arithmetic, done slowly.

Meet Meridian Industries, a fictional manufacturer, with a 10-year bond outstanding: $1{,}000$ face value, a 5% annual coupon. While Meridian is rated BBB, the market demands a 5% yield — the coupon equals the yield, so the bond trades at par, $1{,}000$. The price of a bond is the present value of its coupons plus the present value of its principal, discounted at the yield:

```math
P = \sum_{t=1}^{10} \frac{50}{(1+y)^t} + \frac{1{,}000}{(1+y)^{10}}
```

Now the agencies downgrade Meridian to BB+, and investors demand a 7% yield. Recompute the price at $y = 7\%$:

```math
P = 50 \times \frac{1 - (1.07)^{-10}}{0.07} + \frac{1{,}000}{(1.07)^{10}} = 50 \times 7.0236 + 508.35 = 351.18 + 508.35 = \$859.53
```

The bond has lost about 14% of its value — $140.47 on every $1{,}000$ of face — on a single notch of downgrade. At a 6% yield, the price would have been $926.40, a 7.4% fall. Two points to notice. First, the loss falls entirely on existing bondholders; Meridian itself does not write a cheque when its bonds fall. Second, what Meridian *does* pay is the higher yield on every dollar it borrows from now on. Suppose Meridian needs to refinance $2$ billion of debt, and the downgrade widens its spread over Treasuries by 200 basis points, from 150 to 350. The extra cost is:

```math
0.02 \times \$2{,}000 \text{ million} = \$40 \text{ million per year}
```

Forty million dollars a year, every year until the debt is repaid, for one notch. That is the number a CFO hears when the agencies call, and it is why management teams treat the rating as a strategic asset rather than a report card. It also explains why companies sometimes turn down profitable-looking deals: if the deal requires debt that would cost the company its investment-grade rating, the extra interest on *all* of its future borrowing can dwarf the deal's profits. Kisgen (2006) found that firms close to a rating change behave differently from otherwise similar firms — they issue less debt and more equity, as if protecting the rating were a goal in itself. The rating is a constraint on capital structure, not just a comment on it.

There is a second, quieter cost. Many loan agreements and bond indentures contain **rating triggers**: clauses that change the deal if the rating moves — a coupon step-up of 25 basis points per notch of downgrade, a requirement to post additional collateral, or an acceleration clause letting lenders demand early repayment. Triggers turn a downgrade into a self-reinforcing event: the rating falls, the triggers bite, costs rise, credit weakens further, and the agencies downgrade again. The most famous version of this spiral killed Enron's trading business in 2001, when a downgrade below investment grade triggered collateral calls it could not meet.

## 5. Fallen Angels, Forced Selling, and the Regulatory Amplifier

When a company crosses from investment grade to speculative grade, it becomes a **fallen angel**. The name is apt: it is not just a downgrade, it is an expulsion from one market into another. Ford and General Motors both fell in 2005, in one of the largest fallen-angel events in history, and the mechanics of what followed repeat every cycle.

The first mechanism is **forced selling**. Pension funds, insurers, and investment-grade bond funds have mandates that say, in effect, "investment grade only." When a bond is downgraded to BB+, those holders must sell — not because they think the bond is now a bad investment, but because their rules say so. The selling is mechanical and concentrated, and it hits a market where the natural buyers — high-yield funds — are smaller and slower. The result is a price overshoot: fallen angels typically trade cheap for weeks after the downgrade, not because the company got 14% worse overnight, but because the buyer base changed faster than the price could adjust.

The second mechanism is regulatory. Kisgen & Strahan (2010) studied what happens when regulations *use* ratings — for example, US insurance regulators set capital requirements based on the ratings of the bonds insurers hold, so a downgrade forces an insurer to hold more capital against the same bond. They found that this raises the cost of capital for downgraded firms beyond what the pure credit risk would justify. The rating is not just a signal; it is an input to a rulebook, and the rulebook has teeth: a downgrade raises an insurer's required capital, so the insurer sells, so the price falls, so the yield rises, so the borrower's costs rise.

The third mechanism is the **BBB cliff** itself. The investment-grade market has swollen with BBB-rated debt — the lowest rung of safety — and BBB is where the fallen angels come from. When a recession hits, a wave of BBB issuers can fall at once, overwhelming the high-yield market's capacity to absorb them. In 2020 that wave nearly arrived — Ford was downgraded to junk in March — and it was only the Federal Reserve's decision to buy corporate bonds, including fallen angels, that kept the market orderly. The cliff is a systemic risk, not just a company-specific one.

## 6. When Ratings Lag the Market — and Why Bankers Use Them Anyway

For all their power, ratings have a well-documented weakness: they are slow. The agencies deliberately rate "through the cycle," waiting for evidence rather than reacting to every market move, while the bond market reacts instantly. The market reprices a company's debt weeks or months before the agencies act, and the downgrade arrives as confirmation of something the price already knew.

Enron is the extreme case every critic cites: rated investment grade by all three agencies until days before it filed for bankruptcy in December 2001. The agencies' defence was that Enron had hidden its liabilities in off-balance-sheet vehicles; the critics' reply is that the agencies had access to management, saw the complexity, and chose to believe the story. Both sides have a point: a rating is only as good as the information the issuer provides and the scepticism the analyst applies to it.

The bigger failure was structured finance in 2008. The agencies gave AAA ratings to mortgage-backed securities built from subprime loans, using models that assumed house prices would not fall nationally. When the models failed, the downgrades came in waves, thousands at a time, and the AAA label that had let pension funds and banks hold these securities transmitted the crisis into every regulated balance sheet at once. The post-crisis reforms — Dodd-Frank removed some regulatory reliance on ratings and forced more disclosure — were aimed at this failure. But the issuer-pays model survived, and the concentration survived: three agencies still dominate, and their grades still anchor the rulebooks.

So why do bankers still use ratings, knowing all this? Three reasons. First, the grades are right on average, as the default table in section 2 shows — and "right on average" is enough for a market that needs a common language. Second, the alternatives are worse: every investor doing its own full credit analysis is expensive, and a purely market-based measure like the credit default swap spread is volatile and unavailable for companies without traded CDS. Third, the rating is what the *rules* use. A banker does not need to believe the rating is perfect; they need to know what rating the client needs to keep its investors, satisfy its covenants, and price its deal. Cantor & Packer (1994) made this point thirty years ago: ratings rank default risk accurately, but the meaning of a given grade drifts over time and differs across agencies, and regulations that hard-code the grades are building on sand.

The practical discipline for a banker is therefore simple: use the rating as a starting point and a constraint, never as a substitute for your own credit view. Read the agency's report — it is free, detailed, and often more candid than the company's own filings. Check the market's view against it: if the bond trades at a spread that implies a much lower rating than the agencies give, find out why before you trust either. And when you advise a client on a transaction, ask the rating question first: will this deal keep the rating?

## 7. What Bankers Actually Do With Ratings

Ratings shape banking work in four places. First, in **debt capital markets**: a new bond issue is priced off its rating, and the rating is the first filter investors apply — a BBB+ deal and a BB+ deal are sold to different investors, in different funds, by different salespeople. Second, in **rating advisory**: most large banks have a team that helps clients manage their relationship with the agencies — preparing for the annual review, modelling the impact of a proposed acquisition on leverage ratios, and rehearsing the management presentation. Third, in **leveraged finance and LBOs**: the rating determines how much debt a deal can carry and at what price, and the agencies' leverage thresholds are a hard input to the LBO model from article 08. And fourth, in **restructuring**: a downgrade to CCC can breach covenants, cut off the commercial paper market, and push a struggling company into the process from article 13. In every case, the letter grade is not decoration. It is a variable in the model, a clause in the contract, and a line in the mandate. Treat it that way.

## 8. Common Misconceptions

**"A AAA rating means the bond cannot default."** It means default is very unlikely — about 0.67% over ten years in S&P's long-run data — not impossible. AAA structured securities defaulted in large numbers in 2008. A rating is a probability, and probabilities are not promises.

**"A downgrade means the company got worse overnight."** Usually it means the agencies have finally recognised a deterioration the market priced weeks ago, or that a single event has changed the leverage math. The company changes gradually; the rating changes in steps. That lumpiness is by design.

**"The rating is the agency's prediction of the bond's price."** No. A rating is an opinion about default risk, not about market value. Two bonds with the same rating can trade at very different spreads because of liquidity, maturity, and sector sentiment. If you use the rating to predict price, you will be wrong exactly when being right matters most.

**"Issuer-pays means ratings are bought."** The conflict is real, and ratings shopping happens, but the crude version — that an issuer can simply pay for a AAA — is false. The agencies publish criteria, use committees, and live or die by their reputation with investors. The subtler truth is more worrying: the pressure is usually a drift, not a bribe — criteria applied generously at the margin, bad news absorbed slowly, borderline cases resolved in the issuer's favour.

**"Investment grade is safe and high yield is dangerous."** The default table says otherwise in degree: a BBB bond defaults 1.09% of the time over five years — small, but not zero — and a BB bond defaults 5.05% of the time, which means 95% of the time it does not. The right question is never "is this safe," it is "am I being paid enough for the risk, and can I hold it through the cycle?" A well-diversified high-yield portfolio has historically earned a positive excess return precisely because most investors overstate the danger of the average name.

## Test Yourself

**1.** Meridian Industries has a 10-year, 5% coupon bond with $1{,}000$ face value. It trades at par while Meridian is rated BBB. After a downgrade to BB+, the market demands a 6% yield. What is the new price, and how much has a holder lost per bond?

*Answer: Price $= 50 \times \frac{1-(1.06)^{-10}}{0.06} + \frac{1{,}000}{(1.06)^{10}} = 50 \times 7.3601 + 558.39 = \$926.40$. The holder has lost $\$73.60$ per bond, or 7.4%. At a 7% yield the price would fall further, to \$859.53 — a 14% loss — which is why the size of the spread widening matters as much as the downgrade itself.*

**2.** A BBB- rated company plans to issue $3$ billion of 10-year bonds. If it is downgraded to BB+ before pricing, its spread over Treasuries widens by 150 basis points. What is the extra annual interest cost, and what is the total extra cost over the life of the bonds (ignoring discounting)?

*Answer: Extra annual cost $= 0.015 \times \$3{,}000$ million $= \$45$ million per year. Over ten years that is $\$450$ million of extra interest — which is why the rating decision can matter more than the pricing of any single deal. (In present-value terms the cost is smaller, since the payments are spread over ten years.)*

**3.** Using S&P's 1981–2024 data, a portfolio holds 200 B-rated bonds and 200 BBB-rated bonds. Roughly how many of each would you expect to default within five years? Why might the actual number differ a lot from your expectation in a single five-year window?

*Answer: B-rated five-year cumulative default rate is 14.69%, so about $0.1469 \times 200 \approx 29$ of the B bonds. BBB is 1.09%, so about $0.0109 \times 200 \approx 2$ of the BBB bonds. The actual number could differ a lot because defaults are correlated — they cluster in recessions, so a five-year window containing a crisis will show far more defaults than the long-run average.*

**4.** A fallen angel is downgraded from BBB- to BB+. Its bonds fall 12% in the week after the downgrade, even though the company's cash flows have not changed. Give two mechanisms that explain the fall, and say which one is about the bond's true credit quality and which one is not.

*Answer: (1) Forced selling: investment-grade funds and insurers whose mandates require investment-grade holdings must sell, and the selling is mechanical and concentrated, pushing the price below what the credit alone would justify. This is not about the company's true quality — it is about who is allowed to hold the bond. (2) Higher required yield and rating triggers: investors now demand a higher yield for the higher default risk (the five-year default rate jumps from about 1% to about 5%), and any coupon step-ups or collateral triggers may bite. The lesson: price moves after a downgrade mix a real repricing of risk with a mechanical change in ownership.*

## Next up

Next: **31 | Valuing Technology Companies: Growth, SaaS Metrics, and the Rule of 40** — we have valued banks, buildings, and insurers; now the sector where the standard tools break in the opposite direction, because the earnings are negative and the growth is the whole story.
