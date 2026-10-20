# 10 | The Football Field and Fairness Opinions

*You now have four ways to value a company — and they have never once agreed with each other. This is the part of the job where bankers stop arguing about which method is "right" and draw the picture that lets a board of directors make a decision anyway. The football field. And the legal reason the picture exists: the fairness opinion.*

> **Learning goals.** After this article you can: (1) explain what a football field chart is and why bankers build one; (2) construct a football field from trading comps, precedent transactions, a DCF, and an LBO; (3) read the chart the way a board does — ranges, medians, and what sits where relative to the offer; (4) explain what a fairness opinion is, why boards ask for one, what it certifies, and where its conflicts live.
>
> **Prerequisites.** Articles 04–09 (the four valuation methods and merger math). This article is the capstone of the valuation section — it uses all of them.

## 1. Four methods, four answers — now what?

Think back over what you've built in this series. In article 04 you valued companies off what the market pays today (trading comps). In 05, off what buyers actually paid in control deals (precedent transactions). In 06–07, off the company's own cash flows discounted back to the present (DCF). In 08, off what a leveraged buyer could afford to pay and still hit its return target (LBO). In 09, you modeled what happens to earnings when two companies merge.

Now put yourself in the chair of a director of Northline Industrial — the fictional distributor from article 09, where Crestfield offered **$20 per share** in cash. You are a fiduciary. Shareholders' money is on the line. You have to vote yes or no on the deal, and your bankers hand you four valuations:

- Trading comps say roughly $17–$21.
- Precedent transactions say roughly $21–$26.
- The DCF says roughly $16–$21.
- The LBO says a financial buyer tops out around $18–$20.

So which one is "the value"?

The honest answer, the one every banker knows but clients don't always want to hear: **none of them, and all of them.** Each method measures something different. Trading comps measure what minority shareholders will pay *today, for no control*. Precedent transactions measure what acquirers paid *in the past, for control*. The DCF measures what the company's cash flows are worth *on their own, forever*. The LBO measures what a *leveraged buyer* can pay *and still earn its target return*. These aren't four guesses at one number — they're four different questions with four different answers, and a board needs all of them.

The football field is how bankers present that fact without it looking like a mess.

## 2. Anatomy of the chart

A **football field chart** is a horizontal bar chart. Each row is one valuation methodology; each bar shows the *range* of implied value per share (sometimes per enterprise value); dots or markers show the median or mean of each range. There's usually a vertical line for the offer price and a context bar for the stock's 52-week trading range. It looks like yard lines on a football field — hence the name.

Three things make it more than decoration:

**First, it forces ranges, not points.** Bankers who work in point estimates are either selling something or haven't finished the analysis. The bar is the analysis: a comps range of $17–$21 tells the board that the method's answer depends on which peers you weight and which multiple you pick. Anyone can fake precision; ranges admit the uncertainty honestly.

**Second, medians anchor the eye.** On each bar, bankers mark the median (sometimes the mean). When the board looks at the chart, it compares the *offer* to the *medians*, not just whether the offer touches some bar's edge. An offer that falls inside every bar's range but below every median is a very different story than one that clears most medians.

**Third, the footnotes carry the real content.** A football field without footnotes is a cartoon. Each bar rests on assumptions — which peers, which multiple, what WACC, what exit multiple, what synergies were excluded. The chart is the cover page; the footnotes are the book. When a banker says "per our analysis," everything that matters lives in the small print.

And here's the subtle thing the chart is doing politically: it lets the board show it did its homework. The football field is not just analysis — it's *evidence of a process*. That distinction is about to matter a great deal.

## 3. Building one: Northline's football field

Let's build the chart for Northline, the company Crestfield offered $20/share for. Recap from article 09: 42 million shares, EBITDA $120m, net debt $60m.

### Trading comps

Comparable industrial distributors trade at **6.5x–8.0x EV/EBITDA**, median 7.25x:

