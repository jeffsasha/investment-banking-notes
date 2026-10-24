# 14 | Frontier: Recent Research on M&A and Valuation

*Thirteen articles in, you can build the models. This one asks a ruder question: do the models, and the deals they justify, actually work? The honest answer from the research is messier — and more useful — than any textbook chapter.*

> **Learning goals.** After this article you can: (1) explain why acquirer shareholders so often lose money on announcement even when a deal "creates value"; (2) work through the dollar-versus-percentage trap that makes headline returns misleading; (3) compare the two big explanations for merger waves — industry shocks plus cheap capital versus stock-market misvaluation; (4) explain how CEO overconfidence shows up in deal-making, with numbers; (5) use research findings as a checklist when you look at a real deal, rather than as a verdict.
>
> **Prerequisites.** Articles 04–05 (multiples and premiums), 09 (accretion/dilution), and 11–12 (sell-side and buy-side process). You need to be comfortable with market capitalisation, announcement returns, and the idea that a premium is paid over the pre-announcement price.

## 1. Why Read Papers at All?

Bankers do not get paid to publish papers. They get paid to close deals. So why should a learning series end with academic research?

Because the models in articles 04–10 are tools for *arguing* a price, and every tool has a blind spot. A DCF tells you what a company is worth if your forecasts are right. A comps table tells you what peers trade at, not whether peers are correctly priced. A merger model tells you whether EPS goes up, not whether shareholders get richer. Research is where someone went back, years later, and checked what actually happened to the shareholders.

That is the spirit of this article. It is not a literature review for an exam. It is four well-established findings, each verified before it went in here, and what each one should change about how you read a deal announcement.

A warning that applies to the whole article: a research finding is an average over hundreds of deals. Averages describe populations, not your deal. A finding that "acquirers lose on average" does not mean the deal in front of you is bad, and a finding that "stock deals underperform" does not make every stock deal a mistake. The right use of research is to know which questions to ask harder, not to replace judgement with a statistic.

## 2. The Central Puzzle: Acquirers Lose, Targets Win, Deals Keep Happening

Open any study of merger announcements and the same pattern shows up. Target shareholders gain a lot — typically around 20–30% on announcement, reflecting the premium. Acquirer shareholders lose a little on average — often around 1% or so, sometimes more. And yet deals keep happening, in waves, year after year.

Three explanations compete, and they are not mutually exclusive:

- **Synergy is real but the target captures it.** If a deal creates $1 billion of value but the acquirer pays a $1.2 billion premium, target shareholders win and acquirer shareholders lose, even though the combination itself is worth doing. The premium is the battleground.
- **Managers are not maximising shareholder value.** Empire-building, overconfidence, or simply enjoying running a bigger company can all push a CEO to do a deal that shareholders would not choose. This is the agency story, and it goes back to Jensen (1986) on free cash flow, which we met in article 08.
- **The market is not pricing things correctly in the first place.** If the acquirer's stock is overvalued, paying with that stock is cheap in true-value terms even if it looks expensive in market terms. The announcement return then partly reflects the market waking up, not the deal itself.

Keep those three in mind. Every paper in this article is, at heart, an argument about which of them matters most, and when.

## 3. Percentages Lie; Dollars Tell the Truth

Here is the single most useful habit this article can give you: whenever you see an announcement return, multiply it by the market capitalisation before you react.

### 3.1 The worked example

Suppose Acquirer Co. has a market capitalisation of $50 billion and announces a deal. Its shares fall 1% on announcement. Target Co. has a market capitalisation of $5 billion and its shares rise 25%.

```math
\text{Acquirer dollar change} = \$50{,}000\text{m} \times (-1\%) = -\$500\text{m}
```

```math
\text{Target dollar change} = \$5{,}000\text{m} \times (+25\%) = +\$1{,}250\text{m}
```

```math
\text{Combined dollar change} = -\$500\text{m} + \$1{,}250\text{m} = +\$750\text{m}
```

```math
\text{Combined percentage change} = \frac{+\$750\text{m}}{\$50{,}000\text{m} + \$5{,}000\text{m}} = \frac{750}{55{,}000} \approx +1.36\%
```

