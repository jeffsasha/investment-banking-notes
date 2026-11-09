# 29 | Valuing Insurance Companies: Float, Reserves, and Why Book Value Rules

*Article 27 broke your valuation toolkit on banks, and article 28 broke it on buildings. Insurance breaks it a third way: here the earnings number is mostly a guess about the future, the balance sheet is dominated by a liability nobody can measure exactly, and the company's cheapest source of funding is its own customers — who pay first and claim later. Get those three facts straight and insurers stop looking strange: they are a leveraged bet on underwriting discipline, with a bond portfolio attached.*

> **Learning goals.** After this article you can: (1) explain what insurance float is and compute its cost from the underwriting result; (2) build the combined ratio from the loss ratio and the expense ratio and read it like an underwriter; (3) explain what loss reserves are, why reserve development moves earnings years after the policies were sold, and why that makes book value fragile; (4) value an insurer with the residual income model, derive justified P/B from ROE, cost of equity, and growth, and cross-check it with a dividend discount model; (5) explain embedded value and why life insurers are valued on it instead of earnings; (6) read a P&C comp table without being fooled by a single year's earnings.
>
> **Prerequisites.** Article 02 (financial statements), article 03 (enterprise value), article 06 (DCF I) for the Gordon growth model, article 07 (DCF II) for terminal value, and article 27 (valuing banks) for why financial companies are valued on equity, not on the firm. Nissim (2010) is the backbone of sections 4 and 6; Nissim (2013) underpins the claim that book value predicts insurer earnings; Cummins & Phillips (2005) is the source for the cost-of-equity discussion in section 6.

## 1. An Insurer Sells a Promise, Then Waits

Every business we have valued so far delivers something and then gets paid. An insurer does it backwards. A customer pays a **premium** today — say $1,200 a year for car insurance — and in return the insurer promises to pay if something bad happens later. The product is a promise. The cost of goods sold is not known on the day of the sale; it is revealed over months and years, as claims arrive and get settled.

That reversal shapes everything about the business, and it gives an insurer two separate profit engines instead of one: **underwriting profit** — premiums collected minus claims paid minus the expenses of running the business — and **investment income**, earned by investing the premiums while they sit in the insurer's account between collection and payout.

There are two kinds of insurer, and you should never mix them in a comp set. A **property and casualty (P&C)** insurer covers things and accidents — cars, houses, liability, hurricanes — on mostly one-year policies, with claims arriving fast. A **life** insurer covers people — mortality, longevity, annuities — on policies that run for decades, so its economics look more like asset management with a mortality assumption attached. Sections 2 to 4 are mostly about P&C, where the intuition is cleanest. Section 5 turns to life, which needs its own valuation language.

## 2. Float: Money You Hold Before You Owe It

Float is the money an insurer holds that belongs, in an economic sense, to its policyholders. Premiums come in on day one; claims go out over the following months and years. In between, the insurer invests the cash. The float is not the insurer's money — it will eventually be paid out in claims — but while it sits there, the investment income is the insurer's to keep. What does that funding cost? The answer comes from the underwriting result: an underwriting loss is the price paid for the float, and an underwriting profit means the insurer was *paid* to hold other people's money.

```math
\text{cost of float} = \frac{\text{underwriting loss}}{\text{average float}}
```

Take a simple example. Suppose an insurer holds average float of $8{,}000$ million and its underwriting operation loses $120$ million in a year. The cost of float is:

```math
\frac{120}{8{,}000} = 1.5\%
```

That insurer borrowed $8$ billion at 1.5%, where a bank borrowing in the bond market might pay 5%. The float is a bargain — *as long as the underwriting loss stays small*. Now flip it: suppose the same insurer underwrites well and earns an $80$ million profit. The "loss" is negative $80$ million, so the cost of float is:

```math
\frac{-80}{8{,}000} = -1.0\%
```

Negative cost. The insurer was paid 1% a year to hold $8$ billion. It then invests that $8$ billion — say at 4.5% in a bond portfolio — and earns $360$ million of investment income on top of the $80$ million underwriting profit. Total pre-tax profit: $440$ million. Underwriting discipline sets the cost of the funding; the investment portfolio sets what the funding earns.