| Multiple | Implied EV | Less: net debt | Implied equity | ÷ 42m shares |
|---|---|---|---|---|
| 6.5x | $780m | $60m | $720m | **$17.14** |
| 7.25x (median) | $870m | $60m | $810m | **$19.29** |
| 8.0x | $960m | $60m | $900m | **$21.43** |

Bar: **$17.15–$21.45**, median $19.30.

### Precedent transactions

Recent control deals in the sector closed at **8.0x–9.5x EBITDA**, median 8.75x. (Remember article 05: these prices include control premiums, so they should sit above trading comps — and they do.)

| Multiple | Implied EV | Implied equity | Per share |
|---|---|---|---|
| 8.0x | $960m | $900m | **$21.43** |
| 8.75x (median) | $1,050m | $990m | **$23.57** |
| 9.5x | $1,140m | $1,080m | **$25.71** |

Bar: **$21.45–$25.70**, median $23.55.

### DCF

From article 09's numbers: EBIT $90m, tax 25%, D&A $30m, capex $35m, working-capital build $5m. Year-one unlevered free cash flow:

```math
UFCF_1 = EBIT(1-t) + D&A - \text{capex} - \Delta NWC
       = 90 \times 0.75 + 30 - 35 - 5
       = \$57.5m
```

Grow UFCF at 5% for five years, WACC 10%, terminal growth 2.5%:

| Year | UFCF | Discount factor @10% | PV |
|---|---|---|---|
| 1 | $57.50m | 1.1000 | $52.27m |
| 2 | $60.38m | 1.2100 | $49.90m |
| 3 | $63.39m | 1.3310 | $47.62m |
| 4 | $66.56m | 1.4641 | $45.46m |
| 5 | $69.89m | 1.6105 | $43.39m |
| **PV of UFCF** | | | **$238.65m** |

```math
TV_5 = \frac{UFCF_5 \times (1+g)}{WACC - g} = \frac{69.89 \times 1.025}{0.10 - 0.025} = \$955.2m
```

```math
PV(TV) = \frac{955.2}{1.6105} = \$593.1m
```

```math
EV = 238.65 + 593.1 = \$831.8m \;\;\to\;\; \text{equity } \$771.8m \;\;\to\;\; \textbf{\$18.38/share}
```

Sensitivity — WACC 9.5–10.5%, terminal growth 2–3% — gives a range of **$16.30–$21.10**, centered on **$18.40**. (Article 07 warned you the terminal value does most of the work: here it's $593m of $832m, about 71%. That hasn't changed.)

### LBO analysis

A sponsor pays 7.5x EBITDA ($900m EV), funds it with 4.5x EBITDA of debt ($540m), and writes a $360m equity check. In five years EBITDA grows at 5% to ~$153m; exiting at 8.0x gives $1,225m EV; $190m of debt is paid down, leaving $875m of equity. The implied return on the $360m check:

```math
IRR = \left(\frac{875}{360}\right)^{1/5} - 1 \approx 19.4\%
```

Just below a 20% hurdle. So at a 20% target return, the sponsor tops out around **$19.80/share**. Sensitivity over entry multiples 7.0x–7.5x gives the bar: **$18.00–$19.80**.

### The chart

```
                        $14        $18        $22        $26
                         |          |          |          |
52-wk range        |------*---------------------|
                   13.50      19.20
Trading comps             |-----●---------|
                        17.15  19.30   21.45
Precedent txns                        |-----●---------|
                                    21.45  23.55   25.70
DCF                       |------●------------|
                        16.30   18.40     21.10
LBO                          |--●------|
                             18.00 19.00 19.80
                                                    |
                                                 $20.00 offer
```

Read it like a director. The $20 offer sits: inside the comps range (above its median), inside the DCF range (above its center), just above the LBO ceiling — and *below* the entire precedent-transactions bar. That's a rich but defensible price: a strategic buyer like Crestfield, with synergies the LBO buyer doesn't have, can pay more than a sponsor. It's exactly the kind of marginal case where the board wants professional cover for saying yes. Which is why the fairness opinion exists.

## 4. How bankers actually use the football field