Read that twice. The acquirer "lost" and the deal still created $750 million of combined market value on announcement. The acquirer lost because it paid away some of the value it created; the target captured more than 100% of the combined gain, because the premium exceeded the acquirer's share of the synergy. Both statements are true at once. Headlines that report only the acquirer's percentage return will call this a bad deal. Headlines that report only the combined value will call it a good one. A banker should report both, and then ask who captured what and why.

This is not a toy point. Moeller, Schlingemann, and Stulz (2005) showed that acquiring-firm shareholders lost about 12 cents per dollar spent on acquisitions from 1998 through 2001, for a total loss of about $240 billion — versus about $7 billion lost in all of the 1980s, or 1.6 cents per dollar spent. The percentage returns in the late-1990s wave did not look catastrophic. The dollar losses were enormous, because the acquirers were enormous and highly valued. And the aggregate was driven by a small number of very large deals by very highly valued firms: without those deals, acquiring shareholders would on average have gained. That is the shape of the whole literature in one sentence — a modest average, hiding a fat tail of very large mistakes.

The practical rule: always ask "1% of what?" A 1% fall for a $100 billion acquirer is $1 billion of shareholder wealth. A 30% rise for a $200 million target is $60 million. Anyone who compares those two percentages as if they were comparable has misunderstood the deal.

### 3.2 What the announcement return does not measure

An announcement return is the market's *immediate* verdict, not the deal's final score. It bundles at least four things together:

1. The market's estimate of the synergy, net of the premium.
2. New information about the acquirer itself — announcing a big acquisition tells investors something about what management thinks of its own prospects, and that signal can move the price independently of the deal.
3. The market's revaluation of the acquirer's stock if it was mispriced before.
4. Simple price pressure from merger arbitrage and index mechanics around the announcement.

That is why researchers are careful, and why you should be too: a negative announcement return is evidence, not a conviction. It is the start of the analysis, not the end of it.

## 4. Why Do Deals Come in Waves?

Merger activity does not arrive evenly. It comes in waves — the 1960s conglomerates, the 1980s LBOs, the late-1990s tech and telecom boom, the mid-2000s private-equity boom. Why should hundreds of unrelated boards all decide to do deals at the same time? Two serious answers dominate the literature, and the honest answer is probably "both, in different proportions at different times."

### 4.1 Answer one: shocks plus cheap money (Harford, 2005)

Jarrad Harford's argument, in "What drives merger waves?" (*Journal of Financial Economics*, 2005), is neoclassical: waves start with real economic shocks — a new technology, a deregulation, a shift in input prices — that change the efficient structure of an industry. Firms need to reorganise, and mergers are one way to do it. But a shock alone is not enough. A wave needs *capital liquidity*: when credit is cheap and plentiful, the cost of reorganising falls, and industry-level waves cluster into an economy-wide wave. When liquidity dries up, the wave stops, even if the shock is still there.

The testable implication is neat. If waves were purely about stock-market euphoria, you would expect them to be dominated by stock-financed deals. Harford finds that market-timing variables have little explanatory power once the economic model — shocks plus liquidity — is included, and that cash deals cluster in waves too. Deals, on this view, are mostly a rational response to a changing world, financed when financing is cheap.

For a banker, the Harford lens asks: what is the shock behind this wave, and is the financing environment flattering the returns? A deal that looks brilliant at a 4% borrowing cost can look ordinary at 7%. If your model only works because debt is cheap, say so out loud.

### 4.2 Answer two: overvalued stock is a currency (Shleifer and Vishny, 2003)

Andrei Shleifer and Robert Vishny offer the behavioural mirror image, in "Stock market driven acquisitions" (*Journal of Financial Economics*, 2003). Suppose the market sometimes misprices firms. A firm whose stock is overvalued has a wonderful opportunity: it can buy real assets — a target company — by issuing pieces of paper the market currently overvalues. Rational managers, in this model, exploit mispricing rather than being fooled by it.

The logic is worth walking through slowly, because it flips the usual intuition about "paying too much."

### 4.3 The worked example: paying with overvalued paper

Suppose Acquirer Co.'s shares trade at $100 each, but their true value — what the business is really worth per share — is $80. The stock is 25% overvalued ($100 / $80 − 1 = 25%). Acquirer Co. offers 1 million shares for Target Co., whose true value is $90 million.

```math
\text{Market value of consideration} = 1{,}000{,}000 \times \$100 = \$100\text{m}
```

```math
\text{True value given up} = 1{,}000{,}000 \times \$80 = \$80\text{m}
```

