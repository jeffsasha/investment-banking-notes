# 31 | The Purchase Price Adjustment: Working Capital, Net Debt, and What Actually Changes Hands at Close

*Every deal announcement has a headline number — "Acme agrees to be acquired for $500 million" — and every banker in the room knows that number is not what anyone actually pays. The headline is the enterprise value. The wire transfer at closing is something else entirely: the enterprise value, minus the debt, plus the cash, plus or minus the difference between the working capital the buyer actually receives and the working capital it was promised. This article is about that gap — the purchase price adjustment — because it is where a surprising number of deals quietly gain or lose millions, and where a surprising number of arguments start.*

> **Learning goals.** After this article you can: (1) explain why the announced price of a deal and the cash that changes hands at closing are different numbers, and walk through the bridge between them; (2) define "cash-free, debt-free" and say exactly what the buyer is — and is not — paying for; (3) define closing working capital the way a purchase agreement does, and explain why the definition matters more than the arithmetic; (4) explain how a target working capital "peg" is set, including seasonality; (5) work through a completion-accounts true-up and a locked-box deal with real numbers; (6) name the four places these adjustments most often turn into disputes.
>
> **Prerequisites.** Article 03 (enterprise value vs equity value) for the bridge this article makes real; article 06 (DCF I) for why value is struck on a cash-free, debt-free basis in the first place; article 11 (sell-side M&A) for where the purchase agreement sits in the deal process; article 25 (leveraged finance) for what counts as debt when a company is loaded with it.

## 1. The Headline Price Is Not the Price

Say a buyer agrees to pay $500 million for a company. What does that mean? To a banker, almost always, it means an **enterprise value** of $500 million: the value of the whole operating business, as if it had no cash and no debt. It is the number the valuation work supports — the DCF in article 06, the comps in article 04 — and it is the number that goes in the press release, because it is the cleanest statement of what the business itself is worth.

But nobody buys "the business as if it had no cash and no debt." They buy shares (or assets) of a real company, which on closing day will have some cash in its bank accounts, some debt outstanding, and some working capital sitting in receivables, inventory, and payables. So the price that actually changes hands is the **equity value**, and the bridge from one to the other is the whole subject of this article:

```math
\text{Equity value} = \text{Enterprise value} - \text{Debt} - \text{Debt-like items} + \text{Cash} + (\text{Closing working capital} - \text{Target working capital})
```

Every term in that formula is a negotiation. Every term has produced a lawsuit. The rest of this article takes them one at a time.

One point of intuition first, because it makes everything else click: the buyer is paying for the *engine* — the business that generates the cash flows the DCF valued. The engine needs a normal amount of fuel in the tank to run: that is working capital. It does not need the seller's cash (the seller keeps that), and it should not come saddled with the seller's debt (the seller repays that, or the buyer deducts it). So the deal is priced as if the tank were exactly at its normal level, the cash had already been taken out, and the debt had already been repaid — and then, at closing, the price is adjusted for whatever the tank actually contains.

## 2. Cash-Free, Debt-Free: What the Buyer Is Actually Buying

Most private-company deals are structured **cash-free, debt-free**. The phrase sounds like jargon, and it is, but it is precise jargon. It means:

- **Cash-free:** the seller keeps the company's cash. The buyer does not pay for it, and the buyer does not receive it.
- **Debt-free:** the seller's debt is repaid at or before closing, out of the purchase price. The buyer does not assume it.

Why structure it this way? Because it separates two questions that should never be mixed: *what is the business worth?* and *how is the company's balance sheet arranged today?* The business is worth its enterprise value whatever its cash balance happens to be this month. If the buyer paid for the cash too, then a seller who happened to have $20 million sitting in the bank would get $20 million more for the same business — which is obviously wrong, since that cash is just retained earnings the seller already owns. Cash-free, debt-free makes the price depend on the business, not on the balance sheet on a random Tuesday.

There are two traps here that catch first-timers.

**Trap one: "cash" is not whatever the bank statement says.** Cash that the business needs to operate — minimum balances, cash trapped in a foreign subsidiary that cannot be repatriated without a tax bill, restricted cash held as collateral — is not really the seller's to keep. Purchase agreements usually define cash to exclude these, or treat them as part of working capital instead. A dollar of cash sitting in a subsidiary in a country with capital controls is worth less than a dollar to the seller, and the definition has to say so.

