# 35 | Preferred Stock and Hybrid Capital: The Layer Between Debt and Equity

*Article 34 was about a bond that can turn into stock. This one is about a security that never quite decides what it is — preferred stock, the layer of the capital structure that sits between debt and equity and belongs fully to neither. It pays a fixed dividend like a bond's coupon, but the payment can be skipped like a common dividend. It ranks ahead of common stock in a liquidation, but behind every bond. Bankers reach for it when a company needs capital that is sturdier than debt but less dilutive than common equity, and regulators love it for banks for exactly the same reason. The puzzle is that, on a first look at the tax code, preferred stock should barely exist at all — and understanding why it does anyway tells you a lot about how capital structure really works.*

> **Learning goals.** After this article you can: (1) explain what preferred stock is and where it sits in the capital structure; (2) value a preferred share as a perpetuity and explain why a call provision caps its price; (3) explain the tax wedge — why dividends are not deductible for the issuer but are partly tax-free for a corporate buyer; (4) compute a WACC that includes a preferred layer; (5) describe the main hybrid instruments — trust preferreds, junior subordinated debt, and CoCos — and why banks issue them; (6) explain what "equity credit" from a rating agency means and why it matters.
>
> **Prerequisites.** Article 03 (enterprise value vs equity value) for the capital structure stack; article 06 (DCF I) for discounting and WACC; article 20 (debt capital markets) for how bonds are priced and sold; article 25 (leveraged finance) for subordinated debt; article 34 (convertible bonds) for the idea of a hybrid security; article 30 (credit ratings) for how agencies think about leverage.

## 1. The Layer Between

Every company has a pecking order of claims on its cash flows, and we have now met most of it. At the top sit the secured lenders, then senior unsecured bondholders, then subordinated debt. At the very bottom sit the common shareholders, who get whatever is left. Preferred stock lives in the gap between subordinated debt and common equity — senior to the common, junior to all the debt.

A **preferred share** is a share of stock with a fixed dividend, usually quoted as a percentage of a fixed **par value** (often $25 for retail issues, $1,000 for institutional ones). The dividend is stated, not promised in the way a bond coupon is: if the company fails to pay a bond coupon, it is in default and creditors can force it into bankruptcy; if it fails to pay a preferred dividend, nothing of the sort happens — the dividend is simply skipped, and the consequences depend on the fine print. The preferred holder usually has no vote, no say in management, and no share in the upside if the company does brilliantly. What the preferred holder gets is priority: the preferred dividend must be paid before a single cent of common dividend, and in a liquidation the preferred holders are repaid their par value before common shareholders see anything.

That combination — a fixed return, priority over common, and no vote — is why the security exists. It is the claim for an investor who wants more yield than a bond of the same issuer but is willing to accept a weaker legal position to get it, and for an issuer who wants capital that behaves like equity to a rating agency and a regulator but does not dilute the common shareholders' control the way a new share issue would.

The first thing to notice is how thin the market is compared with debt and common equity. In the United States, most preferred stock is issued by banks, insurers, utilities, and REITs — companies whose business is either regulated capital (banks and insurers) or steady, dividend-paying assets (utilities and REITs). Industrial companies rarely issue it, and the reason is the tax code, which we will get to in section 4.

## 2. The Anatomy: Par, Rate, and the Fine Print

Every preferred issue is described by a small set of terms, and — as with convertibles — each term is doing real work.

**Par value and dividend rate.** A typical issue might be "$25 par, 6%." That means each share pays 6% of $25, or $1.50 a year, usually in quarterly instalments of $0.375. The 6% is a rate on par, not on the market price: if the share later trades at $21, the yield on the market price is $1.50 / $21 = 7.14%, but the dividend itself never changes.