```math
\text{True gain to acquirer shareholders} = \$90\text{m (target received)} - \$80\text{m (true value given)} = +\$10\text{m}
```

On the headline, the acquirer "paid" $100 million for a $90 million company — a premium. In true-value terms, it paid $80 million and gained $10 million. Target shareholders accept, because they value the shares they receive at the market price of $100 million, which exceeds the $90 million their company is truly worth. Both sides feel like winners. The bill arrives later, when the acquirer's share price corrects toward its true value and the long-run returns look poor — exactly the pattern the data shows for stock-financed acquirers.

This model predicts several things that show up in the data: who acquires whom (the more overvalued firm buys the less overvalued one), the choice of payment method (overvalued acquirers prefer stock; undervalued acquirers prefer cash), and why waves coincide with bull markets (misvaluation is most widespread when prices are high). It does not say every stock deal is a con. It says: when you see a stock deal at the top of a bull market, ask who is really paying, in true-value terms, and whether the market price of the currency will survive contact with reality.

### 4.4 Testing the misvaluation story: splitting market-to-book apart

A theory about misvaluation is only useful if misvaluation can be measured. Rhodes-Kropf, Robinson, and Viswanathan (2005), in "Valuation waves and merger activity: The empirical evidence" (*Journal of Financial Economics*, 2005), built the measurement. They decompose a firm's market-to-book ratio (M/B) into three pieces:

```math
\ln\left(\frac{M}{B}\right) = \text{firm-specific error} + \text{sector-wide error} + \text{long-run value-to-book}
```

In words: how far this firm trades above its own sector's current pricing, plus how far the whole sector trades above its long-run pricing, plus the firm's genuine long-run value relative to book. The first two pieces are misvaluation; the third is fundamentals.

A quick illustrative calculation shows how the pieces add up. Suppose a firm has M/B of 3.0, so $\ln(3.0) \approx 1.10$. Suppose its long-run value-to-book contributes $\ln(1.5) \approx 0.41$, the sector-wide error contributes $0.39$, and the firm-specific error contributes $0.30$:

```math
0.41 + 0.39 + 0.30 = 1.10 = \ln(3.0)
```

Check it in levels: $1.5 \times e^{0.39} \times e^{0.30} \approx 1.5 \times 1.48 \times 1.35 \approx 3.0$. The arithmetic closes. What the authors find is that merger activity tracks the misvaluation pieces, not just the fundamental piece: misvaluation affects who buys whom and how they pay, and it combines with — rather than replaces — the neoclassical shock story. That combination is the mature conclusion. Waves have real economic causes *and* a misvaluation amplifier. A banker who only tells one half of that story is selling, not analysing.

The companion theory paper, Rhodes-Kropf and Viswanathan (2004), "Market valuation and merger waves" (*Journal of Finance*), gives the mechanism: when a target cannot tell whether a high bid reflects genuine synergy or an overvalued acquirer trying to spend its paper, overvalued acquirers can pool with genuinely synergistic ones, and merger waves follow. Targets accept stock because they cannot be sure it is overvalued — and that uncertainty is precisely what makes the strategy work.

## 5. Who Does the Deals? The Overconfidence Finding

If waves explain *when* deals happen, Malmendier and Tate (2008) help explain *who* does them. In "Who makes acquisitions? CEO overconfidence and the market's reaction" (*Journal of Financial Economics*, 2008), they classify CEOs as overconfident when, despite being under-diversified, they hold their company's stock options all the way to expiration rather than exercising them — behaviour that only makes sense if the CEO genuinely believes the stock is worth more than the market thinks. Press coverage describing the CEO as "confident" or "optimistic" gives the same classification, which is reassuring: two very different proxies, same result.

The results are stark:

- The odds of making an acquisition are about 65% higher if the CEO is classified as overconfident.
- The effect is largest for diversifying deals — the kind with the weakest synergy story — and for deals that do not require external financing, where no outside lender or investor gets to veto the plan.
- The market seems to know. The announcement reaction for overconfident CEOs is about −90 basis points, versus about −12 basis points for other CEOs. Investors discount the deal before the ink is dry.

