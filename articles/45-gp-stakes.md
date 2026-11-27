# 45 | GP Stakes: When Investors Buy the Manager

*For forty-four articles, every investment we have looked at bought a piece of a company — or a fund that buys companies. This one buys a piece of the buyer. A GP stake is a minority investment in the management company of a private equity firm: instead of committing capital to the fund, you buy a slice of the fees and carried interest the firm earns from all of its funds, forever. It sounds like a small legal distinction. In practice it is a different asset class, with different cash flows, different risks — and, as the research shows, a surprisingly different answer to the question of who is really getting rich in private equity.*

> **Learning goals.** After this article you can: (1) explain what a GP stake is, what exactly the buyer owns, and how it differs from an LP commitment to a fund; (2) split a manager's earnings into fee-related earnings (FRE) and performance-related earnings (PRE) and explain why they are valued at different multiples; (3) value a GP stake from scratch with an FRE multiple plus a carry value, and compute the buyer's implied cash yield; (4) explain why a manager sells a piece of itself and why a pension fund or sovereign wealth fund buys it; (5) tell the Petershill story — the 2021 IPO, the persistent discount, the 2025 delisting — and say what it reveals about valuing managers; (6) summarise what the academic research actually finds about GP stakes and the agency question they raise.
>
> **Prerequisites.** Article 06 (DCF I) for discounting a stream of cash flows and the idea that different cash flows deserve different discount rates; article 08 (LBO) for management fees, carried interest, and the GP/LP split; article 41 (secondary buyouts) for the fund-life clock and why a manager's fee base erodes as funds age; article 43 (permanent capital) for the difference between a finite fund and a permanent firm.

## 1. The Idea in One Paragraph

A private equity firm is two things at once. There are the **funds** — finite partnerships that buy companies, hold them for a few years, and sell them. And there is the **management company** — the permanent firm that employs the partners, raises the funds, and collects the fees. An LP invests in the funds. A GP stake investor invests in the management company. The typical deal is a minority claim — usually 10 to 25 percent — on the management company's future earnings: its management fees and its carried interest, from every fund it manages, current and future. The buyer gets no material control rights. It cannot hire or fire partners, cannot approve deals, cannot vote on strategy. What it gets is a share of the money the machine makes, for as long as the machine keeps running.

The distinction to hold onto is between buying the *assets* and buying the *toll collector*. An LP's return depends on whether the portfolio companies do well. A GP stake's return depends on whether the manager keeps raising funds and collecting fees — which it does even when the portfolio companies do badly. The classic shorthand is "picks and shovels": during a gold rush, the reliable money is not in finding gold but in selling the tools. A GP stake is the picks-and-shovels trade on private equity itself.

## 2. Anatomy: What a Manager Actually Earns

A management company has two income streams, and they behave nothing alike.

**Fee-related earnings (FRE)** are the boring, reliable half. The firm charges a management fee — typically 1.5 to 2 percent of committed capital during a fund's investment period, stepping down to a fee on *invested* capital once the investment period ends — and pays its salaries, rent, and travel out of it. What is left is FRE. It is contractual, recurring, and largely independent of whether the deals work out. A fund can lose money and still pay its management fee in full. That is the point, and also the sore point for LPs.

**Performance-related earnings (PRE)** are the volatile half: carried interest, usually 20 percent of the funds' profits above a preferred return of around 8 percent. Carry arrives in lumps, years after the work was done, and only if the investments actually made money. In a good vintage it can dwarf the fees. In a bad one it can be zero.

| | Fee-related earnings (FRE) | Performance-related earnings (PRE / carry) |
|---|---|---|
| Source | Management fees on AUM | 20% of fund profits above the hurdle |
| Timing | Quarterly, from day one | Lumpy, years later, only on exits |
| Depends on | Fundraising and AUM | Investment performance |
| If the fund loses money | Still paid in full | Zero |
| Valuation multiple | Higher (10–15x) — stable and recurring | Lower (4–8x) — uncertain and cyclical |

This split is the whole valuation problem in one table. You cannot value a manager with a single multiple, because you are valuing two different businesses stapled together: a steady annuity and a call option on future investment skill. Anyone who quotes you one number for a management company without splitting the two is either simplifying or selling you something.