**Cumulative vs non-cumulative.** This is the single most important term. If a preferred is **cumulative**, a skipped dividend accumulates as **dividends in arrears**, and the company must pay all of the arrears, plus the current dividend, before it can pay anything to common shareholders. If it is **non-cumulative**, a skipped dividend is gone forever. Most bank preferred stock issued today is non-cumulative, and that is not an accident: regulators require it, because a dividend the bank *must* eventually pay is a liability in disguise, while a dividend it can skip permanently is genuine loss-absorbing capital. The trade-off is priced: non-cumulative preferreds yield more than cumulative ones from the same issuer.

**Participating vs non-participating.** A **participating** preferred gets its fixed dividend *plus* a share of any extra dividends paid to common shareholders above some threshold. Almost all modern preferreds are non-participating — the holder's upside is capped at the fixed dividend, full stop.

**Callable.** Nearly all preferreds are **callable** by the issuer, typically at par after five years. The call is the issuer's escape hatch: if rates fall, the company can redeem the expensive preferred and reissue cheaper. For the investor it is a ceiling on the price, which is the point of the worked example below.

**Convertible.** Some preferreds convert into common stock, just like the convertible bonds in article 34 — usually at the holder's option, at a fixed conversion ratio. **Convertible preferred** was once a common way to finance growth companies; today it is mostly a niche product, because the convertible bond does the same job with a tax-deductible coupon.

**Voting rights.** Preferred holders normally do not vote. The exception is the tripwire: if the company skips dividends for a specified number of quarters (often six), preferred holders typically gain the right to elect a minority of directors. It is a weak right, but it is the only leverage a skipped preferred holder has.

Put the terms together and you can see the security for what it is: a perpetual, fixed-income claim with an equity label. It has no maturity date — the company never has to repay the par value unless it chooses to call the shares — which is precisely why regulators and rating agencies treat it as equity-like. A bond must be repaid; a preferred never has to be.

## 3. Worked Example: Valuing a Preferred Like a Perpetuity

Because a preferred share pays a fixed dividend forever, with no maturity and no growth, its value is the simplest formula in all of valuation: a perpetuity.

```math
Price = \\frac{Annual\\ dividend}{Required\\ return}
```

Take Harbor Bank, which issues a $25 par preferred paying 6%, so the annual dividend is $25 × 6% = $1.50. Suppose investors require a 7% return on this security — a bit more than Harbor's senior bonds yield, because the preferred is junior and its dividend can be skipped. Then:

```math
Price = \\frac{\\$1.50}{0.07} = \\$21.43
```

The share trades below par, at $21.43, because the required return (7%) is above the dividend rate (6%). Now suppose the market's required return falls to 5% — rates have dropped, or Harbor's credit has improved. Then:

```math
Price = \\frac{\\$1.50}{0.05} = \\$30.00
```

A two-percentage-point fall in the required return lifts the price by 40%, from $21.43 to $30.00. That is the duration risk of a perpetual security: with no maturity date, every future dividend matters, so the price is extremely sensitive to the discount rate. A 30-year bond has the same property in milder form; a preferred has it in full.

Now add the call. Suppose Harbor's preferred is callable at $25 after five years, and rates fall so that the perpetuity formula says the share is worth $30. Would you pay $30 for it? No — because Harbor can redeem it from you for $25 at the next call date. The market price will not rise much above $25; the call caps the upside. In practice the price hovers a little above the call price, reflecting the dividends you collect before the call happens. This is **yield-to-call**: when a callable preferred trades near its call price, investors stop pricing it as a perpetuity and start pricing it as a short-dated instrument that will be redeemed at $25.

One more wrinkle, and it is a common exam trap: the formula assumes the dividend is safe. It is not. The dividend can be skipped, and the price must reflect the probability that it is. A preferred from a shaky issuer is not a perpetuity at all — it is a perpetuity *conditional on the issuer staying healthy*, which is why distressed preferreds trade at deep discounts to the formula. The formula is the starting point, not the answer.

## 4. The Tax Wedge: Why Issuers Hate It and Corporate Buyers Love It