Read that last point carefully, because it is the most banker-relevant finding in this article. The market is not just reacting to the deal; it is reacting to the *manager doing the deal*. The same acquisition, announced by a different CEO, gets a different reception. That is why governance, board scrutiny, and the discipline of having to raise external money matter: they are the few forces that stand between an overconfident CEO and a value-destroying deal. It also connects directly back to Roll (1986) and the hubris hypothesis from article 05: overpayment is not always a valuation error. Sometimes it is a personality trait with a modelling department attached.

A note on fairness: the same trait that overpays for acquisitions can also drive genuinely bold strategies, and the evidence on innovation suggests overconfident managers can be more innovative. The research claim is narrower: overconfidence predicts *more* acquisitions, *worse* ones on average, and a *more negative* market reaction. It does not say confident CEOs never create value.

## 6. What This Changes in Practice

Research earns its place in a practitioner's toolkit only if it changes a decision. Here is the checklist this article's four findings suggest — tape it, mentally, to the side of any deal model you build:

| Question to ask | Research behind it | What a good answer looks like |
|---|---|---|
| Who captures the value, in dollars? | Moeller, Schlingemann, and Stulz (2005) | Combined dollar gain split between acquirer and target; premium versus synergy stated separately |
| What is the shock, and is cheap financing flattering the deal? | Harford (2005) | The industry shock named; returns shown at normalised financing costs, not just today's rates |
| Who is overvalued, and what currency are they paying with? | Shleifer and Vishny (2003); Rhodes-Kropf, Robinson, and Viswanathan (2005) | M/B decomposition discussed; stock deals at market peaks flagged for extra scrutiny |
| Who is the CEO, and who is checking them? | Malmendier and Tate (2008) | Board process, external financing discipline, and diversifying-deal scepticism all visible |
| Is this the average deal, or the tail? | All four papers | Large, stock-financed, diversifying deals by highly valued acquirers treated as guilty until proven innocent |

The useful questions are always the conditional ones: *which* deals, *which* managers, *which* payment method, *which* point in the wave.

## 7. Where the Frontier Goes Next

The honest frontier is less settled than the findings above, and this article will not pretend otherwise. Three directions are genuinely live, and each is a question rather than a conclusion:

- **Valuation in a world of intangibles and platforms.** The M/B decomposition in section 4.4 was built for a world where book value meant something close to invested capital. For a company whose main assets are software, data, and network effects, book value is a faint shadow of the business. How should misvaluation be measured when the denominator is broken? Nobody has a clean answer yet, and any banker valuing a modern technology company is working with that problem daily.
- **How technology changes the banker's job.** Data rooms, document review, and parts of modelling are being automated, and the question is not whether that continues but which judgement stays human: the synergy call, the negotiation, the decision to walk away. This is practitioner observation and open debate, not a settled paper — treat any confident claim here, including any you hear in a pitch, with the same scepticism this article recommends for deal announcements.
- **Governance and the long run.** The overconfidence work points to a deeper question: if who the CEO is matters as much as what the model says, then deal analysis is partly people analysis. The frontier here is connecting deal outcomes to board structure, incentive design, and shareholder voice — the unglamorous machinery that decides whether a bad deal gets stopped in the boardroom instead of announced to the market.

If there is one sentence to carry from this series into real work, it is this: a model tells you what a deal is worth if its assumptions hold; research tells you how often those assumptions fail, and in which direction. Both are necessary. Neither is sufficient.

## Common Misconceptions

**"Acquirers lose on announcement, so mergers destroy value."**
Wrong, or at least incomplete. The acquirer losing and the deal creating value can both be true, as section 3.1 shows: the target can capture more than 100% of the combined gain through the premium. Judge the combined dollar value and its split, not the acquirer's percentage alone.

**"A stock deal means the acquirer thinks its own stock is overvalued."**
Not necessarily. Stock can be the right currency for tax reasons, to share risk, to preserve cash, or because the target's owners want to stay invested. Misvaluation is one motive among several. What the research says is that stock deals *at market peaks by highly valued acquirers* deserve extra scrutiny — not that every stock deal is a signal.

**"Merger waves prove the market is irrational."**
No. Waves can be fully rational responses to industry shocks plus cheap capital, as Harford shows. Misvaluation amplifies waves; it does not have to explain all of them. The two theories are complements, and the evidence supports both.

**"Overconfident CEOs are just bad CEOs."**
Too simple. Overconfidence predicts more and worse acquisitions on average, but the same trait is associated with boldness and innovation elsewhere. The correct inference is narrower: put extra governance around acquisition decisions when the CEO shows overconfident behaviour, especially for diversifying deals funded from internal cash.

