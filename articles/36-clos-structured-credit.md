# 36 | CLOs and Structured Credit: How Loans Become Bonds

*The first time someone told me a pile of B-rated loans could be turned into a AAA bond, I thought it was a joke — or a scam. It is neither. A CLO does not make risk disappear. It sorts risk, prices each slice, and hands each slice to the investor who wants exactly that risk. Done honestly, with the right collateral, that sorting is genuinely useful. Done with the wrong collateral and the wrong assumptions, it produced the worst financial crisis of my lifetime.*

> **Learning goals.** After this article you can: (1) explain what pooling and tranching do, in plain language; (2) build the capital structure of a CLO and compute what the equity tranche earns — and what kills that return; (3) explain the overcollateralization and interest coverage tests, and what happens when they fail; (4) explain how subordination and diversification turn B-rated collateral into AAA-rated bonds — and why that result is hostage to one assumption about correlation; (5) explain why CLOs survived 2008 while the mortgage CDOs did not; (6) explain why CLO demand sets the price of leveraged loans, and therefore of LBO debt.
>
> **Prerequisites.** Article 03 (enterprise value vs equity value) for the capital structure stack; article 06 (DCF I) for discounting; article 08 (LBO analysis) for how leveraged deals are funded; article 20 (debt capital markets) for how bonds are sold; article 25 (leveraged finance) for the loans that feed a CLO; article 30 (credit ratings) for how agencies think about default risk; articles 34–35 (convertibles, preferred stock) for the idea that a capital structure is a stack of claims with different rights.

## 1. The Machine in One Paragraph

A **collateralized loan obligation (CLO)** is a company whose only business is owning loans and issuing bonds. Here is the whole trick in one paragraph. A manager buys a few hundred **leveraged loans** — floating-rate, senior secured loans to below-investment-grade companies, the same loans we met in article 25 — and puts them into a special purpose vehicle, an **SPV**, a bankruptcy-remote company that exists only to hold the loans. The SPV then issues its own securities, in layers, against that pool. The top layer gets paid first and takes losses last; the bottom layer gets paid last and takes losses first. Each layer is called a **tranche** (from the French for "slice"). The top tranche is rated AAA and sold to banks and insurers who want safe yield. The middle tranches are rated AA down to BB. The bottom slice, the **equity tranche**, is not rated at all — it is the residual claim, the first to absorb losses and the last to be paid, and in exchange it keeps whatever is left over after everyone else is paid.

That is all a CLO is: a pile of loans, sliced by priority. Nothing is created and nothing is destroyed — the total risk of the pool is the same as before. What changes is *who bears which part of it*. A bank's treasury cannot buy a B-rated loan, but it can buy a AAA bond backed by a hundred B-rated loans. Whether that AAA label is deserved is the question that decides whether the machine is finance or alchemy, and we will come back to it in section 4.

One more piece of vocabulary, because the names get confusing. **Structured credit** is the general name for any security built by pooling assets and slicing them into tranches. A CLO is one kind, backed by corporate loans. A **CDO** (collateralized debt obligation) is the broader family: back it with bonds and it is a CDO, back it with mortgages and it is an **RMBS**, back it with commercial mortgages and it is a **CMBS**. The 2008 crisis was mostly about CDOs backed by subprime mortgages — and, worse, CDOs backed by *other CDOs*. CLOs, backed by corporate loans, are the member of the family that survived.

## 2. The Anatomy: Who Does What

A CLO has four groups of people, and each one is doing a job that would be familiar from any other deal.

**The manager.** A specialist asset manager picks the loans, buys them, and manages the pool for the life of the deal. During the **reinvestment period**, usually the first four or five years, the manager can sell deteriorating loans and buy new ones, as long as the pool still passes the tests in section 5. After it ends, principal repayments pay down the notes and the deal winds down. The manager is paid around 0.15% a year as a senior fee that gets paid before the debt holders, plus around 0.25% as a subordinated fee that gets paid only after them — part of the manager's pay is at risk, which aligns the manager with the debt investors.

