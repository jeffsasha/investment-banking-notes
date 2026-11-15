# 33 | SPACs and the Blank-Check Boom: When the Deal Goes Public Before It Finds a Target

*Article 32 was about a price that gets paid later, only if the business performs. This one is about a deal that goes public before it has a business at all. In 2021, more than six hundred companies with no operations, no revenue, and no product raised $162 billion from public investors — on the promise that they would find something worth buying later. If that sounds backwards, it is. And the reason it worked, briefly, tells you more about how markets actually function than any textbook chapter on IPOs.*

> **Learning goals.** After this article you can: (1) explain what a SPAC is and how its $10 unit, trust account, and redemption right fit together; (2) walk through the life cycle of a SPAC from its IPO to a merger or a liquidation; (3) compute net cash per share and explain why it is the single most important number in any SPAC deal; (4) explain who gets paid in a SPAC transaction — the sponsor, the underwriter, the PIPE investor, the redeeming shareholder — and who pays for it; (5) name the three reasons a private company might prefer a SPAC merger to a traditional IPO, and the two reasons it usually should not; (6) explain what the 2024 SEC rules changed and why.
>
> **Prerequisites.** Article 19 (IPO pricing and bookbuilding) for how a traditional listing works and what underpricing costs; article 20 (debt capital markets) for how a deal gets sold to investors; article 06 (DCF I) for what a forecast is actually worth; article 32 (earnouts) for how deal structures create incentives that outlive the signing.

## 1. A Company With No Business

A **special purpose acquisition company**, universally called a **SPAC**, is a company whose only business is to find a business. It has no operations, no revenue, no employees in any meaningful sense, and no product. It exists for one purpose: to raise money from the public, park that money in a trust account, and then use it to buy a real private company, taking that company public in the process. The merger that does this is called the **de-SPAC** transaction, or the business combination.

The structure is deliberately simple, and the simplicity is the point. A **sponsor** — usually a small team of investors, sometimes a well-known name — forms the SPAC and takes it public. The SPAC sells **units** to the public at $10.00 each. A unit is typically one share of common stock plus a fraction of a **warrant** — a warrant is an option to buy an additional share later at a fixed price, usually $11.50. The $10 per share goes into a **trust account**, where it sits in Treasury bills earning interest until the SPAC either merges or liquidates. The sponsor, meanwhile, buys **founder shares** — the **promote** — for a nominal price, usually $25,000 in total. Those founder shares are typically 20% of the SPAC's shares after the IPO.

Then the clock starts. A SPAC usually has 18 to 24 months to find a target and complete a merger. If it fails, it liquidates: the trust account is returned to public shareholders, roughly $10 per share plus a little interest, the warrants expire worthless, and the sponsor loses its $25,000 plus whatever it spent on the IPO and the search. The sponsor's promote is worth nothing if there is no deal. That asymmetry — nothing if the SPAC liquidates, a fortune if it merges — is the engine of the entire story, and we will come back to it.

Why would anyone buy a share in a company with no business? Because of the **redemption right**. When the SPAC announces a merger, every public shareholder gets a choice: keep your shares in the combined company, or hand them back and get your $10 (plus accrued interest) out of the trust. You can vote against the deal and still keep your shares, or vote for it and still redeem — the two decisions are separate. The redemption right means a SPAC share is, in the downside case, a nearly risk-free $10 bill with a free warrant attached. That downside protection is what made SPACs sellable to hedge funds, and it is also what quietly destroyed them.

## 2. The Life Cycle: From IPO to Merger or Liquidation

A SPAC's life has four stages, and the incentives change at each one.

**Stage one: the IPO.** The sponsor forms the shell, files an S-1, and sells units at $10. The underwriter takes a fee — typically 5.5% of the amount raised, of which about 2% is paid at the IPO and 3.5% is deferred until the merger closes. Note the structure of that fee: the underwriter only collects the deferred portion if a deal happens. Like the sponsor, the underwriter is paid for a merger, not for a good merger.

