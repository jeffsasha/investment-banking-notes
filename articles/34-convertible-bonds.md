# 34 | Convertible Bonds: When Debt Turns Into Equity

*Article 33 was about a company with no business raising money from the public. This one is about a security that cannot decide what it is — a bond that can turn into stock whenever its owner feels like it. Convertible bonds are the strangest mainstream instrument in corporate finance: they pay interest like a loan, trade like a bond, and behave like equity when things go well. Bankers love them because they solve problems that neither straight debt nor straight equity can solve cleanly, and investors love them because they are, in the honest sense of the phrase, a free option stapled to a bond. The catch, as always, is that the option is not free — it is paid for in the coupon, in the conversion price, and, eventually, in dilution.*

> **Learning goals.** After this article you can: (1) explain what a convertible bond is and decompose it into a straight bond plus a call option; (2) compute the conversion price, conversion value, conversion premium, and the bond floor; (3) value a convertible with a worked example and explain why its price can never fall below the higher of the floor and the conversion value; (4) explain the three academic theories for why companies issue convertibles — backdoor equity, agency costs, and staged financing; (5) explain how a call provision lets an issuer force conversion; (6) describe the main variations, from mandatory convertibles to CoCos and startup convertible notes.
>
> **Prerequisites.** Article 06 (DCF I) for discounting cash flows and WACC; article 20 (debt capital markets) for how a bond deal gets priced and sold; article 03 (enterprise value vs equity value) for what dilution does to per-share value; article 25 (leveraged finance) for how companies choose between layers of debt.

## 1. A Bond That Can Turn Into Stock

A **convertible bond** is a regular corporate bond with one extra feature: the holder can exchange it for a fixed number of shares of the issuer's stock, at any time (or during a specified window), instead of waiting to be repaid in cash at maturity. The bond does not disappear when it converts — it *becomes* the shares. The coupon stops, the principal is never repaid, and the former bondholder is now a shareholder.

The intuition that makes everything else fall into place is the decomposition. A convertible bond is two things stapled together:

```math
Value of convertible = Value of straight bond + Value of conversion option
```

The straight-bond part is the value of the same bond *without* the conversion feature: the present value of the coupons and the principal, discounted at the yield the company would pay on ordinary debt. The conversion option is a call option on the company's stock — the right, but not the obligation, to swap the bond for shares. Everything about how convertibles are priced, sold, and argued over follows from this split.

That split also explains the pricing. A convertible always carries a *lower* coupon than the same company's straight debt, because the investor is paying for the option with forgone interest. A company that would pay 6% on a plain bond might pay 2% on a convertible. The 4 percentage points of annual coupon the investor gives up is the price of the option. There is no free lunch here — only a trade that happens to suit both sides.

And the trade suits a specific kind of company. Convertibles are the financing of choice for growth companies that are too risky for cheap straight debt, too uncertain for a clean equity raise, and too cash-constrained to pay a full coupon. Think of a software company growing 40% a year with no profits yet: straight debt at 9% would strangle it, and an equity issue today would sell shares at a price management believes is far below what the company will be worth in three years. A convertible threads the needle — cheap cash now, equity later, at a price set above today's stock price.

## 2. The Anatomy: Ratio, Price, Parity, Premium

Every convertible is described by a small set of terms. They look like jargon, but each one is just arithmetic.

The **conversion ratio** is the number of shares each bond converts into. A $1,000 bond with a conversion ratio of 25 converts into 25 shares.

The **conversion price** is the effective price per share the bondholder pays when converting. It is not negotiated separately — it falls out of the ratio:

```math
Conversion\ price = \frac{Face\ value}{Conversion\ ratio}
```

For our $1,000 bond with a ratio of 25, the conversion price is $1,000 / 25 = $40 per share.

The **conversion value** (also called **parity**) is what the shares you would receive are worth right now:

```math
Conversion\ value = Conversion\ ratio \times Current\ stock\ price
```

If the stock trades at $32, the conversion value is 25 × $32 = $800. The bond is worth at least $800, because the holder can always convert and sell the shares — nobody would sell the bond for less than the shares inside it are worth.