**The SPV and the trustee.** The SPV is a legal shell that owns the loans and issues the notes. A **trustee** holds the collateral, collects the cash, and enforces the waterfall — the rules for who gets paid, in what order. The SPV is **bankruptcy-remote**: if the manager goes bust, or if one of the borrowers goes bust, the SPV's assets are ring-fenced. Investors in the notes have a claim on the loan pool, not on the manager.

**The debt investors.** They buy the rated tranches. AAA buyers are usually banks, insurers, and money managers who are *required* to hold highly rated assets — regulation forces them into AAA paper, which is exactly why the AAA tranche exists. Mezzanine buyers (AA through BB) are credit funds and hedge funds. All the debt tranches are floating-rate: they pay SOFR plus a spread. That matters, because the loans in the pool are also floating-rate. When rates rise, the loans pay more *and* the notes cost more, and the two roughly offset. What the CLO earns is not a bet on the level of rates; it is the **spread** between the loans and the notes.

The collateral itself is worth a look. A typical CLO holds 150 to 250 leveraged loans, each one a senior secured first-lien loan to a different company, spread across industries, with limits on exposure to any single borrower or industry. The average loan is rated B or B+. These are the loans of LBO'd companies, the very deals article 08 described. The CLO market and the LBO market are the same ecosystem — the CLO is where most LBO loans end up.

## 3. Worked Example: Building a $500 Million CLO

Let's build one. Our manager, Meridian Credit Partners, assembles a $500 million pool of leveraged loans paying, on average, SOFR + 350 basis points. To fund the purchase, the SPV issues the following capital structure:

| Tranche | Size | % of deal | Coupon | Annual interest |
|---|---:|---:|---|---:|
| AAA | $325m | 65% | SOFR + 130 | $4.225m |
| AA | $50m | 10% | SOFR + 180 | $0.900m |
| A | $30m | 6% | SOFR + 230 | $0.690m |
| BBB | $30m | 6% | SOFR + 320 | $0.960m |
| BB | $25m | 5% | SOFR + 550 | $1.375m |
| **Debt subtotal** | **$460m** | **92%** | — | **$8.150m** |
| Equity | $40m | 8% | residual | what's left |
| **Total** | **$500m** | **100%** | — | — |

All the coupons are spreads over SOFR, so SOFR itself cancels out of the analysis: the loans pay SOFR + 350 and the notes cost SOFR plus something smaller. Work in spreads only.

**Step 1: the income.** The pool earns 3.50% on $500 million:

```math
Asset\ income = \$500m \times 3.50\% = \$17.50m\ per\ year
```

**Step 2: the debt cost.** Adding up the interest column, the five debt tranches cost $8.15 million a year — 1.63% of the whole pool.

**Step 3: the fees.** The manager takes 0.40% of the pool — 0.15% senior, 0.25% subordinated — which is $2.00 million a year.

**Step 4: the excess spread.** What is left for the equity is the arbitrage:

```math
Excess\ spread = \$17.50m - \$8.15m - \$2.00m = \$7.35m\ per\ year
```

On $40 million of equity, that is a cash yield of:

```math
Equity\ yield = \frac{\$7.35m}{\$40m} = 18.4\%
```

That 18.4% is *before defaults*. It is the yield if every borrower pays. No borrower pool ever does, so now subtract the losses.

**Step 5: expected losses.** Suppose 2% of the loans default each year, and the recovery on a defaulted senior secured loan is 70% — a typical long-run figure for first-lien loans. The loss rate is:

```math
Loss\ rate = Default\ rate \times (1 - Recovery) = 2\% \times (1 - 0.70) = 0.60\%
```

On a $500 million pool, that is $3.00 million a year. The equity's take falls to $7.35m − $3.00m = $4.35 million, or 10.9% on its $40 million. That is the honest base case: a low-teens cash yield for the riskiest seat in the deal.

**Step 6: the stress test.** Now suppose a bad year: 6% of borrowers default, and recoveries fall to 50%. The loss rate is 6% × 50% = 3.00%, or $15.00 million. The excess spread of $7.35 million does not cover it, so the equity gets **zero** cash that year. But notice who else is hurt: nobody. The $40 million equity cushion absorbs the whole $15 million loss, leaving $25 million of cushion, and the BB tranche — the lowest-rated debt — is still fully covered. Losses have to exceed $40 million, 8% of the pool, before the BB holders lose a single dollar of principal. That is **subordination** in action: the equity is a shock absorber, and its size is the distance between the pool's losses and the debt holders' money.

