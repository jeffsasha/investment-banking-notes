# 05 | Precedent Transactions and Control Premiums

*If trading multiples answer "what is this company worth today," precedent transactions answer a better question for a seller: "what did a real buyer actually pay for something like this?" The gap between the two numbers is the control premium — and understanding it is the difference between quoting a price and negotiating one.*

> **Learning goals.** After this article you can: (1) explain what a precedent transactions analysis is and why it sits next to comps on every football field; (2) define the **control premium** and derive it from an offer price and an "unaffected" price; (3) build a small precedent set, compute deal multiples and premiums, and triangulate a valuation range; (4) name the five classic justifications for paying a premium — and the two that are excuses.
>
> **Prerequisites.** Articles 02–04 (financial statements, EV vs. equity value, trading multiples). You should be comfortable with EV/EBITDA.

## 1. The Two Kinds of Evidence

In 04 we valued companies using **trading multiples**: take public peers, read their market prices, apply the median multiple to your company. That tells you the **standalone value** — what the company is worth as an independent, minority-held entity, with no buyer in sight.

But sellers don't sell standalone value. They sell to a buyer, and buyers pay for something extra: **control** — the right to change the management, merge the operations, fire half the headquarters, and decide the company's future. History is full of prices actually paid for control. A **precedent transactions** analysis ("precs" or "deal comps") collects those prices and asks: what multiples did real buyers pay, and what premium over the market price did they accept?

Think of it this way:

- **Trading comps** = what investors pay for a slice of a company they can't control.
- **Precedent transactions** = what buyers paid for the *whole* company, including the keys.

Both are market evidence. Neither is the "true" value. But a banker arguing that a client should receive $66 per share needs to show that somebody, somewhere, paid like that for something similar. That is what precs are for.

```math
\text{Control premium} = \frac{\text{Offer price per share} - \text{Unaffected price per share}}{\text{Unaffected price per share}}
```

The **unaffected price** is the target's share price *before* the deal leaked or was announced — before the market started pricing in the takeover itself. Everything else in this article hangs off that one fraction.

## 2. Why the Premium Exists (and Why Bankers Care So Much)

Historically, buyers of public companies pay roughly 20–40% over the pre-announcement price. That is not a law of nature; it's an empirical regularity, and it needs an explanation. There are five standard justifications, and you should learn to rank them:

**1. Synergies.** The textbook answer. If combining two companies creates cost savings (one HQ, one IT system) or revenue uplift (cross-selling), the combined firm is worth more than the sum of the parts. The premium is the buyer sharing those synergies with the target's shareholders. This is the only justification that creates genuine economic value — it's also the one bankers are paid to quantify.

**2. Competitive bidding.** In an auction, the price is set by the *second*-most-optimistic bidder plus a dollar. Even if no synergy exists, the winner had to beat someone else. Premiums paid in hot auction processes routinely exceed premiums in negotiated one-on-one deals.

**3. The toehold-to-control arbitrage.** A minority share can't fire the CEO. A 100% stake can. Control has option value — the ability to fix a broken company, sell assets, or change strategy. Shareholders who give up that option charge for it.

