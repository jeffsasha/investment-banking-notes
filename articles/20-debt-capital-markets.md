# 20 | Debt Capital Markets: How a Bond Deal Gets Done

*Last article, we watched a company sell shares for the first time and leave money on the table. This article is about the other, much bigger half of the capital markets — the one that rarely makes headlines. Companies borrow far more money by selling bonds than they ever raise by selling stock, and yet most people outside finance could not tell you how a bond deal actually happens. The short version: a company rents money from strangers, promises to pay it back with interest, and a bank runs an auction to find the price. The long version is where it gets interesting, because the price of a bond is really two prices stacked on top of each other, and the negotiation between the company and its lenders is about which of those two prices moves.*

> **Learning goals.** After this article you can: (1) define a bond's coupon, maturity, face value, yield, and credit spread, and explain how they fit together; (2) price a plain-vanilla bond from its cash flows and explain why price and yield move in opposite directions; (3) walk through a new bond issue from mandate to pricing, including ratings, the roadshow, bookbuilding, and the new issue concession; (4) explain why a company's borrowing cost is a Treasury yield plus a spread, and what makes that spread widen or narrow; (5) explain why debt can be cheaper than equity — and why that does not mean a company should borrow without limit.
>
> **Prerequisites.** Article 03 (enterprise value versus equity value) for the capital structure picture, article 06 (DCF part I) for discounting cash flows, and article 19 (IPO pricing) for the bookbuilding idea, which shows up here too — with one important difference. No new accounting is needed.

## 1. The Quiet Giant: Debt Is Where Most of the Money Is

An **initial public offering** is a rare event in a company's life. Borrowing is routine. A healthy large company might issue stock once a decade and issue bonds every year or two. Add up all the corporate bonds outstanding in the world and the total dwarfs the money raised in IPOs in any given year, usually by an order of magnitude.

Why? Three reasons, and the first two are the same reasons companies like debt in the first place:

- **Interest is tax-deductible, dividends are not.** A dollar of interest reduces taxable income; a dollar of dividends does not. That alone makes debt cheaper than equity, all else equal.
- **Debt does not dilute ownership.** Selling bonds does not give the buyers a vote or a share of future growth. Founders and existing shareholders keep control.
- **The buyers are different.** Stock buyers want growth and accept volatility. Bond buyers — pension funds, insurers, mutual funds — mostly want steady income and their money back. They are a huge, hungry pool of capital, and they will lend to any company whose story they believe at the right price.

But debt has a hard edge that equity does not: it must be repaid on a schedule, whether business is good or not. Miss a payment and you are in default, which is the road to article 13's restructuring world. Equity never has to be repaid. That trade-off — cheaper and non-dilutive, but unforgiving — is the whole story of corporate borrowing, and it is why the bond market spends so much effort pricing risk.

**Debt capital markets (DCM)** is the part of an investment bank that helps companies borrow by selling bonds. Its equity sibling, ECM, handles stock offerings like the IPO in article 19. The two desks sit near each other, use similar tools, and serve the same clients — but the products behave very differently, as we will see.

## 2. Anatomy of a Bond: Four Numbers and a Promise

A **bond** is a loan sliced into tradeable pieces. Instead of borrowing $500 million from one bank, a company sells 500,000 bonds of $1,000 each to hundreds of investors. Each bond is a contract with four numbers:

- **Face value (par):** the amount repaid at maturity. Usually $1,000 per bond.
- **Coupon:** the annual interest rate printed on the bond, paid on the face value. A 5% coupon on a $1,000 bond pays $50 a year, typically in two $25 semiannual installments.
- **Maturity:** when the face value is repaid — 5 years, 10 years, 30 years.
- **Price:** what an investor actually pays for the bond. This is the only one of the four that moves after the bond is issued, and it moves every day.

A bond's **yield** is the return an investor earns if they buy at the current price and hold to maturity, collecting every coupon and the face value. Yield is not printed on the bond; it is *derived* from the price. And here is the relationship that governs everything in fixed income:

> **When a bond's price goes up, its yield goes down. When its price goes down, its yield goes up.**

Why? Think of it as buying a fixed stream of future cash. If you pay less for the same stream, your return is higher. If you pay more, your return is lower. The coupons and the face value never change; only what you pay for them changes. This is not a quirk or a convention. It is arithmetic, and we can prove it with a worked example.

## 3. Pricing a Bond: The Same DCF You Already Know

A bond is just a set of future cash flows, so we price it the way article 06 taught us to price anything: discount each cash flow at the appropriate rate and add them up.

```math
\text{Bond price} = \sum_{t=1}^{n} \frac{\text{Coupon}}{(1 + y)^t} + \frac{\text{Face value}}{(1 + y)^n}
```

Here $y$ is the yield, $n$ is the number of years to maturity, and we are assuming annual coupons to keep the arithmetic clean. Real bonds usually pay semiannually, which just means twice as many smaller payments — the logic is identical.

Take a fictional bond: $1,000 face value, 5% annual coupon ($50 a year), 10 years to maturity.

**Case 1: the market yield is 5%.** Then the discount rate equals the coupon rate, and the price is exactly par:

```math
\text{Price} = 50 \times \frac{1 - (1.05)^{-10}}{0.05} + \frac{1000}{(1.05)^{10}} = 386.09 + 613.91 = 1000.00
```

**Case 2: the market yield rises to 6%.** Now investors demand more return, so they will only buy if the price drops:

```math
\text{Price} = 50 \times \frac{1 - (1.06)^{-10}}{0.06} + \frac{1000}{(1.06)^{10}} = 368.00 + 558.39 = 926.40
```

The bond trades at a **discount** to par — $926.40 for the promise of $1,000 plus coupons. Note that the coupons did not change. The $50 payments are still $50. What changed is what investors will pay for them.

**Case 3: the market yield falls to 4%.** Now the bond's 5% coupon looks generous, and investors bid the price up:

```math
\text{Price} = 50 \times \frac{1 - (1.04)^{-10}}{0.04} + \frac{1000}{(1.04)^{10}} = 405.54 + 675.56 = 1081.11
```

The bond trades at a **premium** to par. Three cases, one rule: price and yield are two sides of the same coin. If someone tells you a bond's price fell, they have also told you its yield rose — which means the company's borrowing cost just went up, even though the company itself did nothing.

One more concept falls out of this math, and bankers use it every day: **duration**. Duration measures how sensitive a bond's price is to a change in yield. Roughly, a bond with a duration of 7 will lose about 7% of its value if yields rise by 1 percentage point (100 basis points). Our 10-year, 5.8% bond from the example later in this article has a modified duration of about 7.4, so a 0.10 percentage point (10 basis point) rise in yield knocks roughly 0.74% off its price. Longer maturity means higher duration means more price swing. This is why a 30-year bond feels like a roller coaster and a 2-year bond feels like a savings account.

## 4. The Spread: Two Prices Stacked on Top of Each Other

So far we have treated "the yield" as one number. In practice, a corporate bond's yield is built from two pieces:

```math
\text{Corporate bond yield} = \text{Treasury yield} + \text{Credit spread}
```

- The **Treasury yield** is the yield on a US government bond of the same maturity — the "risk-free" rate, since the US government is assumed not to default. If the 10-year Treasury yields 4.30%, that is the floor: nobody lends to a company for less than they could get from the government.
- The **credit spread** is the extra yield investors demand for taking the company's credit risk — the chance it defaults, plus compensation for the bond being harder to trade than a Treasury. Spreads are quoted in **basis points (bps)**: 100 bps = 1 percentage point. A spread of 150 bps means 1.50% on top of the Treasury yield.

This decomposition matters because the two pieces move for different reasons. The Treasury yield moves with interest rates, inflation expectations, and Federal Reserve policy — things the company cannot control. The spread moves with the company's own story: its earnings, its leverage, its industry, and the market's appetite for risk. When people say "borrowing costs rose," you should always ask: was it rates, or was it the spread?

