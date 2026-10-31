# 21 | Hostile Takeovers and Takeover Defenses: When the Board Says No

*Every deal so far started with both boards willing to talk. This one starts with an unasked-for letter, a board that says no, and a bidder who goes over the board's head to the shareholders directly. It is the messiest corner of M&A, and the most revealing: it forces you to answer who really owns a company, what a board is for, and how much protection from being bought is too much.*

> **Learning goals.** After this article you can: (1) explain the market for corporate control and why a hostile bid can discipline managers; (2) walk through a tender offer and a proxy fight, and do the arithmetic of a premium, a control threshold, and a poison pill; (3) explain the main takeover defenses and what each one actually blocks; (4) explain the Delaware rules governing defenses — *Unocal* and *Revlon* — in plain terms; (5) weigh the bargaining-chip versus entrenchment arguments against the evidence.
>
> **Prerequisites.** Article 05 (precedent transactions and control premiums) for why buyers pay more than the market price, article 11 (sell-side process) for how a friendly sale normally runs, and article 12 (buy-side) for synergy logic. No new valuation model is introduced here; the math is share counts, percentages, and premiums.

## 1. Who Owns the Company, Really?

Start with a simple, slightly uncomfortable fact. In a public company, the managers run the place day to day, but they do not own it. The shareholders do. That separation — ownership in one set of hands, control in another — is the oldest tension in corporate finance, and it is the reason hostile takeovers exist at all.

Here is the intuition, first put in its classic form by Henry Manne. Suppose shares trade at $40, but under better management the same assets would be worth $60. That $20 gap is an invitation: a bidder that can close it can offer, say, $52 — a premium over $40, a bargain against $60 — and profit from the difference. If managers are doing a good job, the gap is small and no bidder bothers. If they are doing a bad job, the gap is large and the company becomes a target. The *threat* of a takeover thus disciplines managers even when no bid ever arrives.

That is the optimistic version, and it has a name: the **market for corporate control**. Manne, H. G. (1965). *Mergers and the Market for Corporate Control.* Journal of Political Economy, Vol. 73, No. 2, pp. 110–120 — verified by web search before citing.

But the optimistic version is not the whole story. A bidder might also want a target to eliminate a competitor, grab a crown-jewel asset, empire-build, or simply because its own management is overconfident — the hubris story from article 05. A premium is not proof that a deal creates value; it is proof that the bidder is willing to pay. And a board that says no is not automatically entrenched; it might genuinely believe the offer undervalues the company, or that a better offer is coming. The rest of this article is about how those two stories collide, and what tools each side gets.

One definitional point before we go further. A **friendly deal** is negotiated with the target board and recommended to shareholders. A **hostile deal** is one the target board opposes, so the bidder goes directly to shareholders instead. "Hostile" describes the board's posture, not the bidder's manners. Hostile bids can be polite, fully financed, and above the market price; friendly deals can be rushed and bad. Keep the label where it belongs: on the relationship between bidder and board.

## 2. The Two Hostile Routes: Tender Offer and Proxy Fight

A bidder that cannot get through the front door has two ways in. In practice the two are often used together, as a pincer.

### The tender offer: buy the shares directly

A **tender offer** is a public offer to buy shareholders' shares at a stated price, for a stated period, usually conditional on enough shares being tendered. The bidder does not need the board's permission to make the offer. It needs the shareholders' shares.

Work through a clean example, because the arithmetic is the whole game. Imagine a target with 100 million shares outstanding, trading at $40 before any bid — the *unaffected price*, the price before the market knew a bid was coming. Its market capitalisation is therefore:

```math
100{,}000{,}000 \times \$40 = \$4{,}000{,}000{,}000
```

Now the bidder offers $52 per share. The premium is:

```math
\text{Premium} = \frac{52 - 40}{40} = 0.30 = 30\%
```

If every shareholder tenders, the bidder pays:

```math
100{,}000{,}000 \times \$52 = \$5{,}200{,}000{,}000
```