Here is the puzzle. A bond coupon is tax-deductible for the issuer; a preferred dividend is not. On a first pass, no rational company should ever issue preferred stock — it is strictly more expensive than debt after tax. And for most industrial companies, that is exactly the conclusion they reach. The security survives because of two exceptions to that logic, one on each side of the trade.

**The issuer's side.** A company issues preferred when it cannot issue more debt — because its credit rating would suffer, its covenants forbid it, or its regulator requires equity — but does not want to issue common equity, because that dilutes existing shareholders and sends a bad signal. (Myers and Majluf showed in 1984 that issuing common equity signals management believes the stock is overvalued; the market reaction to a preferred issue is far milder — Smith's 1986 survey found that announcements of preferred stock issues drew much smaller negative stock-price reactions than common stock issues, which fell by roughly 3% on average for industrial firms.) Preferred is the compromise: it counts as equity with the rating agencies and the regulators, but it does not dilute voting control and does not carry the adverse-selection stigma of a common issue.

How much does the compromise cost? Take a company with $1,000 million of capital: $400 million of debt at 5%, $100 million of preferred paying 6.5%, and $500 million of common equity costing 10%. The tax rate is 21%. The WACC is:

```math
WACC = w_d \\times r_d \\times (1 - T) + w_p \\times r_p + w_e \\times r_e
```

```math
WACC = 0.40 \\times 5\\% \\times (1 - 0.21) + 0.10 \\times 6.5\\% + 0.50 \\times 10\\%
```

```math
WACC = 1.58\\% + 0.65\\% + 5.00\\% = 7.23\\%
```

Now replace the preferred with straight debt at the same 5% rate. Debt becomes $500 million, equity stays $500 million:

```math
WACC = 0.50 \\times 5\\% \\times 0.79 + 0.50 \\times 10\\% = 1.98\\% + 5.00\\% = 6.98\\%
```

And replace it with common equity instead: debt $400 million, equity $600 million:

```math
WACC = 0.40 \\times 5\\% \\times 0.79 + 0.60 \\times 10\\% = 1.58\\% + 6.00\\% = 7.58\\%
```

The ordering is exactly what the tax code predicts: debt is cheapest (6.98%), preferred sits in the middle (7.23%), and common equity is dearest (7.58%). The preferred layer costs the company an extra 25 basis points of WACC versus funding the same $100 million with debt — the price of the tax shield it gives up. Companies pay that price only when the debt route is closed to them, which is why the market is dominated by banks and insurers whose regulators *require* equity-like capital, and by utilities whose regulators effectively cap their debt.

**The buyer's side.** The reason anyone buys preferreds at a 6.5% yield when the same issuer's bonds yield 5% is not just the extra 150 basis points — it is the **dividends received deduction**, or DRD. Under Section 243 of the Internal Revenue Code, a corporation that receives dividends from another domestic corporation may deduct 50% of the dividend from its taxable income (65% if it owns 20% or more of the payer). Individuals get no such deduction; corporations do. Watch what that does to the after-tax return.

Suppose an insurance company buys $10 million of Harbor Bank preferred paying 6%, collecting $600,000 a year in dividends. With the 50% DRD, only $300,000 is taxable, and at the 21% corporate rate the tax is $63,000. The after-tax income is $537,000 — an after-tax yield of 5.37%. The same $10 million in a Harbor bond paying 6% would produce the same $600,000, but fully taxable: $126,000 of tax, $474,000 after tax, a 4.74% after-tax yield. The preferred wins by 63 basis points after tax, even though the two securities pay the same coupon.

The breakeven makes the point sharper. A corporate buyer is indifferent between a bond yielding 6% and a preferred yielding $y$ when their after-tax yields match:

```math
y \\times (1 - 0.50 \\times 0.21) = 6\\% \\times (1 - 0.21)
```

```math
y = \\frac{4.74\\%}{0.895} = 5.30\\%
```