**"If a paper is published, the debate is settled."**
Papers are arguments with data, and data gets revisited. The findings here have survived replication and extension, which is why they are in this article — but the frontier sections above are open questions precisely because smart people disagree about them. Read the paper, not just the headline about the paper.

## Test Yourself

**1. Acquirer Co. has a market capitalisation of $80 billion and falls 2% on announcing a deal. Target Co. has a market capitalisation of $4 billion and rises 20%. What is the combined dollar change, and did the deal create or destroy combined market value on announcement?**

Acquirer change: $80 billion × (−2%) = −$1.6 billion. Target change: $4 billion × 20% = +$0.8 billion. Combined: −$1.6 billion + $0.8 billion = −$0.8 billion. On announcement, the market judged the deal to have destroyed $800 million of combined value — even though the target's percentage gain (20%) looks far larger than the acquirer's percentage loss (2%). Percentages lie; dollars tell the truth.

**2. An acquirer's shares trade at $120 but are truly worth $100. It issues 500,000 shares to acquire a target truly worth $55 million. What is the true gain or loss to acquirer shareholders from the payment method alone?**

Market value of consideration: 500,000 × $120 = $60 million. True value given up: 500,000 × $100 = $50 million. True gain: $55 million received − $50 million given = +$5 million. The acquirer appears to pay a $5 million premium over true value on headline terms ($60 million versus $55 million) but gains $5 million in true-value terms, because it paid with overvalued paper.

**3. A firm has M/B of 2.0, its long-run value-to-book is 1.2, and its sector-wide error contributes ln(1.25) ≈ 0.22 to log M/B. What is its firm-specific error in log terms?**

Total log M/B: ln(2.0) ≈ 0.69. Long-run component: ln(1.2) ≈ 0.18. Sector error: 0.22. Firm-specific error = 0.69 − 0.18 − 0.22 = 0.29. In levels, the firm trades about $e^{0.29} \approx 1.34$ times its sector's current pricing — a firm-specific premium of roughly 34% above sector pricing, on top of the sector's own elevation above long-run value.

**4. Two explanations for merger waves are put to you: (a) industry shocks plus capital liquidity, (b) stock-market misvaluation. A wave arrives in which cash deals cluster just as much as stock deals, and financing is unusually cheap. Which explanation does this favour, and why?**

It favours (a), the Harford explanation. Cheap capital plus a shock predicts cash deals clustering in waves, because the cost of reorganising has fallen for everyone. A pure misvaluation story predicts waves dominated by stock deals, since the mechanism is spending overvalued paper. Cash deals clustering alongside stock deals, in a cheap-financing environment, is exactly what the shock-plus-liquidity model predicts and what a misvaluation-only model struggles to explain — though the two can coexist, and the wave may still contain misvalued stock deals within it.

## References

All citations below were verified (title, authors, year, journal) before publication:

- Harford, J. (2005). "What drives merger waves?" *Journal of Financial Economics*, 77(3), 529–560.
- Malmendier, U., and Tate, G. (2008). "Who makes acquisitions? CEO overconfidence and the market's reaction." *Journal of Financial Economics*, 89(1), 20–43.
- Moeller, S. B., Schlingemann, F. P., and Stulz, R. M. (2005). "Wealth destruction on a massive scale? A study of acquiring-firm returns in the recent merger wave." *Journal of Finance*.
- Rhodes-Kropf, M., Robinson, D. T., and Viswanathan, S. (2005). "Valuation waves and merger activity: The empirical evidence." *Journal of Financial Economics*, 77(3), 561–603.
- Rhodes-Kropf, M., and Viswanathan, S. (2004). "Market valuation and merger waves." *Journal of Finance*.
- Shleifer, A., and Vishny, R. W. (2003). "Stock market driven acquisitions." *Journal of Financial Economics*, 70(3), 295–311.

Earlier series citations reused here: Jensen, M. (1986). "Agency costs of free cash flow, corporate finance, and takeovers." *American Economic Review*; Roll, R. (1986). "The hubris hypothesis of corporate takeovers." *Journal of Business*.

*Next up: 15 | Distressed DCF and Sum-of-the-Parts: Valuing the Pieces When the Whole Is Broken*