That is $1.2 billion above the pre-bid market value. Control, though, does not require 100%. It requires just over half the votes: 50,000,001 shares. Tendering for only that control block would cost about:

```math
50{,}000{,}001 \times \$52 \approx \$2{,}600{,}000{,}000
```

Two consequences fall out of those numbers. First, the premium is the price of control, and it is expensive: the bidder must believe the deal creates more than $1.2 billion of value (before fees, after tax) if it buys the whole company, or it is transferring wealth from its own shareholders to the target's. Second, shareholders face a real decision. Tendering at $52 locks in a 30% gain over $40. Refusing means betting the board is right that the company is worth more standalone — or that a higher bid will come. The board's "just say no" stance has teeth only if shareholders believe it.

A **bear hug** is the softer cousin of a tender offer: a public letter from the bidder to the board, announcing a premium offer and inviting negotiation. It is called a bear hug because it is hard to wriggle out of gracefully — once shareholders know a $52 offer exists, a board that rejects it without explanation has some explaining to do.

### The proxy fight: win the boardroom instead

A **proxy fight** (or proxy contest) attacks the problem from the other end. Instead of buying shares, the bidder asks shareholders to vote its own slate of directors onto the board at the annual meeting. Shareholders vote by *proxy* — they send in their votes without attending — so the fight is really a campaign for those proxy cards. Win a majority of the board, and the new board can remove the defenses and approve the deal.

The proxy fight matters for a reason that is easy to miss: it is often the *only* way past a poison pill, as we will see next. A tender offer alone cannot beat a well-designed pill, because the pill punishes the buyer. But a newly elected board can redeem — cancel — the pill. So the classic hostile playbook combines both: a tender offer to put a price on the table, and a proxy contest to install directors who will accept it. The bidder asks shareholders two questions at once: do you want $52, and do you want directors who will take it?

That combination also explains the timetable. A tender offer can be launched in weeks. A proxy fight must wait for an annual meeting, and a staggered board can force the bidder to wait for two of them. Time is a weapon in hostile deals, and it usually favours the defence.

## 3. The Defence Toolkit: What Each Defence Actually Blocks

Target boards do not improvise. They draw on a well-stocked toolkit, most of it put in place long before any bidder appears. Here are the main pieces, in the order a banker would think about them.

### The poison pill: dilution as a deterrent

The **poison pill** — formally, a shareholder rights plan — is the single most important defence, and the most misunderstood. It does not literally poison anything. It threatens to dilute any bidder who crosses a threshold (commonly 10–20%) without board approval.

Here is the mechanism, simplified but arithmetically honest. Every shareholder gets a *right*. If an unapproved bidder crosses, say, 15%, the rights held by everyone *except* the bidder become exercisable: each right lets its holder buy one new share at half the market price. Run the numbers on our example company. Before the pill triggers, the bidder owns 15 million of 100 million shares — 15%. The other shareholders hold 85 million rights, and they exercise them, buying 85 million new shares at $26 (half of $52). The share count becomes:

```math
100{,}000{,}000 + 85{,}000{,}000 = 185{,}000{,}000
```

And the bidder's stake collapses, not because it sold anything, but because the denominator exploded:

```math
\frac{15{,}000{,}000}{185{,}000{,}000} \approx 0.081 = 8.1\%
```

To get back to a majority of the new, larger share count, the bidder would need more than 92.5 million shares — it currently has 15 million, so it would need about 77.5 million more. The pill does not make a takeover impossible in some metaphysical sense. It makes it *prohibitively dilutive* to buy control on the open market or by tender without board approval. That is why the proxy fight matters so much: a board elected by shareholders can redeem the pill and let the deal through. A pill without a staggered board delays a bidder; a pill *with* one can stop it for years.

Note what the pill does not do. It does not stop shareholders from selling if the board agrees to a deal, and it does not protect the share price. It hands the board enormous power to say no, which is exactly why courts and shareholders argue about it so much.

### The staggered (classified) board: time as a wall