A few things worth knowing about how this chart functions in practice, beyond the mechanics:

**Bankers don't average the bars.** You'll sometimes hear people ask for "the average of the four methods." Nobody serious does this. The methods measure different things (see section 1); averaging them is like averaging the temperature, the humidity, and the wind speed and calling it "the weather." The board looks at where the offer sits relative to each bar and decides whether the *pattern* supports the deal.

**Weighting is judgment, not math.** In a strategic sale with real synergies, bankers quietly weight precedent transactions and the DCF with synergies more heavily — the buyer is paying for control and for the combination, so the standalone trading comps matter less. In a take-private, the LBO bar is the binding constraint: if the offer exceeds what a sponsor can pay, the sponsor universe is out, and that's the whole story. The chart presents; the banker interprets.

**It sets the negotiation anchors.** On the sell side, the banker points at the precedent-transactions median ($23.55) and argues the buyer should pay up toward it. The buyer points at the DCF center ($18.40) and argues the company is worth its standalone cash flows plus a modest premium. The $20 offer is, visibly, a compromise between those anchors. The football field doesn't resolve the negotiation — it *structures* it, by making both sides' reference points explicit and hard to move.

**The 52-week range is context, not valuation.** It's on every football field, and it matters for one reason: it shows the premium relative to what shareholders could actually have sold for. At $20 against an unaffected price of $18, the premium is 11% — modest, and the board will have to explain why it sold for 11% when precedent deals in the sector paid 30–40% premiums. (The honest answer: Northline's growth is slower than those targets', its margins thinner. Whether the board believes that is the entire ballgame.)

## 5. Why the fairness opinion exists: the board's legal problem

Now the other half of this article. When Northline's board votes on the $20 offer, the directors aren't just making a business call — they're taking on *personal legal risk*. Directors owe shareholders fiduciary duties: the **duty of loyalty** (no self-dealing) and the **duty of care** (make informed decisions). Get the process wrong, and shareholders can sue the directors personally.

The case that made every board in America nervous is *Smith v. Van Gorkom*, 488 A.2d 858 (Del. 1985). The Trans Union board approved the sale of the company at $55 per share after a two-hour meeting, with no prior notice of the meeting's purpose, no review of the merger agreement, no valuation study — and no fairness opinion. The Delaware Supreme Court held the directors **grossly negligent**, stripped them of business-judgment-rule protection, and exposed them to personal liability. The court was blunt: a premium over market price is not, by itself, evidence that a price is fair.

A year later, *Revlon, Inc. v. MacAndrews & Forbes Holdings*, 506 A.2d 173 (Del. 1986), sharpened the point: once the sale of the company becomes inevitable, the board's duty narrows to getting the best price reasonably available for shareholders.

The fairness opinion is the market's answer to this legal environment. The board hires an investment bank to analyze the deal and deliver a formal opinion that the consideration is **"fair, from a financial point of view."** The phrase is doing enormous work — we'll take it apart in the next section. But the function is clear: it is an independent professional's documented judgment, built on the valuation analyses this series has been teaching you, that the price falls within a defensible range. It doesn't make the deal good. It makes the *process* defensible. Under Delaware law (DGCL §141(e)), directors are protected when they rely in good faith on experts selected with reasonable care. The fairness opinion is the expert reliance, in writing, with footnotes.

## 6. What the opinion says — and what it carefully doesn't

A real fairness opinion letter is a masterpiece of precision. Here's what it actually certifies, and the equal number of things it disclaims.

**What it says:** based on the analyses described (trading comps, precedent transactions, DCF, sometimes LBO and accretion/dilution), the consideration to be received by shareholders is fair, from a financial point of view. The opinion includes the valuation work — often the football field itself, plus pages of assumptions — as its evidentiary base.

**What it doesn't say** — read the disclaimers, they're the most honest part:

- It does **not** say the price is the *best* price, or the highest price obtainable. "Fair" means within a reasonable range, not optimal. A $20 offer can be fair even if $22 was theoretically achievable.
- It does **not** opine on the strategic merits of the deal, or whether the board should do it at all. The opinion addresses the financial terms only — not the wisdom of selling.
- It does **not** independently verify the inputs. The bank relies on management's projections, public filings, and the deal terms as given. If management's forecast was rosy, the DCF inside the opinion is rosy too. FINRA Rule 5150 actually requires the opinion to disclose whether the bank independently verified key information — and the standard answer, disclosed in plain text, is that it did not.
- It is addressed to the **board**, not the shareholders — though shareholders read it in the proxy statement. It assumes the deal closes as described, with no material changes.
- It is dated. It speaks as of the opinion date, on the information available then. Markets move; the opinion doesn't update itself.

The three levels from this series apply perfectly here. The *intuition* (an outside expert checked the price against standard valuation methods and it falls in range) is solid. The *strict conclusions* (the analyses, the medians, the sensitivity tables) are the non-negotiable part — they have to be real work. The *judgment calls* (which peers, what WACC, whether to include the LBO) are where the opinion's honesty lives or dies — and where its conflicts live, too.

## 7. The uncomfortable part: who pays for the opinion

Now the part bankers discuss quietly. In the overwhelming majority of deals, the bank rendering the fairness opinion is **the same bank advising on the deal** — and its advisory fee is **contingent on the deal closing**. Read that again: the expert certifying that the price is fair gets paid millions only if the board approves the price as fair. The conflict is structural, not personal, and everyone in the room knows it.

The industry has layered defenses over this conflict:

- **Fairness committees.** Most banks require the opinion to be reviewed and approved by an internal committee including senior bankers *not* on the deal team — people with no fee riding on the outcome. It's a real check, though an internal one.
- **Disclosure rules.** FINRA Rule 5150 (effective 2007) requires the opinion to disclose, in writing: whether the bank acted as advisor and whether its compensation is contingent on closing; any other significant contingent compensation; material relationships with the deal parties over the past two years; whether key information was independently verified; and whether a fairness committee approved the opinion. The conflicts aren't hidden — they're printed in the proxy for every shareholder to read. Whether shareholders read them is another question.
- **Independent second opinions.** Sometimes a board hires a second bank purely for the opinion, with a fixed (non-contingent) fee. It's the gold standard and it's rare, because it costs real money for what amounts to insurance.

Does any of this make the opinions *wrong*? The academic evidence is genuinely mixed, and it's worth knowing. Kisgen, Qian, and Song (2009), in "Are fairness opinions fair? The case of mergers and acquisitions" (*Journal of Financial Economics*, vol. 91(2), pp. 179–207), studied over a decade of deals (1994–2003): 80% of targets and 37% of acquirers obtained opinions. For **targets**, the opinion didn't change deal outcomes at all — premiums were the same with or without one. For **acquirers**, premiums were *lower* when they got an opinion — but the market reacted 2.3% *worse* to those deals, especially at high premiums. Investors, in other words, treated the acquirer's fairness opinion as a signal that management needed cover for an expensive deal. The opinion didn't certify value to the market; the market read it as a warning.

That's the deepest irony in this article: the document exists to reassure, and sophisticated readers treat it as a reason to worry. Both reactions are rational. The opinion is evidence of a careful process *and* evidence that the process needed documenting. Like a prenup: it doesn't mean the marriage is bad, but nobody signs one by accident.

## 8. Reading a fairness opinion like a banker

