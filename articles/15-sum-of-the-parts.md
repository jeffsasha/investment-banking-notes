# 15 | Sum-of-the-Parts Valuation: Valuing a Conglomerate Piece by Piece

*If a company is really three companies wearing a trench coat, why would you value it as one?*

> **Learning goals:** By the end of this article you will be able to (1) explain why a single trading multiple misprices a diversified company, (2) build a sum-of-the-parts (SOTP) valuation from segment financials, (3) bridge from segment values to an implied share price, and (4) explain the conglomerate discount — and why it is not always a bargain signal.
>
> **Prerequisites:** Articles 03 (the EV–equity bridge), 04 (trading multiples), and 06 (DCF basics). You should be comfortable with EV/EBITDA and with the idea that enterprise value belongs to all capital providers, while equity value belongs to shareholders alone.

## 1. The problem with valuing a conglomerate as one company

Picture a company that makes industrial pumps, owns a consumer snack brand, and runs a trucking fleet. A single EV/EBITDA multiple for this company is an average of three different businesses — and averages lie. The snack brand might deserve 12x because branded consumer businesses grow steadily and throw off cash. The trucking fleet might deserve 7x because it is capital-intensive and cyclical. Blend them into one 9x and you have priced a company that does not exist.

This is not a theoretical worry. It is the daily reality of covering conglomerates, holding companies, and any business with segments in different industries. Analysts who cover these names do not have one comps set; they have one comps set *per segment*. Sum-of-the-parts is simply that practice, formalized: value each piece with the tools that fit that piece, then add the pieces up.

The intuition is the same one behind the old saying that a portfolio is worth the sum of its holdings. If you owned the three businesses separately, in three separate listed stocks, the market would price each one on its own merits. SOTP asks: what would this company be worth if the market did that — and then, crucially, what does the gap between that number and the actual share price tell you?

There is a catch, and it is the most interesting part of this article. Most of the time, the SOTP value is *higher* than the market price. The market applies a discount to the bundle. That discount has a name — the conglomerate discount — and forty years of research argues about whether it is real, why it exists, and whether it is an opportunity. We will get there. First, the mechanics.

## 2. The SOTP recipe

A SOTP valuation has five steps. None of them is exotic; you have met all of them in earlier articles. What is new is only the assembly.

**Step 1: Split the company into segments.** Use the segment reporting in the annual report — the same segments management uses to run the business. This is usually clean: companies must disclose segment revenue and operating profit. Segment EBITDA sometimes has to be reconstructed by adding back segment depreciation, which is disclosed in the segment notes.

**Step 2: Value each segment.** Pick the right tool per segment. A mature, profitable segment gets a trading multiple (EV/EBITDA from its own pure-play peers, per Article 04). A fast-growing or unusual segment might get a DCF (Article 06). A segment that is really a pile of assets — a real estate portfolio, say — might get valued on asset value. The point is that each segment is judged against *its own* industry, not the conglomerate's blended average.

**Step 3: Subtract corporate overhead.** Here is the step beginners forget, and it is worth real money. The headquarters is not free. The CEO's office, the central finance team, the listing costs — these cost money every year, and a buyer of the whole company inherits them. The standard treatment is to capitalize annual corporate costs at a multiple (often 8–10x, roughly the blended multiple of the segments) and subtract that from the sum of segment values. Ignore this and you overstate value by hundreds of millions on a large company.

**Step 4: Bridge to equity value.** This is the Article 03 bridge, applied once to the total: subtract net debt, subtract minority interests (the part of subsidiaries the parent does not own), subtract pension deficits and other debt-like items, add non-operating assets like surplus cash or a standalone investment portfolio.

**Step 5: Divide by shares outstanding, and compare.** The result is an implied share price. Compare it to the market price. The gap is the implied conglomerate discount (or, occasionally, premium).

In formula form, with one line per step:

```math
\text{Enterprise Value} = \sum_i (\text{Segment EBITDA}_i \times \text{Segment Multiple}_i) - \text{Capitalized Corporate Costs}
```

```math
\text{Equity Value} = \text{Enterprise Value} - \text{Net Debt} - \text{Minority Interests} - \text{Other Debt-Like Items}
```

```math
\text{Implied Share Price} = \frac{\text{Equity Value}}{\text{Shares Outstanding}}
```

```math
\text{Conglomerate Discount} = \frac{\text{SOTP Equity Value} - \text{Market Capitalization}}{\text{SOTP Equity Value}}
```

That is the whole machine. Now let us run it.

## 3. Worked example: Meridian Group

Meridian Group is fictional, but the numbers are deliberately ordinary — the kind you would see in a real SOTP note. Meridian has three segments, 200 million shares outstanding, and a current share price of $23.00 (a market capitalization of $4,600 million).

### Segment values