Warren Buffett has written about this for decades, and Berkshire Hathaway's insurance operations are the famous case study: disciplined underwriting turned float into a source of funding that cost less than nothing in most years, and that funding helped buy everything else. The lesson is not "float is free money" — that is one of the misconceptions in section 8. The lesson is that float is leverage, and its price is set by underwriting quality. A bad underwriter pays up for float, exactly like a bad borrower pays up for debt. The difference is that the price is not printed on a term sheet. You have to compute it from the combined ratio, which is the next section.

## 3. The Combined Ratio: The Underwriting Scoreboard

Underwriters are judged by one number: the **combined ratio**. It answers the question "for every $100 of premium we earned, how much did we spend on claims and expenses?" Below 100 means an underwriting profit; above 100 means a loss.

```math
\text{combined ratio} = \text{loss ratio} + \text{expense ratio}
```

```math
\text{loss ratio} = \frac{\text{incurred losses}}{\text{earned premiums}}, \qquad \text{expense ratio} = \frac{\text{underwriting expenses}}{\text{earned premiums}}
```

A couple of definitions, because the words matter. **Earned premiums** are the portion of premiums that correspond to coverage already provided — not premiums written, which is the cash collected. **Incurred losses** are claims paid *plus* the change in reserves for claims that have happened but not yet been settled — a number that is partly an estimate, which is why section 4 exists.

Let us build one. Meet Harbor Mutual, a fictional mid-sized P&C insurer:

| Harbor Mutual, 2025 | $ million |
|---|---|
| Earned premiums | 1,000 |
| Incurred losses | 620 |
| Underwriting expenses | 300 |
| **Underwriting profit** | **80** |

```math
\text{loss ratio} = \frac{620}{1{,}000} = 62\%, \qquad \text{expense ratio} = \frac{300}{1{,}000} = 30\%
```

```math
\text{combined ratio} = 62\% + 30\% = 92\%
```

A 92% combined ratio means Harbor kept $8 of underwriting profit on every $100 of premium — $80$ million in total. Now check that against the float math from section 2: Harbor's average float is $8{,}000$ million, so its cost of float is $-80 / 8{,}000 = -1.0\%$. The two sections agree, as they must. The combined ratio *is* the cost-of-float calculation, expressed per dollar of premium instead of per dollar of float.

Three things to notice. First, the loss ratio and the expense ratio tell different stories. A high loss ratio means the insurer is mispricing risk or getting unlucky on claims. A high expense ratio means the operation is inefficient — too many agents, too much overhead. A good underwriter manages both, but they are different problems with different fixes. Second, one bad catastrophe year can blow the loss ratio apart: a single hurricane can add 10 points to a regional insurer's combined ratio in a quarter. Analysts therefore look at the **accident-year combined ratio excluding catastrophes** — the underlying run-rate, stripped of the weather. Third, the combined ratio is the number that decides whether growth is good or bad. At 92%, Harbor should write more business. At 104%, every new policy destroys value.

## 4. Reserves: The Biggest Number on the Balance Sheet Is a Guess

If you open an insurer's balance sheet, the largest liability is usually **loss reserves** — money set aside for claims that have already happened but have not yet been paid. For a long-tail line like workers' compensation, a claim filed today might not be settled for five or ten years. The reserve is management's best estimate of what those claims will ultimately cost. It is a guess, and it is the biggest number in the building.

This is what makes insurance earnings different from almost any other industry's earnings. In most businesses, last year's results are history. In insurance, last year's results get rewritten every year, because the reserves set aside for last year's claims get re-estimated as new information arrives. The difference between the old estimate and the new one is called **reserve development**:

- **Favourable development:** the old reserves turn out to have been too high, so the excess is released and boosts current earnings.
- **Adverse development:** the old reserves turn out to have been too low, so the shortfall is charged against current earnings.

Suppose Harbor Mutual carries $4{,}000$ million of loss reserves. One year its actuaries conclude that old claims will cost $200$ million more than previously reserved — a 5% miss on the reserve base. That $200$ million is charged straight to pre-tax earnings. Compare it with Harbor's underwriting profit of $80$ million: one 5% reserve error wipes out two and a half years of underwriting profit.

This has three consequences you should carry into every insurer analysis:

1. **A single year's earnings are noisy.** A reserve release can make a mediocre underwriter look profitable, and a reserve charge can make a good one look bad. Never value an insurer on one year of earnings — look at five years of combined ratios and reserve development together.
2. **Book value is an estimate, not a fact.** The equity on the balance sheet is assets minus liabilities, and the liabilities contain that giant estimated number. If reserves are understated by 5%, book value is overstated by $200$ million on Harbor's numbers. This is why section 6 values insurers on *sustainable* ROE, not on a single year's print.
3. **Reserve discipline is the real test of management.** Anyone can grow premiums. The question is whether the reserves behind them are honest. Analysts watch the pattern of development year after year, and whether management keeps releasing reserves to flatter earnings — a habit that eventually runs out of road.

There is also a second set of books to know about. US insurers file **statutory accounting** statements with state regulators, which are deliberately more conservative than GAAP. The **risk-based capital (RBC)** ratio — capital relative to the regulator's required minimum — is the constraint that actually binds an insurer's ability to grow and pay dividends. A GAAP balance sheet can look healthy while the RBC ratio is tight.

## 5. Life Insurance Is a Different Business

Everything so far was P&C. Life insurance works differently, and the difference starts with the time horizon. A life policy can run for thirty years. The insurer collects premiums, invests them, and pays out when the policyholder dies, surrenders, or the annuity matures. The economics are driven by four assumptions: mortality (how long people live), persistency (how many keep paying), expenses, and investment returns.

The key valuation concept for life insurers is **embedded value (EV)** — the value of the business already on the books:

```math
\text{embedded value} = \text{adjusted net asset value} + \text{value of in-force business}
```

**Adjusted net asset value (ANAV)** is the shareholders' net assets, adjusted to market value. **Value of in-force business (VIF)** is the present value of the future profits expected from policies already sold, after allowing for the cost of the capital held against them. EV deliberately excludes the value of *future* new business — reported separately as the **value of new business (VNB)**, which tells you whether the policies being sold today are worth writing.

A quick example. Suppose a life insurer reports ANAV of $2{,}000$ million and VIF of $1{,}400$ million:

```math
\text{EV} = 2{,}000 + 1{,}400 = 3{,}400 \text{ million}
```

If its market capitalisation is $3{,}060$ million, it trades at $0.90\times$ embedded value — the market is paying 90 cents for a dollar of embedded value, which usually means investors doubt the assumptions behind VIF, or doubt that new business will be profitable. If the same company writes $180$ million of new business value this year, that is the growth engine: VNB added on top of EV, year after year, is how a life insurer compounds. But VNB is only as good as the assumptions. An insurer can report handsome VNB by assuming rosy mortality improvement and cheap capital, and the truth shows up years later as the in-force book underperforms.

Life insurers are also spread businesses. A fixed annuity takes in a premium, credits the policyholder, say, 3%, invests the money at 5%, and keeps the 2% spread — until interest rates move and the spread compresses. That is why life insurers' earnings are so sensitive to the rate cycle. It is the same duration mismatch you met in article 27 with banks, wearing a different suit.

## 6. How to Value an Insurer: Book Value, Residual Income, and Embedded Value

Now the valuation. Start with what does *not* work. **Enterprise value is meaningless**, for the same reason as with banks: an insurer's liabilities are its raw material — float and reserves are the business, not financing to be stripped out. **P/E is unreliable** as a primary tool: a single year's earnings are polluted by reserve development and investment gains and losses, so a low P/E often means a reserve release, not a bargain. **DCF on free cash flow** fails too, because "free cash flow" for an insurer is not well defined — premium inflows are not revenue in the usual sense, and capital requirements move with the business.

What works is **book value**, and the reason is empirical, not just theoretical. Nissim (2013) studied US insurers and found that, unlike for most firms, an insurer's book value of equity is a reasonable predictor of its future earnings: its assets are mostly bonds carried close to market value, and its liabilities are reserves that — if honestly set — approximate the present value of future claims. That is why the market prices insurers on **price-to-book (P/B)**, and why the residual income model is the natural valuation framework.

The residual income model says a company's value equals its book value plus the present value of the excess of its future earnings over its cost of equity — its **residual income**. Earn exactly the cost of equity forever and the firm is worth exactly book value; earn more and it is worth a premium; earn less and it trades at a discount. With constant ROE, cost of equity $k$, and growth $g$, the model collapses to the justified P/B formula you can derive from the Gordon growth model:

```math
\frac{P}{B} = \frac{\text{ROE} - g}{k - g}
```

Let us value Harbor Mutual. Book value of equity is $5{,}000$ million, with 100 million shares outstanding — book value per share of $50. Sustainable ROE is 12%, the cost of equity is 10%, and long-run growth is 3%.

```math
\frac{P}{B} = \frac{0.12 - 0.03}{0.10 - 0.03} = \frac{0.09}{0.07} = 1.29
```

Value per share is $1.29 \times \$50 = \$64.29$, and equity value is $1.29 \times \$5{,}000$ million $= \$6{,}429$ million.

Cross-check it with a dividend discount model. Next year's earnings are $\text{ROE} \times \text{book} = 0.12 \times 5{,}000 = \$600$ million. To grow book value at 3% while earning 12%, Harbor must retain $b = g / \text{ROE} = 0.03 / 0.12 = 25\%$ of earnings, so it pays out 75% — a dividend of $600 \times 0.75 = \$450$ million. The Gordon growth model gives:

```math
V_0 = \frac{450}{0.10 - 0.03} = \frac{450}{0.07} = \$6{,}429 \text{ million}
```

The two models agree exactly, as they should — they are the same arithmetic in different clothes. Whenever two methods give different answers, one of them has a wrong input, and finding it teaches you something.

Now run the sensitivity that matters most. Suppose Harbor's ROE falls to 9% — below its 10% cost of equity — while growth stays at 3%:

```math
\frac{P}{B} = \frac{0.09 - 0.03}{0.10 - 0.03} = \frac{0.06}{0.07} = 0.86
```

Value drops to $0.86 \times \$5{,}000$ million $= \$4{,}286$ million — *below* book value. Growth at a return below the cost of capital destroys value, and the formula shows it without mercy. This is the single most useful sentence in insurer valuation: an insurer is worth a premium to book only to the extent that it earns more than its cost of equity, sustainably.

A word on the cost of equity itself. Cummins & Phillips (2005) estimated the cost of equity for US property-liability insurers and found something worth remembering: estimates from the Fama-French three-factor model came out significantly *higher* than plain CAPM estimates. Insurer stocks carry exposures that a single market beta does not capture. The practical takeaway is to be careful with a low CAPM beta — if your cost of equity is too low, your justified P/B is too high, and you will overpay. Use a cost of equity with a margin of scepticism built in, and sanity-check it against the market: if your model says an insurer is worth $1.50\times$ book and the market says $1.10\times$, the market is usually telling you something about reserve adequacy or future ROE that your model has not heard yet.

For life insurers, the same logic runs through embedded value instead of book value. Price-to-EV replaces P/B, and the question becomes whether the market believes the VIF assumptions and whether new business is being written at a profit. A life insurer trading well below EV is either a bargain or a warning — and the way to tell is to look at reserve adequacy, persistency, and whether VNB is real.

## 7. Comps: What to Actually Compare

A comp table for P&C insurers looks different from the trading-multiples table in article 04. Earnings multiples are demoted; book value, underwriting quality, and returns take the lead.

| Company | P/B | Combined ratio (5-yr avg) | ROE (5-yr avg) | Dividend yield |
|---|---:|---:|---:|---:|
| Harbor Mutual | 1.29x | 92% | 12% | 2.8% |
| Coastal General | 1.05x | 97% | 10% | 3.1% |
| Summit Re | 0.85x | 101% | 8% | 1.9% |

Read it the way the residual income model says to. Harbor earns 12% against a 10% cost of equity and underwrites at 92% — it deserves its premium to book. Coastal earns its cost of capital and underwrites near breakeven — fairly priced around book. Summit underwrites at a loss and earns 8%, below its cost of capital — the discount to book is the market doing the residual income math for you. The trap is to look at Summit's $0.85\times$ P/B and its low P/E in a reserve-release year and call it cheap. It is cheap because it earns less than its cost of capital. It only becomes a bargain if the underwriting or the reserves improve — and that is a judgement about the business, not a fact about the multiple.

