# 19 | IPO Pricing and Bookbuilding: Why New Listings Pop

*Every IPO story you read in the press has the same arc: a company "soars 30% on its debut," and everyone acts as if the company just made 30% more money overnight. It did not. Somebody sold something too cheaply, somebody else bought it, and the difference changed hands in a single morning. The interesting question is not why the price went up. It is why smart people, advised by the best-paid bankers in the world, keep agreeing to sell too cheaply.*

> **Learning goals.** After this article you can: (1) define an IPO's offer price, first-day return, and "money left on the table," and compute all three; (2) walk through the steps of a bookbuilt IPO from mandate to first trade; (3) explain bookbuilding as a way of paying investors for information, and the winner's curse as a reason uninformed investors need a discount; (4) name the main competing explanations for underpricing and say what evidence would support each; (5) explain why a big first-day pop is not, by itself, proof that a deal was well priced or that the stock is a good buy.
>
> **Prerequisites.** Articles 01 (what banks do), 03 (enterprise value versus equity value), and 04 (comps) are the useful background. We will use comps-style thinking to set a price range, and the bridge from article 03 to move between a share price and a whole-company value. No new accounting is needed.

## 1. The Puzzle: Selling Something for Less Than It Is Worth

An **initial public offering (IPO)** is the first sale of a company's shares to the general public. Before it, shares are held privately — by founders, employees, and venture or private-equity investors. After it, anyone with a brokerage account can buy them. The bank running the deal is the **underwriter** (usually the **lead underwriter** or **bookrunner**, in charge of the book of demand).

Three numbers describe almost every IPO story:

- The **offer price** is the price at which the company sells its new shares to investors in the IPO itself.
- The **first-day closing price** is where the shares end up after their first day of public trading.
- The **first-day return**, often just called the "pop," is the percentage gain from the offer price to the first-day close.

```math
\text{First-day return} = \frac{\text{First-day closing price} - \text{Offer price}}{\text{Offer price}}
```

And the number existing shareholders actually feel is the **money left on the table**: the extra cash the company would have raised by selling at the first-day closing price instead of the offer price.

```math
\text{Money left on the table} = (\text{First-day closing price} - \text{Offer price}) \times \text{Shares sold}
```

Here is a worked example with a fictional company. Suppose NovaCloud, a software company, has 40 million shares outstanding before its IPO. It sells 10 million **new** shares — a **primary offering**, meaning the money goes to the company, not to existing shareholders cashing out — at \$20 per share.

```math
\text{Gross proceeds} = 10{,}000{,}000 \times \$20 = \$200{,}000{,}000
```

After the IPO, NovaCloud has 50 million shares outstanding (40 million old + 10 million new), so its market value at the offer price — its **market capitalization** — is:

```math
\text{Market cap at offer} = 50{,}000{,}000 \times \$20 = \$1{,}000{,}000{,}000
```

The underwriters also take a fee, the **gross spread**, typically around 7% of gross proceeds for a mid-sized US IPO (this is a market convention, not a law, and it varies by deal size). On \$200 million, a 7% spread is \$14 million, leaving NovaCloud with \$186 million before its own legal and accounting costs.

Suppose NovaCloud closes its first day at \$25:

```math
\text{First-day return} = \frac{\$25 - \$20}{\$20} = 25\%
```

The money left on the table is:

```math
\text{Money left on the table} = (\$25 - \$20) \times 10{,}000{,}000 = \$50{,}000{,}000
```

And the market cap at the close is 50 million × \$25 = \$1.25 billion. The company is, on paper, worth \$250 million more than it was priced at, and it raised none of that extra \$250 million. \$50 million is the direct shortfall on the shares it sold; the rest is a paper gain to existing shareholders. The founders are richer on paper, but the company left \$50 million in the pockets of IPO buyers.

So why would anyone agree to this? The short answer, which this article unpacks, is that underpricing is not (usually) a mistake. It is, at least in part, the price of getting the deal done at all: a payment for information, a bribe to keep cautious investors in the game, and sometimes a symptom of conflicts of interest that nobody in the room has much incentive to fix.

