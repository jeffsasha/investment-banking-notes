# 32 | Earnouts and Contingent Consideration: Paying for the Future

*Article 31 was about the price that changes hands at closing. This one is about the price that doesn't — the part of the deal that is promised today and paid later, only if the business does what the seller says it will do. If you have ever watched a buyer and a seller argue over a valuation until the deal nearly dies, you have watched the exact problem an earnout was invented to solve.*

> **Learning goals.** After this article you can: (1) explain what an earnout is and why it exists — the valuation gap between a buyer who doubts the forecast and a seller who believes it; (2) name the four design choices in any earnout contract and explain what each one controls; (3) value an earnout with probability-weighted scenarios and a discount rate, and explain why that discount rate should be higher than the WACC; (4) spot the "cliff" problem in a payout schedule and fix it with a linear tier; (5) explain how contingent consideration is accounted for under ASC 805 and why that accounting creates earnings volatility; (6) name the two agency problems earnouts create even as they solve the valuation problem.
>
> **Prerequisites.** Article 03 (enterprise value vs equity value) for what the headline price means; article 06 (DCF I) for how a forecast becomes a value; article 09 (accretion/dilution) for how the form of payment changes a deal; article 11 (sell-side M&A) for where the purchase agreement sits in the process; article 31 (purchase price adjustment) for the other half of "the price is not the price."

## 1. The Valuation Gap That Kills Deals

Every deal dies the same way: the buyer and the seller agree on the business and disagree on the future. The seller's founder has spent ten years building a company and believes next year's EBITDA will be $30 million. The buyer has spent ten weeks in diligence and believes it will be $20 million. At a 10x EBITDA multiple, the seller hears a $300 million company and the buyer hears a $200 million company. That is a $100 million gap, and no amount of dinner conversation closes it, because the gap is not about politeness. It is about information: the seller knows things the buyer cannot verify, and the buyer knows the seller has every incentive to be optimistic.

This is the classic **adverse selection** problem, and it is the reason so many private-company deals never happen. The seller cannot prove the forecast, the buyer cannot disprove it, and a single fixed price forces one side to eat the entire risk of being wrong. If the buyer pays $300 million and the forecast was fantasy, the buyer overpaid by $100 million. If the seller accepts $200 million and the forecast was real, the seller gave away $100 million.

An **earnout** — also called **contingent consideration** — breaks this deadlock by making the price depend on the future that is actually delivered. Instead of arguing about what next year's EBITDA *will* be, the two sides agree on what they will pay *if* it is $20 million, *if* it is $25 million, and *if* it is $30 million. The buyer pays a lower price up front, and the seller earns the rest by hitting the numbers it claimed it would hit. The argument about the future is replaced by a bet on it — and a bet both sides can sign, because each side is betting on its own belief.

The mechanism is older than the name. Earnouts show up in a small minority of deals overall — Cain, Denis, and Denis (2011) found them in about 4% of completed U.S. acquisitions in their 1994–2003 sample — but they cluster exactly where you would expect: private targets, young companies, businesses whose value lives in growth that has not happened yet.

## 2. Four Design Choices in Every Earnout

An earnout contract is not one clause; it is four decisions, and each one changes who bears what risk.

**Choice one: the metric.** What performance is measured? The most common choices are revenue and EBITDA, because both are hard to fake quickly and both are tied to value. But the menu is wider, and the choice matters enormously:

| Metric | What it rewards | What it invites |
|---|---|---|
| Revenue | Top-line growth, market share | Growth at any cost — including unprofitable growth |
| EBITDA | Operating performance | Arguments about what counts as an "add-back" |
| Net income | True bottom-line profit | Manipulation through depreciation, interest, and tax choices |
| Milestones | A drug approval, a contract win, a product launch | Binary outcomes — all or nothing on one event |
| Stock price (CVRs) | The acquirer's own share price | Market noise the target's managers cannot control |

Revenue is the simplest metric and the most dangerous one, because a manager chasing a revenue target can buy revenue: discount aggressively, sign unprofitable customers, stuff the channel. EBITDA is the workhorse, but it invites a different fight — over the definition. Is the earnout measured on EBITDA *before* the buyer's corporate overhead allocations, or after? Is the earnout measured on the target as a stand-alone business, or as part of the combined company? Article 31's lesson applies here with full force: the definition is the deal.