**Trap two: "debt" is much wider than bank loans.** The purchase agreement defines "indebtedness," and the definition almost always reaches beyond the loans on the balance sheet. The usual suspects:

| Item | Why it counts as debt-like |
|---|---|
| Bank debt and drawn revolvers | The obvious one |
| Capital/finance leases | Economically debt, even if accountants call it a lease |
| Unpaid transaction fees (banker, lawyer, accountant) | The seller's cost of selling; the buyer should not fund it |
| Change-of-control payments to employees | Triggered by the deal itself |
| Underfunded pension obligations | A real claim on future cash |
| Deferred revenue (cash received for services not yet delivered) | The buyer inherits the obligation to do the work |
| Accrued income taxes through closing | The seller's tax bill for the period it owned the business |

Deferred revenue deserves a second look, because it surprises people. A software company that collects $12 million in annual subscriptions in January has $12 million of cash and a $12 million obligation to provide a year of service. If that cash went to the seller and the obligation went to the buyer, the buyer would be doing a year of work for free. So deferred revenue is typically treated as a debt-like item — deducted from the price — which is the buyer's compensation for taking on the work.

## 3. Working Capital: The Definition Is the Deal

**Working capital** is current assets minus current liabilities. That is the textbook definition, and in a purchase agreement it is almost never the definition used. The agreement's definition is narrower, because the whole point of the adjustment is to measure the *operating* working capital the buyer needs to run the business — not the financing items, which are handled separately by the cash and debt adjustments. If an item is counted in both places, someone gets paid twice; if it is counted in neither, someone pays for nothing.

A typical purchase-agreement definition looks like this:

| Included in working capital | Excluded (handled elsewhere) |
|---|---|
| Accounts receivable | Cash and cash equivalents |
| Inventory | Deferred tax assets |
| Prepaid expenses | Income tax receivable |
| Accounts payable | Debt and capital leases |
| Accrued expenses (suppliers, utilities) | Deferred tax liabilities |
| Accrued payroll and bonuses | Income taxes payable |
| | Deferred revenue (debt-like, see above) |

The exclusions are the whole game. Cash is excluded because the seller keeps it. Debt is excluded because it is deducted separately. Income taxes are excluded because they belong to the seller's period of ownership. Deferred revenue is excluded because it is treated as debt-like. Every exclusion exists to prevent a double-count — and every dispute in this area is, at bottom, an argument that something was counted in the wrong column.

There is one more subtlety worth naming: **consistency of accounting policies**. The purchase agreement will say the closing working capital is to be calculated "in accordance with GAAP, consistently applied" — meaning the same policies the company used historically. That sentence exists because the alternative is chaos: a seller who switches from FIFO to LIFO inventory accounting at closing, or who suddenly writes off receivables it had been carrying for years, can move the working capital number by millions without any real change in the business. The agreement pins the policies down, and then the accountants argue about what "consistently applied" means in practice, which is a different and longer argument.

## 4. The Peg: What "Normal" Means

The adjustment compares actual closing working capital to a **target** — the "peg" — agreed before signing. If the business arrives with more working capital than the peg, the buyer pays more; if less, the buyer pays less. The peg is supposed to represent the *normal* level of working capital the business carries: enough to operate without the buyer having to inject cash on day one, and no more.

How is "normal" set? Usually as an average of the working capital over the twelve months before signing — often the monthly average, because a single year-end snapshot can be gamed or can catch a seasonal peak. Consider a distributor whose working capital moves with the seasons:

| Month | Working capital ($m) |
|---|---:|
| Jan | 33 |
| Feb | 34 |
| Mar | 36 |
| Apr | 38 |
| May | 40 |
| Jun | 42 |
| Jul | 44 |
| Aug | 45 |
| Sep | 47 |
| Oct | 45 |
| Nov | 41 |
| Dec | 35 |
| **Average** | **40** |

Twelve months sum to $480 million, so the average is $40 million. That becomes the peg. Notice what the peg does and does not do. It does not promise the buyer $40 million on closing day — the actual number will be whatever it is, and the price adjusts. What it does is fix the *reference point*: the buyer is paying for a business that normally carries $40 million of working capital, so if it arrives with $34 million, the buyer is short $6 million of fuel and pays $6 million less.