One fact to keep in mind: underpricing is not a quirk of one era. Ritter and Welch (2002), surveying US IPOs from 1980 to 2001, found an average first-day return of 18.8%. That is the average deal, not the headline outlier. A phenomenon that persistent is a feature of the system, not a rounding error.

## 2. How a Deal Actually Gets Done

An IPO is not a single event — a company "going public" one morning. It is a months-long process, and the pricing decision happens very late. Here is the standard shape of a US bookbuilt IPO:

| Stage | What happens | Who is in the room |
|---|---|---|
| Mandate and organization | The company picks its underwriters, lawyers, and auditors; the working group is formed | Company, banks, counsel, auditors |
| Due diligence and drafting | The bank verifies the business story and the prospectus (the **S-1** filing) is drafted | Everyone, at length |
| Filing and review | The S-1 is filed with the SEC and goes through rounds of comments | Company, banks, SEC staff |
| Roadshow | Management presents to institutional investors over one to two weeks | Management, bank sales teams, fund managers |
| Bookbuilding | Investors submit **indications of interest**: how many shares they want, and at what price | Investors, bank syndicate desk |
| Pricing | The final offer price is set the night before trading, and shares are allocated | Company, lead underwriter |
| Trading and stabilization | Shares start trading; the underwriter may support the price in the early days | Market, underwriter |

Two features matter for everything that follows. First, the price is not set by an auction in which the highest bidder wins. It is set by negotiation, informed by the book of demand built during the roadshow. Second, the investors who matter most at pricing time are **institutional investors** — mutual funds, pension funds, hedge funds — not retail investors. They submit the indications of interest and receive most of the allocation. A retail investor who buys on day one is, by definition, buying after the pop has already happened.

There are alternatives, and it helps to know why they are rare. In a **direct listing**, a company lists existing shares without selling new ones and without an underwriter setting a price; the market finds the opening price. In a pure **auction IPO**, shares go to the highest bidders. Both avoid the underwriter's pricing discretion — and both give up what bookbuilding provides: a structured way to learn what investors really think the company is worth before a single share trades.

## 3. Bookbuilding: Paying Investors to Tell the Truth

This is the most important idea in the article, and it comes from Benveniste and Spindt (1989). Start with the bank's problem. The company knows its own business, but it does not know exactly what the market will pay. Roadshow investors know more about demand — what peers are really worth to them, how much appetite there is for this sector this month. But they have no reason to reveal that honestly. If an investor says "I would pay \$30," and the bank prices the deal at \$30, the investor gains nothing from having spoken up. Honesty costs them money.

Bookbuilding solves this with a trade. The bank asks investors to reveal demand during the roadshow, and in return it does two things: it **partially** adjusts the price toward what investors revealed, and it rewards truthful, enthusiastic investors with larger allocations of an issue priced below where it will trade. The underpricing is the payment for the information.

That word "partially" is doing real work, and it shows up in the data as the **partial adjustment phenomenon**. Suppose the bank files an initial range of \$18 to \$20, midpoint \$19. During the roadshow, demand is strong: the book is several times oversubscribed, and investors indicate they would buy well above \$20. A fully adjusting price would jump all the way to roughly where the stock will trade on day one. Instead, the bank typically prices above the range but not all the way there: say, at \$22. The stock then closes its first day at \$27.50. The first-day return is:

```math
\text{First-day return} = \frac{\$27.50 - \$22}{\$22} = 25\%
```

Notice what happened. Good news moved the price up (from a \$19 midpoint to \$22, a 15.8% revision), but not fully (the stock still rose another 25% on day one). If the bank had priced at \$27.50, it would have extracted full value for the company — and taught every investor that revealing enthusiasm is punished with a higher price. Next time, nobody would reveal anything, the book would be uninformative, and the bank would be pricing blind. Underpricing is, in this telling, not a failure of price discovery. It is the cost of price discovery.