**Stage two: the search.** The SPAC has roughly two years to find a target. The sponsor negotiates with private companies, and when it finds one, it signs a letter of intent and then a definitive merger agreement. The agreement sets a valuation for the target — usually expressed as an enterprise value — and a price per share for the SPAC's shares, almost always $10. The target's owners receive shares in the combined company, and sometimes cash.

**Stage three: the PIPE.** Because shareholders can redeem, the SPAC does not actually know how much cash it will have at closing. To plug the gap, it typically raises a **PIPE** — a private investment in public equity — from institutional investors who commit to buy shares in the combined company at $10, at the same time as the merger. The PIPE serves two purposes: it backstops the cash, and it validates the price. When a serious fund commits $100 million at $10, the market reads it as a signal that the valuation is real. Gahng, Ritter, and Zhang (2023) find that deals with PIPE participation behave differently from deals without it — the PIPE is the market's substitute for the bookbuilding process a traditional IPO would have had.

**Stage four: the vote and the close.** Shareholders vote on the merger, and anyone who wants out redeems. Whatever cash remains in the trust, plus the PIPE money, goes to the combined company. The target's shareholders get their shares, the sponsor's founder shares convert into ordinary shares, and the combined company starts trading under the target's name. Or, if redemptions are so high that the deal cannot close on its agreed terms, the deal is renegotiated or abandoned — and if no deal closes before the deadline, the SPAC liquidates and returns the trust.

One more feature of stage four matters enormously. Before 2024, the de-SPAC transaction enjoyed a legal advantage no traditional IPO had: the **safe harbor** for forward-looking statements under the Private Securities Litigation Reform Act. An IPO prospectus is a historical document — it describes the past and is liable for what it says. A de-SPAC proxy statement, by contrast, could publish the target's rosy five-year projections with far less liability. For a young company whose value was mostly in a forecast — an electric-truck maker with no trucks, a space company with no revenue — that was the whole attraction. The SEC removed that advantage in its January 2024 rules, which is where section 8 comes in.

## 3. Worked Example: Where the $10 Goes

Here is the arithmetic that decides whether a SPAC deal makes sense, and it is the arithmetic most investors never did. Take a SPAC that raises $200 million by selling 20 million units at $10.00 each.

- **Trust account at IPO:** $200 million, or $10.00 per public share.
- **Sponsor promote:** 5 million founder shares bought for $25,000 — 20% of the 25 million shares outstanding after the IPO.
- **Underwriting fee:** 5.5% of $200 million, or $11 million. $4 million is paid at the IPO; $7 million is deferred and due only if a merger closes.
- **Warrants:** each unit carries half a warrant, so 10 million warrants are outstanding, each exercisable at $11.50.

Now the SPAC finds a target and announces a merger. Public shareholders look at the deal, and 70% of them redeem — a redemption rate that was routine in 2021. Fourteen million shares go back, and $140 million leaves the trust. What is left?

```math
\text{Cash remaining in trust} = 200 - 140 = \$60\text{ million}
```

The deferred underwriting fee of $7 million comes due at closing:

```math
\text{Net cash delivered to the combined company} = 60 - 7 = \$53\text{ million}
```

Now the question that matters: how many shares is that $53 million spread across? The SPAC's own shares outstanding after the merger are the 6 million non-redeeming public shares plus the sponsor's 5 million founder shares — 11 million shares. (The target's shareholders get their own shares on top, but those shares represent the target's own value; the question here is how much cash backs each SPAC share.)

```math
\text{Net cash per share} = \frac{53}{11} = \$4.82
```

Read that number twice. The SPAC raised $10.00 per share from the public. By the time it merges, it delivers $4.82 of cash per share to the combined company. More than half the money is gone — consumed by redemptions, the sponsor's promote, and the underwriting fee. And this is before the warrants, which dilute the share count further if the stock ever rises above $11.50.

