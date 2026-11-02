# 22 | Spin-offs, Split-offs, and Carve-outs: When Breaking a Company Apart Creates Value

*Every deal so far has been about putting companies together. This one runs in the opposite direction — and it is where bankers earn some of their most interesting fees. Sometimes a company is worth more in pieces than as a whole, and the job is to take it apart cleanly, without breaking anything valuable in the process.*

> **Learning goals.** After this article you can: (1) explain the conglomerate discount and why a combined company can trade below the sum of its parts; (2) distinguish a spin-off, a split-off, a carve-out, and a plain sell-off, and say when a banker would recommend each; (3) work through the arithmetic of a spin-off distribution ratio and check that value is conserved on paper; (4) explain the four main reasons breakups create value — focus, capital allocation, information, and incentives — and the four main ways they destroy it; (5) read the academic evidence on spin-offs honestly, including why the famous long-run returns are disputed.
>
> **Prerequisites.** Article 03 (enterprise value versus equity value) for the bridge you will use below, article 15 (sum-of-the-parts) for valuing divisions separately, and article 13 (restructuring) for the idea that a company's structure is a choice, not a fact of nature. No new valuation model is introduced here; the math is multiples, ratios, and share counts.

## 1. The Breakup Paradox: Worth More Apart Than Together?

Start with a puzzle. Suppose a company owns two businesses. Valued separately, using the trading multiples of their own peers, business A is worth $9.0 billion and business B is worth $4.8 billion. Together, that is $13.8 billion of enterprise value. After subtracting $1.8 billion of net debt, the equity should be worth $12.0 billion. But the stock market values the whole company at only $10.0 billion.

That $2.0 billion gap has a name: the **conglomerate discount**. It is the difference between what a diversified company is worth as one listed stock and what its parts would be worth if each traded on its own:

```math
\text{Conglomerate discount} = \text{Sum-of-the-parts equity value} - \text{Market capitalisation}
```

In our example, the discount is $12.0 billion − $10.0 billion = $2.0 billion, or about 17% of the sum-of-the-parts value. A discount that large is an invitation. If the gap is real — if it reflects something about the combined structure rather than a mistake in your multiples — then splitting the company should, in principle, hand shareholders the missing $2.0 billion. The breakup paradox is that destroying the company as a single entity can create value for the people who own it.

But notice the word "if." A sum-of-the-parts valuation is only as good as its multiples. If you valued business B at 12x EBITDA because its peers trade there, but business B is actually a worse business than its peers — slower growth, weaker margins, a looming product problem — then the $2.0 billion gap is not a discount. It is your error. The first job in any breakup analysis is the same as in article 15: be honest about whether the parts really deserve peer multiples. Bankers who skip that step end up recommending breakups that create nothing but fees and press releases.

There is also a deeper question: why would a discount exist at all? If the two businesses are genuinely worth $13.8 billion combined, why does the market not just pay $13.8 billion for the combined company? The rest of this article is an answer to that question, in four parts. But first, the vocabulary, because bankers use four different words for "breaking up," and they mean four different transactions.

## 2. Four Ways to Break a Company Apart

A **spin-off** is a pro-rata distribution of shares in a subsidiary to the parent's existing shareholders. The parent gives away the subsidiary: every parent shareholder receives subsidiary shares in proportion to what they already own, and no cash changes hands. After the spin-off, the same shareholders own two listed companies instead of one. This is the classic breakup, and it is the focus of this article.

A **split-off** is similar, except shareholders choose. The parent offers its shareholders the chance to exchange their parent shares for shares in the subsidiary. Shareholders who want the subsidiary take it; shareholders who prefer the parent keep the parent. A split-off therefore changes the shareholder base: the people who believe in the subsidiary end up owning it, and the people who do not, do not. It also shrinks the parent's share count, because the shares tendered in the exchange are retired.

A **carve-out** (also called an equity carve-out or a partial IPO) is different in kind: the parent sells a minority stake in the subsidiary to the public through an initial public offering, typically around 20%, and keeps control of the rest. The parent receives cash, the subsidiary gets its own stock price and its own currency for acquisitions and pay, and the parent keeps the option of spinning off or selling the remainder later. Carve-outs are often a first step toward a full separation, and sometimes a last step that never gets taken.

