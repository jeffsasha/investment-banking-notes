# 37 | Distressed Debt Investing: Buying a Company's Debt at a Discount

*Somewhere between "this company is fine" and "this company is dead" there is a strange middle zone — the company still operates, still ships product, still pays most of its people, but its debt trades at 40 cents on the dollar. A loan that was worth $100 yesterday is worth $40 today. My first reaction, when I saw a quote like that, was that someone had made a mistake. Nobody makes a mistake like that. The price is telling you something precise: the market thinks this company will not pay back all of what it owes, and it is arguing about how much will be lost, and who will lose it. Distressed debt investing is the business of joining that argument — with a calculator, not a gut feeling.*

> **Learning goals.** After this article you can: (1) explain why a performing loan can trade at a deep discount, and who is forced to sell it; (2) read a capital structure as a waterfall and find the fulcrum security — the layer where value breaks; (3) build a recovery analysis with scenarios, expected value, and a buy price, and judge whether the trade makes money; (4) explain loan-to-own, and why buying debt is sometimes a cheaper way to buy a company than buying its equity; (5) screen for distress with Altman's Z-score and know its limits; (6) explain the three ways a distressed trade dies: wrong valuation, wrong timing, and the company coming back to life worse than before.
>
> **Prerequisites.** Article 03 (enterprise value vs equity value) for the capital structure stack and the idea that enterprise value is the pie everyone splits; article 06 (DCF I) for discounting; article 13 (restructuring) for Chapter 11 and the absolute priority rule; article 16 (distressed DCF) for valuing a company that might not survive; article 25 (leveraged finance) for the loans and bonds that end up distressed; article 36 (CLOs) for who owns most leveraged loans — and why they sometimes have to sell them.

## 1. The Idea in One Paragraph

**Distressed debt** is the debt of a company that is in trouble — or that the market *thinks* is in trouble. The usual working definition on a trading desk is debt that yields more than 1,000 basis points over Treasuries, or that trades well below par; a bond at 40 cents on the dollar is distressed by any measure. The investor's idea is simple to state and hard to execute: buy a claim for less than what the company will ultimately pay on it. If you buy a loan at 60 cents and the company eventually repays 85 cents — through a restructuring, a sale, or a refinancing — you make 25 cents on a 60-cent investment, plus whatever interest you collect while you wait. If you buy the *wrong* layer of the capital structure, the one that gets nothing, you lose nearly everything. The whole game is figuring out, before you buy, which layer gets paid and how much. That is a valuation question, not a trading question — which is why it belongs in this series.

One clarification up front, because the name invites it. "Distressed" does not mean "bankrupt." A company can be distressed for years without ever filing Chapter 11: it misses a covenant, it negotiates with lenders, it sells assets, it muddles through. And bankruptcy does not mean the debt is worthless — secured lenders in Chapter 11 usually recover a large part of what they are owed. The distressed investor lives in the gap between the market price and the recovery value, and the gap exists because of who is selling, which is where we start.

## 2. Why Good Loans End Up on Sale

If a loan is worth 85 cents, why would anyone sell it for 60? Sometimes because they think it is worth 50. But very often the seller is not making a valuation judgment at all. They are selling because they *have* to. This is the single most important fact in distressed debt, and it is the reason the opportunity exists.

**CLOs have to sell.** We met CLOs in article 36: they own hundreds of leveraged loans and issue rated bonds against them. Their indentures contain tests — if too many loans in the pool are rated CCC or are defaulted, the tests fail and cash flow gets diverted away from the equity tranche and toward paying down the AAA notes. The manager's rational move is to sell the weakest loans *before* they trip the test, even at a bad price. A loan downgraded to CCC is a problem for the CLO whether or not it eventually recovers; the CLO sells it because its rules say so.

**Banks have to sell.** A bank holding a loan to a troubled borrower faces higher capital charges and, often, pressure from its regulators and its own credit committee. Selling at a loss is embarrassing; holding a loan that defaults is worse. Banks also have internal rules: once a borrower is classified as non-performing, the loan often has to leave the balance sheet.