In a **staggered board**, directors serve three-year terms in three classes, with only one class — about a third of the board — up for election each year. Take a nine-person board: three seats are contested each year. A bidder that wins every contested seat in year one still holds only three of nine seats — a minority. It must win again the following year to reach six of nine, a majority.

So a staggered board does not block a bid directly. It stretches the proxy fight across two election cycles, roughly one to two years. Combined with a pill, that delay is devastating: the bidder must win two campaigns and keep its financing committed, while the board has time to find alternatives. Bebchuk, Coates, and Subramanian studied exactly this combination. In their sample of hostile bids from 1996–2000, not a single hostile bidder won a ballot-box victory against an *effective* staggered board (a staggered board combined with a pill), its presence nearly doubled the odds that a target stayed independent, and target shareholders ended up worse off by roughly 8–10% in their estimates. Bebchuk, L. A., Coates, J. C. IV, & Subramanian, G. (2002). *The Powerful Antitakeover Force of Staggered Boards: Theory, Evidence, and Policy.* Stanford Law Review, Vol. 54, pp. 887–951 — verified by web search before citing. Treat that 8–10% as an estimate from one period, not a law of nature; the mechanism itself is pure election-calendar arithmetic.

### The rest of the toolkit

| Defence | What it does | What it really blocks |
|---|---|---|
| **Golden parachute** | Large severance payments to executives if control changes and they leave | Raises the cost of a deal slightly; mainly softens management's personal downside, which cuts both ways |
| **Supermajority vote** | Requires, say, 80% shareholder approval for a merger, not a simple majority | Makes a bare-majority win insufficient; the bidder must win over nearly everyone |
| **White knight** | Board invites a friendlier buyer to make a competing offer | Gives shareholders an alternative price and the board a reason to say no to the first bidder |
| **White squire** | A friendly investor buys a large minority stake to block a hostile bidder | Makes the control threshold harder to reach without a full competing bid |
| **Crown jewel defence** | Target sells or commits to sell its most attractive asset if a hostile bid succeeds | Destroys the prize the bidder wanted, so the bid loses its logic |
| **Pac-Man defence** | Target turns around and bids for the bidder | Rare, expensive, and usually theatrical — but it changes the negotiation dynamic |
| **Scorched earth** | Target takes on debt, sells assets, or otherwise makes itself less attractive | Raises the bidder's cost or lowers the target's value; shareholders pay for it too |
| **Dual-class shares** | Founders hold super-voting shares (e.g., 10 votes each) | Makes a hostile takeover nearly impossible without the controller's consent — no defence needed, because control was never really for sale |

Notice the pattern. Every defence works by raising the bidder's cost, delaying the bid, or reducing what the bidder gets. None of them works by making the target more valuable. That asymmetry is the heart of the debate in section 5.

## 4. What Delaware Allows: Unocal and Revlon in Plain Terms

Most large US public companies are incorporated in Delaware, so Delaware courts set the rules of this game. Two cases frame almost every defence decision. They are reasonableness tests, not checklists.

**Unocal (1985): a board may defend itself, but the defence must fit the threat.** Directors must show, first, reasonable grounds for believing a danger to corporate policy and effectiveness existed, and second, a response reasonable in relation to that threat — proportionate, not scorched-earth for a mild threat. A pill adopted against a coercive, low-ball, two-tier offer (front-end cash, back-end junk securities, designed to stampede shareholders into tendering early) looks very different from a pill maintained forever against a full, fairly priced, all-cash offer after shareholders have had their say. The court's question is not "did the board have a defence?" but "was *this* defence, maintained for *this* long, reasonable against *this* threat?"

**Revlon (1986): once a sale is inevitable, the board's job changes.** When a break-up or change of control has become inevitable, the board's role shifts from defender of the enterprise to auctioneer. Its duty becomes getting the highest price reasonably available, and it may not favour one bidder for reasons unrelated to shareholder value (loyalty to management, a favourite buyer, a desire to keep the company intact). A board that has decided to sell cannot simply hand the company to a white knight at a lower price because it likes the knight better; it must run something recognisably like an auction, or explain why not.