**Choice two: the thresholds.** At what level of performance does payment start, and at what level is it capped? A typical structure has a floor (below this, nothing is paid), a target (at this, the full amount is paid), and sometimes a cap above the target. The floor protects the buyer from paying for mediocrity; the cap protects the buyer from paying an unlimited amount for a blowout year.

**Choice three: the payout shape.** Is the payment all-or-nothing at a threshold (a "cliff"), tiered in steps, or linear between the floor and the cap? This is where most earnouts go wrong, and section 4 is devoted to it.

**Choice four: the measurement period.** One year or three? A single year is easy to game — pull next year's sales into this year, delay this year's costs into next year. A longer period, or a cumulative target over several years, is harder to manipulate and measures something closer to real performance. Most earnouts run one to three years; longer than that, and the seller's managers have usually moved on and the incentive has gone cold.

## 3. Worked Example: Bridging a $100 Million Gap

Let us make the opening story concrete. A buyer and a seller are negotiating over a private company. The seller's forecast says next year's EBITDA will be $30 million; the buyer believes it will be $20 million. At 10x EBITDA, the seller's value is $300 million and the buyer's is $200 million.

They agree on this structure:

- **Up-front payment at closing:** $150 million in cash.
- **Earnout:** an additional payment one year after closing, based on that year's EBITDA:
  - Below $22 million: $0.
  - $22 million to $27 million: $30 million.
  - Above $27 million: $60 million.
- **Maximum total price:** $210 million.

Now value the earnout the way a banker would: with scenarios. Suppose the buyer's diligence team assigns probabilities to three outcomes:

| Next-year EBITDA | Probability | Earnout paid |
|---|---:|---:|
| $20 million | 40% | $0 |
| $25 million | 35% | $30 million |
| $30 million | 25% | $60 million |

The **expected earnout** is the probability-weighted average of the payouts:

```math
E[\text{earnout}] = 0.40 \times 0 + 0.35 \times 30 + 0.25 \times 60 = 0 + 10.5 + 15.0 = \$25.5\text{ million}
```

But $25.5 million is not what the earnout is worth today. It is a payment one year from now, and it is a risky payment — the buyer only pays it if the business performs. Risky future cash flows get discounted, and the right discount rate here is *higher* than the company's WACC, because the earnout is a levered claim on performance: it pays zero in the bad state and $60 million in the good state, which makes it more volatile than the business itself. Suppose the banker uses 12%:

```math
PV(\text{earnout}) = \frac{25.5}{1.12} = \$22.8\text{ million}
```

So the deal, in present-value terms, is:

```math
\text{Expected total consideration} = 150.0 + 22.8 = \$172.8\text{ million}
```

Now check the deal from both sides. The buyer believes the business is worth $200 million and expects to pay $172.8 million — a $27.2 million expected gain. The seller believes the business is worth $300 million, and if its own forecast comes true it receives $150 million plus $60 million, or $210 million — still below its $300 million ask, but $60 million better than the $150 million up-front payment alone. And note the discipline in the structure: the buyer only pays the full $210 million in the state of the world where EBITDA hits $30 million, which at 10x is a $300 million business. Even the maximum price is a bargain *in the state where it is paid*.

Two observations worth keeping. First, the earnout let the deal happen at all. Without it, the two sides were $100 million apart with no way to split the difference honestly. With it, each side is paid according to the future it believed in. Second, the maximum earnout — $60 million — is 29% of the maximum total price of $210 million. That lands right around the share that Barbopoulos and Danbolt (2021) associate with the best acquirer outcomes in their study of earnout-financed deals, where acquirers did best when the deferred payment was roughly 30% of deal value. Too small, and the earnout does not bridge the gap; too large, and the seller is effectively still the owner of a business it no longer controls.

## 4. Cliffs, Tiers, and the Perverse Incentive at the Edge

The example above has a flaw, and it is the flaw that causes the most earnout disputes in practice: the payout schedule has **cliffs**. Look at the boundary between the middle tier and the top tier. If EBITDA comes in at $26.9 million, the seller receives $30 million. If it comes in at $27.0 million, the seller receives $60 million. A $100,000 difference in EBITDA — a rounding error, a single invoice timed differently — is worth $30 million.

