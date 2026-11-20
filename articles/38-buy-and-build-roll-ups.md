# 38 | Buy-and-Build: Roll-Up Strategies and the Art of Serial Acquisitions

*The first time I heard a private equity investor describe a roll-up, it sounded like a magic trick. You buy a company for five times its earnings. You buy three more just like it, also for five times. Then you sell the combined company for ten times its earnings — and you keep the difference. The same earnings, the same buildings, the same customers, suddenly worth twice as much. My first thought was that somebody was being fooled. My second thought was that I needed to understand exactly where the extra value comes from, because if it is real, it is one of the most reliable engines in private equity, and if it is not, it is one of the most reliable ways to lose money slowly. This article is the answer I wish I had had then.*

> **Learning goals.** After this article you can: (1) explain what a buy-and-build (or roll-up) strategy is, and why fragmented industries invite it; (2) define multiple arbitrage and compute it from entry and exit multiples; (3) build a simple platform-plus-add-ons model — entry price, financing, exit value, MOIC and IRR — and show where each dollar of value came from; (4) separate real synergies from spreadsheet synergies; (5) explain what the research says about serial acquirers, including why the evidence points in two directions at once; (6) name the five ways roll-ups die.
>
> **Prerequisites.** Article 03 (enterprise value vs equity value) for the EV/EBITDA multiple; article 04 (comps) for how multiples are set; article 08 (LBO) for sources and uses, MOIC and IRR; article 12 (buy-side M&A) for synergies and deal structure; article 25 (leveraged finance) for the debt that funds the add-ons.

## 1. The Idea in One Paragraph

A **buy-and-build** strategy — also called a **roll-up** — starts by buying one decent company in a fragmented industry, the **platform**. Then it buys several smaller competitors, the **add-ons**, and bolts them onto the platform. The combined company is bigger, grows faster, is more diversified, and is run by a professional management team — so when it is sold, buyers pay a higher multiple of EBITDA for it than the sponsor paid for the pieces. The profit comes from three places: the pieces were bought cheap, the combination is worth more than the sum of its parts, and the whole thing was partly bought with debt, which magnifies the equity return. That is the whole idea. Everything else in this article is about the conditions under which it is true, and the ways it falls apart.

A fragmented industry is the hunting ground: hundreds of small, local, owner-operated businesses doing roughly the same thing — commercial cleaning, pest control, dental practices, HVAC repair, veterinary clinics, funeral homes. No single player has more than a few percent of the market. The businesses are too small to hire a banker, too small to run a real auction, and usually owned by someone who wants to retire. That is not a coincidence. A roll-up only works where the targets are small, numerous, and similar enough that one playbook fits all of them.

## 2. Why Small Companies Sell Cheap

The multiple gap is the engine, so it is worth asking why it exists at all. If a small cleaning company earns $2 million of EBITDA, why does it sell for five times earnings when a $20 million cleaning company sells for ten times? Four reasons, none of them mysterious:

**Nobody is bidding.** A $10 million business does not get a banker-run auction with twenty buyers. It gets a phone call from one buyer, maybe two. A sale process with one bidder is not a market; it is a negotiation, and the buyer sets the price. Larger companies get real processes, and processes push multiples up.

**The earnings are fragile.** A small company's EBITDA often depends on one person — the founder who knows every customer by name. If they leave, some customers leave with them. A buyer discounts for that. The founder's salary is also often below market, or the books mix personal and business expenses, so the "EBITDA" being sold needs adjusting before it means anything. (Article 04 covered adjusted EBITDA; in a roll-up, this adjustment is where the first argument always starts.)

**Small means risky, in a measurable way.** A company with three customers and one city is one lost contract away from a bad year. A company with three thousand customers in twenty cities is not. Buyers pay less per dollar of earnings for a riskier stream of earnings. This is the same logic as article 06's discount rate, applied to a whole company: riskier cash flows, lower multiple.

**Small companies cannot borrow.** A $2 million-EBITDA business cannot raise institutional debt on its own. A $20 million platform can. Since the LBO math of article 08 depends on leverage, the platform can afford to pay more — and the add-on, bought with the platform's balance sheet, is suddenly financeable at a scale its own owner could never reach.