This is not a contrived example. Klausner, Ohlrogge, and Ruan (2022) measured this for real: for SPACs that merged between January 2019 and June 2020, the **median** SPAC held just $5.70 in net cash per $10.00 share at the time of its merger, and the **mean** was $4.10. Our example's $4.82 sits right in that range. The $10 share was, at the moment of the merger, a claim on roughly $5 of cash plus a speculative business.

Two things follow. First, the combined company starts public life with far less cash than the headline numbers suggest. A "$200 million SPAC deal" that delivers $53 million of cash is a $53 million capital raise wearing a $200 million costume — and the target's business plan, which was written assuming $200 million, now has to be executed on a quarter of that. Second, the dilution is a transfer, not a loss to the void. The $5.18 per share that vanished went somewhere: to the sponsor, whose $25,000 bought 5 million shares; to the underwriter; and to the redeeming shareholders, who took their $10 back and kept their warrants. Somebody always gets paid in a SPAC. The question is who, and whether it is you.

## 4. Who Gets Paid, and When

Every participant in a SPAC faces a different payoff, and understanding the deal means understanding all four at once.

**The sponsor** has the best deal in finance, if the merger closes. It paid $25,000 for founder shares that convert into 20% of the SPAC. In our example, those 5 million shares are worth $50 million at the $10 merger price — a 2,000x return on $25,000. If the SPAC liquidates instead, the sponsor gets nothing and loses the money it spent on the IPO and the search, which can run into the millions. So the sponsor's incentive is binary and overwhelming: close *a* deal, any deal, before the deadline. A mediocre merger pays the sponsor $50 million; a liquidation pays it nothing. This is why sponsors kept merging with companies that were plainly not ready to be public. The sponsor is paid for the merger, not for the outcome.

**The underwriter** is in the same boat, in miniature. Its deferred 3.5% fee arrives only if the deal closes. It has every reason to help the sponsor find a target and close it.

**The redeeming shareholder** — usually a hedge fund that bought units at the IPO — has the safest trade in the structure. It buys a unit for $10, redeems the share for $10 plus interest, and keeps the warrant for free. If the merger is good, it can choose not to redeem and keep the upside; if the merger is bad, it redeems and still owns a warrant that might pay off later. Gahng, Ritter, and Zhang (2023) document this precisely: IPO investors who redeem optimally earn significant positive returns, while buy-and-hold investors in the merged company lose money. The redemption right turns the SPAC into a free option for the sophisticated buyer.

**The buy-and-hold shareholder** — the retail investor who buys after the merger announcement, or holds through it — pays for everyone else. They own shares in a company that started public life with roughly $5 of cash per $10 share, run by a sponsor who has already been paid, with a warrant overhang waiting to dilute them if the stock rises. Klausner, Ohlrogge, and Ruan found that post-merger market-adjusted returns averaged roughly **negative 50%** over the 18 months following a merger for their 2019–2020 sample. Their follow-up (Klausner & Ohlrogge, 2023) found the pattern held through the boom: SPACs that merged between July 2020 and December 2021 averaged a share price of **$3.85** by December 2022, down more than 60% from the $10 redemption value.

That is the distributional truth of the SPAC: it is a machine that transfers value from the shareholders who stay to the sponsor, the underwriter, and the shareholders who leave. It is not a scam in the legal sense — every term is disclosed in the prospectus. It is a structure whose disclosed terms happen to be very good for the people who designed it.

## 5. Why Would a Company Choose This?

If the arithmetic is that bad, why did hundreds of real companies choose to go public this way? Three reasons, one genuine and two that were mostly regulatory arbitrage.

**Speed and certainty.** A traditional IPO takes months, depends on market conditions at pricing, and can be pulled at the last minute. A SPAC merger negotiates a fixed valuation with the sponsor and, once announced, is much more likely to close. For a company that needs cash on a timetable — or a founder who wants a locked-in valuation — that certainty has real value. This is the honest reason, and it is why SPACs will not disappear entirely: there are companies for which a negotiated deal beats a market-priced one.