There is a second benefit. A bookbuilt deal lets the underwriter choose **who** gets shares, not just how many. Investors who provided useful information and are likely to hold rather than flip on day one can be favored in allocation. An auction cannot do that: it sells to whoever bids highest, including flippers who will sell at the first opportunity. Whether underwriters always use this discretion in the issuer's interest — rather than to reward their own best clients — is a real question, and section 6 returns to it. The mechanism itself is the point: bookbuilding is an information-gathering device disguised as a sales process.

One more piece of machinery: the **greenshoe option** lets underwriters sell up to 15% more shares than the base offering — 1.5 million extra in NovaCloud's case — as a shock absorber for the first month of trading.

## 4. The Winner's Curse: Why the Cautious Investor Needs a Discount

Bookbuilding explains why informed investors need to be paid. The **winner's curse**, from Rock (1986), explains why *uninformed* investors need to be paid — and it is the cleaner argument, because it works even if nobody is lying about anything.

Imagine two kinds of investors. **Informed investors** can tell a good IPO from a bad one before they buy. **Uninformed investors** cannot; they can only buy every deal, or none. Now suppose deals are equally likely to be good (shares truly worth \$30) or bad (truly worth \$10), so the average deal is worth \$20. If the bank prices every deal at \$20 — its expected value — what happens to the uninformed investor who bids on everything?

On good deals, informed investors crowd in, the deal is heavily oversubscribed, and the uninformed investor gets only a fraction of their order — say 50%. On bad deals, informed investors stay away, the deal is undersubscribed, and the uninformed investor gets everything they asked for — 100% of an overpriced asset. This is the curse: **winning the allocation is bad news**, because it means the smart money did not want it.

Put numbers on it. Suppose the uninformed investor orders 100 shares of each deal:

- Good deal: receives 50 shares, each worth \$30, bought at \$20. Profit: 50 × (\$30 − \$20) = \$500.
- Bad deal: receives 100 shares, each worth \$10, bought at \$20. Loss: 100 × (\$10 − \$20) = −\$1,000.
- Expected profit across one good and one bad deal: (0.5 × \$500) + (0.5 × −\$1,000) = \$250 − \$500 = −\$250.

An investor who loses money on average will stop bidding. To keep them in the market — and the market needs them, because informed investors alone cannot absorb every deal — the offer price must fall below the average value. How far? Solve for the price $P$ at which the uninformed investor breaks even:

```math
0.5 \times 50 \times (\$30 - P) + 0.5 \times 100 \times (\$10 - P) = 0
```

```math
25 \times (\$30 - P) + 50 \times (\$10 - P) = 0
```

```math
\$750 - 25P + \$500 - 50P = 0 \quad \Rightarrow \quad \$1{,}250 = 75P \quad \Rightarrow \quad P = \$16.67
```

So the deal must be priced at about \$16.67, a 16.7% discount to the average true value of \$20, just to keep the uninformed investor at break-even. That discount *is* the underpricing. Notice the logic: the discount is not caused by anyone mispricing anything. It is caused by **adverse selection** — the fact that the shares you actually receive are a biased sample of all the shares offered. The more uncertain a deal's value, the worse the adverse selection, and the bigger the discount needed. That prediction — more uncertainty, more underpricing — is one of the most tested in the IPO literature, and it broadly holds: smaller, younger, harder-to-value companies tend to pop more.

The winner's curse also explains why underwriters care about the *investor base*, not just the company: a deal sold mostly to informed, long-term institutions suffers less from the curse than one that must attract retail investors who cannot tell good from bad. The discount is the entry fee for the cautious.

## 5. The Other Suspects: Signaling, Lawsuits, and Agency

No single theory explains every pop, and a good banker — or a good student of banking — should be able to hold several explanations at once and ask which one fits a particular deal. Here are the main alternatives, in the order of how seriously the evidence treats them:

**Signaling.** A high-quality company might deliberately underprice to signal its quality: "We are so confident that we can afford to leave money on the table today; a weak company could not afford the signal," recouping the cost in a later offering at a higher price. This is elegant, but it predicts that the best companies underprice most and then perform better — and the evidence is mixed at best, while the long-run underperformance below sits awkwardly with it.

