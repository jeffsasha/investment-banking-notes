# 44 | Fund Finance: Subscription Lines and NAV Loans — The Leverage Behind the Fund

*Articles 40 through 43 were all about what happens inside a fund's portfolio. This article looks at something quieter, something that happens at the fund level, above the portfolio companies: the fund itself borrowing money. It sounds strange at first. A private equity fund is a pool of other people's money. Why would it need to borrow? The answer is that a fund is not just a pool of money; it is a machine for moving money on a schedule, and borrowing is how the machine smooths out the bumps. Two kinds of borrowing matter — subscription lines and NAV loans — and the first one quietly changes the return number every LP reads in a pitch deck.*

> **Learning goals.** After this article you can: (1) explain what a subscription line of credit is, what backs it, and why a fund draws on it instead of calling LP capital; (2) show, with arithmetic, how delaying a capital call raises a fund's reported IRR while slightly lowering its MOIC; (3) explain what a NAV loan is, how it differs from a subscription line, and why it is riskier; (4) compute the effect of a NAV loan on equity returns in both an up year and a down year; (5) name the three main risks of fund-level borrowing — LP default, lender concentration, and the illusion of performance — and say who bears each one; (6) read a fund's track record and ask how much of its IRR came from borrowing rather than investing.
>
> **Prerequisites.** Article 08 (LBO) for sources and uses, MOIC, IRR, and carry; article 06 (DCF I) for the idea that a dollar's value depends on when it moves; article 41 (secondary buyouts) for the fund-life clock and why distributions matter for fundraising; article 43 (permanent capital) for the difference between closed-end fund capital and everything else.

## 1. The Idea in One Paragraph

A private equity fund does not receive its investors' money on day one. When a **limited partner** (LP) — a pension fund, an endowment, a family office — commits $100 million to a fund, it is making a promise, not writing a cheque. The fund **calls** that capital in pieces, over several years, as it finds deals. A **subscription line of credit**, usually just called a **sub line**, is a short-term loan to the fund that is secured by those uncalled promises. When the fund finds a deal, instead of waiting ten business days for dozens of LPs to wire money, it draws on the sub line, closes the deal the same week, and calls the LP capital a few months later to repay the line. A **NAV loan** is the older sibling's bolder move: a loan secured not by promises but by the value of the portfolio itself — the **net asset value** (NAV) of the companies the fund already owns — used to fund new investments, pay distributions, or bridge a fund that is running out of dry powder. Both are leverage at the fund level, not the company level, and both change the numbers LPs see. The first one changes them in a way that is easy to miss and hard to undo.

The distinction to hold onto is between *where* the leverage sits. In article 08, the leverage sat inside the portfolio company: the LBO borrowed money to buy the business, and the debt was secured by the business's cash flows. Fund finance puts leverage one level up, at the fund. The collateral is either the LPs' promises (sub line) or the portfolio's value (NAV loan). The fund's investments are the same either way. What changes is the timing of the LPs' cash flows — and in private equity, timing is most of what the headline return number measures.

## 2. Why a Fund Borrows at All

Start with the problem the sub line solves, because it is a genuine problem, not a trick. A fund's life has a rhythm: it commits capital to deals as they appear, and it calls capital from LPs to pay for them. A capital call is a formal notice — "send us your share of $50 million within ten business days" — and for an LP with commitments to fifty funds, the notices arrive constantly, in unpredictable sizes, on unpredictable dates. An LP's treasury team has to keep cash ready or sell liquid assets on short notice.

The fund has its own timing problem. Deals do not wait for wire transfers: a seller who has accepted your bid wants to close, and a competitive auction does not pause while forty pension funds process paperwork. If the fund has to call capital before it can sign, every deal carries a two-week delay — and in a hot auction two weeks can lose the deal.