| Segment | EBITDA ($m) | Peer EV/EBITDA | Segment EV ($m) |
|---|---:|---:|---:|
| Industrial equipment | 420 | 9.0x | 3,780 |
| Consumer brands | 260 | 12.0x | 3,120 |
| Logistics services | 180 | 7.0x | 1,260 |
| **Total** | **860** | — | **8,160** |

Check the arithmetic: 420 × 9 = 3,780; 260 × 12 = 3,120; 180 × 7 = 1,260; and 3,780 + 3,120 + 1,260 = 8,160. Note what the blended multiple would have been: 8,160 ÷ 860 = 9.5x. If you had slapped a single 9.5x on the whole company you would have landed in the same place *this time* — but only by accident, and you would have learned nothing about which segment drives the value. The consumer brands segment is 30% of EBITDA but 38% of value (3,120 ÷ 8,160). That is exactly the kind of insight SOTP exists to produce.

### Corporate overhead

Meridian's headquarters costs $60 million a year. Capitalized at 10x — a round number near the blended multiple — that is a $600 million deduction. This is not a plug; it is the present value, in rough form, of paying for a headquarters forever. (A purist would DCF the cost stream; at a 10% discount rate with no growth, the value of $60 million a year forever is $60m ÷ 10% = $600 million. Same answer, which is reassuring.)

### The bridge to equity value

| Item | $m |
|---|---:|
| Sum of segment enterprise values | 8,160 |
| Less: capitalized corporate costs | (600) |
| **Enterprise value** | **7,560** |
| Less: net debt | (1,900) |
| Less: minority interests | (240) |
| Less: pension deficit | (120) |
| **Equity value** | **5,300** |
| Shares outstanding (m) | 200 |
| **Implied share price** | **$26.50** |

So SOTP says Meridian is worth $26.50 a share. The market says $23.00. The implied upside is ($26.50 − $23.00) ÷ $23.00 = 15.2%. And the implied conglomerate discount is ($5,300m − $4,600m) ÷ $5,300m = 13.2%.

That 13.2% is not a coincidence I engineered for narrative effect — well, it is, but it lands exactly where the academic literature says it should. Berger and Ofek (1995) estimated the value loss from diversification at 13–15% over their 1986–91 sample, and Lang and Stulz (1994) found diversified firms trading below equivalent portfolios of specialized firms throughout the 1980s. The market's discount on Meridian is, to a first approximation, the textbook discount.

### Sensitivity: what actually moves the answer

A valuation is only as honest as its sensitivities. Two quick ones:

- **If the industrial multiple is 8.0x instead of 9.0x**, segment value falls by 420 × 1 = $420 million, equity value falls to $4,880 million, and the implied price drops to $24.40 — still above the market price, but the upside shrinks from 15.2% to 6.1%. One turn of multiple on one segment eats more than half the thesis.
- **If logistics is 6.0x instead of 7.0x**, equity value falls by $180 million to $5,120 million, or $25.60 a share.

The lesson: SOTP concentrates your risk in your multiple choices. A DCF has dozens of assumptions to hide behind; a SOTP has one multiple per segment, and each one is doing enormous work. Choose them from real peer sets (Article 04), not from vibes.

## 4. The conglomerate discount: bargain, or fair price?

Here is where SOTP gets philosophically interesting. If the parts are worth more than the whole, why doesn't someone buy the whole, break it up, and pocket the difference? Sometimes they do — that is the entire logic of the break-up activist and the spin-off. But the discount usually persists, and the research suggests several honest reasons why:

**Inefficient internal capital markets.** Inside a conglomerate, headquarters allocates capital between segments. Berger and Ofek (1995) found that diversified firms overinvest in segments with poor opportunities — the strong segments subsidize the weak ones. A standalone snack company would never fund a struggling trucking fleet; a conglomerate does it routinely, because the cash is already inside the building. The discount, on this view, is the market pricing in future misallocation.

**Complexity and opacity.** A conglomerate is harder to analyze than a pure play. Fewer analysts cover it well, its reporting is harder to parse, and investors who want snack exposure cannot buy just the snack segment. Complexity demands a discount, the same way an illiquid stock does.

**Agency costs.** Running an empire is more fun than running one business. The classic agency story — Jensen (1986), from Article 08 — says managers with free cash flow prefer to build empires rather than return cash. Diversification is one way to spend it.

But — and this is the part that keeps the debate alive — the discount is not always real. Later work showed that part of the measured discount comes from *selection*: companies that diversify by acquisition tend to buy businesses that were already trading at a discount before they were acquired. The conglomerate did not destroy the value; it bought discounted value and inherited the measurement. And in some settings — emerging markets with weak external capital markets, or genuinely synergistic combinations — diversification creates value rather than destroying it.

For a banker, the practical takeaway is not to pick a side in the academic debate. It is this: **a SOTP discount is a starting point for a question, not an answer.** If your SOTP says 15% upside, your next question must be: *why* does the market disagree, and is the reason fixable? If the answer is "the market is wrong," you need evidence. If the answer is "a spin-off would fix it," you have just found yourself an M&A idea — which is why SOTP shows up in almost every activist and break-up pitch book.