That is not a contract term. That is a loaded gun pointed at the accounting department. A seller's manager facing that cliff has an overwhelming incentive to find $100,000 of EBITDA before the measurement date: recognize revenue a week early, delay a marketing expense by a month, reclassify a cost as capital expenditure. A cliff turns the earnout period into a game of moving numbers across a line, and the line is worth thirty million dollars.

The fix is to make the payout **linear** between the floor and the cap, so that every dollar of performance is worth the same number of dollars of earnout. Replace the steps with a straight line: no payment below $22 million, the full $60 million at $30 million, and a proportional amount in between:

```math
\text{Earnout} = \$60\text{ million} \times \frac{\text{EBITDA} - 22}{30 - 22}, \quad \text{for EBITDA between \$22m and \$30m}
```

Now the numbers behave. At $25 million of EBITDA, the payout is $60 \times 3/8 = \$22.5$ million. At $26.9 million it is $60 \times 4.9/8 = \$36.75$ million, and at $27.0 million it is $60 \times 5/8 = \$37.5$ million. The $100,000 difference in EBITDA is now worth $750,000 — exactly proportionate, exactly as it should be. Nobody restructures a quarter's accounting for $750,000 the way they would for $30 million.

The lesson generalizes beyond earnouts. Anywhere a contract pays a large amount for crossing a threshold — a bonus, a vesting trigger, a covenant — the threshold creates an incentive to manage the number rather than the business. Linear schedules are boring, and boring is the point: they make the incentive to game the metric exactly as large as the metric itself, and no larger.

## 5. Valuing the Earnout: It Is an Option, Not a Promise

Section 3 valued the earnout by weighting scenarios and discounting. That is the workhorse method, and it is what most bankers actually do. But it is worth understanding what the earnout *is* in financial terms, because the intuition changes how you think about its risk.

An earnout is economically a **call option** on the target's future performance. The seller holds the right to receive a payment if performance exceeds a strike price (the threshold), and nothing if it does not. Like any option, its value rises with the volatility of the underlying performance: a business whose EBITDA could be $10 million or $40 million has a more valuable earnout than a business whose EBITDA will certainly be $25 million, even if the expected EBITDA is the same. That is why the discount rate in section 3 was 12%, above the WACC — the earnout is a riskier claim than the business's ordinary cash flows, and riskier claims get discounted harder.

Under U.S. GAAP — specifically ASC 805, the business-combination standard that replaced the old SFAS 141(R) in 2009 — contingent consideration must be measured at **fair value on the acquisition date** and recorded on the acquirer's balance sheet as part of the purchase price. Then, every quarter after that, the fair value is remeasured, and the change flows through the acquirer's earnings. If the target performs better than expected, the earnout liability grows, and the acquirer records a loss. Read that again: good news about the acquired business shows up as a loss on the acquirer's income statement. Cadman, Carrizosa, and Faurel (2014) studied this regime and found that the fair-value disclosures do contain real information about the economics of the deal — but the earnings volatility is real too, and it surprises first-time acquirers every time.

## 6. The Dark Side: Who Controls the Metric Controls the Money

Earnouts solve the valuation problem by tying payment to performance. But they create a new problem that is just as serious: after closing, the buyer controls the business, and the buyer also controls the number that determines how much it has to pay.

This is **moral hazard** in its purest form. The seller's managers have usually left, or are working for the buyer now. The buyer decides how corporate overhead is allocated to the acquired unit, when to recognize revenue, whether to invest in growth this year or next, and how aggressively to integrate the target into the parent. Every one of those decisions can move the earnout metric — and every one of them moves it in the direction that reduces what the buyer owes. The polite term for this is "sandbagging." The impolite term is what the seller's lawyers use in the dispute that follows.

The data says this is not a theoretical worry. Cain, Denis, and Denis (2011) found that earnout contracts are structured precisely to manage these agency problems: the size of the earnout, the choice of metric, and the length of the measurement period all vary systematically with how much the deal depends on the target managers' continued effort, and how hard their performance is to observe. No definition of EBITDA is airtight against a determined acquirer with control of the books — the contract can only do so much.

