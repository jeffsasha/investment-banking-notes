# 23 | Merger Arbitrage: Betting on Deals Closing

*Every article so far has been about valuing companies or putting deals together. This one is about the people standing on the other side of the announcement — the traders who buy a deal after it is public and get paid, a little at a time, for bearing the risk that it falls apart. It looks like free money. It mostly is not, and the reason why is one of the cleanest lessons in finance about what risk actually is.*

> **Learning goals.** After this article you can: (1) explain what a merger arbitrage spread is and why it exists; (2) work out the trade for a cash deal and for a stock deal, including the hedge ratio; (3) convert a spread into an annualised return and an expected value, and say when a positive spread is still a bad bet; (4) name the five risks a spread is pricing, and read a widening spread as information; (5) explain why merger arbitrage returns look like writing put options, and why the strategy survives despite being well known.
>
> **Prerequisites.** Article 03 (enterprise value versus equity value) for the price-versus-value distinction, article 05 (precedent transactions) for how offer prices are set, and article 21 (hostile takeovers) for the ways deals die. No new valuation model is introduced here; the math is spreads, probabilities, and position sizing.

## 1. The Gap That Appears on Announcement Day

Picture this. A company, TargetCo, trades at $38 on Monday. On Tuesday morning it announces it has agreed to be acquired for $50 per share in cash. You might expect the stock to jump to $50. It does not. It jumps to about $48, and then it sits there, drifting slowly toward $50 over the next few months as the deal grinds toward closing.

That $2 gap has a name: the **deal spread**. It is the difference between the offer price and the market price of the target after announcement:

```math
\text{Spread} = \text{Offer price} - \text{Target share price}
```

The spread exists for a simple reason: the $50 is not certain. Deals break. Regulators block them, shareholders vote them down, financing falls through, or something ugly turns up in diligence and the buyer walks away. Until the deal closes, the $50 is a promise, not a fact, and the market discounts promises by the chance they are broken.

**Merger arbitrage** — also called risk arbitrage — is the trade that harvests that discount. The arbitrageur buys the target at $48, waits, and collects $50 at closing, pocketing the $2 spread as compensation for bearing the risk that the deal fails. The word "arbitrage" is doing a lot of generous work here: this is not a risk-free arbitrage in the textbook sense, where you lock in a profit with certainty. It is a bet, repeated across many deals, that the spreads on average overpay for the risk of failure. The distinction between those two things is the whole subject of this article.

## 2. The Cash Deal: The Simplest Version

Work through the TargetCo example in full, because every complication later is a variation on it.

- Offer price: $50 cash per share.
- Price before announcement: $38.
- Price after announcement: $48.
- Expected time to close: 4 months.

The gross spread is $50 − $48 = $2 per share, or $2 / $48 = 4.17% of the price you pay. But 4.17% over four months is not the same as 4.17% over a year, so the first thing a professional does is annualise it:

```math
\text{Annualised return} = \left(\frac{50}{48}\right)^{\frac{12}{4}} - 1 = 1.0417^{3} - 1 \approx 13.0\%
```

A 13% annualised return sounds excellent — until you remember it is not guaranteed. That is the question the rest of the analysis answers: is 13% enough for the risk?

Two adjustments come first, because beginners forget both. First, **dividends**: if TargetCo pays a $0.40 dividend before closing, the arbitrageur, as a shareholder, receives it, so the effective spread is $2.40, not $2. Second, **financing costs**: if you bought on margin, or if you are a fund paying for the capital tied up in the position, the interest cost over four months comes off the return. A spread that looks like 13% gross can easily be 10% net. Professionals quote spreads net of these items, and you should too.

The other number that matters is the **deal premium**: how far above the pre-announcement price the offer sits. Here it is ($50 − $38) / $38 = 31.6%, a normal-looking control premium of the kind article 05 discussed. The premium is what the target's original shareholders gain. The spread is what the arbitrageur gains. They are different people earning different returns for different risks, and confusing them is the first misconception to avoid.

## 3. The Stock Deal: Hedging the Acquirer