The sub line solves both problems at once. The fund negotiates a revolving credit facility with a bank — typically sized at 10 to 30 percent of total commitments — secured by the LPs' uncalled capital. When a deal needs funding, the fund draws on the line the same day. The deal closes. Months later, the fund calls the capital and repays the line. The LPs get fewer, larger, more predictable calls. The fund gets speed and certainty. The cost is interest on the line, usually SOFR plus a spread of roughly 150 to 250 basis points, plus an unused commitment fee on the undrawn part. For a line drawn for a few months, that cost is small. So far, so sensible.

But here is the catch, and it is the whole point of this article. The sub line does not only change *when* the LP's money moves. It changes the fund's reported IRR — the single number that most determines whether the fund can raise its next fund. And it changes it in only one direction: up.

## 3. The Subscription Line, Mechanically

Here is the sequence for a fund with $1 billion of commitments and a $200 million sub line.

1. **The fund finds a deal.** It needs $100 million to close an acquisition.
2. **Instead of calling capital, it draws $100 million from the sub line.** The money moves the same day. The deal closes.
3. **The fund holds the draw for a few months.** Industry practice is 90 to 180 days per draw, though some funds stretch this to a year or more.
4. **The fund calls the capital.** LPs wire their $100 million. The line is repaid, with interest.
5. **The fund's books show the investment as if it had been funded by LP capital** — except that the LP's cash left their account months after the investment was made.

The collateral explains why banks love this lending: the bank is not lending against illiquid portfolio companies but against the promises of pension funds, endowments, and sovereign wealth funds — some of the most creditworthy borrowers on earth. If an LP defaults, the fund agreement lets the bank call that LP directly. That is why sub lines are cheap, and why they are available to almost any established fund.

There is one more mechanical detail worth knowing: the sub line is usually *revolving*. The fund can draw, repay, and draw again, so the same $200 million facility can fund several deals in sequence. When uncalled capital shrinks — late in a fund's life, most commitments have been called — the line shrinks with it. That is why sub lines are a young fund's tool and why NAV loans, which are secured by the portfolio instead, take over later in the fund's life.

## 4. The Worked Example: How a Six-Month Delay Moves the IRR

This is the section to do slowly, because the result feels wrong the first time you see it. The same deal, the same exit, the same dollars of profit — and a different reported return. Nothing about the investment changed. Only the timing of the LP's cheque changed.

**Without a subscription line.** The LP wires $100 million at year 0 and receives $180 million at year 5.

```math
\text{MOIC} = \frac{180}{100} = 1.80x
```

```math
\text{IRR} = \left(\frac{180}{100}\right)^{1/5} - 1 = 1.80^{0.2} - 1 \approx 12.5\%
```

The MOIC — multiple on invested capital — is 1.80x: the LP got back $1.80 for every $1.00 invested. The IRR — the annualised rate that equates the cash out to the cash in — is about 12.5%.

**With a subscription line.** The fund draws $100 million from the line at year 0 and closes the deal. The LP's capital is not called until six months later, at year 0.5. The line charges interest: say 5.5% a year, so six months of interest on $100 million is

```math
100 \times 0.055 \times 0.5 = \$2.75 \text{ million}
```

Exit proceeds are still $180 million, but $2.75 million goes to pay the line's interest, so the LP receives $177.25 million at year 5, having wired $100 million at year 0.5.

```math
\text{MOIC} = \frac{177.25}{100} = 1.77x
```

```math
\text{IRR} = \left(\frac{177.25}{100}\right)^{1/4.5} - 1 = 1.7725^{1/4.5} - 1 \approx 13.6\%
```

Read that again. The LP made *less* money — $177.25 million instead of $180 million, because the interest came out of their pocket. The MOIC fell, from 1.80x to 1.77x. And yet the reported IRR *rose*, from 12.5% to 13.6% — a gain of more than a full percentage point.

Why? Because IRR is a time-weighted measure. It answers the question "how fast did my money compound?" — and the sub line shortened the time the LP's money was actually at work, from five years to four and a half, without shortening the time the investment itself was compounding. The LP's cash arrived later and left at the same time. Fewer years, nearly the same dollars, higher annualised rate. The interest cost shaved a little off the total; the shorter clock added a lot to the rate.

