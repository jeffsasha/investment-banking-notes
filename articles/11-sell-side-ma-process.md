# 11 | Sell-Side M&A: From Mandate to Close

*You spend ten articles learning how to value a company, and then the sell-side assignment arrives: don't just value it — get someone to pay more than your valuation says it's worth. This is where the math meets the marketplace: the actual playbook bankers run, from the day the mandate is signed to the day the wires clear.*

> **Learning goals.** After this article you can: (1) describe the sell-side M&A process end to end — mandate, buyers list, NDA, teaser, CIM, IOIs, management presentations, final bids, purchase agreement, closing; (2) explain when bankers run an auction versus a negotiated sale, and what the evidence says about which gets higher prices; (3) read a Confidential Information Memorandum the way a bidder does, including the adjusted-EBITDA walk; (4) explain how deal protections (no-shop/go-shop, matching rights, termination fees) and closing mechanics (shareholder vote, antitrust review, funds flow) work; (5) compute banker fees, bid premiums, and termination fees on a worked example.
>
> **Prerequisites.** Articles 04–10 (all four valuation methods, the football field, and the merger math in 09). The football field from article 10 is a sell-side weapon — this article shows you how bankers wield it.

## 1. What a sell-side banker is actually selling

When a company hires an investment bank on the sell side, the mandate letter says "provide financial advisory services in connection with a potential sale of the company." Read it the way a banker does: the client is not buying advice. The client is buying *competition*.

A sell-side banker's job is to manufacture the maximum number of informed, motivated buyers, give them all the same deadline, and let the desire to win do the pricing. The CIM and the data room and the process letter are just the machinery. The product is the auction itself.

The banker gets paid almost entirely on success. A typical sell-side fee is a percentage of deal value — often on a sliding scale like the old Lehman formula (5% of the first $1 million, 4% of the second, 3% of the third, 2% of the fourth, 1% of everything above), which on a large deal works out to roughly 0.5–1.5% of enterprise or equity value. The key feature: the fee is *contingent on closing*. That aligns the banker with the seller on getting the deal done — and creates the conflicts from article 10, because a banker paid only if the deal closes has an incentive to favor *a* deal over the *best* deal.