Cash deals are simple because the payoff is a fixed number. Stock deals are where the trade gets interesting. Suppose instead that AcquirerCo offers 0.5 of its own shares for each TargetCo share — a **fixed exchange ratio**. AcquirerCo trades at $80, so the implied offer value is:

```math
0.5 \times \$80 = \$40 \text{ per TargetCo share}
```

TargetCo trades at $38.50 after announcement, so the spread is $40 − $38.50 = $1.50 per share. But you cannot just buy TargetCo and wait, because the thing you will receive at closing is not $40 — it is half a share of AcquirerCo, worth whatever AcquirerCo trades at when the deal closes. If AcquirerCo falls to $70, your half-share is worth $35, and you lose money even though the deal closed exactly as promised.

So the arbitrageur **hedges**: for every TargetCo share bought, they short 0.5 AcquirerCo shares. The ratio of shares shorted to shares bought is the **hedge ratio**, and for a fixed exchange ratio deal it is just the exchange ratio itself. Run the numbers on 1,000 TargetCo shares:

- Long: 1,000 TargetCo shares at $38.50 = $38,500.
- Short: 500 AcquirerCo shares at $80 = $40,000 of proceeds.
- Net cash in: $1,500, which is the spread, already in your pocket in a sense.

Now suppose the deal closes with AcquirerCo at $76. Your TargetCo shares convert into 500 AcquirerCo shares worth 500 × $76 = $38,000 — a $500 loss on the long leg. But you cover your short at $76, buying back for $38,000 what you sold for $40,000 — a $2,000 gain. Net: $2,000 − $500 = $1,500, the spread, exactly as promised. The hedge worked: the acquirer's price move cancelled out, and only the spread remained.

Now suppose the deal **breaks**. TargetCo falls to $34 — below even its pre-announcement price, because the market is disappointed — and AcquirerCo rises to $84 on relief. The long leg loses ($38.50 − $34) × 1,000 = $4,500. The short leg loses ($84 − $80) × 500 = $2,000, because you sold something that went up. Total loss: $6,500. This is the signature pain of merger arbitrage in stock deals: when a deal breaks, both legs tend to move against you at once. The target falls and the acquirer rises, and the hedge that protected you on the way to closing hurts you on the way out.

There is one more wrinkle worth knowing: **collars**. Some stock deals do not use a fixed exchange ratio but a fixed value — say, $40 of acquirer stock per target share, with the ratio floating to deliver exactly $40. Others use a collar: the ratio is fixed within a range of acquirer prices and floats outside it. Collars change the hedge ratio, sometimes daily, and they are the reason stock-deal arbitrage desks employ people whose whole job is adjusting hedges. The principle stays the same — hold the target, short the right amount of the acquirer — but the "right amount" moves.

## 4. What the Spread Is Actually Pricing

A spread is not a free lunch; it is a price. Like any price, it reflects a bundle of risks. When a spread is wide, the market is saying something. Here are the five things it is usually saying:

| Risk | What it means | How you spot it |
|---|---|---|
| Regulatory | Antitrust authorities (FTC, DOJ, or foreign regulators) block or delay the deal | A second request for information, a lawsuit to block, political attention |
| Shareholder vote | Target or acquirer shareholders reject the deal | A large holder publicly opposes, a competing bid emerges, a low preliminary vote |
| Financing | The buyer's debt package falls through | A leveraged deal, a shaky lender, credit markets seizing up |
| Material adverse change | Something bad turns up and the buyer claims a MAC to walk away | Earnings collapse, fraud, a lost key customer between signing and closing |
| Timing and complexity | The deal simply takes longer than expected, eroding the annualised return | Cross-border approvals, multiple regulators, a long outside date |

The spread on any given deal is, roughly, the market's estimate of the probability-weighted loss from these risks. A 2% spread on a friendly domestic cash deal closing in two months is the market saying "this is very likely to close." A 20% spread on a hostile cross-border deal under antitrust review is the market saying "this might not happen, and if it doesn't, the target falls a long way."