**4. Agency motives (the buyer's CEO just wants to be bigger).** Managers with diffuse ownership spend shareholders' money on empire-building. Roll (1986) called this the **hubris hypothesis**: acquirers systematically overpay because their CEOs overestimate their own ability to run the target. This isn't a justification — it's an explanation of why premiums are often too high. Know the difference.

**5. The market price was "wrong."** Sometimes the target was genuinely undervalued — temporarily depressed earnings, a misunderstood segment, a stock nobody covered. The buyer is paying for value the market hadn't recognized yet. Plausible, but dangerous to assert, because it's unfalsifiable: *any* premium can be relabeled as "the market was wrong."

Academic evidence keeps bankers honest here. Andrade, Mitchell, and Stafford (2001) survey decades of merger data and find that mergers do create value on average — but **most of the gains accrue to the target's shareholders**, i.e., the premium. The acquirer's shareholders, on average, get roughly nothing. That fact alone should make you skeptical every time a CEO says "we paid a full price because the synergies are real."

And the type of buyer matters. Bargeron, Schlingemann, Stulz, and Zutter (2008) find that public targets get **63% higher premiums from public acquirers than from private equity buyers** (and 14% higher than from private operating firms) — the gap is tied to the agency incentives of the bidder's own managers. Keep that in your pocket: when you build a prec set, separate strategic buyers from sponsors. They don't pay the same prices.

> **Citations (verified):**
> - Andrade, G., Mitchell, M., & Stafford, E. (2001). *New Evidence and Perspectives on Mergers.* Journal of Economic Perspectives, 15(2), 103–120.
> - Bargeron, L. L., Schlingemann, F. P., Stulz, R. M., & Zutter, C. J. (2008). *Why do private acquirers pay so little compared to public acquirers?* Journal of Financial Economics, 89(3), 375–390.
> - Roll, R. (1986). *The Hubris Hypothesis of Corporate Takeovers.* Journal of Business, 59(2), 197–216.

## 3. Building the Precedent Set: The Screening Rules

A prec analysis is a table of past deals. Its credibility lives or dies on which deals you let in. The standard screens:

1. **Industry and business model match.** A logistics deal tells you nothing about a software target. Bankers usually restrict to the same sub-sector, or at most adjacent ones.
2. **Recency.** Deals older than ~3–5 years get stale — the market regime, interest rates, and strategic logic have moved on. In a rising-rate environment, a 2021 multiple is a different animal than a 2025 one.
3. **Deal size.** A $50m tuck-in acquisition and a $5bn take-private are different markets with different buyer universes. Keep enterprise values within a reasonable band of your target.
4. **Deal structure.** Majority-control transactions only. Minority investments don't carry a control premium, so including them pollutes the set. Take-privates, strategic acquisitions, and sponsor buyouts qualify.
5. **Buyer type.** Tag each deal: strategic vs. financial sponsor. As the Bargeron et al. finding suggests, these are two different price distributions. Many bankers show them as separate rows or footnotes.

For each deal you record: announcement date, target, acquirer (+ type), deal enterprise value, the target's LTM financials (revenue, EBITDA — the **last twelve months before announcement**, not after), the offer price per share, and the unaffected price per share.

The two derived statistics:

```math
\text{Deal EV/EBITDA} = \frac{\text{Enterprise value paid}}{\text{Target LTM EBITDA}}
```

```math
\text{Premium paid} = \frac{\text{Offer price} - \text{Unaffected price}}{\text{Unaffected price}}
```

Median and mean of each column become your valuation inputs. The median is the workhorse — it ignores the one crazy outlier deal that would drag the mean around.

## 4. The "Unaffected Price" Problem

The trickiest judgment call in the whole analysis is choosing the unaffected price. The naive choice — the closing price the day before announcement — is often wrong, because deals leak. A stock that drifts up 15% in the three weeks before announcement was probably already pricing in takeover rumors. Using the day-before price then *understates* the true premium.

Standard practice:

- **1-day premium:** offer vs. close one trading day before announcement. Simple, but contaminated by leaks.
- **1-week / 1-month premium:** offer vs. the price 5 or 20 trading days before announcement. The 1-month figure is the industry default for "unaffected" — far enough back to predate most leaks, recent enough to reflect the same market.
- Bankers typically show all three and lean on the 1-month. If the stock ran up hard in the month before announcement, they'll say so in a footnote and adjust their read of the premium downward.

There is no perfect answer. The honest version of the analysis shows multiple unaffected dates and lets the reader see how sensitive the premium is. The dishonest version — the one you should watch for in a sell-side pitch — quietly uses the 1-day premium when the stock already ran up, making a mediocre offer look generous.

## 5. Worked Example: Valuing Beacon Logistics

Let's put it together. Our fictional target is **Beacon Logistics**, a US regional freight company:

- Unaffected share price (1 month pre-rumor): **$52.00**
- Fully diluted shares: **20.0m** → unaffected equity value = 52.00 × 20.0 = **$1,040m**
- Net debt: **$80m** → unaffected EV = 1,040 + 80 = **$1,120m**
- LTM EBITDA: **$140m** → unaffected EV/EBITDA = 1,120 / 140 = **8.0x**

We screen five comparable control transactions from the last three years:

| # | Target (fictional) | Buyer type | Deal EV ($m) | LTM EBITDA ($m) | EV/EBITDA | Offer ($/sh) | Unaffected ($/sh) | Premium |
|---|---|---|---|---|---|---|---|---|
| 1 | Atlas Freight | Strategic | 1,140 | 120 | 9.5x | 54.00 | 43.00 | 25.6% |
| 2 | Copperline Transport | Strategic | 1,530 | 150 | 10.2x | 72.00 | 58.00 | 24.1% |
| 3 | Harborline Inc. | Sponsor | 650 | 65 | 10.0x | 33.00 | 26.50 | 24.5% |
| 4 | Meridian Cargo | Strategic | 1,890 | 180 | 10.5x | 91.00 | 72.00 | 26.4% |
| 5 | Dockside Logistics | Sponsor | 1,078 | 110 | 9.8x | 50.00 | 46.00 | 8.7% |

Check one premium by hand (deal 1): (54.00 − 43.00) / 43.00 = 11.00 / 43.00 = **25.58% ≈ 25.6%**. ✓

Summary statistics:

```math
\text{Median EV/EBITDA} = 10.0x \quad (\text{mean} \approx 10.0x)
```

```math
\text{Median premium} = 24.5\% \quad (\text{mean} = 21.9\%)
```

**Method A — deal multiples.** Implied EV = 140 × 10.0 = **$1,400m**. Equity value = 1,400 − 80 = **$1,320m**. Per share = 1,320 / 20.0 = **$66.00**. Using the min/max multiple (9.5x–10.5x) gives a range of **$62.50–$69.50** per share.

**Method B — premium cross-check.** Unaffected equity $1,040m × (1 + 24.5%) = **$1,295m** → **$64.75** per share.

The two methods land within ~2% of each other ($64.75 vs. $66.00). That convergence is the whole point: deal multiples and premiums are two lenses on the same evidence, and when they agree, the answer is credible. A banker would present the $62.50–$69.50 range from the multiples as primary, and the $64.75 premium-implied price as the sanity check.

One more read of the table: the sponsor deals (3 and 5) sit at the low end of the premium distribution — deal 5's 8.7% premium is the outlier dragging the mean down, which is exactly why we use the median, and exactly the Bargeron et al. pattern (sponsors pay less) showing up in miniature. If your buyer is a strategic, you might fairly argue the relevant premium is the strategic-only median: 25.6%.

## 6. Adjustments, Footnotes, and How This Gets Abused

Precs are the easiest valuation method to manipulate, because the analyst chooses the sample. The standard defenses:

- **Show your screens.** Every prec table should state the date range, size band, and industry filter. If a pitch shows seven deals and the sector had thirty, ask what got excluded.
- **Adjust for the cycle.** A multiple paid at the top of a freight cycle is not the same as one paid at the bottom. Some bankers normalize using mid-cycle EBITDA; at minimum, flag where each deal sits in the cycle.
- **Watch the currency and the regime.** Cross-border deals embed FX moves; 2021 deals embed near-zero rates. Neither transfers cleanly to today.
- **Don't mix announced and rumored.** Only use deals with disclosed, binding terms. A "reported" price that later fell apart is not evidence of anything.
- **The premium is not the recommendation.** A 25% median premium says buyers *have paid* that much. It does not say your buyer *will* — or *should*. The analysis is descriptive, and the negotiation starts where the math ends.

A final structural point: precedent transactions look backward by construction. In a sector being disrupted — say, freight brokerage being eaten by software — the last three years of deals may describe a world that no longer exists. Precs tell you what the market *was* willing to pay. The DCF (articles 06–07) is where you get to argue about what the future is worth.

## 7. Common Misconceptions

**"The control premium is always 20–40%, so just add 30% to the stock price."** No. The premium is an output of comparable deals, not an input you assume. Applying a generic 30% without a prec set is astrology with a spreadsheet.

**"A higher premium means a better deal for the buyer."** Backwards. The premium accrues to the *target's* shareholders. For the buyer, a high premium is a high hurdle: the synergies have to be real and large enough to earn it back. Andrade et al.'s finding — acquirers gain roughly nothing on average — is the empirical shadow of this mistake.

**"Deal multiples and trading multiples should be the same."** They shouldn't, and the gap is informative. Deal multiples embed control value and are paid with real money changing hands; trading multiples reflect minority expectations. If your prec multiples are *below* your trading comps, something is off — stale deals, a distressed sample, or a target whose standalone value has genuinely deteriorated.

**"The unaffected price is just the price the day before announcement."** Only if the deal never leaked, which is rare for large caps. The 1-month unaffected price exists precisely because information seeps. Using the 1-day price on a leaked deal understates the premium and flatters the offer.

**"Sponsor deals and strategic deals are interchangeable data points."** The evidence says otherwise. Sponsors pay with leverage and a required IRR; strategics pay with synergies they hope are real. They are different buyer universes with different price distributions — tag them, and ideally show them separately.

## 8. Test Yourself

**Q1.** A target's shares trade at $40.00 (unaffected). A buyer offers $51.00 per share. What is the control premium?

**Q2.** Why do bankers prefer the median over the mean when summarizing precedent deal multiples?

**Q3.** In the Beacon Logistics example, the sponsor deals showed lower premiums than the strategic deals. Name the paper that documents this pattern at scale, and state its headline finding in one sentence.

**Q4.** A banker shows you a prec table where every deal is from 2021, interest rates were near zero then, and the target is being valued today. What is the specific danger, and what would you ask the banker to do about it?

<details>
<summary>Answers</summary>

**A1.** (51.00 − 40.00) / 40.00 = 11.00 / 40.00 = **27.5%**.

**A2.** The mean is pulled around by outliers — one unusually rich or distressed deal distorts it. The median reflects the typical deal paid and is robust to the tails, which is what you want when the sample is small (often 5–10 deals).

**A3.** Bargeron, Schlingemann, Stulz, & Zutter (2008), *Why do private acquirers pay so little compared to public acquirers?*, Journal of Financial Economics. Headline: public targets receive roughly 63% higher premiums from public acquirers than from private equity buyers, and the gap is driven by the agency incentives of the bidder's managers.

**A4.** The 2021 multiples embed a near-zero-rate financing environment — cheap debt inflated what buyers could pay. Applied to today's higher-rate world, they overstate achievable value. Ask the banker to restrict the set to recent deals under comparable rate conditions, or to show the multiples alongside prevailing rates so you can judge the regime mismatch yourself.
</details>

---

*Next up: 06 | DCF Valuation I: UFCF and WACC — we stop asking what the market paid and start asking what the company's own cash flows are worth.*