The insurer will accept a preferred yielding just 5.30% over a bond yielding 6%. That 70-basis-point gap is the DRD at work, and it is the reason the preferred market clears: issuers pay more than their bond yield, corporate buyers accept less than a bond yield, and the tax code funds the difference. It is also the reason the retail $25-par market and the institutional market behave differently — the retail buyer, taxed as an individual, gets no DRD and needs the full yield to compensate for the junior position.

## 5. Hybrid Capital: When the Layer Gets Engineered

Preferred stock is the original hybrid, but bankers have spent forty years engineering variations that keep the equity-like treatment while recovering the tax deduction that plain preferred gives up. Three of them matter.

**Trust preferred securities (TruPS).** The cleverest and now mostly extinct. A bank holding company set up a trust, the trust issued preferred securities to investors, and the bank issued junior subordinated debt to the trust. The investors' payments were legally interest on the bank's debt — tax-deductible for the bank — but the trust's securities counted as Tier 1 regulatory capital, because they were preferred in form. At the peak, around year-end 2008, roughly 1,400 bank holding companies had issued over $148 billion of TruPS. The lunch ended with the Dodd-Frank Act of 2010: the Collins Amendment phased TruPS out of Tier 1 capital for bank holding companies with more than $15 billion in assets, over three years starting in 2013, and most were gone by the end of 2015. The lesson is one bankers relearn every cycle: a security whose entire value comes from a regulatory classification dies when the classification changes.

**Junior subordinated debt.** The successor. A deeply subordinated bond with a very long maturity (often 30 to 60 years, sometimes perpetual), with the issuer allowed to defer interest for up to five years. The interest is tax-deductible, which makes it cheaper than preferred; the rating agencies give it partial equity credit, because it is subordinated, long-dated, and deferrable. Moody's, for example, assigns qualifying corporate hybrids 50% equity credit — it treats half the issue as equity when it computes leverage. In 2024 Moody's raised that treatment for U.S.-issued subordinated hybrids from 25% to 50%, which set off a wave of new issuance. The catch is the fine print the agencies police aggressively — if the deferral right is too easy to use, or the call language too generous to the issuer, the equity credit drops to zero, sometimes overnight.

**Contingent convertibles (CoCos) and AT1.** The bank version, and the most important hybrid in the world today. Under Basel III, a bank's capital stack is 4.5% common equity Tier 1 (CET1), plus 1.5% Additional Tier 1 (AT1), plus 2% Tier 2 — an 8% minimum in total. AT1 is filled with perpetual, non-cumulative preferred shares and CoCos: bonds that convert into equity, or are written down to zero, when the bank's CET1 ratio falls below a trigger (commonly around 7%). The conversion is automatic and mechanical — no board vote, no negotiation, no bankruptcy filing. When Credit Suisse collapsed in March 2023, roughly $17 billion of its AT1 CoCos were written down to zero, exactly as designed — and the holders discovered, to their fury, that the equity below them was *not* wiped out first.

The trigger math is simple and worth doing once. A bank with $100 billion of risk-weighted assets and a 12% CET1 ratio holds $12 billion of common equity. A CoCo with a 7% trigger converts when CET1 falls below $7 billion — that is, after the bank has lost more than $5 billion. The CoCo holder is betting the bank will not lose $5 billion before the trigger saves it; the bank is betting it will never need the trigger.

Why does all of this exist? Modigliani and Miller showed in 1958 that, in a world without taxes, bankruptcy costs, or regulation, the mix of debt and equity does not change a firm's value at all. Every hybrid in this article is a response to one of the frictions M&M assumed away: the tax code makes debt cheaper than equity, regulators require banks to hold equity-like capital, rating agencies reward instruments that look like equity, and information asymmetry makes common equity expensive to issue. Preferred stock and its engineered cousins are not violations of M&M; they are the market's answer to the question M&M posed.

## 6. Who Issues, Who Buys