Two things follow. First, MOIC and IRR can move in opposite directions: MOIC tells you the truth about dollars, IRR the truth about timing. Second, a GP whose pay and fundraising depend on IRR has a direct incentive to use the sub line as much as possible, for as long as possible — every extra month of delay is a little more IRR, at a cost borne mostly by the LP.

## 5. What the Research Actually Finds

Two independent research teams found the same thing with different data.

Albertus and Denes (2019), in "Distorting Private Equity Performance: The Rise of Fund Debt" (Kenan Institute, UNC), used confidential data on U.S. buyout funds and found that funds using subscription lines raised their IRR-based performance by **6.1 percentage points** on average, while their multiples-based performance *slightly declined*. That is the pattern from our worked example, at fund scale: IRR up a lot, MOIC down a little. They also found sub lines more common among poorly performing funds, and that using them increased the GP's carried interest.

Schillinger, Braun, and Cornel (2019), in "Distortion or Cash Flow Management? Understanding Credit Facilities in Private Equity Funds" (Technical University of Munich), simulated hypothetical sub lines across 6,353 buyout deals and 700 funds. Their conclusion was more moderate: when sub lines were used for six months or less, the median fund's net IRR improved by only **0.20 percentage points** (mean: 0.47 points) — a cash-flow management tool, not a distortion machine. But when maturities were stretched to two years, **44.4% of funds improved their ranking by at least one decile**. The effect is small when the line is used as designed and large when it is stretched. Duration is the variable that matters.

MSCI's research (January 2024) lands between the two: for recent vintages of buyout and real estate funds, the median sub line inflated current IRRs by approximately **100 basis points** — with the effect growing as delays lengthened. The median buyout fund delayed calls by around 45 days in recent vintages, up from 20 days for the 2015 vintage. The direction of travel is toward longer delays, which is toward larger distortions.

The honest summary: a sub line used for a few months is mostly plumbing. A sub line used for a year or two is mostly marketing. The ILPA, the trade body for LPs, published guidance in 2017 urging GPs to disclose sub line usage and to report performance both with and without its effect — because the only cure is transparency.

## 6. NAV Loans: Borrowing Against the Portfolio

A NAV loan is a different animal, and a riskier one. Where a sub line is secured by promises — uncalled capital — a NAV loan is secured by the portfolio itself. The lender takes a security interest in the fund's equity in its portfolio companies, and sometimes in its right to receive distributions. The loan is typically sized at 10 to 25 percent of NAV, with a term of two to five years, and it is used for one of three purposes.

**To fund new investments late in a fund's life.** A fund in year seven has invested most of its capital and has little uncalled capital left, so the sub line has shrunk to almost nothing. A NAV loan lets it fund a good add-on acquisition without calling the last of the LPs' capital.

**To pay distributions.** A fund that wants to show distributions — remember from article 41 that distributions are the currency of fundraising — can borrow against the portfolio and distribute the proceeds to LPs. The LP receives cash, the fund's NAV falls by the amount borrowed, and the portfolio companies are now leveraged twice over: once at the company level, once at the fund level.

**To bridge a continuation fund or a GP-led secondary.** In articles 41 and 42, the fund needed cash to buy assets from itself. A NAV loan can provide it.

Why is a NAV loan riskier than a sub line? Three reasons. First, the collateral is the portfolio, which is illiquid and whose value is the GP's own estimate. Second, the loan is longer and larger, so the interest cost is material. Third, the lender's claim sits *above* the LPs in the fund's capital structure. If the portfolio falls in value, the lender still gets paid first, and the LPs absorb the loss — leveraged, as the example below shows.

## 7. The Worked Example: A NAV Loan in an Up Year and a Down Year

Take a fund with a portfolio worth $200 million of NAV and no debt. It borrows $40 million — a 20% loan-to-value — at 8% interest for one year, and uses the cash to make a distribution to LPs. The LPs now hold $40 million in cash plus a fund interest worth $160 million of equity.