None of this is a market inefficiency in the textbook sense. It is the price of illiquidity, concentration, and key-person risk. The roll-up thesis is that those discounts shrink or disappear once the businesses are combined — and that the sponsor, not the original seller, captures the difference.

## 3. Multiple Arbitrage: The Engine

The core calculation is simple enough to do on a napkin. Suppose the platform trades at a multiple of $M_{platform}$ and an add-on is bought at $M_{addon}$, with $M_{platform} > M_{addon}$. The add-on has EBITDA of $E$. The sponsor pays $E \times M_{addon}$ for it. At exit, if the combined company sells at the platform multiple, that same EBITDA is worth $E \times M_{platform}$. The gain from re-rating alone is:

```math
Value from re-rating = E × (M_platform − M_addon)
```

A $2 million-EBITDA add-on bought at 5.0x costs $10 million. If the combined company exits at 10.0x, that $2 million of EBITDA is worth $20 million. The $10 million difference is **multiple arbitrage** — value created not by growing the business, but by changing the multiple the market applies to it.

Three things to notice before this starts looking like free money. First, the arbitrage is only realized at exit, and only if the buyer at exit actually pays the platform multiple. If the market cools, or if the combined company turns out to be less attractive than advertised, the exit multiple can be 8.0x or 7.0x, and the arbitrage shrinks or vanishes. Second, the add-on's EBITDA has to be real — adjusted, sustainable, and not inflated by a seller who cut maintenance spending for two years to dress up the numbers. Third, the sponsor pays transaction costs and integration costs to capture the gain, and those come straight out of it. The napkin math is the gross return. The net return is what matters, and we will compute it properly in the next section.

One more piece of intuition. Multiple arbitrage is just the comps logic of article 04, run in reverse. In article 04, we valued a company by applying its peers' multiple. In a roll-up, the sponsor *buys* at a low multiple and *sells* at the peers' multiple. The whole strategy is a bet that the multiple gap between small and large companies in this industry is durable — that it reflects something structural about size, not something temporary about the market.

## 4. The Worked Example: Beacon Building Services

Let us build the whole thing, with financing, because the equity return is what the sponsor actually cares about. **Beacon Building Services** is a fictional commercial cleaning company. All numbers are in millions of dollars.

**The platform.** Beacon earns $10m of EBITDA. The sponsor buys it at 8.0x EBITDA:

```math
Platform EV = $10m × 8.0 = $80m
```

**The add-ons.** Over the next two years, the sponsor buys three small regional cleaning companies. Each earns $2m of EBITDA and is bought at 5.0x:

```math
Each add-on EV = $2m × 5.0 = $10m
Total add-on EV = 3 × $10m = $30m
Total add-on EBITDA = 3 × $2m = $6m
```

**Entry position.** Combined enterprise value at entry is $80m + $30m = $110m. Combined EBITDA at entry is $10m + $6m = $16m. The blended entry multiple is therefore $110m / $16m = 6.875x — already below the platform's 8.0x, because the add-ons were bought cheaply.

**Synergies.** Combining the four companies allows real savings: one back office instead of four, one insurance policy, bulk purchasing of supplies, and denser cleaning routes so crews spend less time driving between sites. Management estimates $2m of annual run-rate cost synergies. Pro forma EBITDA is therefore $16m + $2m = $18m. Note what we are assuming here: that the synergies are real, that they survive contact with four different company cultures, and that they cost little to implement beyond what is already in the cash flow forecast. Section 5 comes back to this.

**The exit.** Four years after the platform purchase, the sponsor sells the combined company. It is now a $18m-EBITDA business with a regional footprint, a professional management team, and a growth record from acquisitions. Buyers pay a 10.0x platform multiple:

```math
Exit EV = $18m × 10.0 = $180m
```

**Where did the $70m of value creation come from?** Decompose it:

| Source of value | Calculation | Amount |
|---|---:|---:|
| Platform re-rating | $10m × (10.0 − 8.0) | $20m |
| Add-on re-rating (multiple arbitrage) | $6m × (10.0 − 5.0) | $30m |
| Synergies, valued at the exit multiple | $2m × 10.0 | $20m |
| **Total value creation** | | **$70m** |

Check: entry EV $110m + value creation $70m = $180m exit EV. The arithmetic closes, which is how you know the decomposition is complete. The biggest single source is the add-on re-rating — the multiple arbitrage — but the platform's own re-rating and the synergies are each material. A roll-up that depends on only one of the three is a fragile thesis.

**Financing and the equity return.** The entry is financed like an LBO (article 08): 50% debt, 50% equity.

| Sources | Amount |
|---|---:|
| Term loan | $55m |
| Sponsor equity | $55m |
| **Total sources** | **$110m** |

Over four years, the company's free cash flow — after interest, taxes, maintenance capex, and integration costs — pays down $5m of debt a year, so debt at exit is $55m − $20m = $35m. (This is an assumption, and a demanding one: it requires the business to actually generate that cash while integrating three acquisitions.)

```math
Exit equity value = Exit EV − Exit debt = $180m − $35m = $145m
MOIC = $145m / $55m = 2.64x
IRR = 2.64^(1/4) − 1 ≈ 27%
```

A 2.64x multiple of invested capital and roughly a 27% IRR over four years. That is the number that makes the strategy famous. Now the honest version — the counterfactuals, because the base case assumes everything goes right:

| Scenario | Exit EV | Exit equity | MOIC | IRR |
|---|---:|---:|---:|---:|
| Base case: exit at 10.0x, synergies achieved | $180m | $145m | 2.64x | ~27% |
| No re-rating: exit at 6.875x (blended entry multiple), synergies achieved | $123.75m | $88.75m | 1.61x | ~13% |
| No re-rating, no synergies: exit at 6.875x on $16m EBITDA | $110m | $75m | 1.36x | ~8% |

Check the middle row: $18m × 6.875 = $123.75m; minus $35m of debt is $88.75m; $88.75m / $55m = 1.61x. And the bottom row: $16m × 6.875 = $110m — exactly the entry EV, so the only equity gain is the $20m of debt paydown: $75m / $55m = 1.36x.

The lesson of the table is the whole article in miniature. The return is not driven by the business getting better. It is driven by the multiple going up and the synergies arriving. If neither happens, four years of work and three integrations produce an 8% IRR — worse than a boring index fund, with far more risk. The roll-up is a bet on the exit multiple. Everything else is execution.

## 5. Synergies: The Part That Has to Be True

Synergies are the most abused number in M&A, and roll-ups are where the abuse is most systematic, because every add-on comes with a synergy slide. Three kinds are real, and one test separates them from the rest.

**Cost synergies** are the most reliable: duplicate back offices, overlapping routes, combined purchasing. They are also the most limited — there is only one head office to eliminate, and after the first few add-ons, the savings per deal shrink. A sponsor that underwrites the same $2m of savings on the tenth add-on that it claimed on the first is double-counting.

**Revenue synergies** are the most exciting and the least reliable: cross-selling services to the other company's customers, winning national contracts that no single small player could bid for, raising prices on a larger customer base. They require customers to behave differently, which they may not. Bankers discount revenue synergies heavily, and you should too.

**Multiple synergies** are not synergies at all — they are the re-rating from section 3, and calling them synergies double-counts the same dollar. If you have already credited the add-on's EBITDA at the 10.0x exit multiple, you cannot also claim a synergy for it.

The test is simple: a real synergy is a change in how the combined company operates that a standalone company could not achieve, stated in dollars, with an owner and a date. "We will save $2m by consolidating four accounting teams into one by June of year two, and Sarah will run it" is a synergy. "We will benefit from scale" is a slogan. In diligence, ask for the slogan's phone number — who, specifically, will make it happen, and what happens to their bonus if it does not.

## 6. What the Research Says

Two papers frame the debate, and they point in different directions, which is itself informative.