The pattern of issuance follows the logic of the last two sections. Banks issue preferred and CoCos because regulators force them to hold AT1 capital and the coupon is cheaper than issuing common equity. Insurers issue preferred because their regulators like it and their own investment portfolios are full of other insurers' preferreds — the DRD makes the whole sector a natural buyer of its own paper. Utilities issue it because they are steady, regulated, dividend-paying businesses whose capital structure is effectively negotiated with a regulator. REITs issue it because they must pay out most of their income as dividends anyway, so the non-deductibility of preferred dividends costs them nothing.

The buyers split into two markets that barely touch. The **retail market** trades in $25-par shares on the NYSE, in small lots, bought by individual investors hunting for yield. These shares behave like long-dated bonds with a call cap, and their prices swing with interest rates — the perpetuity math from section 3 is the whole story. The **institutional market** trades in $1,000-par shares, in blocks, bought by insurers and other corporations for the DRD, and by banks for capital treatment. The two markets can price the same issuer's preferreds differently, because the buyers are buying different things: the retail buyer is buying yield, the corporate buyer is buying an after-tax yield, and the bank buyer is buying regulatory capital.

## Common Misconceptions

**"Preferred stock is safe because it pays a fixed dividend."** The dividend is fixed in amount, not in payment. A non-cumulative preferred's skipped dividend is gone forever, and even a cumulative preferred's arrears are only paid if the company recovers. In a genuine distress, the preferred holder is an equity holder with a fixed claim — and fixed claims on a failing company are worth whatever the liquidation produces, which is often very little.

**"Preferreds are just like bonds, so I can compare their yields directly."** You can compare yields only after adjusting for taxes and for the call. A 6% preferred and a 6% bond from the same issuer are not the same return: the bond's interest is taxed in full for every holder, the preferred's dividend is partly deductible for corporate holders and taxed as a qualified dividend for individuals, and the preferred is callable at par, which caps its upside when rates fall. The right comparison is after-tax yield-to-call, not headline yield.

**"The tax deduction makes hybrids always cheaper than preferred."** Cheaper for the issuer, yes — but the rating agencies and regulators do not give a junior subordinated bond the same equity credit as a preferred share, and the market charges a higher yield for a security whose coupon can be deferred for five years. A hybrid that gets 50% equity credit instead of 100% may cost the issuer its credit rating, which is a far larger cost than the tax saving. The cheapest security on a pre-tax basis is not the cheapest once regulation and ratings are counted.

**"A high preferred dividend means the company is generous."** A high dividend rate on a new preferred usually means the market demands it — because the issuer is risky, rates are high, or the security is non-cumulative. A 9% preferred from a solid bank would be a gift; a 9% preferred from a shaky one is the market pricing the chance the dividend gets skipped. Read the yield as a price of risk, not as a reward.

**"M&M says capital structure doesn't matter, so hybrids are a waste of time."** M&M says capital structure does not matter *in a frictionless world*. Taxes, regulation, bankruptcy costs, and information asymmetry are the frictions, and they are the whole game. Hybrids exist precisely because the world has frictions — a world without them would have no preferred stock, no CoCos, and no TruPS. The theorem is not an argument against hybrids; it is the tool that tells you *which* friction each hybrid is exploiting.

## Test Yourself

**1.** Harbor Bank's $25 par preferred pays a 6% dividend ($1.50 a year). (a) If investors require a 6.25% return, what is the fair price? (b) If the required return falls to 5%, what is the fair price? (c) If the preferred is callable at $25, what happens to your answer in (b)?

*Answer: (a) Price = $1.50 / 0.0625 = $22.00. (b) Price = $1.50 / 0.05 = $30.00. (c) The price will not rise to $30 — Harbor can redeem the shares for $25, so the market price caps out near the $25 call price (plus a little for the dividends collected before the call). The call turns a perpetuity into a short-dated instrument.*

**2.** A company has $300 million of debt at 4.5%, $150 million of preferred paying 7%, and $550 million of equity costing 11%. The tax rate is 21%. (a) What is the WACC? (b) If the preferred were replaced with debt at 4.5%, what would the WACC be — and why is the difference the tax shield?