If you ever read a real one (they're exhibits to every merger proxy statement on EDGAR — free, public, and excellent study material), read it in this order:

1. **The valuation ranges table first.** Find the low–high for each method and the medians. Ask: does the offer clear the medians, or just touch the ranges? In Northline's case, $20 clears comps and DCF but not precedent medians — that's the whole debate in one glance.
2. **The assumptions second.** Which peers were included or excluded? What WACC and terminal growth? What exit multiple? The assumptions section is where an opinion is won or lost — a DCF with a 7% WACC and 4% terminal growth will bless almost any price.
3. **The disclaimers third.** Non-verification of projections, no view on strategic merits, no "best price" claim. Know exactly what wasn't promised.
4. **The conflicts disclosure last.** Contingent fee? Staple financing offered to bidders? (That's when the sell-side bank also offers to finance the buyers — the most conflicted arrangement in M&A, disclosed under Rule 5150.) Past-two-years relationships? Read it, then re-read the valuation with it in mind.

The pattern to internalize: **the opinion's conclusion is one sentence; its credibility is in the hundred pages behind it.** Bankers who do this work well obsess over the hundred pages. The sentence takes care of itself.

---

## Common Misconceptions

- **"A fairness opinion means the price is the best price."** No. It means the price falls within a defensible range of fair value. Best price is a process question (did the board shop the company? run an auction? — that's article 11's territory), not something an opinion can certify after the fact.
- **"The football field proves what the company is worth."** It proves what four methods imply under stated assumptions. Change the WACC by a point, swap two peers, pick a different exit multiple, and the bars move. The chart is a disciplined argument, not a measurement.
- **"Fairness opinions are rubber stamps because the bank is conflicted."** The conflict is real and disclosed, but the work behind a major opinion is genuinely rigorous — dozens of bankers, committee review, and every number exposed in a public filing where plaintiffs' lawyers will read it. The incentive to do sloppy work is low; the incentive to choose *favorable assumptions within defensible bounds* is the thing to watch.
- **"If the DCF says $18.40 and the offer is $20, the buyer overpaid."** The DCF values the company standalone, without synergies and without control. A strategic buyer isn't buying the standalone company — it's buying the combination. Overpayment is judged against what the buyer *gets* (article 09's accretion math, article 12's synergy math), not against the standalone DCF.
- **"Boards get fairness opinions because the law requires them."** No statute requires one. Boards get them because *Van Gorkom* showed what happens to directors who approve a sale without documented, expert-backed analysis. It's risk management, not compliance.

## Test Yourself

**Q1.** Northline's board is shown the football field above. The offer is $20. A director asks: "It's below the precedent-transactions median of $23.55 — should we reject it?" Give the banker's answer.
*A1. Not on that basis alone. Precedent medians reflect past control deals for (presumably) faster-growing or higher-margin targets; Northline's own DCF centers on $18.40 and comps on $19.30, and no sponsor can pay $20 at a 20% IRR — so $20 is full relative to standalone value and the financial-buyer universe. The right question is whether a credible higher strategic bidder exists (go-shop? auction? — article 11), not whether past deals paid more for different companies.*

**Q2.** A fairness opinion states the $20 consideration is "fair, from a financial point of view." List three things this sentence does NOT promise.
*A2. Any three of: (a) it is not the best/highest achievable price; (b) no view on whether the board should sell at all (strategic merits); (c) the bank did not independently verify management's projections; (d) it speaks only as of the opinion date; (e) it is addressed to the board, not a recommendation to shareholders on how to vote.*

**Q3.** Why might an acquirer's stock fall *more* on announcement when the acquirer obtained a fairness opinion? (Hint: Kisgen, Qian & Song 2009.)
*A3. Investors read the opinion as a signal that management anticipates skepticism — the board felt it needed professional cover, which suggests the premium is high or the strategic case is weak. Empirically, acquirers with opinions paid lower premiums but suffered 2.3% worse announcement returns, concentrated in high-premium deals: the market treats the opinion as a warning, not a certification.*

**Q4.** A bank is advising the seller, will earn a $12m fee contingent on closing, and also offers staple financing to the bidders. Which disclosures does FINRA Rule 5150 require in its fairness opinion?
*A4. That it acted as financial advisor and its compensation is contingent on completion; any other significant contingent compensation (including the staple financing economics if contingent on the deal); material relationships with transaction parties over the past two years; whether key supplied information was independently verified; whether a fairness committee approved the opinion; and whether it opines on insider compensation fairness.*

---

*Next up — **11 | Sell-Side M&A: From Mandate to Close**: the auction process, the CIM, management presentations, and how the football field becomes a negotiating weapon.*