**The projections safe harbor.** Before 2024, a de-SPAC proxy could publish forward-looking projections with liability protection that an IPO prospectus did not enjoy. For companies whose entire value was a forecast — pre-revenue electric vehicle makers, space startups, biotech firms years from a product — this was not a side benefit. It was the product. A traditional IPO prospectus for a company with no revenue is an awkward document; a SPAC deck could show a hockey-stick revenue chart for 2027 and call it a plan. Nikola went public by merging with the SPAC VectoIQ in June 2020, reached a peak market cap near $30 billion, and later settled SEC fraud charges for $125 million; its founder was convicted of securities and wire fraud. The safe harbor did not protect fraud, but it protected optimism — and in 2020 and 2021, optimism was the inventory.

**PIPE validation instead of bookbuilding.** In a traditional IPO (article 19), the bookbuilding process tests the price against real demand from institutional investors. In a SPAC merger, the PIPE plays that role — a few large investors commit at $10, and their commitment is presented as evidence the price is right. The problem is that a PIPE commitment is not the same test. PIPE investors often receive warrants or other sweeteners, and their commitment is negotiated with the sponsor, not discovered in a market. When the PIPE investors are also the ones who will redeem, the validation is thinner than it looks.

There were good SPAC deals. DraftKings went public through Diamond Eagle in April 2020 and became a real public company. Virgin Galactic merged with Social Capital Hedosophia in 2019. But the good deals were the exception in a flood: in 2020, 248 SPACs raised about $83 billion; in 2021, 613 SPACs raised about $162 billion — more than every previous year of SPACs combined. The structure was built for a trickle and was asked to carry a river, and the quality of the targets fell as the number of SPACs chasing them rose.

## 6. The Boom and the Bust

The boom had a simple cause: in a zero-interest-rate world, the redemption right made SPAC units nearly risk-free, the sponsor promote made forming SPACs nearly free money, and the safe harbor made the pitch decks nearly consequence-free. Celebrities formed SPACs. Athletes formed SPACs. By early 2021, SPACs were more than half of all U.S. IPOs by count.

The bust had an equally simple cause: the arithmetic in section 3 does not care about enthusiasm. Companies that went public with $5 of cash per $10 share and a forecast for a business that did not yet exist mostly failed to become that business. Redemption rates climbed through 2021 — in many deals above 80%, and in some above 90% — which meant the cash delivered kept shrinking even as the headline deal values grew. Post-merger stocks fell, the SEC proposed sweeping new rules in March 2022, and issuance collapsed: 86 SPAC IPOs in 2022, down from 613 the year before, and 31 in 2023. The SPAC market did not die — issuance has partially recovered since — but the 2021 version of it did, and it died of its own arithmetic.

The lesson is not that SPACs are fraud. The lesson is that a security's price is not its value, and a structure's disclosed terms are not the same as its economics. The $10 share was always a $5 claim plus a lottery ticket; the market spent two years pricing it as a $10 claim plus a lottery ticket. When the two sides of that equation met, the gap closed from the price side, not the value side.

## 7. What the Research Says

Three findings are worth carrying into any conversation about SPACs.

**Going public via SPAC is more expensive than an IPO.** Gahng, Ritter, and Zhang (2023) — "SPACs," *Review of Financial Studies* — compare the all-in cost of going public through a SPAC merger against a traditional IPO and find the SPAC route much more expensive, once dilution from the promote, the warrants, and the underwriting fees is counted. The headline fee looks smaller than IPO underwriting; the true cost, measured in value transferred away from the company's shareholders, is larger.

**Dilution predicts returns.** Klausner, Ohlrogge, and Ruan (2022) — "A Sober Look at SPACs," *Yale Journal on Regulation* — show that the lower a SPAC's net cash per share at merger, the worse its post-merger stock performance. The relationship is strong enough that net cash per share is close to a sufficient statistic for how the deal will turn out for the shareholders who stay. This is why section 3's arithmetic is the whole game: if you can compute net cash per share, you know most of what matters.