The **conversion premium** measures how far the stock has to rise before conversion starts to make sense:

```math
Conversion\ premium = \frac{Conversion\ price}{Current\ stock\ price} - 1
```

Here that is $40 / $32 − 1 = 25%. The stock must rise 25% before the conversion value reaches the $1,000 face value. Typical new issues price the premium at 25–35% above the current stock price. That number is the heart of the negotiation: a higher premium means the issuer is selling future equity at a better price; a lower premium means the option is worth more to the investor, so the coupon can be lower.

Finally, the **bond floor** (or **investment value**) is the value of the straight-bond component — the present value of the coupons and principal at the yield on the issuer's ordinary debt. It is the price the convertible would trade at if the stock went to zero and the option became worthless. The bond floor is the investor's downside protection, and it is the reason convertibles are sometimes described as "equity with a safety net."

Put the pieces together and you get the one rule that governs convertible pricing at all times:

```math
Convertible\ price \geq \max(Bond\ floor,\ Conversion\ value)
```

The convertible can never trade below the bond floor (or an arbitrageur would buy it for the coupons and principal alone) and never below the conversion value (or an arbitrageur would buy it, convert, and sell the shares). The market price sits above whichever is higher, and the gap above it is the time value of the option — the value of the chance that the stock rises further before maturity.

One more term bankers use constantly: **delta**. Delta measures how much the convertible's price moves when the stock moves $1. A deep out-of-the-money convertible — stock far below the conversion price, conversion value well below the bond floor — behaves like a bond, with a delta near 0. A deep in-the-money convertible — stock far above the conversion price — behaves like the shares it converts into, with a delta near 1. In between, the delta is somewhere in the middle, and the convertible is genuinely a hybrid: part bond, part equity, and the mix changes every day with the stock price. Traders who run convertible arbitrage books live and die by delta, hedging the equity exposure and collecting the coupon and the volatility.

## 3. Worked Example: Pricing NovaTech's Convertible

Let us make this concrete. NovaTech Inc. is a profitable-but-still-growing software company. Its stock trades at $32. It wants to raise $500 million and issues a 5-year convertible bond with these terms:

| Term | Value |
|---|---|
| Face value | $1,000 |
| Coupon | 2% per year, paid annually ($20) |
| Maturity | 5 years |
| Conversion ratio | 25 shares |
| Conversion price | $40 ($1,000 / 25) |
| Conversion premium | 25% ($40 / $32 − 1) |
| Yield on NovaTech straight debt | 6% |
| Shares outstanding | 100 million |

**Step 1: the conversion value.** Today the conversion value is 25 × $32 = $800. Since $800 is below the $1,000 face value, no rational holder converts today. The bond is out of the money.

**Step 2: the bond floor.** Discount the coupons and principal at 6%, the yield NovaTech would pay on straight debt:

```math
Bond\ floor = \sum_{t=1}^{5} \frac{20}{(1.06)^t} + \frac{1{,}000}{(1.06)^5}
```

The annuity factor for 5 years at 6% is (1 − 1.06⁻⁵) / 0.06 = 4.2124, so the coupons are worth 20 × 4.2124 = $84.25. The principal is worth $1,000 / 1.06⁵ = $1,000 × 0.7473 = $747.26. Adding them:

```math
Bond\ floor = \$84.25 + \$747.26 = \$831.51
```

If NovaTech's stock went to zero tomorrow, the bond would still be worth about $831.51 on the strength of its coupons and principal alone. That is the floor.

**Step 3: the market price.** Suppose the convertible actually trades at $880. That is above both the floor ($831.51) and the conversion value ($800), as it must be. The decomposition tells us what the $880 consists of:

```math
Option\ value = \$880.00 - \$831.51 = \$48.49
```

The investor is paying $48.49 for the call option on NovaTech stock, and the "premium over parity" — the extra paid above the conversion value — is ($880 − $800) / $800 = 10%.