This is why **a widening spread is information**. If you own a position and the spread blows out from $2 to $6, something has changed — a regulator asked a hard question, a shareholder objected, a journalist reported trouble. The arbitrageur's job is not just to collect spreads but to read them: is the widening an overreaction you should buy into, or the market learning something you have not yet? Amateurs treat a wide spread as a bargain. Professionals treat it as a warning and go find out why.

## 5. Expected Value: When a Positive Spread Is a Bad Bet

Here is the calculation that separates the professional from the tourist. Go back to TargetCo: offer $50, current price $48, expected close in four months. Suppose you estimate a 90% chance the deal closes at $50 and a 10% chance it breaks, in which case the target falls to $35. The expected value of the share is:

```math
\text{Expected value} = 0.90 \times \$50 + 0.10 \times \$35 = \$45.00 + \$3.50 = \$48.50
```

The market price is $48, so the trade has a positive expected value of $0.50 per share. Good trade, right? Look closer. The upside is $2 (4.2%); the downside is $13 (27.1%). You are risking $13 to make $2, and you need to be right 90% of the time just to break even — the break-even probability is $13 / ($13 + $2) = 86.7%. If your 90% estimate is even slightly optimistic — if the true chance of closing is 85% — the trade loses money on average:

```math
0.85 \times \$50 + 0.15 \times \$35 = \$42.50 + \$5.25 = \$47.75 < \$48
```

This asymmetry is the defining feature of merger arbitrage. Most of the time you make a little; occasionally you lose a lot. The return distribution is not a gentle bell curve — it is a long run of small wins interrupted by sharp losses. That shape has two consequences.

First, **position sizing matters more than deal selection**. A classic tool is the Kelly criterion, which sizes a bet from its edge and its payoff odds. For our deal, with win probability $p = 0.90$ and a gain-to-loss ratio of $2 / \$13 \approx 0.154$:

```math
f^* = p - \frac{1 - p}{\text{gain/loss}} = 0.90 - \frac{0.10}{0.154} \approx 0.90 - 0.65 = 0.25
```

Full Kelly says bet 25% of capital on this single deal; most professionals use half-Kelly or less, about 12%, because their probability estimates are uncertain and a single broken deal at 25% weight is a career event. The point is not the exact number. The point is that the math forces humility: a 90%-likely deal still only justifies a modest position, because the loss side is so much bigger than the win side.

Second, **diversification is not optional**. One deal is a coin flip with bad odds structure; fifty deals is a portfolio where the law of large numbers does its work. Merger arbitrage funds hold dozens of positions precisely because any single deal can break for reasons no spreadsheet predicted.

## 6. Why the Spread Survives: The Limits of Arbitrage

If merger arbitrage earns positive returns on average, why doesn't competition compress the spread to zero? This is the same question article 14's research on market efficiency raises, and merger arbitrage is one of the best-documented cases where the answer is "because arbitrage is harder than it looks."

Baker and Savasoglu (2002) studied merger arbitrage from 1981 to 1996 and found that a diversified portfolio of risk arbitrage positions earned abnormal returns of roughly 0.6–0.9% per month. They traced the persistence to practical limits: arbitrageurs' risk-bearing capacity is constrained by deal completion risk and by the size of the position they hold. Returns were higher precisely where completion risk was higher and where targets were larger — that is, where the risk was hardest to bear. And when the total capital available to arbitrageurs grew, spreads narrowed. The spread, in other words, is the wage paid to a limited pool of capital willing to bear a risk others cannot or will not diversify.

The limits are concrete, not theoretical. Shorting the acquirer in a stock deal requires borrowing shares, and borrow can become expensive or unavailable. Some deals are too small to absorb institutional capital; some are too large for any one fund to hold safely. A fund that loses 20% on a broken deal faces redemptions, which force it to sell other positions at the worst moment. And unlike textbook arbitrage, there is no offsetting position that removes the risk entirely — you cannot hedge "the regulator changes its mind." The spread persists because the risk is real, the capital willing to bear it is finite, and the losses arrive in clusters.

## 7. What the Evidence Says: It Looks Like Writing Puts