**Step 7: the disaster case.** Losses of $45 million — say, a 15% default rate with 40% recoveries (15% × 60% = 9% × $500m = $45m). The equity is wiped out entirely, and the remaining $5 million of loss eats into the BB tranche: BB holders lose $5 million of their $25 million, a 20% principal loss. The BBB tranche and everything above it is still untouched. For the AAA holders to lose money, losses would have to exceed $175 million — the equity plus BB, BBB, A, and AA combined (40 + 25 + 30 + 30 + 50 = $175 million), or 35% of the pool. That is why the AAA tranche can be rated AAA even though the underlying loans are rated B: it is protected by 35% of subordination.

Hold that number — 35% — in mind, because it is the whole argument for the rating. The question is whether the argument is sound.

## 4. The Alchemy Question: How Does B Become AAA?

The honest answer has two ingredients, and one hidden assumption.

**Ingredient one: subordination.** As the example shows, the AAA tranche only loses money if more than 35% of the pool's value disappears. The rating agencies run models of the pool's loss distribution and ask: how likely is a loss bigger than 35%? If the answer is "about as likely as a AAA corporate bond defaulting," the tranche gets a AAA rating. Subordination is not magic; it is arithmetic — the same logic as the capital structure stack in article 03, applied to a pool instead of a single company.

**Ingredient two: diversification.** A single B-rated loan has a meaningful chance of defaulting — say 5% in a given year. But a pool of 200 loans to 200 different companies is not 200 independent coin flips, and it is not one coin flip either. The truth is in between, and where exactly in between is the hidden assumption: **correlation** — how likely is it that many borrowers default at the same time?

Here is a toy example that shows why the assumption matters so much. Take two loans, each with a 5% chance of defaulting. If their defaults are *independent* — one company's trouble has nothing to do with the other's — the chance both default is:

```math
P(both\ default) = 5\% \times 5\% = 0.25\%
```

But if their defaults are *perfectly correlated* — whatever kills one kills the other — the chance both default is simply 5%. A senior tranche that only loses money when *both* loans default is twenty times riskier under perfect correlation than under independence (5% / 0.25% = 20). Same loans, same individual default probabilities, same subordination — a twenty-fold difference in the risk of the senior tranche, driven entirely by one assumption about how defaults cluster.

That is the core finding of the most important academic paper on structured finance, Coval, Jurek, and Stafford (2009). They showed that the ratings of structured tranches are extraordinarily sensitive to the correlation assumption, and that the historical data used to calibrate those assumptions came mostly from good times, when defaults were rare and looked independent. In a recession, defaults cluster, and the correlation that looked low in the data turns out to be much higher in the crisis. The AAA rating was computed with the good-times correlation. This is not a flaw in the arithmetic of tranching; it is a flaw in the inputs. And it is why Coval and his co-authors could write, in 2009, that by mid-2007 some 37,000 structured finance issues in the United States carried a AAA rating — more AAA securities than there were AAA-rated companies by an order of magnitude.

Benmelech and Dlugosz (2009) documented the same mismatch from the other side, with hand-collected data on 3,912 CLO tranches. The average loan in a CLO pool was rated around B, yet more than 70% of the dollar value of the CLO securities was initially rated AAA. They called it "alchemy," and their point was not that the transformation is impossible — subordination is real. Their point was that the *amount* of AAA being manufactured was only justified if you believed the models, and the models were fed optimistic assumptions about how independently borrowers default.

So the right way to think about it is not "AAA means safe." It is "AAA means: this tranche loses money only in a scenario where more than a third of the pool is wiped out, *assuming* defaults behave the way they did in the data the rating agency used." Always ask what the assumption was.

## 5. The Tests That Keep the Machine Honest

A CLO is not a "set it and forget it" structure. The deal documents contain **coverage tests** that are checked every quarter, and they are the reason the structure can correct itself when the collateral deteriorates. There are two, and they work together.