*Answer: (a) Total capital is $1,000 million, so the weights are 0.30, 0.15, and 0.55. WACC = 0.30 × 4.5% × (1 − 0.21) + 0.15 × 7% + 0.55 × 11% = 1.0665% + 1.05% + 6.05% = 8.17%. (b) Debt becomes $450 million and equity $550 million: WACC = 0.45 × 4.5% × 0.79 + 0.55 × 11% = 1.60% + 6.05% = 7.65%. The 52-basis-point saving has two pieces: the coupon gap — debt costs 4.5% where the preferred costs 7%, worth 2.5% × 0.15 = 37.5bp — plus the tax shield on the new debt's interest, worth 21% × 4.5% × 0.15 = 14.2bp. Together that is about 52bp. The company pays the extra WACC only if it needs the preferred's equity treatment from a rating agency or regulator.*

**3.** An insurance company buys $2 million of preferred stock paying 6.5% a year. The corporate tax rate is 21% and the dividends received deduction is 50%. (a) What is the after-tax income and after-tax yield? (b) What would the after-tax yield be on a bond paying the same 6.5%? (c) What preferred yield would leave the insurer indifferent between the preferred and a 6.5% bond?

*Answer: (a) The dividend is $2,000,000 × 6.5% = $130,000. With the 50% DRD, $65,000 is taxable, so the tax is $65,000 × 21% = $13,650, after-tax income is $116,350, and the after-tax yield is $116,350 / $2,000,000 = 5.82%. (b) The bond's $130,000 is fully taxable: tax is $27,300, after-tax income is $102,700, an after-tax yield of 5.14%. (c) The breakeven preferred yield y solves y × (1 − 0.5 × 0.21) = 6.5% × (1 − 0.21) = 5.135%, so y = 5.135% / 0.895 = 5.74%. The insurer accepts a preferred yielding 5.74% over a bond yielding 6.5% — the DRD is worth 76 basis points.*

**4.** A company is liquidated for $90 million. Its capital structure is: $60 million of senior debt, $20 million of subordinated debt, $40 million par of cumulative preferred (which has two years of unpaid $2-per-share dividends, with 1 million shares outstanding), and common stock. (a) How much does each layer receive? (b) Before the liquidation, how much would the company have to pay the preferred holders before it could resume paying a common dividend?

*Answer: (a) Senior debt is paid first: $60 million, leaving $30 million. Subordinated debt is next: $20 million, leaving $10 million. The preferred holders are owed $40 million of par plus $4 million of arrears (2 years × $2 × 1 million shares), but only $10 million remains, so they receive $10 million — 25 cents on the dollar of their par claim — and the common shareholders receive nothing. (b) The arrears are 2 × $2 × 1,000,000 = $4 million, plus the current year's $2 million dividend: the company must pay $6 million to the preferred holders before a single cent can go to the common. If the preferred were non-cumulative, the arrears would be zero and only the current $2 million would stand in the way — which is exactly why cumulative preferreds yield less than non-cumulative ones.*

---

*Next up: 36 | CLOs and Structured Credit: How Loans Become Bonds.*

---

**Papers cited**

- Modigliani, F. & Miller, M. (1958). *The Cost of Capital, Corporation Finance and the Theory of Investment.* American Economic Review, 48(3), 261–297. — In a frictionless world, capital structure does not change firm value; every hybrid in this article is a response to a friction M&M assumed away.
- Smith, C. W. (1986). *Investment Banking and the Capital Acquisition Process.* Journal of Financial Economics, 15(1–2), 3–29. — Announcements of preferred stock issues drew far smaller negative stock-price reactions than common stock issues, which fell roughly 3% on average for industrial firms.
- Myers, S. & Majluf, N. (1984). *Corporate Financing and Investment Decisions When Firms Have Information That Investors Do Not Have.* Journal of Financial Economics, 13(2), 187–221. — Why issuing common equity signals bad news, and why preferred sits lower on the adverse-selection scale.