A **sell-off** is the simplest of all: the parent sells the division outright to a buyer for cash, as in a normal M&A sale. It is not really a "breakup" in the ownership sense — the division ends up owned by someone else, not by the parent's shareholders — but bankers analyse it alongside the other three because it is the main alternative. A sell-off gives the parent cash and a clean break; a spin-off gives shareholders the asset itself.

Here is the comparison a banker puts in front of a board:

| | Spin-off | Split-off | Carve-out (IPO) | Sell-off |
|---|---|---|---|---|
| Cash to parent? | No | No | Yes, from the IPO | Yes, from the buyer |
| Do shareholders keep the asset? | Yes, all of them | Yes, those who choose it | No, mostly (parent keeps control) | No |
| Parent control afterwards? | None | None | Yes, majority stake | None |
| Tax treatment (US, generally) | Can be tax-free to shareholders | Can be tax-free to exchanging shareholders | Taxable only on the stake sold | Taxable gain on the sale |
| Best when… | The asset deserves to stand alone | Shareholders disagree about the asset | Parent wants cash plus optionality | A buyer will pay a full price |

The tax row deserves a careful note, because it is often the deciding factor. In the United States, a spin-off can generally qualify as tax-free to both the parent and its shareholders under Section 355 of the tax code, provided conditions are met — the parent must distribute control (at least 80% of the subsidiary), both companies must conduct an active trade or business that is at least five years old, and the spin-off must have a real business purpose rather than being a device for distributing earnings. A spin-off that fails the test becomes a taxable dividend of the subsidiary's full value, which can be ruinously expensive. Nothing here is tax advice; it is the shape of the rule bankers design around, and specialist counsel decides whether a given deal qualifies.

## 3. The Arithmetic: A Worked Spin-off

Work through the example from section 1 in full, because the arithmetic is where most confusion lives. The parent, call it HoldCo, has 200 million shares trading at $50, so its market capitalisation is:

```math
200{,}000{,}000 \times \$50 = \$10{,}000{,}000{,}000
```

HoldCo owns two divisions. CoreCo earns $900 million of EBITDA; its peers trade at 10x, so CoreCo's enterprise value is $9.0 billion. NewCo earns $400 million of EBITDA; its faster-growing peers trade at 12x, so NewCo's enterprise value is $4.8 billion. Total enterprise value is $13.8 billion. HoldCo has $1.8 billion of net debt, so the sum-of-the-parts equity value is:

```math
\$13{,}800{,}000{,}000 - \$1{,}800{,}000{,}000 = \$12{,}000{,}000{,}000
```

That is $60 per HoldCo share ($12.0 billion ÷ 200 million shares), versus the $50 market price. The conglomerate discount is $2.0 billion.

Now the spin-off. The board decides to distribute 100% of NewCo to HoldCo shareholders, and to split HoldCo's debt between the two companies: NewCo takes $600 million of debt, HoldCo keeps $1.2 billion. NewCo's equity value is therefore $4.8 billion − $0.6 billion = $4.2 billion. NewCo will have 80 million shares outstanding. Two numbers follow immediately.

First, the **distribution ratio**: how many NewCo shares each HoldCo shareholder receives per HoldCo share:

```math
\text{Distribution ratio} = \frac{80{,}000{,}000 \text{ NewCo shares}}{200{,}000{,}000 \text{ HoldCo shares}} = 0.4
```

Every HoldCo shareholder receives 0.4 NewCo shares for each HoldCo share they own. Own 1,000 HoldCo shares, receive 400 NewCo shares. (Fractional shares are normally sold for cash, so a holder of 3 HoldCo shares would receive 1 NewCo share plus cash in lieu of the 0.2 fraction.)

Second, the implied per-share values after the spin. NewCo's equity of $4.2 billion divided by 80 million shares is $52.50 per NewCo share. HoldCo's remaining equity is CoreCo's $9.0 billion minus its $1.2 billion of debt, which is $7.8 billion, or $39.00 per HoldCo share. Now check that value is conserved — that the two pieces add back to the sum-of-the-parts value:

```math
\$39.00 + (0.4 \times \$52.50) = \$39.00 + \$21.00 = \$60.00
```