**The overcollateralization (OC) test.** For each debt tranche, the deal requires that the value of the collateral, divided by the amount of that tranche (plus everything senior to it), stays above a minimum ratio. For the AAA tranche, the minimum is typically around 121.6%. In our example, at closing:

```math
AAA\ OC\ ratio = \frac{\$500m}{\$325m} = 153.8\%
```

That passes comfortably — the test only fails if the collateral value falls below $325m × 1.216 = $395.2 million, which would take more than $104.8 million of losses, about 21% of the pool. But the numerator is not simply the par value of the loans. Defaulted loans count at their market or recovery value, not par, and loans downgraded to CCC are **haircut**: only a limited amount of CCC-rated loans (usually around 7.5% of the pool) counts at par, and any excess counts at market value. So a wave of downgrades can push the OC ratio down even before any borrower actually defaults — which is by design, since the test is meant to catch deterioration early.

**The interest coverage (IC) test.** This one compares the interest the pool actually collects with the interest owed on each tranche. For the AAA tranche in our example:

```math
AAA\ IC\ ratio = \frac{\$17.50m}{\$4.225m} = 414\%
```

Again, it passes by a wide margin at closing. It starts to bind when borrowers stop paying interest — which happens before they formally default.

**What happens when a test fails?** The cash waterfall changes. Interest cash that would normally flow down to the equity — and, depending on which test failed, to the junior debt tranches — is **diverted** to pay down the senior notes until the test passes again. The deal deleverages itself: the senior investors get their money back early, and the equity investors get nothing until the test is cured. That is why CLO equity is the shock absorber twice over: it takes the first losses, and it is the first cash flow to be switched off when the tests trip. In 2008 and in 2020, many CLOs failed their OC tests, diverted cash to the senior notes, and the AAA tranches were repaid early instead of taking losses.

## 6. Why CLOs Survived 2008 While Mortgage CDOs Did Not

The CDOs that blew up in 2008 were backed by subprime mortgages, and in many cases by *tranches of other CDOs* — CDO-squared — where the correlation assumption was not just optimistic but untestable, because the underlying assets had almost no history. When US house prices fell nationally for the first time since the Depression, the correlation the models assumed was low turned out to be nearly perfect, and the AAA tranches of mortgage CDOs lost 20%, 30%, even 40% of their value.

CLOs were different in four ways:

**The collateral was real and recoverable.** A leveraged loan is a senior secured claim on an operating company, with covenants, collateral, and a bankruptcy process that historically returns around 70 cents on the dollar. A subprime mortgage in 2006 was a claim on a house whose price depended on the assumption that house prices only go up. When loans defaulted in 2009 — the leveraged loan default rate peaked near 10% — recoveries held up, and the losses stayed inside the equity cushion of most CLOs.

**The collateral was diversified.** A CLO holds loans across dozens of industries. A mortgage CDO held mortgages that all depended on one thing: the US housing market. Diversification only works if the risks are actually different, and the CLO's risks were.

**The manager could trade.** During the reinvestment period, a CLO manager who saw a borrower deteriorating could sell the loan — at a loss, but before it became a default — and buy something healthier. A mortgage CDO was a static pool: once the bad mortgages were in, they were in.

**The tests bit early.** As section 5 showed, OC and IC tests divert cash to the senior notes at the first sign of trouble. Mortgage CDOs had triggers too, but theirs were based on the same ratings that turned out to be wrong, so they fired too late.

The result is a fact worth stating plainly: according to S&P's data, **no AAA-rated CLO tranche has ever defaulted** — not in 2008, when leveraged loan defaults peaked near 10%, not in the COVID shock of 2020, not since. S&P's 2025 study found zero AAA defaults across more than 5,900 ratings issued since 2010, and zero across the 1,541 ratings issued before the financial crisis. Even AA tranches have an essentially clean record. That does not mean the AAA rating was "right" in some deep sense — Coval's point about correlation still stands, and a AAA CLO tranche fell sharply in price in March 2020 even though it never defaulted. Price risk and default risk are different things.