The practical protections are unglamorous and essential: define the metric like a lawyer, not like a banker — the agreement should specify the exact accounting policies, whether corporate overhead is allocated, and whether the target is measured stand-alone or as part of the combined company; keep the seller's people in the room, with their own compensation tied to the same metric; give the seller audit and dispute rights, including referral to an independent accountant, because without them the earnout is a promise the buyer grades itself; and keep the period short — a one-year earnout limits the buyer's window to move numbers around, while a three-year earnout gives it three years of control over the metric.

## 7. Earnouts as Retention: Paying the People, Not Just the Shares

There is a second reason earnouts exist, and it has nothing to do with valuation. In many private-company deals, the value of the target *is* its people: the founder who knows every customer, the engineers who built the product, the sales team with the relationships. Buy the shares without the people, and you have bought an empty office.

An earnout paid to the selling shareholders doubles as a retention mechanism, because the people who must deliver the performance are usually the same people who receive the payment. Kohers and Ang (2000), in the foundational study of earnouts, found that they serve two functions that are not mutually exclusive: reducing the risk of misvaluing a target with high information asymmetry, and retaining the target's human capital. In their sample, earnout payments were frequent, and a high share of target managers stayed beyond the earnout period — the contract did what it was designed to do.

This is why earnouts are common in exactly the industries where the people are the asset: professional services, software, healthcare, and biotech — and why the metric in those deals is often a milestone rather than a financial number, a drug approval or a key contract renewal, because the thing the buyer is really paying for is the team staying long enough to deliver it.

But notice the tension: the same earnout that retains the team gives the buyer an incentive to make the team fail — or at least, not to help it succeed — and gives the retained managers an incentive to maximize the metric over the earnout period at the expense of the business's long-term health. Cut R&D, slash marketing, defer maintenance, and let next year's manager deal with the consequences. An earnout aligns incentives for two or three years and misaligns them the day after it expires. Good bankers say that out loud before the client signs.

## 8. What the Research Says

Three findings from the academic literature are worth carrying into any negotiation:

**Earnouts are a response to uncertainty, not a sign of weakness.** Cain, Denis, and Denis (2011) — "Earnouts: A Study of Financial Contracting in Acquisition Agreements," *Journal of Accounting and Economics* — examined 990 acquisitions completed between 1994 and 2003 and showed that earnout terms vary systematically with valuation uncertainty and with the need to motivate target managers. Earnouts are not a fallback for deals that could not agree on price; they are the efficient contract when the price cannot be known yet.

**The two functions are real and separable.** Kohers and Ang (2000) — "Earnouts in Mergers: Agreeing to Disagree and Agreeing to Stay," *Journal of Business* — showed that earnouts both reduce misvaluation risk and retain human capital: target managers stay, and earnout payments are actually made. The title is the summary: the two sides agree to disagree about value, and agree to stay together long enough to find out who was right.

**Size matters, and around 30% looks like the sweet spot.** Barbopoulos and Danbolt (2021) — "The Real Effects of Earnout Contracts in M&As," *Journal of Financial Research* — found that acquirers of unlisted targets using earnouts gain more than those paying fully up front, and that acquirers realize the highest returns when the deferred payment is around 30% of deal value. Smaller, and the earnout is too small to discipline the disagreement; larger, and the seller retains too much exposure to a business it no longer runs.

One honest caveat: almost all of this research studies deals from the 1990s and 2000s, and the earnout market has changed since — particularly after the 2009 accounting reform made earnouts visible on the balance sheet. The findings are directionally reliable; the magnitudes should be treated as history, not as law.

## 9. Common Misconceptions

**"An earnout means the buyer and seller couldn't agree on price."**
They couldn't agree on the *future*, which is a different thing — and an honest thing. A fixed price in the face of genuine uncertainty is not agreement; it is one side surrendering. The earnout is what agreement looks like when the future is genuinely uncertain.

**"The earnout is free money for the buyer — it only pays if the business does well."**
It is not free. The seller accepts a lower up-front payment *because* of the earnout, and the earnout has a fair value on day one that sits on the balance sheet as a liability. A buyer who treats a $60 million maximum earnout as if it costs nothing has not read ASC 805.