Put together, the two cases draw a line bankers live by: a board can say "not at this price, not on these terms, not yet" — and use defences to buy time to prove it — but it cannot say "never, to anyone, at any price" once the game has clearly become a sale. Where that line falls in any given fight is, famously, litigated, and that uncertainty is itself part of the defence.

A caution: this is Delaware doctrine in general terms. Other states differ, some favouring boards more, and charter provisions can change the picture. Treat *Unocal* and *Revlon* as the starting framework for the most common case, not universal law.

## 5. Do Defences Help Shareholders? The Honest Argument, Both Ways

This is where the article earns its keep, because both sides have a real point and the evidence does not settle it cleanly.

**The bargaining-chip argument.** A board with no defences has no leverage. A bidder can make a low-ball offer, threaten to go hostile, and pick the company up cheaply before a competing bidder hears about it. A pill and a staggered board buy time: to negotiate a higher price, find a white knight, or publish results proving the standalone plan is worth more. On this view, defences do not prevent sales; they prevent *cheap* sales.

**The entrenchment argument.** The same tools that buy negotiating time also buy job security for managers who deserve to lose their jobs. A board that can block any bid indefinitely never faces the market for corporate control, and shareholders pay for that comfort in a lower share price. The evidence leans this way more often than defence advocates admit. Gompers, Ishii, and Metrick built a governance index from 24 provisions — many of them takeover defences — across about 1,500 large firms in the 1990s, and found firms with the strongest shareholder rights outperformed firms with the weakest by an abnormal 8.5% per year in their sample, alongside higher firm value and fewer value-destroying acquisitions. Gompers, P. A., Ishii, J. L., & Metrick, A. (2003). *Corporate Governance and Equity Prices.* Quarterly Journal of Economics, Vol. 118, No. 1, pp. 107–155 — verified by web search before citing.

Read that result with care. It is an association in a specific decade, and the authors are careful about causality: firms with weak shareholder rights might be weak for other reasons, and the market may have been learning to price governance in the 1990s in a way it would not repeat. It does not prove that removing one pill from one company adds 8.5% a year. Combined with the staggered-board evidence, though, it shifts the burden of proof. If you claim a defence helps *these* shareholders, *this* time, say how: what higher price, from whom, by when? "Trust us, we are protecting you" is not an answer, because the defence itself removes shareholders' ability to check.

A practical rule of thumb falls out of this debate. Defences that *delay* a bid and force a real negotiation or auction tend to help shareholders. Defences that *permanently* block a bid, or survive after shareholders have voted for change, tend to hurt them. The difference is not the tool — a pill can do either — it is how long the board holds it, and whether shareholders ultimately get a vote that counts.

## 6. The Banker's Job in a Hostile Fight

Hostile deals are where the M&A banker's role splits most visibly in two, and it is worth seeing both sides, because you may sit on either.

**On the bidder's side**, the banker builds the case for the price (article 05's premiums, article 06's DCF, article 08's affordability logic — a hostile bidder still cannot pay more than the deal is worth to it), lines up financing that survives a long fight, drafts the tender offer and proxy materials, and counts votes the way a campaign counts delegates. The bidder's banker must also be honest about the downside: a hostile win can leave you owning a demoralised company, key staff may leave, customers may flee, and the premium is gone whether the synergies arrive or not.

**On the target's side**, the banker runs *raid defence*: monitoring the shareholder register for stake-building, preparing a defence playbook before any bid arrives (normal, ongoing work, not panic), valuing the standalone plan credibly enough that "we are worth more alone" is a number and not a slogan, and, if a bid lands, finding the white knight or structuring an alternative that gives shareholders a genuine choice. The target banker's hardest moment is telling a board that its defence has become a liability — shareholders have heard the $52, they like the $52, and continuing to block it will cost the directors their seats. Good defence advice sometimes ends with: take the deal, but negotiate it up.