Seasonality is where pegs get contentious. If the deal closes in September, when working capital is at its $47 million peak, the buyer pays $7 million above the peg — and the seller's shareholders pocket the seasonal peak. If it closes in January, the buyer pays $7 million below. Neither side is being cheated; the mechanism is doing exactly what it was designed to do. But the seller who understands this will push to close in September, and the buyer who understands it will push for a peg set on the *closing month's* historical average rather than the annual average. The negotiation over which average to use is one of the quietest and most valuable arguments in a deal.

A related point: the peg is usually set from *historical* working capital, which embeds the company's historical accounting policies and historical business mix. If the business has changed — a new product line, a different customer mix, a renegotiated supplier contract — the historical average may no longer describe "normal." A good banker flags this early, because a peg built on stale history is a dispute waiting for a closing date.

## 5. Completion Accounts: Pay Now, Measure Later, True Up

In the United States, the dominant mechanism is **completion accounts**. It works in three steps:

1. **Estimate.** Shortly before closing, the seller prepares an estimated closing balance sheet. The parties compute an estimated purchase price from it and the buyer pays that amount at closing.
2. **Measure.** Within 60 to 90 days after closing, the buyer (now the owner) prepares the completion accounts — the actual closing balance sheet, calculated under the agreement's definitions and accounting policies.
3. **True up.** The seller reviews the completion accounts, the two sides argue, and the difference between the estimated price and the final price is paid by whoever owes it — usually out of an escrow account funded at closing.

The escrow is the mechanism that makes the true-up real. A portion of the purchase price — commonly 5 to 10 percent, or a negotiated dollar amount — is held back by a third-party escrow agent for the true-up period (and often longer, to cover indemnity claims). Without it, the seller would have every incentive to dispute the completion accounts forever, because the money would already be in its pocket.

Completion accounts have one structural feature that matters: **the buyer prepares them, but the buyer now owns the company.** The buyer's accountants are measuring a balance sheet of a company the buyer controls, under definitions negotiated when the buyer was an outsider. The seller's protection is the right to review, object, and ultimately take the dispute to an independent accountant — the "expert determination" clause — whose decision is binding. Practitioner data suggests that a majority of completion-accounts deals involve at least some dispute over the working capital number, with the disputed amounts typically running to a few percent of enterprise value, and a meaningful minority ending up before the expert. The numbers are not enormous, but they are real money, and they are almost entirely avoidable with a tighter definition at signing.

## 6. Locked Box: Fix the Price, Charge Interest

Europe's dominant mechanism is the **locked box**, and it is the mirror image of completion accounts. Instead of measuring the balance sheet at closing, the parties fix the price by reference to a historical balance sheet — the "locked box date," usually the last audited year-end or quarter-end before signing. The equity value is computed once, from that balance sheet, and it does not change. There is no true-up, no completion accounts, and no working capital dispute after closing.

The buyer is protected differently: by **leakage** provisions and by interest. Leakage is any value that leaves the company between the locked-box date and closing for the seller's benefit — dividends, management fees paid to the seller, assets sold to the seller below market value. The agreement forbids leakage, and if it happens, the buyer is compensated dollar for dollar. And because the buyer is paying for a business valued as of a date in the past, the buyer pays **interest** — a "ticking fee" — on the equity value from the locked-box date to closing, compensating the seller for the time value of money and for the profits the business generated in the interim, which the buyer will now receive.

Why would a seller prefer a locked box? Price certainty: the seller knows exactly what it will receive, with no post-closing adjustment. Why would a buyer accept it? Simplicity and speed, and because in a competitive auction the seller can demand it. The trade-off is that the buyer takes the risk that the business deteriorates between the locked-box date and closing — the buyer pays the locked-box price regardless. That is why locked-box deals usually have a shorter gap between the locked-box date and closing, and why buyers in locked-box deals spend more time on interim-period covenants: promises that the seller will run the business normally until closing.

| | Completion accounts | Locked box |
|---|---|---|
| Price fixed | At closing, from actual balance sheet | At signing, from historical balance sheet |
| Post-closing adjustment | Yes — the true-up | No |
| Seller's price certainty | Low until accounts are final | High |
| Buyer's risk | Low — pays for what it gets | Higher — pays a historical price |
| Disputes | Common, over the closing balance sheet | Rare, mostly about leakage |
| Where dominant | United States | United Kingdom and continental Europe |