**The structure exists because investors disagree.** Banerjee and Szydlowski (2024) — "Harnessing the Overconfidence of the Crowd: A Theory of SPACs," *Journal of Financial Economics* — model SPACs as a way to exploit disagreement. Optimistic investors are willing to pay $10 for a claim worth $5 of cash because they overvalue the target's prospects; the redemption right lets pessimistic investors exit with their $10 intact. The SPAC, in this telling, is a machine for separating optimists from their money while letting everyone else take a fee. It is a model, not a verdict — but it fits the data uncomfortably well.

One honest caveat, in the spirit of article 14: the research above mostly studies the 2019–2021 period, and the post-2024 SPAC looks different — smaller promotes, better disclosure, no safe harbor. Whether the new structure produces better outcomes is an open question, and the honest answer is that we do not have enough post-reform mergers yet to know.

## 8. The 2024 Rules Change the Game

On January 24, 2024, the SEC adopted final SPAC rules (Release No. 33-11265) by a 3–2 vote, effective July 1, 2024. Three changes matter for bankers:

**The safe harbor is gone for de-SPAC projections.** Forward-looking statements in a de-SPAC transaction no longer enjoy the PSLRA safe harbor. A target's five-year forecast is now subject to the same liability discipline as an IPO prospectus. The hockey-stick chart is still legal; it is no longer cheap.

**Dilution must be disclosed, plainly.** SPACs must now disclose the sponsor's compensation, conflicts of interest, and the dilution embedded in the structure — including a version of the net cash per share arithmetic from section 3. The number that used to require an academic paper to compute is now in the filing.

**The playing field with IPOs is closer to level.** The rules align de-SPAC disclosure and liability more closely with traditional IPOs, which removes the regulatory arbitrage that was, for many targets, the main reason to choose the SPAC route. What remains is the genuine reason: speed and a negotiated valuation.

Whether that is enough to sustain a healthy SPAC market is the live question. A SPAC without the safe harbor and without hidden dilution is a more honest instrument — and a less exciting one. The sponsor promote still exists, the redemption right still exists, and the incentive to close any deal before the deadline still exists. The 2024 rules fixed the disclosure; they did not fix the incentives.

## 9. Common Misconceptions

**"A SPAC is a cheaper way to go public than an IPO."**
The underwriting fee is smaller, and that is where the comparison usually stops. The all-in cost — promote, warrants, deferred fees, dilution from redemptions — is larger, as Gahng, Ritter, and Zhang document. A SPAC looks cheaper the way a zero-down mortgage looks cheaper: the cost is not gone, it is deferred into the structure.

**"The $10 share price means the company is worth $10 a share."**
The $10 is the redemption value, not a valuation. It is the amount in the trust, and it is what you get if you leave. It says nothing about what the combined company is worth — which, at merger, is backed by roughly $5 of cash per share plus a business whose value is an open question. Treating the redemption price as a market price is the single most common error in SPAC investing.

**"High redemption rates mean the deal is bad."**
High redemptions do mean the cash delivered will be small, which is bad for the combined company. But redemptions are also the mechanism working as designed: shareholders who doubt the deal get their money back. The problem is not the redemption itself. The problem is that the deal can still close with 90% of the cash gone, because the sponsor and the target want it to close. The redemption right protects the individual shareholder; it does not protect the company.

**"The sponsor and the shareholders want the same thing."**
They do not. The sponsor is paid if a deal closes and paid nothing if it does not; the shareholder is paid if the *right* deal closes at the *right* price. A sponsor choosing between a mediocre merger and a liquidation is choosing between a fortune and zero. A shareholder choosing between the same two options is choosing between a bad investment and their money back. Same vote, opposite interests — and the sponsor usually controls the process.