**Funds have mandates.** A high-yield fund's prospectus may say it cannot hold debt rated below CCC, or cannot hold defaulted securities. When a bond is downgraded or defaults, the fund sells — not because the manager changed their mind about value, but because the mandate changed their hands. Insurance companies have similar rating-based rules.

The result is a market with **forced sellers and few natural buyers**. The buyer on the other side is a distressed fund — a hedge fund or specialist manager whose entire mandate is to buy exactly this stuff. They have locked-up capital, so nobody can force them to sell; they can wait out a two-year restructuring; and they are paid to do the legal and valuation work that a CLO manager or a bank credit officer has no time for. The discount is, in part, the price of illiquidity, complexity, and patience. You are not being paid for being smarter than the seller. You are being paid for being *allowed to hold* what the seller is not allowed to hold.

There is a second reason prices overshoot, and it is psychological: the market prices the *average* outcome, but the distressed investor is buying a specific outcome. If a company has a 50% chance of recovering fully and a 50% chance of recovering nothing, the debt trades around 50 cents. That is fair on average — but the investor who has done the work on this specific company's assets, its contracts, and its management may conclude the odds are really 70/30. The work is the edge. Without the work, you are just buying the average and paying fees for the privilege.

## 3. The Waterfall, the Fulcrum, and Where Value Breaks

Everything in distressed investing starts from article 03's idea: enterprise value is the pie, and the capital structure is the order in which people get slices. In a restructuring, the pie is the reorganized company's value — usually estimated by a DCF or by a multiple of EBITDA — and the claims are paid from the top of the stack down.

Suppose a company has this capital structure:

| Claim | Face value | Seniority |
|---|---:|---|
| First-lien term loan | $400m | Secured, first priority |
| Senior unsecured notes | $300m | Unsecured |
| Equity | — | Residual |

If the reorganized company is worth $350m, the waterfall is simple: the term loan gets the first $350m of value, which is 87.5 cents on its $400m face. The unsecured notes get nothing. The equity gets nothing. The term loan is **impaired** — it is not made whole — so it is the layer where the value breaks. That layer is called the **fulcrum security**.

The fulcrum matters for two reasons. First, it is where the recovery math is interesting: every dollar the company's value rises or falls lands on the fulcrum first. Second, in Chapter 11, the fulcrum class usually becomes the new owner. Under the absolute priority rule (article 13), a class that is not paid in full gets the reorganized company's equity in exchange for its claim. So the fulcrum creditors are the ones who will own the company after the restructuring — which is why distressed funds fight so hard to *be* the fulcrum. Buy the fulcrum cheap, and you may end up owning a decent company at a bargain price. Buy the layer *above* the fulcrum and you get paid in full but earn little; buy the layer *below* it and you get nothing.

Here is the intuition to carry: the fulcrum is the only layer whose price is really a bet on the company's value. The senior layer is a bet on the company being worth at least its own claim — a low bar. The junior layer is a bet on the company being worth more than everything above it — a high bar. The fulcrum is the bet on the company's actual value, and that is the bet a distressed investor wants to make, at the right price.

## 4. The Worked Example: Meridian Packaging

Let's make it concrete. **Meridian Packaging** is a fictional maker of corrugated boxes — a boring, cyclical business. It was bought in an LBO in 2022, loaded with debt, and then its biggest customer moved volume to a competitor. EBITDA has fallen from $120m to $70m, and the debt has not moved at all. Current prices:

| Claim | Face | Price (cents per $1) | Market value |
|---|---:|---:|---:|
| First-lien term loan | $400m | 62 | $248m |
| Senior unsecured notes | $300m | 28 | $84m |
| **Total debt** | **$700m** | | **$332m** |