Notice what neither banker does: decide the outcome. Shareholders do, by tendering or by voting. Everyone else is trying to persuade the same group of owners.

## Common Misconceptions

**"A poison pill makes a company takeover-proof."** No. A pill makes an *unapproved* purchase prohibitively dilutive. A board can redeem it, and shareholders can elect a board that will. The pill is a delay and a forcing device, not a wall. Companies with pills get acquired all the time — after negotiation.

**"Hostile means the bidder is being aggressive or unfair."** Hostile means the board said no. The offer itself can be all-cash, fully financed, and at a large premium. Conversely, a friendly deal recommended by the board can be a bad deal for shareholders if the board negotiated poorly or had conflicts. Judge the price and the process, not the adjective.

**"Defences protect shareholders, full stop."** Sometimes they do, by buying time for a better price. Sometimes they protect managers, by blocking a price shareholders would accept. The Bebchuk and Gompers evidence both point the same way: on average, stronger defences have been associated with worse outcomes for target shareholders. A defence needs a specific, time-limited justification, not a general claim of protection.

**"If the premium is large, the deal must create value."** The premium is a transfer, not a creation. In our section 2 example, the $1.2 billion premium is value moving from the bidder's shareholders to the target's. The deal creates value only if the combined company is worth more than the two standalone companies plus that $1.2 billion plus fees. A 30% premium on a bad deal is just an expensive mistake with a press release.

**"Shareholders who refuse to tender are irrational."** Not necessarily. Refusing is a bet — on a higher bid, on the standalone plan, on the board's leverage — and bets can be rational even when they lose. But it has a real cost if the bid succeeds and the holdout becomes a minority shareholder in a controlled company, or if the bid fails and the price falls back toward $40.

## Test Yourself

**1.** A target has 80 million shares trading at $25 unaffected. A bidder offers $32. What is (a) the premium, (b) the pre-bid market capitalisation, and (c) the total cost if all shares are tendered?

*Answer: (a) Premium = (32 − 25) / 25 = 0.28 = 28%. (b) Market capitalisation = 80,000,000 × $25 = $2,000,000,000. (c) Total cost = 80,000,000 × $32 = $2,560,000,000 — a $560 million premium over the pre-bid value.*

**2.** Return to the section 3 pill example: 100 million shares, bidder holds 15 million, other holders exercise rights for 85 million new shares. (a) What is the bidder's new percentage? (b) How many shares would it need to hold a bare majority of the enlarged share count, and how many more is that than it has?

*Answer: (a) 15 / 185 ≈ 8.1%. (b) A bare majority of 185 million is more than 92.5 million shares, so at least 92,500,001. That is about 77.5 million more than the 15 million it holds. The pill did not change the bidder's share count by one share — it changed the denominator.*

**3.** A target has a nine-person staggered board, three seats up each year. A bidder wins every contested seat it can in year one. How many board seats does it hold, and why is that not enough? How many election cycles must it win to control the board?

*Answer: Three of nine — a minority. It must win two election cycles to reach six of nine, a majority, which is why a staggered board plus a pill can delay a hostile bid by roughly one to two years.*

**4.** A board adopts a poison pill against a low-ball, coercive tender offer, then refuses to redeem it two years later against a higher, all-cash, fully financed offer that most shareholders say they want. Using *Unocal* and *Revlon* in plain terms, why might the second refusal be much harder to defend than the first?

*Answer: Under Unocal, the defence must be reasonable in relation to the threat. A coercive low-ball offer is a plausible threat justifying a pill; a fairly priced all-cash offer that shareholders want is a much weaker threat, so maintaining the pill looks disproportionate. And if a sale has become inevitable, Revlon shifts the board's job toward maximising shareholder value — blocking the higher price without a better alternative is hard to square with that duty. The tool did not change; the threat and the context did, and that is what the law tests.*

---

*Next up: Spin-offs, Split-offs, and Carve-outs: Breaking Companies Apart to Create Value — the friendly mirror image of this article, where a board decides to break itself up before anyone else does it for them.*