A strong, household-name company might borrow at Treasury + 80 bps. A solid but unremarkable company might pay Treasury + 150 bps. A company with real problems might pay Treasury + 500 bps or more — and past a certain point, the bond market simply closes: at some spread, no investor wants the risk at any price the company can afford, and the company must find another way to fund itself (usually a bank loan, or, in the worst case, restructuring).

What actually determines the spread? The structural view of credit risk, pioneered by Merton (1974), says a company's debt and equity are both claims on the same underlying asset value: equity is like a call option on the firm's assets, and debt is what is left over. In that framework, the spread should depend on leverage, asset volatility, and time to maturity — the riskier the assets and the thinner the equity cushion, the wider the spread. Reality is messier. Collin-Dufresne, Goldstein, and Martin (2001) studied thousands of bonds and found that the variables structural models predict should explain spread *changes* — leverage, volatility, rates — actually explain only a small part of them. Much of the month-to-month movement comes from a common factor that looks a lot like supply and demand in the bond market itself: when investors are hungry for bonds, spreads tighten for everyone; when they retreat, spreads widen for everyone, regardless of any single company's news. That is an honest, useful warning: spreads are not a pure report card on one company. They are also a weather report on the whole market.

## 5. How a Deal Gets Done: From Mandate to Pricing

Now the part the textbooks usually skip: what actually happens, in order, when a company issues a bond. The process takes about one to two weeks for a standard deal, and it rhymes with the IPO process in article 19 — with one crucial difference we will get to.

**Step 1: The mandate.** The company picks one or more banks as **bookrunners**. Often it runs a quick competitive process, but for frequent issuers the relationship is ongoing: the banks that cover the company pitch ideas all year, and when the company decides to borrow, it picks its favorites. The bookrunners agree on the rough shape of the deal — maturity, size, maybe a target spread.

**Step 2: Ratings.** Most large bond deals carry credit ratings from agencies like Moody's, S&P, and Fitch — letters from AAA down to D that summarize default risk. Investment-grade means BBB-/Baa3 or above; below that is **high yield** (or, less politely, junk). The rating largely determines who is allowed to buy: many pension funds and insurers can only hold investment-grade bonds. A rating is not a guarantee — agencies get things wrong, sometimes spectacularly — but it is the market's shared shorthand, and losing investment-grade status (a "fallen angel") can force selling by funds that are no longer allowed to hold the bond.

**Step 3: Documentation.** Lawyers draft the **indenture**, the contract between the company and bondholders. The key parts are the **covenants**: promises like "we will not take on debt above X times earnings" or "we will not sell our core assets." Covenants are the lenders' seatbelts. Strong companies get loose covenants ("cov-lite"); weaker ones accept tight ones. This negotiation is quiet but real: every covenant is a trade between the company's freedom and the lenders' safety, and the spread reflects the outcome.

**Step 4: The roadshow and the bookbuild.** The company and the banks present the deal to investors — in person, by phone, or by video — and then open the **book**: investors submit orders stating how much they want and at what spread. The banks announce **initial price thoughts (IPTs)**, a deliberately wide starting spread, and then tighten it as orders pile in. This is exactly the IPO bookbuild from article 19, but with a key difference: bond investors mostly compete on *price* (the spread), not on whether they get in at all, and the book is usually covered several times over, which gives the banks room to tighten.

**Step 5: Pricing and allocation.** When the book is big enough, the banks set the final spread, the coupon is fixed (usually at a level that prices the bond at par), and orders are allocated. Investors who bid at the final spread get bonds; those who demanded a wider spread do not. The company gets its money, the banks earn a fee (much smaller, in percentage terms, than an IPO fee — bond fees are typically well under 1% of the deal), and the bond starts trading.