One more mechanical detail matters before we do the numbers. A manager's fee base is not permanent. Funds have a ten-year life, and fees step down after the investment period — usually from a percentage of *committed* capital to a percentage of *invested* capital, which shrinks as companies are sold. A manager that stops raising new funds sees its fee income decay over a decade even if it does nothing wrong. So the value of a GP stake depends, above all, on one assumption: that the manager keeps raising the next fund, and the one after that. Fundraising is the engine; everything else is the exhaust.

## 3. The Worked Example: Valuing a GP Stake

Take a mid-sized buyout manager. It manages $10 billion of AUM across several funds, charges an average management fee of 1.5 percent, and runs at a 45 percent operating margin — a realistic figure for an established firm, where the partners' compensation is the largest cost and the back office is already built.

**Step 1: fee revenue.**

```math
\text{Fee revenue} = \$10{,}000\text{ million} \times 1.5\% = \$150\text{ million per year}
```

**Step 2: fee-related earnings.**

```math
\text{FRE} = \$150\text{ million} \times 45\% = \$67.5\text{ million per year}
```

**Step 3: value the FRE.** Stable, recurring earnings in asset management typically trade at 10 to 15 times earnings. Use 12x.

```math
\text{Value of FRE} = \$67.5\text{ million} \times 12 = \$810\text{ million}
```

**Step 4: value the carry.** Suppose the firm's funds generate, on average, $150 million a year of gross profit above the hurdle rate — an assumption, and the most fragile one in the whole exercise, because carry depends on future exits that have not happened yet. At a 20 percent carry, that is $30 million a year. Because carry is lumpy and uncertain, value it at a much lower multiple — say 6x.

```math
\text{Expected carry} = \$150\text{ million} \times 20\% = \$30\text{ million per year}
```

```math
\text{Value of carry} = \$30\text{ million} \times 6 = \$180\text{ million}
```

**Step 5: total firm value, and the stake.**

```math
\text{Firm value} = \$810\text{ million} + \$180\text{ million} = \$990\text{ million}
```

A buyer taking a 15 percent stake pays:

```math
\text{Stake price} = \$990\text{ million} \times 15\% = \$148.5\text{ million}
```

**Step 6: what the buyer actually receives.** Each year, the buyer collects 15 percent of the firm's earnings — 15 percent of the $67.5 million of FRE plus 15 percent of the $30 million of carry:

```math
\text{Buyer's annual earnings} = 15\% \times (\$67.5 + \$30)\text{ million} = \$14.6\text{ million}
```

```math
\text{Implied cash yield} = \frac{\$14.6\text{ million}}{\$148.5\text{ million}} \approx 9.8\%
```

That 9.8 percent is the pitch in a single number: a near-double-digit cash yield, mostly from contractual fees, plus upside if the firm raises bigger funds or its carry comes in above the assumption. It is also the number to interrogate. The yield is only as good as the assumptions behind it — above all the 12x FRE multiple and the $150 million of assumed annual profit above the hurdle. Change the FRE multiple to 9x and the firm is worth $787.5 million, the stake costs $118 million, and the same $14.6 million of earnings is suddenly a 12.4 percent yield — which sounds better only because you paid less for the same cash flows. The multiple is not a fact of nature. It is a price, and prices are where the negotiation lives.

## 4. Why Would a Manager Sell a Piece of Itself?

If the management company is a money machine, why sell 15 percent of it? The reasons are more human than financial.

**Founder liquidity and succession.** A private equity firm is a partnership, and a partner's wealth is trapped inside the firm. A founder in her sixties who built a $10 billion manager is, on paper, very rich — and in cash terms, often not. She cannot sell shares on a stock exchange. A GP stake sale is how she realises some of that value without selling the firm, and how the next generation of partners buys in without taking on ruinous personal debt. Succession, in practice, is the single most common reason a stake gets sold.

**Growth capital.** The proceeds fund the things that make the next fund bigger: hiring senior deal partners, opening an office in a new city, seeding a new strategy — private credit, say, or infrastructure. A firm that wants to grow from $10 billion to $25 billion of AUM needs capital before the fees from the bigger funds arrive.