## 7. A Worked Example, End to End

Time to put numbers on all of this. Acme Industrial Supplies, a distributor: the buyer and seller agree an enterprise value of **$500 million**, cash-free, debt-free, with a target working capital peg of **$40 million** (the twelve-month average from section 4). The deal is structured with completion accounts and a $10 million escrow. Closing is 30 June.

**Step 1: the estimated price at closing.** The seller's estimated closing balance sheet shows cash of $18 million, debt of $120 million, debt-like items of $6 million (an underfunded pension of $4 million plus $2 million of the seller's unpaid transaction fees), and working capital of $34 million. The estimated equity value is:

```math
\begin{aligned}
\text{Equity value} &= \text{EV} - \text{Debt} - \text{Debt-like items} + \text{Cash} + (\text{Closing WC} - \text{Peg}) \\
&= 500 - 120 - 6 + 18 + (34 - 40) \\
&= 500 - 120 - 6 + 18 - 6 \\
&= \$386\text{ million}
\end{aligned}
```

The buyer pays $386 million at closing: $376 million to the seller, $10 million into escrow. Notice how far the wire is from the headline: $114 million less than the announced $500 million, and every dollar of the difference is explained — $120 million of debt the seller's lenders are repaid from the proceeds, $6 million of debt-like items, $6 million of working capital shortfall, partly offset by $18 million of cash the seller keeps.

**Step 2: the completion accounts.** Ninety days later, the final closing balance sheet comes in: cash is actually $19 million, working capital is actually $37 million, debt is $120 million, debt-like items $6 million. The final equity value is:

```math
\begin{aligned}
\text{Equity value} &= 500 - 120 - 6 + 19 + (37 - 40) \\
&= 500 - 120 - 6 + 19 - 3 \\
&= \$390\text{ million}
\end{aligned}
```

The true-up is $390 million − $386 million = **$4 million owed by the buyer to the seller**. You can check it two ways: cash came in $1 million higher than estimated and working capital $3 million higher, and $1 million + $3 million = $4 million. The $4 million is released from escrow, and the remaining $6 million of escrow stays held for indemnity claims.

**Step 3: the locked-box alternative.** Suppose instead the deal had been done as a locked box, with the locked-box date of 31 December, when Acme's balance sheet showed cash of $25 million and debt of $45 million (before the seller drew the revolver in the spring). The equity value would be fixed at $500 + 25 − 45 = **$480 million**, and the buyer would pay interest on that amount from 31 December to the 30 June closing — say 5% per annum for four months of the interest period the parties agreed to (the gap between the locked-box date and signing is often excluded):

```math
\text{Interest} = 480 \times 5\% \times \frac{4}{12} = 480 \times 0.05 \times \frac{1}{3} = \$8\text{ million}
```

Total payable: $480 million + $8 million = **$488 million**, with no true-up and no escrow for working capital. The two mechanisms produce very different numbers — $386 million estimated under completion accounts versus $488 million under the locked box — but they are not comparable, because the underlying balance sheets are different: the locked-box price was struck before the seller drew $75 million of additional debt in the spring. That is the whole point. The mechanism matters less than the balance sheet it is applied to, and the balance sheet moves.

## 8. Where Deals Actually Fight

Four disputes recur so often that bankers treat them as checklists.

**The definition fight.** "Is this item in working capital, or is it debt-like?" Deferred revenue, accrued bonuses, warranty reserves, and restructuring provisions all sit on the border. The side that wins the definition wins the dollars, so the definition schedule in the purchase agreement is negotiated line by line — and the items that get missed are the ones that produce the dispute. A good habit: for every line on the target's balance sheet, ask which column it belongs in, and write the answer down.

**The gaming fight.** A seller who knows the closing date can move the working capital number without changing the business. The classic moves: recognising revenue early or shipping product before the customer asked for it — accounts receivable rise, working capital rises, and the buyer pays more for sales that may never be collected. Or under-accruing expenses — bonuses, warranty costs, supplier invoices that have arrived but not been booked — so that current liabilities look smaller than they are. The protections are the consistency-of-accounting-policies clause, the buyer's right to review the completion accounts, and the escrow. None of them is perfect, which is why the escrow exists.