Exactly the $60 sum-of-the-parts value per share. That conservation is the point of the exercise, and also its warning: on paper, before any market reaction, a spin-off creates nothing. It rearranges $60 of value into a $39 piece and a $21 piece. Whether shareholders end up with more than $60 depends on whether the market re-rates either piece once they trade separately — whether CoreCo's multiple expands now that it is a pure play, whether NewCo attracts growth investors who would never have bought HoldCo, whether either management team performs better on its own. The spin-off is a bet that the structure was suppressing value, not a machine that manufactures it.

One more number bankers watch: the announcement reaction. Studies consistently find that parent shares rise roughly 3% when a spin-off is announced. In our example, a 3% rise takes HoldCo from $50 to $51.50, adding:

```math
200{,}000{,}000 \times \$1.50 = \$300{,}000{,}000
```

of market value on the announcement alone — about $300 million of the $2.0 billion discount closing immediately, with the rest depending on execution. An announcement pop is not proof the deal will work; it is the market's opening bid on the idea.

## 4. Why Breakups Create Value: Four Mechanisms

**Focus.** This is the most-cited reason, and the most intuitive. A management team can only pay attention to so many businesses. A conglomerate CEO splitting time between, say, industrial pumps and a software division will understand neither as well as a dedicated CEO would. Investors face the same problem: a fund manager who specialises in software will not buy a stock that is half pumps, and a fund manager who specialises in industrials will not buy a stock that is half software. Each division is therefore owned by generalists rather than specialists, followed by fewer expert analysts, and priced with a fog discount. Separation lets each business be owned, followed, and managed by people who actually understand it.

**Capital allocation, or the internal capital market problem.** Inside a conglomerate, divisions do not raise money from the market; they ask headquarters. Headquarters, being human, tends to spread capital around — funding weak divisions to keep them alive, starving strong ones of what they need, and cross-subsidising in ways no outside investor would approve. Once separated, each company faces the market's discipline directly: if NewCo wants to invest, it must persuade lenders and shareholders on its own merits, and if it cannot, it does not get the money. That discipline is worth something, particularly where a weak division has quietly consumed a strong division's cash for years.

**Information.** A combined company reports combined numbers. An investor trying to value the software division inside a conglomerate must disentangle segment disclosures, allocated corporate costs, and shared services — and segment disclosure is often thin. After a spin-off, each company files its own financial statements, holds its own earnings calls, and gets its own analyst coverage. The information fog lifts, and assets that were hard to value get valued more accurately. This is not just a theory about fairness: it is a claim that opacity itself costs money, because investors charge a discount for what they cannot see clearly.

**Incentives and takeover exposure.** A division manager inside a conglomerate is typically paid in parent stock, which reflects every division's performance, not their own. After a spin-off, they can be paid in their own company's stock, so their pay tracks their own decisions. Separation also exposes each company to the market for corporate control from article 21: a badly run standalone company can be acquired, while a badly run division buried inside a conglomerate usually cannot. That threat, even unexercised, sharpens management.

## 5. Why Breakups Destroy Value: Four Costs

A good banker argues against their own deal before recommending it. Breakups have real costs, and boards that ignore them end up with two weaker companies instead of one discounted one.

**Lost synergies.** Sometimes the divisions genuinely belong together: shared customers, shared distribution, shared research, a single brand. Splitting them destroys real cost savings and revenue benefits. The test is the same as the synergy test in article 12, run in reverse: if the synergies are large and hard to replicate by contract (a supply agreement, a licensing deal), the conglomerate discount may be smaller than the synergy value, and the breakup destroys wealth.

**Dis-synergies and stranded costs.** Separation creates costs that did not exist before: two boards, two audit fees, two headquarters, duplicated IT systems, and a corporate cost base that cannot be cut as fast as the revenue it supported. Bankers call the leftover piece **stranded costs** — the parent's headquarters costs that remain after the division leaves, spread over a smaller company. A spin-off model that forgets stranded costs overstates the gain by exactly that amount.

**The leverage and rating problem.** Debt has to be divided, and the division is not always fair or painless. Load too much debt onto the spun-off company and it starts life distressed; load too little and the parent is left under-levered with a bloated balance sheet. Either company can lose its credit rating in the process, raising its borrowing costs. The $600 million / $1.2 billion split in section 3 looks neat on paper; in a real deal it is negotiated against rating agency models, lender consents, and bond covenants, and it is often the hardest part of the transaction.