One number from this process deserves its own name: the **new issue concession**. New bonds usually price at a slightly wider spread than the company's existing bonds trade at — investors get a small discount for buying a new, untested bond instead of a seasoned one. If the company's existing 10-year bonds trade at Treasury + 140 bps and the new bond prices at Treasury + 150 bps, the concession is 10 bps. Bankers argue about it constantly, because 10 bps on a $500 million deal is $500,000 a year in extra interest — real money, paid for years.

## 6. A Full Worked Example: Meridian Manufacturing Borrows $500 Million

Let us put it all together with a fictional company, Meridian Manufacturing, a maker of industrial equipment with steady cash flows and a BBB rating — solidly investment grade, not a star.

Meridian wants $500 million for 10 years to build a new plant. The 10-year Treasury yields 4.30%. Its existing bonds trade around Treasury + 140 bps. The banks sound out investors and open the book with initial price thoughts of Treasury + 165 bps — a generous starting point with room to tighten.

Demand is strong: the book reaches $2.1 billion of orders, more than four times the deal size. The banks tighten in two steps, first to Treasury + 155 bps, then to a final spread of Treasury + 150 bps — a 10 bps concession over where Meridian's old bonds trade. The final yield is:

```math
\text{Yield} = 4.30\% + 1.50\% = 5.80\%
```

The coupon is set at 5.80%, so the bond prices at par: investors pay $1,000 per bond, Meridian receives $500 million, and its annual interest bill is:

```math
500{,}000{,}000 \times 5.80\% = 29{,}000{,}000
```

$29 million a year, every year for 10 years, plus $500 million back at maturity. That 15 bps of tightening from initial price thoughts to final pricing — from 165 down to 150 — saves Meridian real money:

```math
500{,}000{,}000 \times 0.15\% = 750{,}000 \text{ per year}
```

$750,000 a year for ten years, or $7.5 million total, saved because investors competed for the deal. This is why companies care so much about the bookbuild, and why banks compete so hard to run it: a well-run auction is worth millions to the issuer.

But notice the risk Meridian now carries. Suppose six months later Treasury yields rise by 1 percentage point and Meridian's spread widens by 1 point too. Its bond, with a modified duration of about 7.4, would fall roughly 14.8% in price — but that does not hurt Meridian directly, because Meridian already has the money and its coupon is fixed. The pain falls on the investors holding the bond. Meridian's real risk is different: in 10 years it must repay or refinance $500 million. If the market is closed or its spread has blown out by then, refinancing could be painful or impossible. Debt is a promise to be creditworthy *in the future*, not just today, and the maturity schedule — when each chunk of debt comes due — is one of the first things a credit analyst checks.

## 7. Why Not Just Borrow Forever?

If debt is tax-deductible, non-dilutive, and often cheaper than equity, why does any company issue stock at all? Because debt has a breaking point, and the market enforces it.

First, **interest must be paid in cash, on time, in bad years too**. A company whose earnings swing wildly cannot promise fixed payments with confidence. Second, **lenders ration credit**: as leverage rises, spreads widen, covenants tighten, and eventually the market says no. Third, **distress is expensive**: the costs of near-default — lost customers, departing employees, suppliers demanding cash upfront — arrive long before actual bankruptcy, and they destroy value fast. The classic trade-off theory of capital structure says companies balance the tax benefit of debt against these expected distress costs, and borrow up to the point where the next dollar of debt costs more in risk than it saves in tax.

There is also a signaling angle worth remembering from earlier articles. Myers and Majluf (1984) argued that issuing equity signals bad news — managers sell stock when they think it is overvalued — which is one reason companies prefer debt and prefer internal cash most of all. The bond market, in this view, is not just a funding channel; it is a place where a company's choice of *how* to fund itself tells investors something about what management believes. A company that suddenly issues a lot of equity when it could have borrowed is saying something, whether it means to or not.

## Common Misconceptions

**"A bond's coupon is its return."** No. The coupon is a fixed payment; the return is the yield, which depends on what you paid. Buy a 5% coupon bond at $926 and your yield is 6%. Buy the same bond at $1,081 and your yield is 4%. Same bond, same coupons, different returns. Confusing the two is the single most common beginner error in fixed income.