**Lawsuit avoidance.** Pricing low reduces the chance that investors who lose money sue over misrepresentation in the prospectus. This was once popular, but underpricing is not cleanly highest where litigation risk is highest. It may be a secondary consideration, not the main driver.

**Behavioral and sentiment explanations.** Sometimes the pop is not about the offer price being too low but about the first-day price being too high — enthusiasm, media attention, and retail demand pushing the first trade above any sober valuation. This fits the dot-com bubble well: Loughran and Ritter (2004) document average first-day returns of about 7% in the 1980s, nearly 15% in 1990–1998, and 65% in 1999–2000, before reverting to about 12% in 2001–2003. A theory explaining a steady 15% cannot, by itself, explain a jump to 65% and back; something about sentiment, the company mix, or incentives must have changed.

**Agency: the underwriter's incentives.** This is the explanation that makes bankers uncomfortable, and Loughran and Ritter (2004) argue it became increasingly important. The issuer pays the underwriter, but the underwriter's repeat customers are the institutional investors who buy IPOs. An underwriter that consistently prices deals to pop keeps its buyside clients happy: they receive allocations that rise on day one — effectively a transfer from issuer to investor, arranged by the bank. The issuer may tolerate this because founders focus on the paper value of their retained shares (which also rises), because it values research coverage, or — in the bubble-era extreme Loughran and Ritter document — because allocations of hot IPOs went to the personal brokerage accounts of issuing-company executives, a practice known as **spinning**, giving those executives a personal reason to prefer an underwriter known for severe underpricing. No conspiracy is needed; each party's incentives just point slightly away from maximizing the issuer's proceeds. When you see a pop, always ask: who was paid, in what currency, and by whom?

The honest summary is that underpricing is probably **overdetermined**: information revelation, the winner's curse, sentiment, and agency all push toward a price below the first-day close. That is why the pop is so persistent — and why no single fix (a better auction, a smarter formula, a tougher negotiation) eliminates it, because removing one cause leaves the others standing.

## 6. Reading a Pop Like a Banker

Four habits will keep you honest when you see a headline pop:

**First, ask who got the shares.** A 30% pop accruing to long-term institutions who will support the company differs from one captured by flippers who sold by lunchtime. Allocation detail is not always public, but the shareholder register, the lock-up structure, and early trading volume tell you a great deal. A **lock-up** — typically 180 days during which insiders and pre-IPO shareholders cannot sell — prevents the market from being flooded on day one; watch what happens when it expires, because that is often when the real supply arrives.

**Second, separate the offer price from the trading price.** The offer price reflects a negotiation informed by comps (article 04), a DCF (articles 06–07), and the book of demand. The first-day close reflects, in addition, sentiment, scarcity (only a small **float** — the fraction of shares actually available to trade — is in the market at first), and momentum. A company can be fairly priced at \$20 and still trade at \$25 because only 20% of its shares are floating and demand exceeds that small supply. The pop measures the gap between two different mechanisms, not a single "true value" that one of them got wrong.

**Third, remember the long run.** Ritter and Welch (2002) found that an investor who bought at the first-day close and held for three years earned 22.6% on average — but underperformed the broad market index by 23.4 percentage points, and similar seasoned companies by 5.1 points. The pop is a transfer to IPO buyers, not a forecast of superior returns for everyone else. Buying after the pop has historically been, on average, a worse deal than buying the market. Averages hide enormous variation, but the base rate is not your friend.

**Fourth, do the money-left-on-the-table arithmetic before forming an opinion.** A 10% pop on a \$50 million offering leaves \$5 million on the table; on a \$5 billion offering, \$500 million. The percentage makes the headline, but the dollars are what the board should discuss. NovaCloud raised \$186 million net and left \$50 million behind — more than a quarter of what it could have raised. Whether that was worth paying is a judgment call, but it should be made with the number in front of you, not the headline.

## 7. Common Misconceptions

**"A big pop means the IPO was a success."** For investors who received allocations, yes. For the company, a pop is money not raised. A successful IPO raises the capital the company needs, at a fair price, with a stable shareholder base — and a modest pop (enough to reward IPO buyers for taking risk, not so much that the company gave away the store) is often the sign of that. Bankers sometimes celebrate pops publicly because pops make their buyside clients happy; do not confuse the celebration with the issuer's interest.