**Orphaning and index effects.** A spun-off company starts life small, often too small for the index funds and large institutions that owned the parent. When it leaves a major index, index funds must sell it mechanically, whatever they think of the business. It can also lack analyst coverage for months, trade thinly, and be owned initially by shareholders who never wanted it — parent shareholders who received it by distribution rather than by choice. That forced selling is one reason spun-off stocks can look cheap at first, and one reason the long-run return evidence is hard to interpret.

## 6. What the Evidence Actually Says

Spin-offs are one of the most studied events in corporate finance, and the evidence is genuinely mixed — which makes it a good place to practise reading research honestly.

The announcement effect is the least controversial finding. Across decades of studies, parent companies gain roughly 3% on average when they announce a spin-off. That is a real, repeatable market reaction, and it is consistent with the market believing, on average, that breakups help.

The long-run evidence is where it gets interesting, and where you should be careful. Cusatis, Miles, and Woolridge (1993) studied spin-offs from 1965 to 1988 and found positive long-run abnormal returns for both parents and spun-off companies — but with a twist: the gains were concentrated in companies that were subsequently acquired. Their interpretation was that the market underestimates, at announcement, how much a spin-off increases a company's chance of being taken over, and the takeover premium arrives later. Desai and Jain (1999) then showed that the long-run gains were much larger for **focus-increasing** spin-offs — where the spun-off unit operates in a different industry from the parent — than for spin-offs that did not change the parent's focus. In their sample, parents in focus-increasing spin-offs earned abnormal returns of about 25% over the three years after completion, and the spun-off subsidiaries about 54%, while non-focus-increasing spin-offs showed no significant long-run gains. Daley, Mehrotra, and Sivakumar (1997) found a matching pattern in operating performance: focus-increasing spin-offs improved operating results, others did not. The focus story, in other words, is not just a banker pitch; it shows up in both stock returns and accounting performance.

But there is a serious objection, and a good analyst states it plainly. Eugene Fama (1998) argued that long-run event studies of this kind are fragile: because the returns of companies that spun off in the same period move together, the usual statistical tests overstate how significant the results are, and small changes in method — the benchmark used, the weighting, the sample window — can make the "abnormal" returns shrink or vanish. European studies point the same way, finding the announcement pop but little or no long-run outperformance. So the honest summary: the announcement pop is reliable, the focus story is supported, and the famous long-run gains are suggestive, not settled.

## 7. The Banker's Job in a Separation

If the board approves a spin-off, the banker's work shifts from persuasion to plumbing. The separation plan must decide which assets, contracts, employees, intellectual property, and liabilities go with each company — including awkward shared items like a headquarters lease or a pension plan. Debt must be refinanced or allocated, and each company needs a standalone capital structure that rating agencies will accept. A Form 10 registration statement must be filed for the new company, with audited carve-out financial statements showing what the division would have looked like standalone — a difficult exercise when costs were shared. Shareholders need an information statement explaining the distribution ratio, the tax treatment, and the trading arrangements, including **when-issued trading**, where NewCo shares trade before the distribution date on the understanding that the spin-off will complete. The new company's management team, board, incentive plan, and investor story must all be built from scratch, usually while the division is still run as part of the parent. Nine to twelve months is a normal timetable; the announcement is the beginning, not the end.

There is also a strategic choice bankers frame explicitly: spin now, or carve out first? A carve-out IPO tests the market's appetite for the division and gives it a visible stock price, which makes a later spin-off easier to size and explain. But a carve-out leaves the parent in control, creates a minority shareholder base with its own interests, and can complicate a later full separation. The carve-out-then-spin route suits divisions whose value is uncertain or contested; the direct spin suits divisions whose value is clear and whose shareholders are ready to own them.

## 8. Common Misconceptions

**"A spin-off creates value out of nothing."** No. On paper it rearranges value, as section 3 shows: $39 plus $21 equals $60. Value is created only if the separated companies are worth more apart than together — better management, better capital allocation, better information, or a takeover that was previously impossible. The spin-off is the mechanism, not the magic.

**"The parent's share price falls by the value of the spun-off company, so shareholders lose."** The parent's price does fall on the distribution date, mechanically, because the parent no longer owns the subsidiary. But shareholders receive the subsidiary's shares, so their combined holding is unchanged on paper. Judging a spin-off by the parent's price alone is like judging a stock split by the lower post-split price: it mistakes the unit for the wealth.