The most important academic finding about merger arbitrage comes from Mitchell and Pulvino (2001), who built a portfolio of merger arbitrage positions from 1963 to 1998 and studied how it behaved. Their headline result is strange and worth understanding properly.

In normal markets, the portfolio's beta — its sensitivity to the overall stock market — was close to zero, about 0.02. It did not move with the market. But in severely down markets, the beta jumped sharply. The reason is intuitive once you see it: deals are more likely to break when markets crash. Financing dries up, acquirers get cold feet, shareholders revolt. So merger arbitrage loses money exactly when the rest of the market is losing money, and the losses are concentrated in the worst months.

That payoff pattern — small steady gains most of the time, large losses in bad states of the world — is exactly the payoff of **writing put options**: collecting a premium every month and occasionally paying out big when the market falls. Mitchell and Pulvino showed that once you account for this option-like character, the apparent "alpha" of merger arbitrage shrinks to roughly 0.3% per month — positive, but much smaller than a naive comparison suggests, and a reminder that part of what looks like skill is compensation for a risk that hides in calm markets.

The honest summary, then, is threefold. Merger arbitrage earns a genuine but modest excess return. That return is compensation for bearing deal-break risk that cannot be diversified away within a single deal and that correlates with market stress. And anyone who reports merger arbitrage returns without mentioning the down-market beta is flattering the strategy — the risk is not in the average month, it is in the worst ones.

## 8. How Deals Actually Break: A Field Guide

Textbook risk lists are tidy; real deal breaks are messy. A few patterns recur often enough to be worth recognising:

**The regulator says no, slowly.** The most common killer of large deals is not a dramatic rejection but a long review that bleeds the spread. A second request from antitrust authorities can add six to twelve months, during which the annualised return collapses even if the deal eventually closes. Arbitrageurs call this "time decay," and it is the quiet way spreads punish patience.

**The financing market closes.** Leveraged deals depend on debt markets staying open between signing and closing. In 2007–2008, several large LBOs collapsed or were renegotiated because lenders refused to fund commitments made in a different credit environment. The target's shareholders got less than promised, or nothing at all.

**A better bid appears — and that is good news, mostly.** A competing bidder can raise the price, which helps the long position. But it can also mean the original deal is replaced by a messier one, or that the target's board, having shopped the company, ends up with no deal at all. And a "bump" is never free: the new bid has its own closing risk.

**Shareholders vote no.** This is more common than beginners expect, especially when the acquirer's shareholders must approve a stock deal and the acquirer's price has fallen since announcement. A deal that dilutes acquirer shareholders at a bad price can fail its own vote.

**The MAC clause gets invoked.** Material adverse change clauses let buyers walk away if the target deteriorates badly. They are rarely successfully invoked in court — Delaware courts set a very high bar — but the *threat* of a MAC claim is a powerful renegotiation tool, and renegotiated prices are a common form of partial loss for arbitrageurs.

The practical lesson: when you look at a deal, do not ask "will it close?" Ask "what specifically could stop it, and what would the target trade at if that happened?" The second question is the one the spread is answering.

## 9. Common Misconceptions

**"Merger arbitrage is risk-free arbitrage."** No. True arbitrage locks in a profit with certainty. Merger arbitrage locks in a profit only if the deal closes. The spread is compensation for risk, not a pricing error, and the risk shows up exactly when you least want it — in market crashes, when deals break together.

**"A wide spread means a bargain."** A wide spread means the market thinks the deal is risky. Sometimes the market overreacts and the wide spread is an opportunity. Sometimes the market knows something you do not. The spread is a starting question — "why is this wide?" — not an answer.

**"The annualised return is the return."** Only if the deal closes on schedule. A 13% annualised spread on a deal that takes eight months instead of four is a 6% return, and a deal that breaks is a large loss. Annualising assumes the schedule; the schedule is part of the risk.

**"You just buy the target."** In a stock deal, buying only the target leaves you exposed to the acquirer's price. The hedge is not optional decoration; it is the trade. And in a cash deal, the equivalent mistake is ignoring dividends, financing costs, and the possibility of a price cut on renegotiation.