**"The underwriter mispriced the deal."** Sometimes, but underpricing is usually systematic, not accidental. If a bank mispriced one deal, that would be an error. When thousands of deals across decades are priced below their first-day close by an average of nearly 19%, something structural is going on — information costs, adverse selection, or incentives. Blaming the analyst who built the model misses the system the model sits inside.

**"Retail investors can just buy the IPO and capture the pop."** Mostly, they cannot. Allocations in hot deals go overwhelmingly to institutions. A retail investor typically buys in the aftermarket, after the pop, at the first-day price — which, as section 6 notes, has historically underperformed the market over the following three years. The pop is, in large part, a transfer between institutions, arranged by the bank and paid for by the issuer.

**"Auctions or direct listings would fix this, so bookbuilding must be a racket."** Auctions and direct listings remove the underwriter's pricing discretion, but also the information-gathering and allocation functions in section 3. Direct listings work best for well-known companies with an existing shareholder base and no need to raise capital — which is why they remain the exception. The right question is not "bookbuilding or auction?" in the abstract, but "for this company, at this size, with this investor base, which mechanism's costs are smaller?"

## 8. Test Yourself

**1.** A company sells 8 million new shares at \$15. The stock closes its first day at \$18. What is the first-day return, the gross proceeds, and the money left on the table?

*Answer: First-day return = (\$18 − \$15) / \$15 = 20%. Gross proceeds = 8 million × \$15 = \$120 million. Money left on the table = (\$18 − \$15) × 8 million = \$24 million.*

**2.** In the winner's-curse example in section 4, why does the uninformed investor lose money if deals are priced at their average value of \$20? What price makes them break even, and why?

*Answer: Allocation is biased: they get only 50 shares of good deals (worth \$30) but all 100 shares of bad deals (worth \$10). At \$20 they make \$500 on good deals and lose \$1,000 on bad ones, an expected loss of \$250 per pair. Solving 25 × (\$30 − P) + 50 × (\$10 − P) = 0 gives P = \$16.67, a 16.7% discount to average value — compensation for adverse selection, since a full allocation is itself bad news.*

**3.** During bookbuilding, demand is strong and the bank revises the offer price above the initial range, but the stock still pops 25% on day one. Under the Benveniste–Spindt logic, why might the bank deliberately stop short of the price investors seemed willing to pay?

*Answer: Fully adjusting would punish investors for revealing strong demand — honesty would mean paying more — so next time they would hide their information. Partial adjustment, with underpricing as the reward for truthful revelation, keeps the book informative in future deals. Underpricing is the payment for information, not just a pricing error.*

**4.** Two IPOs both pop 40% on day one. Deal A allocated most shares to long-term institutions and raised \$2 billion; Deal B allocated heavily to short-term traders and raised \$100 million. Which pop cost its issuer more, and which pop should worry a board more about price stability? Explain in one or two sentences each.

*Answer: Deal A's pop cost more in dollars: 40% of its offer price applied to a \$2 billion offering is far larger in absolute money left on the table than 40% of \$100 million — percentages hide scale. Deal B should worry the board more about stability, because flippers sell quickly, adding supply and volatility, whereas long-term holders are more likely to hold through early trading; also, Deal B's small float makes its first-day price a weaker signal of long-run value.*

## Papers cited

- Rock, K. (1986). *Why New Issues Are Underpriced.* Journal of Financial Economics, 15, 187–212.
- Benveniste, L. M., & Spindt, P. A. (1989). *How Investment Bankers Determine the Offer Price and Allocation of New Issues.* Journal of Financial Economics, 24, 343–361.
- Ritter, J. R., & Welch, I. (2002). *A Review of IPO Activity, Pricing, and Allocations.* Journal of Finance, 57(4).
- Loughran, T., & Ritter, J. R. (2004). *Why Has IPO Underpricing Changed Over Time?* Financial Management, 33(3).

*Next up: Debt Capital Markets — How Companies Borrow in the Bond Market.*