**"SPACs are dead."**
Issuance collapsed in 2022 and 2023, but SPACs are still being formed, and the 2024 rules made them a cleaner instrument rather than abolishing them. The 2021 boom is dead. The structure is not. The right question is not whether SPACs exist; it is whether the next generation's terms — the size of the promote, the disclosure of dilution, the quality of the targets — are better than the last one's. That question is still open, and it is the one worth watching.

## 10. Test Yourself

**1. A SPAC raises $300 million by selling 30 million units at $10. Its sponsor holds 7.5 million founder shares. Underwriting fees total 5.5%, of which $10.5 million is deferred to closing. At the merger, 80% of public shares redeem. What is the net cash per SPAC share delivered to the combined company? (Ignore warrants.)**

*Answer:* Redemptions: 80% × 30 million = 24 million shares, so $240 million leaves the trust. Cash remaining: $300m − $240m = $60m. Less the deferred fee of $10.5m: net cash = $49.5m. SPAC shares outstanding after the merger: 6 million non-redeeming public shares + 7.5 million founder shares = 13.5 million. Net cash per share = $49.5m / 13.5m = **$3.67**. The $10 share delivers $3.67 of cash — worse than our section 3 example, because the redemption rate is higher.

**2. A sponsor paid $25,000 for founder shares equal to 20% of a SPAC. The SPAC merges and the combined company's shares trade at $10. The sponsor's stake is worth $50 million. Explain in one sentence why the sponsor would prefer this merger to liquidating, even if the target is a bad business.**

*Answer:* Because the sponsor's payoff is binary — roughly $50 million if any merger closes and roughly zero (minus its sunk costs) if the SPAC liquidates — so a bad merger is worth $50 million more to the sponsor than no merger at all.

**3. An investor buys SPAC units at $10 at the IPO, redeems the shares at the merger for $10.10 including interest, and keeps the warrants. A second investor buys shares in the merged company at $10 and holds them for 18 months. According to Gahng, Ritter, and Zhang (2023) and Klausner, Ohlrogge, and Ruan (2022), which investor is likely to have done better, and why?**

*Answer:* The first investor. Gahng, Ritter, and Zhang find that IPO investors who redeem optimally earn significant positive returns — they get their money back plus a free warrant — while Klausner, Ohlrogge, and Ruan find that post-merger buy-and-hold returns average roughly negative 50% over 18 months, driven by the dilution measured by net cash per share. The structure pays the investor who leaves and charges the investor who stays.

**4. A pre-revenue company is choosing between a traditional IPO and a SPAC merger in 2025. Its bankers say the SPAC is better because it can publish five-year revenue projections in the merger documents. What changed in 2024 that makes this advice wrong, and what reason for choosing a SPAC would still be legitimate?**

*Answer:* The SEC's January 2024 final rules removed the PSLRA safe harbor for forward-looking statements in de-SPAC transactions, so the projections now carry the same liability discipline as an IPO prospectus — the regulatory advantage is gone. The legitimate reason that remains is speed and valuation certainty: a negotiated merger price and a higher likelihood of closing on a timetable, rather than a market-priced IPO that can be pulled.

---

**Papers cited:** Gahng, M., Ritter, J. R. & Zhang, D. (2023). "SPACs." *Review of Financial Studies*, 36(9), 3463–3501. · Klausner, M., Ohlrogge, M. & Ruan, E. (2022). "A Sober Look at SPACs." *Yale Journal on Regulation*, 39(1), 228. · Klausner, M. & Ohlrogge, M. (2023). "Was the SPAC Crash Predictable?" *Yale Journal on Regulation Bulletin*, 40, 101. · Banerjee, S. & Szydlowski, M. (2024). "Harnessing the Overconfidence of the Crowd: A Theory of SPACs." *Journal of Financial Economics*, 153, 103787.

*Next up: Convertible Bonds — debt that turns into equity, and why companies issue it when neither straight debt nor straight equity quite fits.*