**The GP commitment.** Every fund requires the GP to invest 1 to 3 percent of the fund's capital alongside the LPs — its "skin in the game." For a $5 billion fund, that is $50 to $150 million the partners must find. Stake sale proceeds are a clean way to fund it, and the irony is deliberate: selling a share of the firm's economics lets the partners put *more* of their own money into the funds.

**The alternatives are worse.** A manager that needs firm-level capital has three options: sell a stake, borrow, or go public. Borrowing is hard — a firm's main asset is its people, and banks do not lend easily against human capital. Going public works — Blackstone, KKR, and Carlyle all did it — but it means quarterly earnings calls, public disclosure of compensation, and a share price that falls when fundraising slows. A GP stake is the quiet middle path: permanent capital, no public listing, no bank covenants.

## 5. Why Would Anyone Buy?

The buyers are a distinctive crowd: sovereign wealth funds, large pension funds, insurers, and fund-of-funds managers. They are buying four things.

**Yield.** A 9 to 10 percent cash yield, mostly from contractual fees, is hard to find elsewhere — especially yield that is not tied to interest rates or public market valuations.

**Duration.** An LP commitment lasts ten years and then returns your capital. A GP stake is permanent. It is a claim on every fund the manager will ever raise, including funds that do not exist yet. For a pension fund with liabilities stretching thirty years, that permanence is the product.

**Diversification.** A GP stake's returns are driven by AUM growth and fee rates, not by whether any single deal works. That makes it only loosely correlated with the rest of a portfolio — including with the buyer's own LP commitments to the same manager's funds.

**The picks-and-shovels logic.** If you believe private markets will keep growing as a share of the financial system — and the last twenty years give you reason to — then owning a slice of the managers is a way to own that growth without picking which funds will outperform.

The market has noticed. Cumulative GP stakes transaction volume grew from under $10 billion in 2015 to over $50 billion by 2024, according to industry research compiled by Omnigence Asset Management from PitchBook data. The dedicated buyers are now household names in the industry: Petershill at Goldman Sachs, Blackstone Strategic Capital, Dyal Capital — which became part of Blue Owl Capital in 2021 — and Neuberger Berman's Dyal platform. What began as an odd trade between partnerships is now an asset class with its own funds, conferences, and league tables.

## 6. The Petershill Story: The Listed Experiment

The cleanest way to see how the market values a GP stake is to look at the one time a portfolio of them was listed on a stock exchange.

Petershill began in 2007 as a team inside Goldman Sachs Asset Management, buying minority stakes in alternative asset managers. For fourteen years it operated as a series of closed-end funds. Then, in September 2021, Goldman listed Petershill Partners on the London Stock Exchange: 19 minority stakes in managers overseeing $187 billion of AUM, valued at £4 billion, raising about £1.2 billion of new money. The pitch was elegant — a listed, permanent vehicle giving public investors access to the economics of private markets.

The public market disagreed. The shares fell by more than half from the IPO price and traded at a persistent discount of roughly 50 percent to the portfolio's stated value, as Citywire reported in 2023. Critics pointed to thin disclosure — valuing minority stakes in private managers requires assumptions about future fundraising that are hard to audit from the outside — and to the uncomfortable fact that the buyer of a minority stake has no control over the manager, no ability to force a sale, and no say in how the proceeds are used. In September 2025, Petershill announced it would delist from the London Stock Exchange, concluding that public investors would not pay full value for the assets.

The lesson is not that GP stakes are bad investments. It is that they are hard to price in public, and that the price depends on who is doing the valuing. A pension fund buying a stake directly can diligence the manager, negotiate protections, and hold forever; it can pay 12x FRE with confidence. A public shareholder buying a listed portfolio of such stakes cannot diligence anything, cannot negotiate anything, and marks the position to market every day — and it applies a discount for all of that. The same cash flows, two different prices. Which brings us back to the worked example: the multiple is not a fact of nature. It is a price, and the price depends on who is paying.

## 7. What the Research Actually Finds

GP stakes were, until recently, almost unstudied by academics — the early literature was industry research from PitchBook and the managers themselves. Two studies have now filled the gap, and they agree on the facts while disagreeing, politely, on what the facts mean.