**"Past merger arbitrage returns prove it is easy money."** The historical excess return is real but modest once you adjust for the option-like risk, and it was earned by diversified professionals with access to borrow, to deal flow, and to information about regulatory processes. A concentrated amateur portfolio in a few wide-spread deals is not the same strategy; it is a lottery ticket with better branding.

## 10. Test Yourself

**1.** A target trades at $60 after a $65 cash offer is announced, with expected close in 3 months. What is the gross spread in dollars and percent, and what is the annualised return? If the target pays a $0.50 dividend before closing, what is the effective spread?

*Answer.* Gross spread: $65 − $60 = $5, or $5 / $60 = 8.33%. Annualised: $(65/60)^{12/3} - 1 = 1.0833^4 - 1 \approx 37.7\%$. With the dividend, the effective spread is $5.50, or 9.17% gross. Note how a short expected close makes the annualised figure look dramatic — and how sensitive it is to any delay: if closing slips to 6 months, the annualised return on the $5 spread falls to $(65/60)^2 - 1 \approx 17.4\%$.

**2.** An acquirer trading at $100 offers 0.25 shares per target share (fixed exchange ratio). The target trades at $23 after announcement. You buy 4,000 target shares. How many acquirer shares do you short, and what is your net cash position at inception? If the deal closes with the acquirer at $92, what is your total profit?

*Answer.* Hedge ratio = 0.25, so short 4,000 × 0.25 = 1,000 acquirer shares. Long cost: 4,000 × $23 = $92,000. Short proceeds: 1,000 × $100 = $100,000. Net cash in: $8,000. At close, the target shares convert into 1,000 acquirer shares worth 1,000 × $92 = $92,000 — exactly the long cost, so the long leg breaks even. Covering the short costs $92,000 against $100,000 of proceeds, a gain of $8,000. Total profit: $8,000, the spread (implied offer $25 − market $23 = $2 per share × 4,000 shares). The acquirer's fall from $100 to $92 did not hurt you, because the hedge cancelled it.

**3.** A cash deal offers $40. The target trades at $38. You estimate an 80% chance of closing and a 20% chance of breaking to $30. What is the expected value, and is the trade positive expected value? What closing probability would make it exactly break even?

*Answer.* Expected value = 0.80 × $40 + 0.20 × $30 = $32 + $6 = $38. Exactly the market price — zero expected edge. Break-even probability: solve $p \times 40 + (1 - p) \times 30 = 38$, giving $10p = 8$, so $p = 80\%$. At any closing probability below 80%, the trade loses money on average despite the visible $2 spread. The spread alone tells you nothing without the break price and the probability.

**4.** Why does merger arbitrage show a near-zero beta in normal markets but a high beta in market crashes, and what does that imply for how you should judge a merger arbitrage fund's returns?

*Answer.* In normal markets, deal outcomes are mostly idiosyncratic — driven by regulators, votes, and financing specific to each deal — so the portfolio does not move with the market. In crashes, deals break together: financing vanishes and acquirers retreat, so the portfolio falls with the market. The payoff resembles writing put options: steady small premiums, large losses in bad states. Judging the fund only by its average return or its Sharpe ratio overstates its quality, because those measures underweight the crash-state losses; you should also ask how it performed in the worst market months, and compare its returns against an option-like benchmark, as Mitchell and Pulvino did.

## Next up

Next up: 24 | Reading a Merger Agreement: Break Fees, MAC Clauses, and Go-Shops — the fine print that decides what happens when a deal wobbles, and why bankers fight over clauses most shareholders never read.

---

*Papers cited in this article (all verified by web search before citing): Mitchell, M. L., & Pulvino, T. C. (2001). Characteristics of Risk and Return in Risk Arbitrage. Journal of Finance, Vol. 56, pp. 2135–2175. Baker, M., & Savasoglu, S. (2002). Limited Arbitrage in Mergers and Acquisitions. Journal of Financial Economics, Vol. 64, pp. 91–116.*

*Learning in public. Not investment advice.*