A few practical rules for insurer comps: compare P&C with P&C and life with life, never mixed; use five-year averages for the combined ratio and ROE, not single years; check reserve development alongside the combined ratio, because a 95% combined ratio built on reserve releases is not a 95% underwriting result; and check the RBC ratio, because an insurer that cannot grow without breaching capital requirements cannot compound no matter how good its underwriting is.

## 8. Common Misconceptions

**"Float is free money."** Float is leverage, and its price is the underwriting result. At a 92% combined ratio it is wonderfully cheap. At a 110% combined ratio it is expensive debt with a friendly name. Buffett's insurers made float look free because they underwrote well; a bad underwriter pays dearly for the same privilege. Always compute the cost of float before admiring its size.

**"A combined ratio below 100% means a good insurer."** Not necessarily. The combined ratio includes reserve releases, so a company can print 95% while its current accident-year underwriting is running at 102% and old reserves are quietly being drained. Look at the accident-year ratio excluding catastrophes, and at reserve development over five years.

**"P/E works the same for insurers as for industrials."** A single year's earnings for an insurer are a cocktail of underwriting, reserve changes, and investment gains. A reserve release can halve the P/E overnight without the business improving at all. P/B, operating ROE, and the combined ratio are steadier guides — and when you do use P/E, use operating earnings that strip out realised investment gains and reserve development.

**"Book value is hard and reliable."** Book value is only as honest as the reserves behind it. A 5% reserve shortfall on Harbor's $4{,}000$ million of reserves is $200$ million of phantom equity, and GAAP book value can flatter a life insurer whose VIF assumptions are optimistic. Book value is the *best* starting point for insurers, which is not the same as a safe one. Verify the reserves before you trust the book.

**"High ROE means a great insurer."** ROE can be juiced by leverage — writing more premiums against the same capital — and by reserve releases. A 15% ROE built on a 98% combined ratio and aggressive reserving is worth less than a 12% ROE built on a 92% combined ratio and conservative reserves. Ask what the ROE is made of before you admire it.

## Test Yourself

**1.** A P&C insurer reports earned premiums of $500$ million, incurred losses of $310$ million, and underwriting expenses of $145$ million. What are its loss ratio, expense ratio, combined ratio, and underwriting profit?

*Answer: Loss ratio $= 310/500 = 62\%$. Expense ratio $= 145/500 = 29\%$. Combined ratio $= 91\%$. Underwriting profit $= 500 - 310 - 145 = \$45$ million. Yes — at 91% it earns $9$ per $100$ of premium before investment income, so its float has a negative cost.*

**2.** An insurer holds average float of $2{,}000$ million and reports an underwriting loss of $30$ million. What is its cost of float, and how does it compare with borrowing $2{,}000$ million in the bond market at 6%?

*Answer: Cost of float $= 30/2{,}000 = 1.5\%$. Borrowing the same money at 6% would cost $120$ million a year; the float costs $30$ million, so the insurer saves $90$ million a year — but only as long as the underwriting loss stays small.*

**3.** An insurer has book value per share of $40, sustainable ROE of 11%, a cost of equity of 9%, and long-run growth of 2%. What is its justified P/B and its value per share? What happens to value if ROE falls to 8%?

*Answer: Justified P/B $= (0.11 - 0.02)/(0.09 - 0.02) = 0.09/0.07 = 1.29\times$. Value per share $= 1.29 \times \$40 = \$51.43$. If ROE falls to 8%: P/B $= (0.08 - 0.02)/0.07 = 0.06/0.07 = 0.86\times$, value per share $= \$34.29$ — below book, because the insurer now earns less than its cost of equity.*

**4.** An insurer carries loss reserves of $3{,}000$ million and reports $150$ million of adverse reserve development. What is the pre-tax earnings impact, and what does a 5% reserve miss imply about the reliability of its book value?

*Answer: The $150$ million is charged directly against pre-tax earnings — a dollar-for-dollar hit. A 5% miss means book value was overstated by $150$ million until the correction, which is why a single year's earnings and a point-in-time book value both need checking against the history of reserve development before you trust them.*

## Next up

Next: **30 | Credit Ratings and the Rating Agencies: Who Grades the Debt?** — we have valued equity from every angle, but the debt side has its own gatekeepers, and their letter grades decide what borrowing costs.