**Step 4: what happens if the stock rises?** Suppose NovaTech executes well and the stock rises to $50. The conversion value is now 25 × $50 = $1,250. The bond floor is roughly unchanged at $831.51. The convertible must now be worth at least $1,250, and in practice it trades a little above that — say $1,280 — because the option still has time value. Notice what happened: the stock rose 56% (from $32 to $50), and the convertible rose 45% (from $880 to $1,280). The convertible captured most of the upside while having started from a protected floor. That asymmetry is the whole pitch to investors.

**Step 5: what does it cost the issuer?** On $500 million of straight debt at 6%, NovaTech would pay $30 million a year in interest. On the convertible at 2%, it pays $10 million — a saving of $20 million a year, roughly $100 million over the five-year life. But the saving is not free. If the stock rises and the bonds convert, NovaTech issues new shares: $500 million / $1,000 = 500,000 bonds × 25 shares = 12.5 million new shares, against 100 million outstanding — 12.5% dilution. The real cost of the convertible is the equity it gives away later, at $40 a share, in exchange for cheap cash now. Whether that is a good deal depends entirely on what the stock is worth when conversion happens. If the stock is at $80, the company sold $40 shares for an asset now worth $80 — expensive financing, in hindsight. If the stock is at $35, the bonds never convert, and the company got five years of 2% money — a bargain.

## 4. Why Issuers Do It: Three Theories

Academics have argued about convertibles for forty years, and three explanations have survived. They are not mutually exclusive — a single issue can be driven by all three at once — but they point at different companies.

**Backdoor equity (Stein, 1992).** Jeremy Stein's argument is the most quoted, and the most intuitive. Some companies believe their stock is undervalued but cannot prove it to the market. Issuing equity today would sell shares too cheaply, and the market would read the issue as a signal that management thinks the stock is overvalued — the adverse-selection problem Myers and Majluf described in 1984, which we met in article 14. A convertible is delayed equity: the company borrows now and sells the shares later, at the higher conversion price, *if* the stock rises to justify it. If the stock never rises, the company simply repays the debt. Stein's title says it plainly: "Convertible bonds as backdoor equity financing" (Stein, 1992, *Journal of Financial Economics*). The empirical fingerprint is that convertible issuers tend to be companies with high growth options and high information asymmetry — exactly the companies for which a straight equity issue would be most costly.

**Taming the agency conflict (Green, 1984).** Richard Green pointed at a different problem: the conflict between shareholders and bondholders. When a company has straight debt outstanding, shareholders have an incentive to take wild risks — the "asset substitution" or risk-shifting problem. If the gamble pays off, shareholders keep the upside; if it fails, bondholders eat the loss. Bondholders know this and charge for it. A convertible softens the conflict, because the bondholders now share in the upside: if the risky project succeeds and the stock soars, the bondholders convert and take part of the gain. Green (1984, *Journal of Financial Economics*) showed that convertibles can reduce this agency cost, which is why they are common in companies whose value depends on risky, hard-to-monitor investment decisions — young technology and biotech firms, in practice.

**Staged financing (Mayers, 1998).** David Mayers noticed that convertibles fit companies with *sequential* investment opportunities: a project today, and the option to invest in a follow-on project later, but only if the first one works out. Issuing all the money up front invites overinvestment — managers with cash in hand find ways to spend it. Issuing equity in stages is expensive and slow. A convertible solves it: the company raises the money now, and the follow-on financing arrives automatically, *only if* the first project succeeds and the stock rises enough to trigger conversion — at which point the issuer can call the bond and force the conversion, effectively injecting the equity exactly when the good project needs it. Mayers (1998, *Journal of Financial Economics*) called this "the matching of financial and real investment options."

In practice, the bankers on a convertible deal do not cite these papers in the pitch meeting. They cite the coupon saving and the conversion premium. But the theories explain *which* companies the pitch works for: growth companies with uncertain futures, real options, and a genuine disagreement with the market about what the stock is worth. A mature utility with stable cash flows has no reason to issue a convertible — it can borrow cheaply and does not need the optionality.

## 5. Why Investors Buy It: Floor, Upside, and Arbitrage

From the investor's side, the pitch is the asymmetry we computed for NovaTech: if the stock craters, you still hold a bond paying 2% and returning $1,000 at maturity (assuming the company survives — the floor is only as good as the credit behind it); if the stock doubles, you participate in most of the gain. It is equity upside with a bond's downside, and that combination appeals to a specific buyer: the convertible arbitrage hedge fund.