Two valuation anchors. First, the going-concern value: comparable packaging companies trade at about 5.0x EBITDA (article 04's comps, applied loosely), and Meridian's EBITDA is $70m, so enterprise value is roughly $70m × 5.0 = $350m. Second, the liquidation value — what the plants and equipment would fetch in a fire sale — is estimated at $260m. A restructuring keeps the company alive, so $350m is the better anchor for the waterfall, with $260m as the floor if things go wrong.

**Step 1: The base-case waterfall at $350m of value.**

```math
Loan recovery = min(EV, loan face) / loan face = 350 / 400 = 87.5 cents
Notes recovery = max(0, EV - loan face) / notes face = 0 / 300 = 0 cents
```

At the base case, the loan recovers 87.5 cents and the notes recover nothing. The loan is the fulcrum.

**Step 2: Scenarios, because a single value is a guess dressed up as a number.** Three cases:

| Scenario | EV | Probability | Loan recovery | Notes recovery |
|---|---:|---:|---:|---:|
| Bull: volumes stabilize, multiple 6.0x | $420m | 30% | 100.0¢ | 6.7¢ |
| Base: as above, multiple 5.0x | $350m | 50% | 87.5¢ | 0.0¢ |
| Bear: another customer leaves | $300m | 20% | 75.0¢ | 0.0¢ |

The bull case notes recovery: the loan takes its full $400m, leaving $20m for $300m of notes, so 20 / 300 = 6.7 cents. The bear case loan recovery: 300 / 400 = 75 cents.

**Step 3: Expected recovery.**

```math
E[loan recovery] = 0.30 × 100.0 + 0.50 × 87.5 + 0.20 × 75.0
                 = 30.0 + 43.75 + 15.0
                 = 88.75 cents

E[notes recovery] = 0.30 × 6.7 + 0.50 × 0 + 0.20 × 0
                  = 2.0 cents
```

**Step 4: Compare to the price.**

```math
Loan:  expected recovery 88.75¢, price 62¢ → profit 26.75¢ per $1 of face
       return on cost = 26.75 / 62 = 43.1% (before coupon and before time)

Notes: expected recovery 2.0¢, price 28¢ → loss 26.0¢ per $1 of face
       return on cost = -26.0 / 28 = -92.9%
```

The loan is the trade; the notes are a trap. Notice how stark the difference is: the two claims are claims on the *same company*, and one is a 43% expected gain while the other is a 93% expected loss. The difference is entirely about where value breaks. The notes trade at 28 cents because somebody, somewhere, is hoping for the bull case — but even in the bull case they recover only 6.7 cents. The price is not a bet on recovery. It is a bet on *hope*: that a buyer appears, that the company is sold whole at a higher multiple, that the notes get refinanced. Hope is not a recovery analysis.

A few refinements a real analyst would add. First, the coupon: the term loan pays interest while you hold it — say SOFR plus 350 basis points, roughly 8% on face value. On a $10m face position bought for $6.2m, that is $0.8m a year, a 12.9% current yield on cost (8 / 62 = 12.9%). That income is real money, and it pays you to wait. Second, time: if recovery takes three years, that 43% is not an annualized return — it is a three-year return, roughly 13% a year compounded, plus the coupon. Still attractive, but the headline flatters the trade if you ignore the clock. A rough yield-to-maturity check, assuming the base-case recovery of 87.5 cents arrives in three years, gives:

```math
YTM ≈ (coupon + (recovery - price) / years) / ((recovery + price) / 2)
    = (8 + (87.5 - 62) / 3) / ((87.5 + 62) / 2)
    = (8 + 8.5) / 74.75
    ≈ 22.1%
```

Third, a cross-check: the market value of all the debt is $248m + $84m = $332m, close to our $350m enterprise value estimate. The market, in aggregate, roughly agrees with our valuation. The disagreement is not about the pie — it is about how the pie is split. That is exactly what a recovery analysis is for.

Finally, the margin of safety. Our expected recovery of 88.75 cents rests on a 5.0x multiple and $70m of EBITDA. What if EBITDA is really $60m and the multiple is 4.5x? Then EV is $270m and the loan recovers 67.5 cents — still above the 62-cent price, but barely. What if EBITDA falls to $50m? EV $225m, loan recovery 56.25 cents, and the trade loses money. So the honest statement of the trade is: *the loan makes money unless EBITDA falls by more than about 25% from here, or the multiple compresses below about 4.4x*. That is the sentence that should be in the investment memo, not "expected return 43%."

## 5. Loan-to-Own: Buying Debt to Become the Owner

There is a second, more aggressive way to play the same hand. Instead of buying the loan to collect a recovery, you buy *enough* of the loan to control the restructuring — and end up owning the company. This is called **loan-to-own**.

The logic is arithmetic. Meridian's equity is worthless and its notes are worthless; the fulcrum loan will be converted into most of the reorganized company's equity. If you buy $250m face of the $400m loan at 62 cents, you pay $155m. After the restructuring, your claim converts into roughly 62.5% of the new equity (your share of the loan class), and the reorganized company is worth about $350m. Your 62.5% is worth about $219m — against a $155m cost. You have bought control of a $350m company for $155m, plus the costs and time of the bankruptcy process.

Why doesn't everyone do this? Three reasons. First, **blocking positions**: you need a large enough share of the class to influence the vote on a plan of reorganization — typically a majority of the class by amount, and other distressed funds are trying to do the same thing. Second, **time and legal cost**: a Chapter 11 case takes a year or more, lawyers and advisors are expensive, and your capital is locked up while the case runs. Third, **you might not want the company**. Owning a corrugated-box maker means running it — or finding someone to run it. Many distressed funds are happy to take the equity and sell it; some are not set up to be operators at all.

There is also a defensive version of this strategy. Suppose you already own the notes at 28 cents. Your recovery analysis says they are worth 2 cents. But if you buy enough of the loan to sit at the negotiating table, you can argue — in the valuation fight, in court — that the company is worth more than $350m, and that the notes deserve something. The restructuring negotiation is, in part, a negotiation about what the company is worth, and the people at the table are the people who own the fulcrum. Buying into the fulcrum buys a seat.

## 6. Screening for Distress: The Z-Score

How do distressed investors find candidates before the market does? One old tool is still in use: **Altman's Z-score**, published by Edward Altman in 1968. Altman took a sample of bankrupt and non-bankrupt manufacturers and asked which combination of financial ratios best separated the two groups. The answer, for listed manufacturers, was:

```math
Z = 1.2 × (Working Capital / Total Assets)
  + 1.4 × (Retained Earnings / Total Assets)
  + 3.3 × (EBIT / Total Assets)
  + 0.6 × (Market Value of Equity / Total Liabilities)
  + 1.0 × (Sales / Total Assets)
```

Zones: above 2.99 is considered safe, 1.81 to 2.99 is a grey zone, below 1.81 is distress. Let's run Meridian through it. Suppose working capital is $40m on $400m of assets (0.10), retained earnings $20m (0.05), EBIT $8m (0.02), market value of equity $90m against $300m of liabilities (0.30), and sales $480m (1.20):

```math
Z = 1.2 × 0.10 + 1.4 × 0.05 + 3.3 × 0.02 + 0.6 × 0.30 + 1.0 × 1.20
  = 0.12 + 0.07 + 0.066 + 0.18 + 1.20
  = 1.64
```

1.64 is below 1.81 — the distress zone. The screen flags Meridian. But note what the score is and is not. It is a **screen**, built from accounting ratios, calibrated on 1960s manufacturers. It does not know Meridian's debt maturity schedule, its covenant headroom, or whether its biggest customer is about to leave. It cannot tell you the recovery value of the loan — that is the work of section 4. What it can do is sort a universe of thousands of companies into a shortlist worth reading. Altman himself later published a four-ratio version (Z″) for private and non-manufacturing companies, which drops the market-value term and the sales term — worth knowing if you ever apply the screen to a company that is not a listed manufacturer.

A related practical point: distressed investors also watch the bond market itself. When a bond's yield spread over Treasuries crosses 1,000 basis points, index providers move it into the distressed bucket, and the forced selling described in section 2 begins. The screen is often the *price*, not a ratio.

## 7. What Can Go Wrong

Distressed investing has a reputation for big returns, and the reputation is partly earned. But the failure modes are specific, and they are worth naming precisely.

**Wrong valuation.** This is the big one. Your whole trade is a bet that the company is worth more than the market thinks, and the market's estimate is embedded in the price. If your $350m is really $280m, the loan recovers 70 cents — still a gain from 62, but a thin one — and the notes recover nothing. If it is $220m, the loan recovers 55 cents and you lose. Valuation fights in Chapter 11 are fought by experts in court, and both sides hire good ones. The judge picks a number, and the number decides who gets paid. Be humble about your multiple: a 5.0x on $70m of EBITDA is an opinion, and in a declining business the right multiple is often lower than the historical one, because the buyer is buying a shrinking stream.

**Wrong timing — the company gets worse while you wait.** A distressed company is a melting ice cube. Customers leave, suppliers demand cash up front, good employees quit, and management is distracted by the restructuring. EBITDA can fall 20% in a year while the case drags on. The recovery you modeled at $350m can become $280m before the judge ever rules. This is why distressed funds care about the *rate* of decline, not just the level: a company losing $5m of EBITDA a quarter is a different investment from one that has stabilized.

**The company survives — and stays bad.** Not every distressed company files Chapter 11. Some refinance, extend maturities, and limp on for years as "zombie" companies. Your loan keeps paying its coupon, which is fine, but the recovery event you underwrote — the restructuring that pays you 88 cents — never arrives, and you are stuck holding a loan in a mediocre company at a mediocre yield. Worse, if you bought the equity of the reorganized company, the research is not kind: Hotchkiss (1995) studied 197 public companies that emerged from Chapter 11 and found that over 40% were still reporting operating losses three years after emergence, and 32% re-entered bankruptcy or privately restructured their debt. Emerging from Chapter 11 is not the same as being fixed. Loan-to-own only works if the *business* is fixable, not just the balance sheet.

**Legal surprises.** Fraud, environmental liabilities, pension underfunding, tax claims, and fraudulent-transfer lawsuits can all jump the queue ahead of you or shrink the pie. A claim you thought was senior can turn out to be subordinated by a lien you missed. Distressed investing is partly a legal exercise, and the legal work is not optional.

**Illiquidity.** Distressed debt trades by appointment. When you want to sell, there may be no buyer that week, or the only bid may be 10 points below the last trade. If your fund has redemptions, or if you simply change your mind, the exit can cost more than the thesis was worth.

## Common Misconceptions

**"Buying at 40 cents means the market thinks the company is 60% dead."** No. A price of 40 cents on a senior secured loan usually means the market expects a recovery of around 40 cents — but that is an average across scenarios, and it is also contaminated by forced selling, illiquidity, and the fact that the seller may not be allowed to hold the asset at any price. The price is information, not a verdict. Your job is to decide whether the price is wrong, and by how much, and why.

**"Distressed debt is just buying bankrupt companies."** Most distressed investing happens before any filing, and many of the best trades never involve a courtroom at all — an out-of-court exchange, an asset sale, a refinancing. Chapter 11 is one path to recovery, not the only one, and sometimes it is the worst one, because the process itself burns value.

**"The cheapest claim is the best bargain."** The notes at 28 cents look cheaper than the loan at 62 cents. They are not a bargain; they are a claim on value that does not exist. Price per dollar of face is meaningless without the waterfall. The right question is always: price versus *expected recovery*, layer by layer. A claim at 90 cents that recovers 100 is a better investment than a claim at 10 cents that recovers zero.

**"If the company survives, the debt is fine."** Survival and recovery are different things. A company can survive for years while its debt trades at 60 cents, because survival just means it keeps paying the coupon — it does not mean it will ever repay the principal. And a company can emerge from Chapter 11 and still be a bad business, as Hotchkiss's numbers show. The question is never "will it survive?" It is "what is the enterprise worth, and where does the value break?"

**"A high yield means a high return."** A loan yielding 20% is yielding 20% because the market thinks some of that yield will never be paid. Yield is compensation for risk, and in distressed debt the risk is that the principal does not come back. The return is the recovery minus the price, plus the coupons you actually collect — not the yield printed on the screen.

## Test Yourself

**1.** A company has a $200m first-lien loan and $150m of unsecured bonds. Enterprise value is estimated at $230m. The loan trades at 85 cents and the bonds at 10 cents. What is each claim's recovery at the base case, and which (if either) is mispriced?
*Answer: Loan recovery is min(230, 200) / 200 = 100 cents — the loan is made whole. At 85 cents it is cheap by 15 cents, assuming the $230m value is right. Bond recovery is (230 − 200) / 150 = 20 cents. At 10 cents the bonds are also cheap by 10 cents. Both are mispriced in the same direction, which usually means the market disagrees with your $230m — check the valuation before buying either. If EV were really $200m, the loan recovers 100 and the bonds zero.*

**2.** Rework the Meridian example: suppose the bear case is worse — EV $260m (the liquidation value) with 20% probability, and the base case stays $350m at 50%, bull $420m at 30%. What is the loan's expected recovery now, and is 62 cents still a good price?
*Answer: E[recovery] = 0.30 × 100 + 0.50 × 87.5 + 0.20 × (260/400 = 65) = 30 + 43.75 + 13 = 86.75 cents. Still above the 62-cent price, by 24.75 cents — the trade survives a worse bear case because the bear case only has 20% weight and the loan still recovers 65 cents even in liquidation. That is the point of seniority: the loan has a cushion. The notes, meanwhile, still recover ~2 cents. The trade's sensitivity is to the base case, not the tail.*

**3.** A distressed fund buys $50m face of a second-lien loan at 45 cents. The capital structure is: first lien $300m, second lien $200m, unsecured $250m. The reorganized EV comes in at $380m. What does the fund recover, and what is its profit or loss?
*Answer: First lien takes $300m, leaving $80m for the second lien: recovery is 80 / 200 = 40 cents. The fund paid 45 cents, so it loses 5 cents per dollar of face: on $50m face, cost $22.5m, recovery $20m, loss $2.5m (−11.1%). The second lien was the fulcrum — and the fund paid more than the value that broke to it. Note that a $20m higher EV ($400m) would have made it whole at 50 cents. The fulcrum is where small valuation errors become losses.*

**4.** Meridian's Z-score is 1.64. A colleague says "the model says it will go bankrupt, so the loan is a bad buy." What is wrong with that statement — three things?
*Answer: (1) The Z-score is a screen calibrated on 1960s manufacturers, not a prediction for a specific company, and it says nothing about recovery values — a company can be "distressed" and its senior loan still a good buy at the right price. (2) The model uses market value of equity, which collapses as distress becomes known, so the score partly measures the market's opinion rather than independent evidence. (3) Bankruptcy is not the same as loss: in Chapter 11 the senior loan would likely recover most of its face. The question is price versus recovery, not whether the Z-score is below 1.81.*

## Papers worth reading

- Altman, E. I. (1968). *Financial Ratios, Discriminant Analysis and the Prediction of Corporate Bankruptcy.* Journal of Finance, 23(4), 589–609. — The Z-score: five ratios, one number, and a screen that is still used sixty years later. Remember it is a screen, not a valuation.
- Hotchkiss, E. S. (1995). *Postbankruptcy Performance and Management Turnover.* Journal of Finance, 50(1), 3–21. — 197 companies emerge from Chapter 11; over 40% still lose money three years later, and a third end up back in distress. The balance sheet can be fixed faster than the business.

*Next up: 38 | Covenants and Credit Agreements: What Actually Protects a Lender*