**"If a bond's price falls, the company is in trouble."** Not necessarily. A bond's price falls whenever yields rise, and yields rise when Treasury rates rise — which can happen because the economy is doing *well*. To judge the company, look at the spread, not the price. A falling price with a stable spread is a rates story. A widening spread is a company story.

**"High yield means high return."** High yield means high *promised* return. The extra yield is compensation for default risk, and some of those bonds will default. The realized return on a portfolio of high-yield bonds is much lower than the headline yield, because the defaults eat part of it. Yield is not return; yield minus losses is.

**"The company sets the interest rate on its bonds."** The company proposes, the market disposes. The coupon is set at pricing to match the yield investors demand. If the company insists on a coupon below what the market wants, the bond prices at a discount — investors still get their yield, just in a different form. Either way, the market, not the issuer, decides the cost of borrowing.

**"A bond deal is done at pricing."** Pricing is the beginning of the bond's life, not the end. The bond then trades for years, its price moves with rates and spreads, it may be downgraded or upgraded, called early if it has a call feature, or tendered for in a refinancing. Bankers who ran the deal keep watching it, because the next deal depends on how this one performed.

## Test Yourself

**1.** A $1,000 par bond pays a 6% annual coupon and matures in 5 years. If the market yield is 6%, what is its price? If the yield rises to 8%, does the price rise or fall — and why, in one sentence?

*Answer: At a 6% yield the price is par, $1,000 — the coupon rate equals the yield, so the discounted cash flows sum exactly to face value. At 8% the price falls below par (to about $920.15): investors discount the same fixed coupons and principal at a higher rate, so they will only pay less for the same stream.*

**2.** Meridian's new bond yields 5.80% when the 10-year Treasury yields 4.30%. What is the credit spread in basis points? If Treasury yields rise to 5.30% while the spread is unchanged, what is the bond's new yield — and does Meridian's annual interest bill change?

*Answer: The spread is 5.80% − 4.30% = 1.50%, or 150 bps. The new yield is 5.30% + 1.50% = 6.80%. Meridian's interest bill does not change: its coupon is fixed at 5.80% for the life of the bond. The higher yield means the bond's price falls in the secondary market, hurting current holders, not the issuer.*

**3.** A company's existing bonds trade at Treasury + 120 bps. Its new bond prices at Treasury + 135 bps. What is the new issue concession, and what does it cost the company per year on a $400 million deal?

*Answer: The concession is 135 − 120 = 15 bps. On $400 million that is 400,000,000 × 0.15% = $600,000 per year in extra interest versus borrowing at its existing spread.*

**4.** Two companies each issue a 10-year bond. Company A is rated AA and prices at Treasury + 70 bps. Company B is rated BB and prices at Treasury + 420 bps. Which company's bond has the higher yield, and name two reasons an investor might still prefer Company A's bond despite its lower yield.

*Answer: Company B's bond has the higher yield (by 350 bps). An investor might still prefer A's bond because (a) default risk is far lower — the promised yield on B is partly compensation for bonds that will not pay in full — and (b) A's bond is more liquid and easier to sell, and may be eligible for portfolios that cannot hold below-investment-grade debt.*

## References

- Merton, R. C. (1974). "On the Pricing of Corporate Debt: The Risk Structure of Interest Rates." *Journal of Finance*, 29(2), 449–470. — The structural model of credit risk: equity as a call option on the firm's assets, debt priced from the same asset value.
- Collin-Dufresne, P., Goldstein, R. S., & Martin, J. S. (2001). "The Determinants of Credit Spread Changes." *Journal of Finance*, 56(6), 1939–1975. — The variables structural models predict should move spreads explain only a small share of actual spread changes; a common supply-and-demand factor drives much of the rest.

*Next up: Leveraged Finance: High-Yield Bonds and Leveraged Loans — what happens when the borrower is not investment grade at all.*