One more definition before we start, because it organizes everything: **strategic buyers** versus **financial buyers**. A strategic buyer is an operating company in the industry — it pays for the target partly with *synergies* (cost savings, cross-selling, pricing power), which is why strategics can usually pay more. A financial buyer is typically a private equity firm — it pays based on what the business can support in debt and still earn its return target (that's your LBO from article 08).

## 2. The first decision: auction or negotiation?

Before anything is written, the banker and the board choose the sale method, and there are really only two: a **broad auction** (contact many potential buyers, run a formal multi-round process) or a **negotiated sale** (talk to one bidder, or a small handful, privately).

The naive intuition is that auctions always get higher prices — more bidders, more competition, higher price. That's the classic auction-theory result (Bulow and Klemperer, 1996): an extra bidder is worth more than any amount of negotiating skill.

But the data is more interesting than the theory. Boone and Mulherin (2007) dug into the actual private sale process behind hundreds of deals — the SEC filings that describe who was contacted and when — and found that **roughly half of firms are sold through auctions and half through one-on-one negotiations**, with *similar* bid premiums in both groups. Targets, it seems, choose the method that fits their situation, and choose well.

Why would a board ever choose a negotiation? Three honest reasons: **confidentiality** (a broad auction exposes your financials to competitors, and a failed auction damages the company), **deal complexity** (bespoke terms like earnouts and carve-outs don't fit standardized auction formats), and **the preemptive bid** (a single bidder who moves fast and bids high can *deter* competition — why would a rival spend millions on diligence if the first bidder already offered a full price?).

That last point is formalized in a lovely paper: Aktas, de Bodt, and Roll (2010) show that in negotiated deals, the *threat* of an auction — latent competition, the possibility that the seller could shop the deal — pushes the negotiated bidder to pay up. The competition doesn't have to be real to be effective. It just has to be credible.

**The working rule:** auction when the asset is broadly attractive and easy to understand; negotiate when the buyer universe is naturally small, confidentiality is paramount, or one bidder's synergies dwarf everyone else's. In practice, most sell-side processes are limited auctions — 10–15 hand-picked parties — wearing the word "auction" like a tailored suit.

## 3. Designing the process: the buyers list

Once the method is chosen, the banker builds the buyers list — and this is where industry knowledge is the entire job. The list typically runs 30–100 names, split into strategics and financials, and each name needs a thesis: *why would this specific buyer pay more than the others?* A strategic consolidating a fragmented market pays for market share. A PE firm that already owns a platform in the space pays for the add-on that doubles its platform's EBITDA (and its exit multiple — the multiple arbitrage from article 08).

The banker also thinks about who *not* to call. Direct competitors get the teaser last, with the thinnest information, because the risk is that they learn your margins and walk away. Buyers who can't finance the deal are worse than useless; they burn weeks and leak the process.

Before any outreach, the banker and the company align on valuation expectations using — you guessed it — the football field from article 10. The board needs to know what "a good outcome" looks like before the first bid arrives, because once bids are on the table, anchoring takes over and everyone forgets the pre-process view.

## 4. The documents that run the auction

A sell-side process runs on four documents, each with a specific job:

**The NDA (non-disclosure agreement).** Signed before any buyer sees anything real. The key term bankers fight over: the standstill provision — the buyer agrees not to buy the company's stock in the open market or launch a hostile bid for 12–24 months. This is what keeps an auction from turning into a raid.

**The teaser.** A one- to two-page anonymous profile — "Leading Southeast distributor of industrial fasteners, $180m revenue, 14% EBITDA margins" — with no company name. Its job is to get a signed NDA back, nothing more. Good teasers are specific enough to excite the right buyers and vague enough that nobody can identify the company. (Everyone in the industry figures it out anyway.)

**The CIM (Confidential Information Memorandum).** The main event — 50 to 100+ pages describing the business, the market, the financials, and the projections. Only signed-NDA parties get it. Section 5 below is about reading it like a bidder, because the CIM is where sell-side storytelling meets buy-side skepticism.

**The process letter.** The rules of the game, sent with the CIM. It sets the deadlines, the bid format, and what the seller expects to see (price, form of consideration, financing sources, key conditions). The process letter is how the banker keeps two dozen independent companies marching to the same timetable. Miss the deadline without a good excuse, and you're out — the threat has to be real for it to work.

## 5. Reading the CIM like a bidder

Open a CIM and you'll find the same architecture every time: business overview, industry and market, operations, management team, historical financials, and — the pages everyone actually reads — the projections and the adjusted EBITDA walk.

**Adjusted EBITDA** deserves a careful look, because this is where the seller's story lives or dies. Reported EBITDA gets "adjusted" for items the seller argues a buyer shouldn't count: above-market owner compensation, one-time legal settlements, the costs of a closed facility, "run-rate" savings from initiatives already underway. Each adjustment makes EBITDA bigger and the multiple look cheaper. Bidders re-underwrite each one: *is this truly one-time, or is it the kind of "one-time" charge this company takes every eighteen months?*

The classic sell-side trick is the **hockey-stick projection** — flat history followed by growth that bends sharply upward, always justified by initiatives conveniently just beginning. Every bidder knows the trick. Every CIM does it anyway, because the CIM's job isn't to be believed — it's to frame the negotiation. The bidder builds its own model (articles 06–08), but it builds it *starting from the seller's numbers*, which is a head start for the seller.

One more CIM feature: the **quality of earnings report**, usually prepared by the seller's accounting firm — an independent scrub of revenue recognition, working capital, and those EBITDA adjustments. Sellers commission it because it pre-answers the questions that kill deals late: nothing derails a closing like discovering in week nine that receivables were overstated.

## 6. Round one: indications of interest

By the process letter's deadline, interested buyers submit **IOIs — indications of interest**: non-binding letters stating a valuation range, the form of consideration, financing sources, and key conditions. "Non-binding" is doing a lot of work in that sentence — an IOI is legally worthless and strategically essential. It's the first time anyone puts a number on paper.

The banker then does the most judgment-heavy part of the job: **the shortlist**. From, say, 25 IOIs, the banker and the board pick 5–8 parties to invite to management presentations. Price matters most, but it's not the only thing. A top-of-range IOI from a buyer with no financing lined up and a history of retrading (lowering the price late in the process) loses to a slightly lower bid from a buyer who will actually close. Certainty of close is a real variable with a real price.

## 7. Management presentations and the data room

Shortlisted bidders get a day with management, and the keys to the **data room** — a secure online repository with contracts, financial detail, HR data, litigation files, everything diligence requires.

The management presentation is theater with a purpose. The CEO tells the growth story; the CFO walks through the numbers. Bidders watch for two things beyond the slides: does management believe its own projections, and does it want to stay after the deal? For PE buyers, management's willingness to roll over equity alongside the buyer is diligence you can't buy — nobody knows the warts better than the people running the business.

Meanwhile the data room is where deals quietly live or die. Bidders' advisors crawl through thousands of documents looking for the thing that changes the price: customer concentration, pending litigation, change-of-control clauses that let key contracts terminate on a sale, environmental liabilities at the old plant. The banker's job during diligence is triage — surface issues early and frame them before the bidder's advisors do. A surprise discovered by the buyer costs twice what a disclosed issue costs: once in the price, once in trust.

## 8. Final bids and the purchase agreement

The process letter's second deadline brings **final bids**: binding (or nearly binding) offers with a marked-up **purchase agreement** attached. The terms that move value:

- **Representations and warranties** — the seller's promises about the business (financials are accurate, no undisclosed liabilities, taxes paid). Broader reps mean more risk stays with the seller after closing.
- **Indemnification and escrows** — if a rep proves false, who pays? Typically 5–15% of deal value sits in escrow for 12–24 months as security.
- **The MAC clause (material adverse change)** — the buyer's walk-away right if the business deteriorates between signing and closing. Its exact wording is negotiated like a separate deal: narrow definitions favor the seller, broad ones favor the buyer.
- **Earnouts and contingent consideration** — part of the price paid later, only if targets are hit. Earnouts bridge valuation gaps: the seller believes the hockey stick, the buyer doesn't, so the seller gets paid extra *if the stick materializes*. Elegant in theory; the leading cause of post-closing litigation in practice.

The banker builds a **bid comparison matrix**: price per share, enterprise value, premium to unaffected price, form of consideration, financing certainty, escrow size, MAC breadth, closing timeline, regulatory risk. The board doesn't pick the highest number — it picks the best risk-adjusted outcome. This matrix, plus the football field showing where each bid sits against the valuation ranges, is the board book for the decision meeting.

## 9. The fine print that decides deals: protections and the go-shop

Between signing and closing, the seller's shareholders haven't voted yet — and another buyer could appear with a better offer. **Deal protections** manage this window: the signed buyer wants certainty its deal won't be jumped; the board needs to preserve its fiduciary ability to take a better deal if one appears.

- **No-shop clause.** After signing, the seller agrees not to *actively solicit* other bids. Standard — and it cannot override the board's fiduciary duty to consider an unsolicited superior offer.
- **Go-shop provision.** For 30–60 days after signing, the seller may *actively* shop the signed deal. Common in PE-backed take-privates. If nobody tops the signed price, that's strong evidence the price was fair — which is exactly why boards like having it in the record.
- **Matching rights.** If a topping bid appears, the original buyer gets a few business days to match it before the board can change its recommendation. Each round grinds the price upward — or exhausts the interloper.
- **Termination (break) fees.** If the seller walks to take a better deal, it pays the jilted buyer — typically 2–3% of equity value. Big enough to compensate wasted costs and deter frivolous deal-jumping; small enough that a genuinely better offer still goes through. (The worked example below shows the calibration.)
- **Reverse termination fees.** The mirror image: if the *buyer* walks away (usually because its financing falls through), it pays the seller — often 3–6%+, especially in LBOs where the financing risk sits with the buyer.

Notice the economics: every protection has a price, and the price is denominated in the seller's optionality. A tighter no-shop with a bigger break fee gets you a higher signed price (the buyer pays for certainty); a go-shop with a small fee preserves optionality but the buyer shades its bid down. There's no free certainty — just certainty someone paid for.

## 10. Closing: votes, regulators, and the funds flow

Signing is not closing. Between the two — typically 2–6 months — three gates have to clear:

1. **The shareholder vote.** For a public company sale, shareholders vote, and the proxy statement they receive includes the background of the merger — a narrative, extracted from board minutes, describing every contact, every bid, every negotiation. (This is the document Boone and Mulherin mined for their research, and it's the single best public source for learning how real processes run.)
2. **Regulatory approvals.** In the US, **Hart-Scott-Rodino (HSR) antitrust** filing is the standard gate — deals above the statutory threshold (adjusted annually; roughly $120m+ in recent years) must wait out a 30-day review period. Cross-border deals add foreign investment reviews (CFIUS in the US for sensitive sectors). Bankers assess this risk during the process — a bid that's 5% higher but carries a 12-month antitrust fight often loses to the clean bid.
3. **Financing.** The buyer's lenders finalize debt commitments — its own parallel process with its own drama, and the reason reverse termination fees exist.

Then **closing day**: the funds flow. Purchase price wires from buyer to the paying agent; the paying agent distributes to shareholders; option and RSU holders get cashed out; escrow funds move to the escrow agent; the banker's success fee wires to the bank; old debt gets repaid and liens released. Dozens of wire transfers, choreographed by lawyers, landing within hours. When people say "the deal closed," this — money actually moving — is what they mean.

## 11. Worked example: selling Northline Industrial

Let's put numbers on the whole machine. Recall Northline Industrial from articles 09–10: the fictional distributor, Crestfield's $20/share cash offer on the table, trading comps at $17–$21, precedent transactions at $21–$26, DCF at $16–$21, LBO capacity at $18–$20.

The board hires a banker on a Lehman-scale fee and runs a limited auction. Twenty-eight parties sign NDAs; sixteen submit IOIs; six make the shortlist; four submit final bids. The bids (enterprise value):

| Bidder | Type | EV bid | Equity value¹ | $/share² |
|---|---|---|---|---|
| Crestfield (original) | Strategic | $255m | $235m | $20.00 |
| Bidder B | Strategic | $270m | $250m | $21.28 |
| Bidder C | Financial (PE) | $248m | $228m | $19.40 |
| Bidder D | Strategic | $262m | $242m | $20.60 |

¹ Net debt of $20m deducted from EV. ² 11.75m fully diluted shares outstanding.

**Step 1: premiums.** Northline's unaffected price (before deal rumors) was $17.00. Bidder B's $21.28 implies a premium of:

```math
\text{Premium} = \frac{21.28 - 17.00}{17.00} = \frac{4.28}{17.00} = 25.2\%
```

A 25% premium sits squarely in the normal range for control transactions (article 05's precedent transactions cluster around 20–40%). Note how the football field frames this: $21.28 lands at the top of trading comps, the middle of precedent transactions, and above the LBO's max — exactly the picture the banker wants the board to see.

**Step 2: the banker's fee.** The winning equity value is $250m. On the Lehman scale:

```math
\begin{aligned}
\text{First \$1m} &: 5\% \times 1 = \$50{,}000 \\
\text{Second \$1m} &: 4\% \times 1 = \$40{,}000 \\
\text{Third \$1m} &: 3\% \times 1 = \$30{,}000 \\
\text{Fourth \$1m} &: 2\% \times 1 = \$20{,}000 \\
\text{Remaining \$246m} &: 1\% \times 246 = \$2{,}460{,}000 \\
\hline
\text{Total fee} &= \$2{,}600{,}000
\end{aligned}
```

$2.6m on $250m of equity value — about **1.04%**. Now the alignment question: the fee difference between Bidder B ($250m) and Bidder D ($242m) is 1% of the $8m gap, or $80,000, while the *shareholders'* difference is $8m. The banker is paid to close, not to squeeze the last dollar — which is why the board, not the banker, makes the final call.

**Step 3: the termination fee.** Set at 3% of equity value:

```math
\text{Break fee} = 3\% \times \$250\text{m} = \$7.5\text{m}
```

If a topping bidder appears during the go-shop at $22.00/share ($258.5m equity value), the interloper must cover the $7.5m fee — effectively paying $266m, or $22.64/share, to beat Bidder B. The fee does its job: topping bids have to be *meaningfully* better, not just technically better.

**Step 4: the decision.** The board picks Bidder B: highest price, all-cash, committed financing, narrow MAC, 45-day go-shop with the 3% fee. Bidder D was close on price but wanted 15% of consideration in its own stock — and the board didn't want Northline's shareholders holding the acquirer's paper. Price is 60% of the decision. The other 40% is everything in sections 8–10.

## Common Misconceptions

**"The highest bid always wins."** No — the best *risk-adjusted* bid wins. A $21 bid with committed financing, a narrow MAC, and a clean antitrust profile beats a $22 bid funded by "highly confident" letters, a broad MAC, and a 12-month regulatory fight. Boards are fiduciaries; certainty of close is part of value.

**"Auctions always produce higher prices than negotiations."** The evidence says otherwise. Boone and Mulherin (2007) find similar premiums across the two methods — targets self-select the right method, and a negotiation conducted under the *threat* of an auction (Aktas, de Bodt, and Roll, 2010) carries competitive pressure without the auction's costs. The method is a tactic, not a religion.

**"The CIM's projections are the banker's valuation."** The CIM is a marketing document wearing a valuation's clothes. Its projections anchor the negotiation, but every serious bidder rebuilds the model from scratch — which is why articles 04–08 taught you to build your own.

**"Once the deal is signed, it's done."** Signing starts the most fragile phase. Shareholder votes fail, regulators block, financing collapses, MAC clauses get invoked. The break fee, the go-shop, the HSR filing — the whole apparatus of sections 9–10 exists because a signed deal is a promise, and promises need enforcement mechanics.

**"The banker works for the shareholders."** The banker is hired by the board and paid a success fee contingent on closing. The banker's incentives *mostly* align with getting a good price, but "mostly" is doing heavy lifting in that sentence. Read the proxy's fee disclosures. They're there for a reason.

## Test Yourself

**Q1.** A target with an unaffected price of $40 receives final bids of $48 (strategic, all-cash, committed financing), $50 (PE, subject to financing, broad MAC clause), and $49 (strategic, 50% stock). Which bid should the board prefer, and what besides price should the bid matrix capture?

*A1. Not automatically the $50. The $48 all-cash bid with committed financing offers the highest certainty of close; the $50 bid's financing contingency and broad MAC mean the premium may never materialize — and a failed deal leaves the target damaged. The $49 half-stock bid exposes shareholders to the acquirer's share price. The matrix should capture consideration form, financing certainty, MAC breadth, escrow terms, regulatory risk, and closing timeline — price is necessary but not sufficient.*

**Q2.** Why might a board rationally choose a negotiation over a broad auction? Cite the evidence.

*A2. Confidentiality (a broad auction exposes financials to competitors, and a failed auction damages the company), deal complexity (bespoke terms like earnouts don't fit standardized formats), and preemptive bidding (a fast, full-price bid deters rivals from spending on diligence). Boone and Mulherin (2007) find roughly half of firms are sold via negotiation with similar premiums across methods — targets self-select optimally. Aktas, de Bodt, and Roll (2010) add that latent competition — the credible threat of an auction — pushes negotiated bidders to pay up.*

**Q3.** A deal with $400m equity value has a 3% seller termination fee. A topping bidder offers $415m during the go-shop. Does the topping bid clearly win? Show the math.

*A3. Not clearly. The break fee is 3% × $400m = $12m, payable by the seller if it takes the topping bid — so the interloper's effective cost is $427m, a 6.75% premium over the signed price, not 3.75%. The board must also weigh the original buyer's matching rights and the topping bidder's certainty of close. The fee is calibrated exactly for this: painful enough to deter frivolous jumps, small enough that a genuinely superior bid still clears it.*

**Q4.** In the Northline worked example, the banker's fee on the winning $250m bid was $2.6m. Suppose Bidder D at $242m equity value had instead bid $252m — $2m above Bidder B — but with 15% stock consideration and a financing condition. How much extra would the banker earn on D's bid, and why might the board still choose B?

*A4. The banker's incremental fee is roughly 1% × $2m = $20,000 — trivial. The board might still choose Bidder B because B's bid is all-cash with committed financing: shareholders get $21.28 in cash with near-certain close, versus $21.45 partly in acquirer stock subject to financing risk. This is the contingent-fee conflict in miniature — the banker's economics barely distinguish the bids, so the board must.*

---

*Next up — **12 | Buy-Side M&A: Synergies and Deal Structures**: how acquirers decide what a target is worth to them, synergy math, and cash vs. stock.*

**Papers cited in this article** (all verified before writing — title, authors, year, journal):
- Boone, A. L. & Mulherin, J. H. (2007). *How Are Firms Sold?* Journal of Finance, 62, 847–875. — Half of firms sell via auction, half via negotiation; premiums are similar across methods.
- Aktas, N., de Bodt, E. & Roll, R. (2010). *Negotiations Under the Threat of an Auction.* Journal of Financial Economics, 98, 241–255. — Latent competition raises premiums in negotiated deals.