Gahng and Jackson, in "Selling Private Equity Fees" (first posted on SSRN in 2022; revise and resubmit at *Management Science*), built a panel of 2,862 private equity firms from 1990 to 2021 using PitchBook, Preqin, and regulatory filings. Their headline facts: the share of PE industry AUM overseen by firms that have sold a GP stake rose from 6.3 percent in 2000 to 31.8 percent in 2021 — nearly a third of the industry now sits inside staked firms. Sellers see AUM rise by 84 percent and income by 64 percent in the ten years after a sale, and every $1 of stake-sale proceeds is associated with an incremental $18 of AUM — a "PE multiplier" that works like a money multiplier for a manager's balance sheet. After selling, firms increase investment staff by about 25 percent and offices by about 15 percent, and their funds go on to earn public market equivalents of roughly 1.2 to 1.3 — outperforming the S&P 500 by 20 to 30 percent after fees. Fund performance does not deteriorate after a stake sale.

Fogelström and Gustafsson, in "GP Stakes in Private Equity: An Empirical Analysis of Minority Stakes in Private Equity Firms" (MSc thesis, Stockholm School of Economics), used a hand-collected dataset of 201 GP stake deals from 1988 to 2020 and a difference-in-differences design. They find that the firms most likely to receive a stake are large, young, and fast-growing in fund size — and that the buyers are disproportionately sovereign wealth funds and fund-of-funds managers. But their fund-level result is a flat zero: a GP stake has no significant effect on the staked manager's subsequent fund-size growth or return performance. From that, they draw a sharper conclusion than Gahng and Jackson do — that the official reasons firms give for selling a stake (fund new strategies, enter new markets, increase GP commitments) are not what the data supports, and that the real motivation is, more often than the press releases admit, the owners realising value.

Read together, the two studies describe the same market from opposite ends. Gahng and Jackson show that staked firms grow enormously after selling — but their own caveat matters: the results are not necessarily causal. The firms that sell stakes are the best firms, screened by sophisticated buyers; they may have grown anyway. Fogelström and Gustafsson show that, once you control for that selection, the stake itself adds nothing measurable to fund growth or returns — which is consistent with the stake being, at its core, a financing transaction for the owners rather than a growth elixir for the funds. Both findings can be true at once. That is usually the sign that you are looking at the real answer.

## 8. The Agency Question: Does Selling Skin in the Game Hurt LPs?

This is the question an LP should ask before committing to a staked manager's next fund, and it has a clean theoretical shape. Jensen and Meckling's agency logic says that when a manager sells a share of its future profits, its incentive to exert costly effort falls — it now keeps 80 cents of every dollar of value it creates instead of a full dollar. If the GP tries less hard, the LPs' returns suffer. A GP stake, on this view, is the GP quietly reducing its skin in the game.

The evidence, so far, says the worry is overstated — but the reason why is instructive. First, selling a stake usually makes the firm *bigger*, and a smaller percentage of a much bigger firm can still be more skin in the game in absolute dollars. Gahng and Jackson find exactly this: sellers increase their own commitments to their funds after selling, funded by the sale proceeds, so the partners' absolute exposure rises even as their percentage falls. Second, the proceeds get reinvested in the firm — more investment staff, more offices — which is the opposite of coasting. Third, the funds' performance, measured by public market equivalents, stays strong after stake sales.

But there are honest limits to that reassurance. The evidence is about averages, and averages hide the cases that matter. A stake sold by a hungry firm to fund expansion is a different transaction from a stake sold by a tired founder cashing out before retirement — and the data cannot always tell them apart in advance. The protection for LPs is not a theory but diligence: ask how the proceeds are being used, ask whether the partners are increasing their fund commitments or decreasing them, and ask whether the key people are staying. A GP stake is a financing decision by the manager. Like any financing decision, its wisdom depends on what the money is for.

## 9. Common Misconceptions

**"A GP stake is just another way to invest in private equity."** It is a different exposure entirely. An LP's return depends on the portfolio companies. A GP stake's return depends on the manager — its fundraising, its fee rates, its survival. If every fund loses money, the LP loses money and the GP stake still collects fees. If the manager fails to raise its next fund, the LP's existing funds run off normally while the GP stake's fee base decays to zero.