**Up year: the portfolio grows 10%.** Assets are now $220 million. The debt has grown with interest to $40 \times 1.08 = \$43.2$ million. Equity is $220 - 43.2 = \$176.8$ million, on a starting equity base of $160 million.

```math
\text{Levered return} = \frac{176.8}{160} - 1 = 10.5\%
```

The unlevered portfolio returned 10.0%; the levered equity returned 10.5%. The loan amplified the gain by half a point, because the fund earned 10% on $200 million of assets while paying 8% on $40 million of debt — a positive spread of 2% on the borrowed money.

**Down year: the portfolio falls 10%.** Assets are now $180 million. The debt is still $43.2 million. Equity is $180 - 43.2 = \$136.8$ million.

```math
\text{Levered return} = \frac{136.8}{160} - 1 = -14.5\%
```

The unlevered portfolio lost 10.0%; the levered equity lost 14.5%. The same leverage that added half a point on the way up took away four and a half points on the way down. That asymmetry is the point: the interest is fixed and the asset return is not.

Now add the second-order risk. The loan is secured by the portfolio, and the lender has covenants — typically a maximum loan-to-value ratio. If the portfolio falls far enough to breach the covenant, the lender can demand repayment, force asset sales, or take control of distributions. In a down year, the fund may be forced to sell a company at the worst possible moment to repay a loan that was taken out to pay a distribution in a good year.

## 8. The Three Risks, and Who Bears Them

Fund-level borrowing has three risks, and they fall on different people.

**LP default risk — borne by the bank, and then by everyone.** A sub line works because the bank trusts the LPs. If a large LP defaults on a capital call — a pension fund in distress, a sovereign fund under sanctions, a family office that over-committed — the bank's collateral shrinks. Most facilities can exclude a defaulting LP from the borrowing base, which protects the bank. But a fund with several weak LPs can find its line cut exactly when it needs it most, mid-deal.

**Lender concentration and the denominator effect — borne by the LP.** The sub line market is dominated by a small number of banks, and those banks lend to many funds at once. In a crisis, a bank worried about its own balance sheet can pull or reprice lines across the whole market at once — as happened, briefly, in March 2020 and during the 2023 regional bank stress. Separately, the sub line creates a *denominator effect* for the LP: because the LP's cash is called later, the LP's allocation to private equity looks smaller than it really is — until the calls arrive all at once, and the LP is suddenly over-allocated and short of cash.

**The illusion of performance — borne by the next fund's LPs.** A fund that reports a 25% IRR built partly on sub line timing will raise its next fund on the strength of that number. If the next fund uses sub lines less — because rates are higher, or because LPs now ask for the unadjusted numbers — its reported IRR will be lower, and the new LPs will feel misled. The cost of the illusion is paid by whoever believed the number last.

## 9. How to Read a Track Record That Used a Sub Line

If you are ever on the LP side of the table — and article 27's valuation work means you may one day be evaluating a fund rather than a company — here is the practical checklist.

- **Ask for the IRR both ways.** A GP that uses sub lines should be able to show you the fund's IRR calculated on the capital-call dates alongside the reported IRR. If the gap is more than a percentage point, the sub line did real work on the number.
- **Look at the MOIC, and at the DPI.** MOIC is not affected by timing, so it is the cleaner measure of how much value was actually created. **DPI** — distributions to paid-in capital — is even cleaner, because it cannot be flattered by a valuation or a delay. A fund with a high IRR, a mediocre MOIC, and a low DPI is a fund whose story is mostly timing.
- **Ask how long draws stay outstanding.** Ninety days is plumbing. A year is a choice. Two years is a strategy.
- **Ask what the line costs.** Interest and fees come out of the fund's returns, and in a high-rate environment the cost can exceed the benefit. When SOFR was near zero, the sub line was nearly free IRR; at 5%, it is not.
- **For NAV loans, ask what the proceeds were used for.** A NAV loan that funded a good add-on acquisition is a different decision from one that funded a distribution. And ask about the covenants: what loan-to-value triggers a forced repayment, and what happens if the portfolio is marked down 20%?