**The double-count fight.** The same dollar counted twice. The common version: a receivable is collected just before closing, so the cash is in the bank — and the seller keeps it, because the deal is cash-free — but the working capital schedule, prepared from a balance sheet a week old, still shows the receivable. The buyer pays for the receivable in the working capital adjustment and the seller keeps the cash. The fix is a cut-off discipline: the completion accounts must be prepared as of the closing moment, not the last convenient month-end.

**The seasonality fight.** As section 4 showed, closing in a peak month versus a trough month moves the price by millions, and both sides know it. The argument is never stated as "we want to close in September because working capital is high"; it is stated as "the peg should reflect the closing month's average." Same money, different words.

## 9. Common Misconceptions

**"The announced price is what the seller receives."** No. The announced price is the enterprise value. The seller receives the equity value — enterprise value minus debt and debt-like items, plus cash, plus or minus the working capital adjustment — and then pays its own taxes and transaction fees out of that. In the worked example, the seller received $386 million on a $500 million headline, and $120 million of that difference went straight to the lenders.

**"Working capital is just current assets minus current liabilities."** In a textbook, yes. In a purchase agreement, working capital is a defined term that excludes cash, debt, taxes, and deferred revenue, because those are handled elsewhere in the bridge. Using the textbook definition in a deal would double-count cash and debt — the two most common arithmetic errors in junior models.

**"A higher peg is always better for the seller."** Not necessarily. The peg is a reference point, not a payment. A higher peg means the buyer pays less when actual working capital comes in below it — and actual working capital usually does come in below an inflated peg, because the peg is set from the seller's preferred historical period. What matters is the gap between the peg and the working capital the business actually delivers, and a peg set above the business's real normal level is a liability to the seller, not an asset.

**"Locked box means no adjustments at all."** It means no *working capital* true-up. The price still reflects the locked-box balance sheet, the buyer still pays interest for the interim period, and leakage is still policed — and policed aggressively, because it is the buyer's only protection. A seller who pays itself a dividend the week before closing in a locked-box deal has not found a loophole; it has created a claim.

**"The completion accounts are the buyer's numbers, so the buyer always wins."** The buyer prepares them, but the seller reviews them, the agreement's definitions bind both sides, and an independent accountant decides the disputes. In practice the process is adversarial in exactly the way it should be: each side's accountants check the other's work, and the escrow makes sure the money is still there when they finish.

## 10. Test Yourself

**1.** A buyer agrees to an enterprise value of $200 million, cash-free, debt-free. At closing, the target has cash of $10 million, debt of $50 million, debt-like items of $5 million, and working capital of $22 million against a peg of $30 million. What is the equity value the buyer pays?

*Answer: $200 − 50 − 5 + 10 + (22 − 30) = $147 million. The working capital shortfall of $8 million reduces the price, and the $10 million of cash partly offsets the debt.*

**2.** In the Acme example in section 7, suppose the final completion accounts had shown working capital of $31 million instead of $37 million, with everything else unchanged. What would the true-up be, and who pays whom?

*Answer: Final equity value = 500 − 120 − 6 + 19 + (31 − 40) = $384 million. The estimated price was $386 million, so the true-up is $2 million owed by the seller to the buyer — paid out of the escrow.*

**3.** A seller proposes a working capital peg based on the highest month of the last twelve rather than the average, arguing that the business "normally" carries that much. The deal closes in the lowest month of the year. Who benefits from the seller's peg, and why?

*Answer: The buyer benefits. If the peg is set at the peak ($47 million in the section 4 example) and closing working capital is at the trough ($33 million), the adjustment is 33 − 47 = −$14 million — the buyer pays $14 million less than it would against a $40 million average peg. A peg above the business's true normal level is a liability to the seller, not an asset.*

**4.** In a locked-box deal, the seller pays a $20 million dividend to itself between the locked-box date and closing. The purchase agreement has a standard leakage clause. What happens?

*Answer: The dividend is leakage — value leaving the company for the seller's benefit after the price was fixed. The buyer is compensated dollar for dollar, usually by a reduction in the price payable at closing (or a claim for the $20 million). The locked box fixes the price, but it does not give the seller a free right to strip cash out of the business.*

---

**Next up:** 32 | Valuing Asset Managers: AUM, Fee Rates, and Why the Multiple Follows the Mix — the financials valuation series continues, this time with the companies that manage everyone else's money.