**"Buying the manager is safer than buying the fund."** Half of it is. The fee stream is stable; the carry stream is not, and the value of the stake rests heavily on assumptions about future fundraising that no one can verify in advance. And a GP stake has no maturity date — there is no fund life forcing a realisation. Your exit is a sale to another buyer, an IPO, or nothing at all.

**"A GP stake means the GP has sold out and stopped caring."** On average, the research says the opposite: staked firms invest more in staff, commit more of their own money to their funds, and their fund performance does not deteriorate. But "on average" is doing real work in that sentence — check the specific deal, not the category.

**"Petershill's IPO proves GP stakes are a great listed investment."** It proved something narrower and more useful: that a portfolio of minority, non-controlling stakes in private managers is hard for public markets to value, and that public markets will discount it heavily for illiquidity, opacity, and lack of control. The asset works better inside a closed-end fund, held by an investor who can diligence the manager, than on a stock exchange.

**"The GP stake buyer controls the manager."** Typically it does not. A 10 to 25 percent stake, usually non-voting, buys economics, not control. The buyer can sometimes negotiate information rights, a board observer seat, or consent rights over narrow issues — but it cannot run the firm. If you want control, buy the whole firm. Nobody is selling it.

## 10. Test Yourself

**1.** A manager oversees $20 billion of AUM, charges an average fee of 1.25 percent, and runs at a 40 percent operating margin. Value its FRE at 11x. What is the firm worth on FRE alone? If a buyer takes a 20 percent stake at that value, what does it pay, what annual FRE does it receive, and what is its implied yield?

*Answer: Fee revenue = $20,000 million × 1.25% = $250 million. FRE = $250 million × 40% = $100 million. FRE value = $100 million × 11 = $1,100 million. A 20% stake costs $220 million and receives 20% × $100 million = $20 million of FRE a year — an implied yield of $20 / $220 ≈ 9.1%. (This ignores carry, which would add value and income on top.)*

**2.** A fund loses 20 percent in a year. The manager still collects its full management fee, and its carry for the year is zero. Explain why a GP stake investor still gets paid, and why an LP in the same fund does not.

*Answer: The GP stake is a claim on the management company's earnings, and management fees are charged on committed or invested capital regardless of performance — the fee is a contractual charge, not a share of profit. The LP's return is a share of the fund's investment profit, so a down year means losses for the LP and no carry for the manager. The fee stream is what makes the GP stake's cash flows stable — and it is also why LPs sometimes resent it.*

**3.** Gahng and Jackson estimate that every $1 of GP stake proceeds is associated with an incremental $18 of AUM. A manager sells a 15 percent stake for $150 million. What incremental AUM does the multiplier imply? And why should you be careful about reading that number as a promise?

*Answer: $150 million × 18 = $2.7 billion of incremental AUM. Be careful because the estimate is an association, not a causal guarantee: the firms that sell stakes are screened by sophisticated buyers and are already the fastest-growing firms, so part of the $18 reflects selection — the kind of firm that can sell a stake — rather than the effect of the sale itself. Fogelström and Gustafsson's finding of no significant effect on fund-size growth after controlling for selection is the other side of the same coin.*

**4.** Petershill listed in September 2021 at a £4 billion valuation and announced its delisting in September 2025 after the shares traded at roughly a 50 percent discount. What does that gap tell you about valuing minority stakes in asset managers?

*Answer: It tells you that the value of a GP stake depends heavily on who holds it. A direct buyer can diligence the manager, negotiate protections, and hold indefinitely, and will pay something close to a full FRE multiple. A public shareholder in a listed portfolio of minority stakes cannot diligence, cannot negotiate, and cannot control anything — and it discounts the same cash flows for illiquidity, opacity, and lack of control. The £4 billion was the price of the pitch; the 50 percent discount was the price of the reality.*

## Next up

**46 | Co-Investments: Investing Alongside the Fund** — what happens when an LP stops buying the fund and starts buying the deals directly, and why the cheapest capital in private equity is also the hardest to get.