None of this makes fund finance bad. A sub line that closes a deal a week earlier, or that spares forty pension funds an emergency wire, is genuinely useful. The problem is a number that looks like a measure of investing skill and is partly a measure of financing technique — and a market that, for a decade, mostly did not ask which part was which.

## 10. Common Misconceptions

**"A subscription line increases a fund's returns."** It increases the reported IRR and *decreases* the MOIC, because the interest is a real cost. It increases the speed at which the LP's money is put to work, not the amount of profit the investments generate.

**"NAV loans and subscription lines are the same thing."** They are secured by different things — promises versus portfolio value — they have different maturities, different sizes, and different risk. A sub line is short-term bridge financing; a NAV loan is medium-term leverage on the fund's own balance sheet.

**"Leverage at the fund level is the same as leverage at the company level."** It is not. Company-level debt in an LBO is non-recourse to the fund: if the company fails, the lender takes the company and the fund loses its equity. Fund-level debt is secured by the LPs' commitments or the whole portfolio, so a failure at the fund level can reach across the portfolio and across the LPs. The blast radius is larger.

**"If the IRR is high, the fund must be good."** IRR is sensitive to timing, to leverage, and to the order of cash flows. A fund can report a high IRR with mediocre investments if it delays calls long enough, and a fund can report a low IRR with good investments if it calls capital early and holds for a long time. Read the IRR with the MOIC and the DPI, and ask for the unadjusted numbers, before concluding anything about skill.

## 11. Test Yourself

**1.** A fund invests $50 million at year 0 and exits at $110 million at year 4. What are the MOIC and the IRR, with no subscription line? Now suppose a sub line delays the LP's $50 million call by one year, at a $3 million interest cost, so the LP receives $107 million at year 4. What are the new MOIC and IRR?

*Answer: Without the line, MOIC = 110/50 = 2.20x, and IRR = 2.20^(1/4) − 1 ≈ 21.8%. With the line, MOIC = 107/50 = 2.14x, and IRR = (107/50)^(1/3) − 1 = 2.14^(1/3) − 1 ≈ 28.9%. The LP made $3 million less, the MOIC fell, and the IRR rose by about 7 percentage points — because the holding period shrank from four years to three.*

**2.** Why is a subscription line cheap for the bank to provide, and what is the bank actually lending against?

*Answer: The bank lends against the LPs' uncalled capital commitments — legal promises from pension funds, endowments, and sovereign wealth funds — not against illiquid portfolio companies. If an LP defaults, the fund agreement typically lets the lender call that LP directly, which is why the spread over SOFR is only around 150–250 basis points.*

**3.** A fund has $300 million of NAV, borrows $60 million at 9% for one year, and the portfolio returns 12% over that year. What is the levered equity return? What if the portfolio returns 0%?

*Answer: Assets grow to $336 million; debt grows to $60 × 1.09 = $65.4 million; equity is $336 − $65.4 = $270.6 million on $240 million of starting equity, a return of 12.75% — slightly better than the unlevered 12%. If the portfolio returns 0%, assets stay at $300 million and equity is $300 − $65.4 = $234.6 million, a return of −2.25%. The loan cost the LPs 2.25% in a flat year.*

**4.** A GP shows you a fund with a 22% net IRR, a 1.5x MOIC, and a 0.6x DPI. What should you suspect, and what two numbers would you ask for before committing?

*Answer: Suspect that the IRR is flattered by timing — subscription line delays, early distributions, or both — rather than by value creation, because a 1.5x MOIC over a typical fund life does not naturally produce a 22% IRR, and a 0.6x DPI means most of the value is still unrealised paper gains. Ask for the IRR calculated on the capital-call dates and for the average length of time sub line draws stayed outstanding.*

## Next up

**45 | GP Stakes: When Investors Buy the Manager** — what happens when the money stops buying funds and starts buying the firms that run them.