## 5. Where SOTP breaks

SOTP is powerful precisely because it is simple, and simple tools break in predictable ways. Watch for these:

**Shared costs allocated arbitrarily.** Segment profit in annual reports is after an allocation of shared costs — IT, procurement, brand spending. If headquarters allocates costs to make a weak segment look better, your segment EBITDA is wrong, and so is everything built on it. Always ask how costs are allocated, and whether the allocation would survive a separation.

**Inter-segment sales.** If the industrial segment sells pumps to the logistics segment at a friendly internal price, both segments' profits are distorted. A SOTP on reported segment numbers inherits the distortion. In a real break-up analysis, bankers restate inter-segment sales at arm's-length prices.

**Sum-of-the-parts is not break-up value.** SOTP values the segments as if they were standalone listed companies. An actual break-up also pays taxes on asset sales, separation costs, stranded headquarters costs (you cannot fire the whole HQ on day one), and dis-synergies — the purchasing power or shared customers that disappear when the segments split. Break-up value is almost always below SOTP value. Conflating the two is the single most expensive mistake in this whole topic.

**The holding-company discount on top.** For holding companies that own listed stakes, the market often applies an *additional* discount to the value of the stakes themselves (a "holdco discount" of 10–30% is common), on top of any segment-level discount. If your SOTP values a stake at its market price and then you apply no holdco discount, you will overstate value relative to how the market actually prices holdcos.

## Common Misconceptions

**"SOTP proves the stock is undervalued."** No. SOTP proves the parts *would be worth more if valued like peers*. The market may have good reasons for the discount — misallocation, complexity, agency costs. The SOTP gap is a hypothesis, and it needs a catalyst (a spin-off, an activist, a divestiture) before it becomes a return. Without a catalyst, a discount can persist for a decade. Value traps wear this costume often.

**"The conglomerate discount means diversification is always bad."** The evidence is about averages, and averages hide enormous variation. Related diversification (segments that share customers, technology, or distribution) shows a much smaller discount than unrelated diversification in Berger and Ofek's own results. And some conglomerates — the ones with disciplined capital allocation — trade at premiums. The discount is a warning about governance, not a law of physics.

**"You can just add up the segment DCFs."** You can, but you must then also value corporate costs as a negative DCF, and you must use a different discount rate per segment — a snack brand and a trucking fleet do not share a cost of capital. Using one WACC for all segments (Article 06) reintroduces exactly the blending error SOTP was supposed to fix.

**"Corporate overhead is small, so ignore it."** On Meridian it was $600 million — 11% of equity value. On a real conglomerate with a heavy headquarters, it can be larger than the smallest segment. Ignoring it is how SOTP notes quietly overstate value by double digits.

## Test Yourself

**1.** A conglomerate has two segments: A with EBITDA of $500m valued at 10x, and B with EBITDA of $300m valued at 6x. Corporate costs are $40m a year, capitalized at 10x. Net debt is $1,000m and there are 100m shares. What is the implied share price?

*Answer: Segment values: A = $5,000m, B = $1,800m, total $6,800m. Less corporate $400m → EV $6,400m. Less net debt $1,000m → equity $5,400m. ÷ 100m shares = $54.00.*

**2.** The stock in Question 1 actually trades at $45.00. What is the implied conglomerate discount?

*Answer: Market cap = $45 × 100m = $4,500m. Discount = ($5,400m − $4,500m) ÷ $5,400m = 16.7%.*

**3.** Why is break-up value typically lower than SOTP value? Name at least two reasons.

*Answer: Any two of: taxes on asset sales or separation, separation and restructuring costs, stranded corporate costs that cannot be eliminated immediately, and lost synergies (shared purchasing, customers, distribution) that disappear when segments split.*

**4.** A conglomerate's SOTP value is 20% above its market price, and it has been for five years. Give one reason this might be a value trap rather than a bargain.

*Answer: The discount may reflect real, persistent problems — e.g., an internal capital market that keeps funding a weak segment, or governance that investors do not trust — with no catalyst (spin-off, activist, divestiture) on the horizon to close the gap. A discount without a catalyst is not a return.*

## References

- Berger, P. & Ofek, E. (1995). "Diversification's Effect on Firm Value." *Journal of Financial Economics*, 37(1). — The SOTP method itself: value each segment as if standalone, compare to the actual firm, and find a 13–15% average value loss from diversification.
- Lang, L. & Stulz, R. (1994). "Tobin's Q, Corporate Diversification, and Firm Performance." *Journal of Political Economy*, 102(6). — Diversified firms have lower q than equivalent portfolios of specialized firms.
- Jensen, M. (1986). "Agency Costs of Free Cash Flow, Corporate Finance, and Takeovers." *American Economic Review*, 76(2). — The agency-cost logic behind empire-building and the discount.

---

*Next up: 16 | Distressed DCF: Valuing Companies That Might Not Survive — what changes when survival itself is uncertain.*