**Fuller, Netter, and Stegemoller (2002)**, *"What Do Returns to Acquiring Firms Tell Us? Evidence from Firms That Make Many Acquisitions,"* Journal of Finance, studied the shareholders of firms that made five or more acquisitions within three years — 3,135 bids between 1990 and 2000. Their headline result is encouraging for the roll-up model: these frequent acquirers earned, on average, a positive announcement return of about 1.77% over a five-day window. But the average hides a sharp split: bidder shareholders *gained* when buying a private firm or a subsidiary, and *lost* when buying a public firm. The authors' explanation is the liquidity discount — private targets sell cheaply because they cannot be sold easily, and the buyer captures part of that discount. That is the same mechanism as section 2's multiple gap, observed in public-market data. It is also a warning: the roll-up advantage is specific to *private* targets. Buying public companies serially does not show the same benefit.

**Laamanen and Keil (2008)**, *"Performance of serial acquirers: Toward an acquisition program perspective,"* Strategic Management Journal, looked at the most active acquirers in seven US industry sectors in the 1990s and found the opposite pressure: both a *high rate* of acquisitions and a *high variability* of that rate were negatively related to performance over three years. Buying fast, and buying in bursts followed by pauses, hurt. The damage was smaller for larger acquirers, for more experienced ones, and for broader programs — size and experience moderate the harm, they do not remove it. But the same paper's longer-horizon robustness checks add a twist: the most frequent acquirers of all — those doing ten or more deals — earned median excess returns of about 12.6% a year, against −3.9% for firms doing four to nine deals.

Read together, the two papers describe a capability, not a free lunch. Buying private companies cheaply works; buying them *fast* and *erratically* does not. The acquirers that win are the ones that turn acquisition into a repeatable process — a steady pace, a fixed playbook, an integration team that has done it before — and the ones that lose are the ones that treat each deal as a one-off heroic effort. That is a management conclusion, not a valuation conclusion, and it is why section 7 matters as much as section 3.

## 7. How Roll-Ups Die

Roll-ups rarely die from one bad deal. They die from the accumulation of small failures that the model assumed away. The five usual causes:

**1. Integration indigestion.** Each add-on needs its systems merged, its staff reassigned, its customers reassured, its culture absorbed. An organization can integrate roughly one deal at a time well; two at once is hard; four at once is chaos. The symptom is always the same: the platform's organic growth stalls because management is busy integrating instead of running the business. The EBITDA that was supposed to grow, does not.

**2. Paying up.** The multiple gap exists because add-ons are bought quietly. Once a roll-up becomes known in an industry, every owner of a small cleaning company knows a buyer is coming, and the local banker starts running auctions. Add-on multiples drift from 5.0x to 6.5x to 8.0x, and the arbitrage narrows to nothing. The sponsor, committed to a growth story, keeps buying anyway. This is the most common way a good thesis becomes a bad investment: the price paid rises faster than the value created.

**3. Leverage.** Add-ons are often bought with incremental debt, and the debt stack grows with each deal. A business that was conservatively financed at the platform stage can be aggressively financed by the fifth add-on. Then one bad year — a lost contract, a recession — breaches a covenant, and the lenders, not the sponsor, decide what happens next. (Articles 25 and 37 cover the mechanics.)

**4. The exit multiple disappears.** The entire return rests on selling at 10.0x. If interest rates rise, if buyers cool on the sector, or if the market decides the combined company is just a collection of small companies stapled together, the exit multiple can be 7.0x — and the middle row of the section 4 table becomes the actual outcome. A roll-up is a leveraged bet on the M&A market staying open, and the M&A market does not stay open forever.

**5. The founder leaves, and the customers follow.** In owner-operated businesses, the seller *is* the relationship. The standard fix is an earnout or a retention agreement (article 32), but those only delay the problem. If the customers were loyal to a person rather than a brand, the EBITDA bought at 5.0x starts shrinking the day the founder's non-compete expires.

None of these is exotic. They are the ordinary frictions of buying and combining real businesses, and the base case in section 4 assumed every one of them away. That is why the counterfactual table exists.

## 8. Common Misconceptions