**"Earnouts always align incentives."**
They align incentives over the measurement period and misalign them around its edges. The seller's managers will maximize the metric, not the business; the buyer will minimize the metric, not the business. Both sides are rational, both are doing what the contract pays them to do, and the business is the thing caught in the middle. Alignment is a design goal, not a property of the instrument.

**"A bigger earnout is always better for the buyer, because it means paying less up front."**
A bigger earnout means the seller keeps more exposure to the business after closing — and exposure without control breeds disputes. It also means a larger liability on the acquirer's balance sheet and more earnings volatility from remeasurement. Beyond roughly 30% of deal value, the research suggests the benefits start to reverse.

**"Revenue is the safest earnout metric because it's the hardest to manipulate."**
Revenue is the *easiest* metric to inflate without creating value: cut prices, offer generous payment terms, sign customers who will never pay. EBITDA is harder to game precisely because it nets out the costs of generating that revenue — which is why it is the standard, despite the definitional fights.

## 10. Test Yourself

**1. A buyer values a target at $180 million; the seller values it at $260 million. The buyer offers $150 million up front plus an earnout of up to $80 million, payable if the target hits its forecast EBITDA. The banker's probability-weighted expected earnout is $35 million, discounted at 10% over one year. What is the expected total consideration in present-value terms, and does the buyer expect to gain or lose relative to its own valuation?**

*Answer:* PV of the earnout = $35m / 1.10 = $31.8m. Expected total consideration = $150m + $31.8m = $181.8m. The buyer values the business at $180m, so on expectation it pays $1.8m *more* than its own valuation — either the up-front payment should come down, or the earnout thresholds should go up.

**2. An earnout pays $0 below $10 million of EBITDA, $20 million at $10 million or above, with no cap. Next year's EBITDA comes in at $9.9 million. What is the problem, and how would you fix the contract?**

*Answer:* The contract has a cliff: $100,000 of EBITDA is worth $20 million. The seller's managers have an enormous incentive to find $100,000 before the measurement date, and the buyer has the opposite incentive. Fix it with a linear payout — for example, $0 below $8 million, scaling linearly to $20 million at $12 million — so that each dollar of EBITDA is worth the same amount of earnout.

**3. The target beats its earnout forecast in the first year after closing. The acquirer records a loss on its income statement in the same quarter. Has something gone wrong?**

*Answer:* No — this is the accounting working as designed. Under ASC 805, the earnout is a liability measured at fair value. Better-than-expected performance increases the expected payout, which increases the liability, and the increase flows through earnings as a loss. It is counterintuitive but correct: the loss is the mirror image of the good news, not a separate problem.

**4. A founder is selling her software company and will stay on as CEO for two years. The buyer proposes an earnout based on revenue; the founder proposes one based on EBITDA. Who is right, and why might each side prefer its own metric?**

*Answer:* The founder's EBITDA metric is the better choice for the business, because revenue can be bought with discounts and unprofitable growth while EBITDA measures operating performance. The preferences are not accidental: the buyer may prefer revenue because it is simpler to measure and harder for the founder to manipulate through cost allocations. The metric should match what the buyer actually bought (profitable growth), defined precisely enough that neither side can move it without moving the business.

---

**Papers cited:** Kohers, N. & Ang, J. (2000). "Earnouts in Mergers: Agreeing to Disagree and Agreeing to Stay." *Journal of Business*, 73(3), 445–476. · Cain, M. D., Denis, D. J. & Denis, D. K. (2011). "Earnouts: A Study of Financial Contracting in Acquisition Agreements." *Journal of Accounting and Economics*, 51(1–2), 151–170. · Barbopoulos, L. G. & Danbolt, J. (2021). "The Real Effects of Earnout Contracts in M&As." *Journal of Financial Research*, 44(3), 607–639. · Cadman, B., Carrizosa, R. & Faurel, L. (2014). "Economic Determinants and Information Environment Effects of Earnouts: New Insights from SFAS 141(R)." *Journal of Accounting Research*, 52(1), 37–74.

*Next up: SPACs and the Blank-Check Boom — what happens when the deal itself goes public before it finds a target.*