One caution, because this article would be dishonest without it: the record is about the past. The CLO market today is larger than it was in 2007 — the global market is over $1.2 trillion — and the collateral has changed. A growing share of leveraged loans now carry PIK toggles and weaker covenants, the "cov-lite" loans of article 25. The tests still work, but they work on worse inputs. The machine is only as good as the loans you feed it.

## 7. Why a Banker Cares: The CLO Bid

Everything so far has been about how a CLO works. Here is why it matters to an investment banker: **CLOs are the buyers of leveraged loans.** They own roughly two-thirds to more than 70% of the outstanding institutional leveraged loan market — over $1 trillion of loans. When a bank underwrites an LBO, it does not plan to hold the debt. It plans to sell the term loan to CLOs. If the CLO market is hungry, the loan clears easily at a low spread and the LBO works. If the CLO market freezes, as it did in early 2008 — when first-quarter CLO issuance was down 85% from a year earlier — the loan cannot be sold, the bank is stuck holding it, and the LBO market shuts down. The "CLO bid" is not a side detail of leveraged finance; it is the demand curve for the whole product.

That makes the CLO market a leading indicator a banker watches every week. New CLO issuance, AAA spreads, and the arbitrage — the gap between loan spreads and CLO liability costs — tell you whether leveraged deals can get funded and at what price. When the arbitrage is wide, managers rush to form new CLOs, which bids up loan prices, tightens loan spreads, and narrows the arbitrage. It is a self-correcting loop, and it connects the abstract structure of this article to the price of an LBO on a Monday morning.

There is also a direct lesson for the equity investor in a CLO, which generalizes: the equity's return is **levered excess spread minus losses**. If loan spreads compress, the excess spread shrinks. If CLO debt spreads widen, the excess spread shrinks. If defaults rise, losses eat the return directly. The equity is a leveraged bet that the spread between B-rated loans and AAA funding will stay wide enough, for long enough, to cover the defaults.

## Common Misconceptions

**"A CLO turns bad loans into good bonds, so the risk disappears."** No. Tranching redistributes risk; it does not reduce the total risk of the pool by a single dollar. The AAA tranche is safer because the equity and mezzanine tranches absorb the losses first — the risk is concentrated at the bottom, not eliminated.

**"AAA means the same thing for a CLO as for a government bond."** A credit rating is a statement about the probability of default, not about the *kind* of risk. A AAA CLO tranche and a AAA government bond have similar estimated default probabilities, but very different loss profiles: the CLO tranche's risk is concentrated in a bad tail scenario (a severe recession with correlated defaults). They also behave very differently in a crisis: the CLO tranche's price can fall 20% in a month even if it never defaults. Same letters, different risks.

**"CLOs caused the 2008 crisis."** They did not. The crisis was driven by subprime mortgages and the CDOs built on them, plus the leverage in the banking system. CLOs were a sideshow in 2008 — many equities were wiped out, but their senior tranches did not default, and the CLO market restarted within a couple of years while the mortgage CDO market never came back.

**"The equity tranche is free money — 18% yields!"** The 18.4% in our worked example was *before* defaults, and it assumed the excess spread stays constant. In practice the equity's cash flow is the first to be switched off when the OC test fails, it absorbs the first losses, and in a bad year it receives nothing for quarters at a time. Its long-run return is much closer to the 10.9% base case — or worse — than to the headline number.

**"Diversification means defaults can't cluster."** Diversification reduces *idiosyncratic* risk — one company failing for its own reasons. It does not reduce *systematic* risk — many companies failing because the economy fails. A CLO diversified across industries still has all its borrowers exposed to the same recession and the same credit cycle. The correlation assumption is the whole game, and it is the assumption most likely to be wrong precisely when it matters most.

## Test Yourself

**1.** Using the worked example in section 3: (a) What is the equity's cash yield if the default rate is 4% and the recovery rate is 60%? (b) What if the default rate is 8% and the recovery rate is 50%? (c) At what loss rate does the BB tranche start losing principal?