Convertible arbitrage is one of the oldest hedge fund strategies, and it works by exploiting the decomposition directly. The fund buys the convertible and shorts the underlying stock, in proportion to the convertible's delta. If the delta is 0.5, the fund shorts shares equal to half the conversion exposure. Now the position is, in theory, insulated from small stock moves — the gain on the convertible when the stock rises is offset by the loss on the short, and vice versa. What remains is the coupon income, plus the profit from the option's volatility: the fund re-hedges as the delta changes, buying low and selling high in small increments, and collects the difference between the implied volatility it paid for (embedded in the convertible's price) and the volatility that actually occurs. When convertibles are issued cheaply — which happens often, because issuers focus on the coupon and the conversion premium rather than the option value — the arbitrageur's edge is real. When they are issued rich, the edge disappears, and the funds walk away.

There is a catch for ordinary investors: convertibles are usually *subordinated*, *unsecured*, and *callable* by the issuer, and their liquidity is much thinner than either the stock or a plain bond. In a bankruptcy, convertible holders stand behind secured lenders and senior unsecured bondholders. The "safety net" of the bond floor only holds if the company can actually pay its debts — in a genuine distress scenario, the floor falls with the credit, which is exactly when you most wanted it to hold.

## 6. The Call: How Issuers Force Conversion

Most convertibles are callable: after a protection period (typically 3 years, or sometimes none), the issuer can redeem the bonds at a set call price — often par plus a small premium — by giving 30 days' notice. This call right is the issuer's most important tool, and it is routinely misunderstood.

The naive view is that a call is bad for the holder: the issuer takes the bond back. But a call is almost never exercised when the bond is out of the money. Issuers call when the conversion value is *above* the call price. At that point the holder has a choice during the 30-day notice period: surrender the bond for the call price in cash, or convert it into shares worth more. Any rational holder converts. The call therefore *forces conversion* — it lets the issuer extinguish the debt and replace it with equity, on the issuer's timetable rather than the holder's.

This is how the staged financing story ends in practice. NovaTech's stock hits $50, the conversion value is $1,250, and NovaTech calls the bonds at $1,030. Every holder converts. The $500 million of debt vanishes from the balance sheet, 12.5 million new shares appear, and NovaTech never pays the remaining coupons. The company got its cheap financing, the bondholders got their upside, and the debt is gone without a refinancing. The call provision is what turns "maybe equity someday" into "equity, now, when we choose."

## 7. Variations on the Theme

The plain-vanilla convertible is only the starting point. A few variants appear often enough in deals and headlines that you should recognise them:

**Mandatory convertibles.** These convert into shares on a fixed date whether the holder likes it or not — no option, no choice. They are economically a forward sale of equity, and they are used by companies that want equity credit from the rating agencies while delaying the actual dilution. The pricing is a negotiation over the conversion ratio at different stock prices.

**Contingent convertibles (CoCos).** Issued mostly by banks, CoCos convert automatically — or get written down — when the bank's capital ratio falls below a trigger. They are designed to recapitalise a bank precisely when it is in trouble, without a government bailout. They behaved exactly as designed in the Credit Suisse collapse of 2023, when $17 billion of CoCos were written to zero — and the holders discovered, to their fury, that "automatic" means the equity below them in the capital structure was *not* wiped out first. The fine print of a conversion trigger matters more than the marketing.

**Zero-coupon convertibles.** Some convertibles pay no coupon at all and are issued at a deep discount to face value. The investor's return comes entirely from the discount and the conversion option. They are popular with issuers that want to preserve cash at all costs.

**Exchangeables.** Same structure, different stock: the bond converts into shares of *another* company, usually a listed subsidiary or an investment the issuer holds. It is a way to sell a stake gradually, with a coupon attached.

**Startup convertible notes.** In venture capital, a convertible note is the standard bridge instrument: an investor lends a startup money that converts into shares at the next priced funding round, usually at a discount (say 20%) and sometimes with a valuation cap. The logic is identical to the public-market version — nobody can agree on the company's value today, so the note postpones the valuation argument until the next round sets a price. The discount and the cap are the startup world's version of the conversion premium.

## Common Misconceptions

**"Convertibles are free money — cheap debt and no dilution."** No. The coupon saving is the price of the option, and the dilution is real and arrives exactly when the company is doing well — which is when existing shareholders least want to share the upside. A convertible is cheap debt *or* expensive equity, depending on how the stock performs. It is never both at once.

**"The bond floor means I can't lose money."** The floor is the present value of the coupons and principal *assuming the issuer pays*. It is a credit-dependent number, not a guarantee. In distress, the yield on the company's debt spikes, the floor collapses, and the convertible falls with it — at the same time as the conversion value is falling. Convertibles protect you against a falling stock price in a healthy company, not against a failing company.

**"A high conversion premium means the deal is good for shareholders."** A high premium looks shareholder-friendly, because the company is selling future shares at a high price. But the premium and the coupon are a seesaw: a higher premium means a less valuable option, so investors demand a higher coupon. A 40% premium with a 4% coupon may cost the company more than a 25% premium with a 1% coupon. Judge the package, not one term.

**"Issuers call convertibles to hurt bondholders."** Issuers call to force conversion, which is the *good* outcome for holders — it happens precisely when the shares are worth more than the call price. A call is the issuer saying "your option is now so valuable that we would rather you owned the stock." The holders who lose from a call are the ones who wanted to keep collecting coupons — but they were always going to lose the coupons the moment the stock performed.

**"Convertible arbitrage is risk-free because the position is hedged."** The hedge removes small stock moves. It does not remove credit risk, liquidity risk, or the risk that volatility collapses and the option decays. Convertible arbitrage funds lost heavily in 2008, when credit spreads blew out and convertible prices fell far below any model value, because the hedges were in the stock while the losses were in the credit.

## Test Yourself

**1.** A $1,000 convertible bond has a conversion ratio of 20, and the stock trades at $40. What is the conversion price, the conversion value, and the conversion premium? Is the bond in the money?

*Answer: Conversion price = $1,000 / 20 = $50. Conversion value = 20 × $40 = $800. Conversion premium = $50 / $40 − 1 = 25%. The bond is out of the money — the conversion value ($800) is below the face value ($1,000), so no holder would convert today.*

**2.** A 3-year convertible pays a 1% annual coupon ($10) on a $1,000 face value. The issuer's straight-debt yield is 5%. What is the bond floor? Show the calculation.

*Answer: Discount the coupons and principal at 5%. The 3-year annuity factor is (1 − 1.05⁻³) / 0.05 = 2.7232, so the coupons are worth 10 × 2.7232 = $27.23. The principal is worth $1,000 / 1.05³ = $1,000 × 0.8638 = $863.84. Bond floor = $27.23 + $863.84 = $891.07.*

**3.** A convertible has a bond floor of $900 and a conversion value of $1,200. It is trading at $1,260. What is the lowest price it could trade at without creating an arbitrage, and what does the $60 gap represent?

*Answer: The lowest arbitrage-free price is the higher of the two components: max($900, $1,200) = $1,200. Below $1,200, an arbitrageur could buy the bond, convert, and sell the shares for a riskless profit. The $60 gap above $1,200 is the time value of the conversion option — the value of the chance that the stock rises further before maturity.*

**4.** A company issues $300 million of convertibles at a 1.5% coupon instead of straight debt at 6%, with a conversion ratio of 30 shares per $1,000 bond and 80 million shares outstanding. (a) How much coupon does it save per year? (b) How many new shares appear if all bonds convert, and what percentage of the current share count is that?

*Answer: (a) The coupon saving is (6% − 1.5%) × $300 million = $13.5 million per year. (b) $300 million / $1,000 = 300,000 bonds × 30 shares = 9 million new shares, which is 9 / 80 = 11.25% of the current share count. That dilution is the true cost of the cheap coupon — and it arrives exactly when the stock has risen enough to make conversion attractive.*

---

*Next up: 35 | Preferred Stock and Hybrid Capital: The Layer Between Debt and Equity.*