**"Multiple arbitrage is free money."** It is a bet, not a gift. It pays only if the exit multiple holds, the add-on's EBITDA is real, and the integration costs do not eat the gain. In the worked example, if the exit multiple is 6.875x instead of 10.0x, the IRR falls from ~27% to ~13% — and that assumes the synergies still arrive.

**"Bigger is always worth a higher multiple."** Size earns a higher multiple only when it brings something the market values: faster growth, diversification, lower risk, or better margins. A roll-up of five mediocre businesses is a bigger mediocre business, and buyers will price it that way. Growth by acquisition without improvement is just aggregation.

**"Serial acquirers always beat the market."** The research says the opposite about pace: Laamanen and Keil found that a high and variable acquisition rate *hurt* performance. The winners are not the fastest buyers; they are the most disciplined ones, with a steady rhythm and a repeatable integration playbook.

**"Synergies are guaranteed because the spreadsheet says so."** A synergy is a forecast about human behavior — that two teams will merge, that customers will accept a new price, that a founder will stay. Forecasts about human behavior deserve a discount, and revenue synergies deserve the largest discount of all.

**"Roll-ups work in any industry."** They work where targets are small, numerous, similar, and cheap — and where combining them actually changes something: purchasing power, route density, a national sales force. In industries where the product is bespoke, the customers are few, or the key asset walks out the door every evening, there is nothing to roll up.

## 9. Test Yourself

**1.** A platform earns $8m of EBITDA and is bought at 9.0x. An add-on earns $3m of EBITDA and is bought at 5.0x. There are no synergies and no growth. The combined company is sold at 10.0x. How much value is created by re-rating the add-on alone, and how much by re-rating the platform?

**2.** A sponsor buys a platform for $60m of enterprise value, funded with $30m of debt and $30m of equity. Three years later it sells for $90m, with debt paid down to $24m. What is the MOIC and the IRR?

**3.** Fuller, Netter, and Stegemoller (2002) found that frequent acquirers' shareholders gained when buying private firms or subsidiaries but lost when buying public firms. Why — what economic mechanism explains the difference?

**4.** A roll-up buys add-ons at 7.0x EBITDA when the platform trades at 8.0x, and pays integration costs equal to 1.0x the add-on's EBITDA on each deal. Before synergies, is the multiple arbitrage attractive? What would have to be true for the deal to make sense?

<details>
<summary>Answers</summary>

**1.** Add-on re-rating: $3m × (10.0 − 5.0) = **$15m**. Platform re-rating: $8m × (10.0 − 9.0) = **$8m**. Total re-rating value is $23m: check — entry EV is $72m + $15m = $87m, exit EV is $11m × 10.0 = $110m, and $110m − $87m = $23m. Notice the platform's re-rating is worth more than half as much as the add-on's, even though the platform was bought at a higher multiple — because the platform is bigger.

**2.** Exit equity = $90m − $24m = $66m. MOIC = $66m / $30m = **2.20x**. IRR = 2.20^(1/3) − 1 ≈ **30%** per year. Check: 1.30³ = 2.197, close enough to 2.20.

**3.** The **liquidity discount** (plus tax and control effects). Private firms and subsidiaries cannot be sold easily, face a thin market of buyers, and are usually sold without a competitive auction — so they change hands at a discount to comparable public companies. The buyer captures part of that discount as a gain. Public targets are auctioned, priced by the market, and often sold at a premium, so the buyer overpays on average. The mechanism is the same multiple gap from section 2, measured in announcement returns.

**4.** No — before synergies it is roughly breakeven. Per $1m of add-on EBITDA: the sponsor pays $7m and the stake is worth $8m at exit, a $1m gain; but integration costs of $1m wipe it out entirely, before counting transaction fees or the time value of money. For the deal to make sense, the sponsor needs real synergies worth more than the integration costs, a wider multiple gap than 7.0x versus 8.0x, or add-ons bought at a lower price. A narrow multiple gap plus real integration costs is how roll-ups quietly stop working.
</details>

---

*Next up: 39 | Take-Privates: When Public Companies Go Private — what changes when the target is listed, and why taking a company private is a different deal from buying a small private one.*