*Answer: (a) Loss rate = 4% × (1 − 0.60) = 1.60%, so losses are $8.00m. Equity gets $0 cash — the losses exceed the $7.35m excess spread — and the extra $0.65m eats into equity principal. (b) Loss rate = 8% × 50% = 4.00%, losses $20.00m. Equity gets $0 cash and its principal falls from $40m to $20m; the BB tranche is still untouched. (c) Once cumulative losses exceed the $40m equity cushion — a loss rate above 8% of the pool.*

**2.** The AAA OC test requires collateral / AAA notes ≥ 121.6%. Our CLO has $500m of collateral and $325m of AAA notes. (a) What is the OC ratio at closing? (b) How far can the collateral value fall before the test fails? (c) Why might the test fail *before* that much principal is actually lost?

*Answer: (a) $500m / $325m = 153.8%. (b) The test fails when collateral falls below $325m × 1.216 = $395.2m — a fall of $104.8m, about 21% of the pool. (c) The numerator is not par: defaulted loans count at market/recovery value, and CCC-rated loans above the usual ~7.5% bucket are haircut to market value. A wave of downgrades can shrink the measured collateral value well before the loans actually default.*

**3.** Two loans each have a 5% chance of default. A senior note loses money only if *both* loans default. (a) What is the probability of loss if defaults are independent? (b) What if they are perfectly correlated? (c) What does this tell you about what a AAA rating on a structured tranche actually depends on?

*Answer: (a) 5% × 5% = 0.25%. (b) 5% — if one defaults, the other does too. (c) Enormously: the same loans and the same subordination give a loss probability twenty times higher under perfect correlation. A AAA rating is a statement about the assumed correlation as much as about the collateral — which is why Coval, Jurek, and Stafford (2009) focused on it.*

**4.** A new CLO manager proposes a deal with the same $500m pool and loan spreads, but only $20m of equity and $480m of debt instead of $40m/$460m — keeping the AAA tranche at $325m and adding the extra $20m as more BB notes. (a) Roughly what happens to the base-case equity yield before defaults? (b) What happens to the protection of the BB tranche? (c) The AAA tranche's subordination is unchanged at $175m — so is the deal just as safe as before? Why or why not?

*Answer: (a) The extra BB debt costs $20m × 5.50% = $1.10m a year, so the excess spread falls to $17.50m − $9.25m − $2.00m = $6.25m. But that smaller spread is now spread over only $20m of equity: $6.25m / $20m = 31.25% before defaults, up from 18.4%. The equity is levered twice as hard. (b) The BB tranche's protection halves: losses need only exceed $20m (4% of the pool) before BB starts losing principal, versus $40m (8%) before — and the BB tranche is now $45m instead of $25m. (c) No. The AAA tranche is equally protected in pure principal terms, but the structure is more fragile: the equity cushion is half as thick, so losses reach the rated notes sooner, the OC tests trip sooner, and the mezzanine investors will demand wider spreads, shrinking the excess spread that made the equity yield look attractive.*

---

*Next up: 37 | Mezzanine Debt and PIK Notes: The Layer Between the Loan and the Equity.*

---

**Papers cited**

- Coval, J., Jurek, J. & Stafford, E. (2009). *The Economics of Structured Finance.* Journal of Economic Perspectives, 23(1), 3–25. — The clearest explanation of pooling and tranching, and the paper that showed how sensitive structured ratings are to the correlation assumption; by mid-2007, about 37,000 structured finance issues in the US carried a AAA rating.
- Benmelech, E. & Dlugosz, J. (2009). *The Alchemy of CDO Credit Ratings.* Journal of Monetary Economics, 56(5), 617–634. — Using hand-collected data on 3,912 CLO tranches: the average collateral was rated around B, yet more than 70% of the dollar value of the securities was initially rated AAA.
- Keys, B. J., Mukherjee, T., Seru, A. & Vig, V. (2010). *Did Securitization Lead to Lax Screening? Evidence from Subprime Loans.* Quarterly Journal of Economics, 125(1), 307–362. — Securitized subprime loans defaulted roughly 10–25% more than similar loans that were not securitized: when the originator can sell the risk, screening gets worse. The CLO answer to that problem is the manager's retained equity and the coverage tests — skin in the game, enforced by contract.