**"Every conglomerate discount is a breakup opportunity."** Only if the discount exceeds the lost synergies plus the separation costs. Some conglomerates are discounted because they deserve to be — a weak division, poor management, a bad acquisition history — and splitting them just produces two discounted companies with higher costs. The discount is a question, not an answer.

**"Tax-free means free."** A tax-free spin-off avoids shareholder-level tax on the distribution, but the transaction still costs real money: advisory fees, separation costs, duplicated overhead, refinancing, and management time. "Tax-free" describes the tax treatment, not the price tag.

**"Spun-off stocks always outperform, so buy every spin-off."** The long-run evidence is disputed (section 6), the early trading is distorted by forced selling and thin coverage, and the average conceals enormous variation: focus-increasing spin-offs did well in the classic studies, others did not. Buying every spin-off is a bet on an average that may not survive better statistics.

## 9. Test Yourself

**1.** A parent has 150 million shares at $40 ($6.0 billion market cap). Its two divisions are worth $5.0 billion and $2.5 billion of enterprise value, and it has $1.0 billion of net debt. What is the sum-of-the-parts equity value per share, and what is the conglomerate discount?

*Answer.* Sum-of-the-parts enterprise value is $7.5 billion; minus $1.0 billion of net debt, equity is $6.5 billion, or $43.33 per share ($6.5 billion ÷ 150 million). The conglomerate discount is $6.5 billion − $6.0 billion = $500 million, about 7.7% of sum-of-the-parts equity.

**2.** The parent spins off the $2.5 billion division, which takes $400 million of debt and will have 50 million shares. What is the distribution ratio, and what are the implied per-share values of the two companies after the spin? Check that they add back to the sum-of-the-parts value.

*Answer.* Distribution ratio = 50 million ÷ 150 million = 0.333 shares per parent share. The spun-off company's equity is $2.5 billion − $0.4 billion = $2.1 billion, or $42.00 per share. The remaining parent's equity is $5.0 billion − $0.6 billion = $4.4 billion, or $29.33 per share. Check: $29.33 + (0.333 × $42.00) = $29.33 + $14.00 = $43.33, the sum-of-the-parts value. (Rounding: $29.333… + $14.00 = $43.333….)

**3.** A board is choosing between spinning off a division and selling it to a strategic buyer who will pay a 25% premium to its standalone value. Name one reason to prefer the spin-off despite the lower headline price, and one reason to prefer the sale.

*Answer.* Prefer the spin-off if the division's value is uncertain or contested (the market may re-rate it above the buyer's price once it trades standalone), if the sale would trigger a large tax bill that a qualifying tax-free spin-off avoids, or if shareholders specifically want to keep owning the asset. Prefer the sale if the buyer pays full value in certain cash today, if the division has few standalone prospects or heavy separation costs, or if the parent needs the cash for debt reduction or investment.

**4.** Why might a spun-off stock fall in its first weeks of trading even if the business is sound?

*Answer.* Forced and indifferent selling: index funds that must sell because the new stock is not in their index, and parent shareholders who received shares by distribution rather than by choice and sell them to restore their original portfolio. Thin analyst coverage and low initial liquidity amplify the pressure. Early weakness is therefore weak evidence about the business — it may reflect who owns the stock, not what the company is worth.

## Next up

Next up: 23 | Merger Arbitrage: Betting on Deals Closing — how arbitrageurs price the gap between a deal's announcement and its close, and what that spread is really telling you.

---

*Papers cited in this article (all verified by web search before citing): Cusatis, P., Miles, J., & Woolridge, J. R. (1993). Restructuring through spinoffs: The stock market evidence. Journal of Financial Economics, Vol. 33, pp. 293–311. Desai, H., & Jain, P. C. (1999). Firm performance and focus: Long-run stock market performance following spinoffs. Journal of Financial Economics, Vol. 54, pp. 75–101. Daley, L., Mehrotra, V., & Sivakumar, R. (1997). Corporate focus and value creation: Evidence from spinoffs. Journal of Financial Economics, Vol. 45, pp. 257–281. Fama, E. F. (1998). Market efficiency, long-term returns, and behavioral finance. Journal of Financial Economics, Vol. 49, pp. 283–306.*

*Learning in public. Not investment advice.*
