# 18 | AI in Investment Banking: What Changes, What Doesn't

*Every banker I know has the same two reactions to AI, usually in the same week: "this just wrote my first draft in ten minutes" and "this just confidently invented a multiple that doesn't exist." Both reactions are correct. The job now is knowing which one you're looking at.*

> **Learning goals.** After this article you can: (1) sort a banker's tasks into the ones AI genuinely speeds up and the ones it quietly makes worse; (2) explain the "jagged technological frontier" in plain language and apply it to a deal workflow; (3) run a simple time-and-error calculation before deciding whether to use AI on a task; (4) describe what AI cannot replace in banking — and why that list is longer than the hype suggests.
>
> **Prerequisites.** Articles 01 (what banks do), 04 (comps), and 11 (the sell-side process) are the useful background here. No machine-learning knowledge required — we will define every technical term as it appears.

## 1. Start With the Job, Not the Tool

Most writing about AI in banking starts with the model: what it can do, how many parameters it has, which vendor just raised another round. That is the wrong starting point. Start with the job instead. An analyst's week is not one thing called "banking." It is a bundle of very different tasks, and AI is good at some of them and dangerous at others. If you average across the bundle, you learn nothing.

Here is a rough map of where an analyst's hours actually go on a live sell-side mandate (article 11 walked through this process end to end):

| Task | What it really involves | AI's natural fit |
|---|---|---|
| Gathering public data | Pulling filings, prices, comps inputs, precedent deals | Strong — retrieval and formatting |
| First drafts | CIM sections, management presentation pages, process letters | Strong — fluent prose from an outline |
| Arithmetic | Building the model, checking the bridge, sensitizing outputs | Weak alone — arithmetic needs a calculator, not a storyteller |
| Judgment | Which buyers to call, what the story is, where the risks sit | Weak — judgment needs context the model doesn't have |
| Relationships | Client calls, buyer conversations, negotiation | None — trust is not a text-generation problem |

Notice the pattern. The tasks AI handles best are the ones where the input is public, the format is standard, and a mistake is easy to spot. The tasks it handles worst are the ones where the input is private, the situation is novel, and a mistake looks exactly like a correct answer. That pattern has a name in the research literature, and it is the single most useful idea in this article.

A **large language model (LLM)** is, at its core, a system trained to predict plausible text given the text that came before it. "Plausible" is the key word. It is not trained to be true; it is trained to sound like the kind of thing that would usually come next. Most of the time, plausible and true overlap — which is why the output reads so well. But when they diverge, the output still reads well. That is the whole danger in one paragraph, and everything below is just working out its consequences for banking.

## 2. What the Evidence Actually Says

Banking has a lot of AI marketing and very little AI measurement. So let's anchor on two field experiments — real workers, real tasks, measured outcomes — rather than vendor claims. Both are about knowledge workers generally, not bankers specifically, and I will be honest about that gap rather than pretend it away. The mechanisms, though, transfer directly.

**Study 1: customer support agents.** Brynjolfsson, Li, and Raymond (2023) studied the staggered rollout of a generative AI assistant to 5,179 customer support agents at a Fortune 500 software company. Access to the tool raised productivity — issues resolved per hour — by 14% on average. The gains were wildly uneven: novice and low-skilled workers improved by about 34%, while experienced, highly skilled workers saw minimal change. The authors' interpretation is worth remembering: the model seemed to spread the best practices of the strongest workers to everyone else, pulling newcomers down the experience curve faster. Later published as Brynjolfsson, Li, and Raymond (2025) in the *Quarterly Journal of Economics*.

**Study 2: consultants.** Dell'Acqua, McFowland, Mollick, Lifshitz-Assaf, Kellogg, Rajendran, Krayer, Candelon, and Lakhani (2023) ran a preregistered field experiment with 758 consultants at Boston Consulting Group (BCG). Consultants were randomly assigned to no AI access, GPT-4 access, or GPT-4 access plus a prompt-engineering overview, and given 18 realistic consulting tasks. On tasks inside the AI's capabilities, the AI group completed 12.2% more tasks, 25.1% more quickly, and with quality rated over 40% higher. But on a task deliberately chosen to sit *outside* the frontier, consultants using AI were 19 percentage points less likely to produce the correct solution than those without it.

Read those two results together and you get the honest picture. AI is a skill leveler: it helps the least experienced most, because it hands them the patterns that experts already carry in their heads. And it has a cliff edge: past a certain point, it doesn't just stop helping — it actively hurts, because a fluent, confident answer discourages the user from thinking independently. The authors call this uneven landscape the **jagged technological frontier**: capability is not a smooth slope where harder tasks are uniformly harder for AI. Some seemingly difficult tasks are easy for it, and some seemingly similar tasks are beyond it, and there is no obvious line between them until you test.

The BCG study also noticed two styles of successful use. **Centaurs** split the work: they delegated some subtasks to the AI and kept others for themselves, like the mythical half-human, half-horse division of labor. **Cyborgs** wove the AI into every step, checking and steering continuously. Both beat the control group. The common thread was not the style — it was that the human stayed in charge of deciding which parts to trust.

## 3. The Jagged Frontier, Applied to a Deal

Let's map the frontier onto work you already know from this series.

**Inside the frontier — use it, with checks:**

- *Drafting standard prose.* A CIM company overview, a market section, a process update email. The structure is conventional, the facts come from documents you supply, and you can read the draft in five minutes and spot nonsense.
- *Reformatting and summarizing.* Turning a 60-page earnings transcript into a two-page summary, or a messy comps output into a clean table. The source exists; you can verify against it.
- *First-pass research.* "Find precedent transactions in European packaging since 2022." The AI will miss some and invent none if you force it to cite sources — but treat its list as a starting point, never as the final set. Article 05 taught you why a missing precedent deal can move a valuation range.
- *Brainstorming buyer lists and angles.* As a divergent-thinking partner it is excellent, because a bad idea in a brainstorm costs nothing.

**Outside the frontier — do not delegate:**

- *Any number that will go to a client or a board.* Multiples, growth rates, synergy estimates, valuation outputs. An LLM can produce a perfectly formatted comps table with a wrong EBITDA in row three. Nothing in the formatting signals the error. This is the single most common AI failure mode in banking work, and it is invisible by design.
- *Judgment calls with private context.* Which buyer is bluffing, whether the CEO actually wants to sell, what the board will accept. The model has none of this context and cannot ask for it.
- *Anything novel.* A deal structure nobody has done before, a regulatory question with no precedent, a fairness opinion (article 10). Novelty is precisely where "plausible continuation of past text" breaks down, because there is no past text to continue.
- *Confidential information.* Pasting a client's unannounced financials or a live deal document into a public AI tool is not a productivity hack; it is a confidentiality breach. Banks that allow AI use do so through approved, ring-fenced tools for exactly this reason. When in doubt, assume the tool keeps what you type.

The practical rule falls out of the frontier idea: **use AI where verification is cheap, and never where verification is impossible.** Drafting is cheap to verify — you read it. A multiple in a table is cheap to verify too, *if you actually re-tie it to the source*, which means the time saving is smaller than it first looks. A judgment call is impossible to verify, because there is no source to check it against. That is the test to run on every task before you reach for the tool.

## 4. The Economics: Time Saved Minus Errors Made

Hype counts only the time saved. A banker should count the time saved *minus* the expected cost of errors. Here is a simple model that makes the trade-off explicit. Define:

```math
T_{total} = T_{draft} + T_{review}
```

where $T_{draft}$ is the time to produce a first version and $T_{review}$ is the time to check it properly — re-tying every number to its source, not just reading it over. And define the expected cost of an error as:

```math
E[\text{error cost}] = p \times C
```

where $p$ is the probability that a material error survives review and $C$ is the cost if it does — a corrected page, a lost evening, or in the worst case, a credibility hit with a client. AI is worth using on a task when both conditions hold: $T_{total}$ with AI is lower than without it, *and* $p$ stays tiny because review is real.

**Worked example — refreshing a comps table.** Say a comps refresh takes an analyst 12 hours by hand: 8 hours gathering and entering data, 4 hours formatting and checking. With AI assistance, drafting and formatting take 2 hours, but proper review — re-tying each company's revenue, EBITDA, and share price to the filing or market source — still takes 4 hours, because review cannot be skipped and sources must be opened one by one:

```math
T_{manual} = 12 \text{ hours}
```

```math
T_{AI} = 2 + 4 = 6 \text{ hours}
```

```math
\text{Time saved} = 12 - 6 = 6 \text{ hours, or } 50\%
```

That is a real saving — half a working day. But notice what happened to the composition: review went from one-third of the job to two-thirds of it. The analyst's job shifted from *producing* to *verifying*. Now add errors. Suppose an unchecked AI draft has a 1-in-5 chance ( $p = 0.20$ ) of containing a material error, and proper review catches 19 out of 20 errors, leaving a residual $p = 0.20 \times 0.05 = 0.01$. If a surviving error costs, conservatively, one full day of rework and embarrassment — say 10 hours of equivalent cost — then:

```math
E[\text{error cost}] = 0.01 \times 10 = 0.1 \text{ hours}
```

The expected error cost is small *because review is thorough*. But if the analyst skims instead of re-tying — review catches only half the errors, so $p = 0.20 \times 0.50 = 0.10$ — then:

```math
E[\text{error cost}] = 0.10 \times 10 = 1.0 \text{ hour}
```

and, worse, the errors that survive are exactly the confident-looking ones. The model makes the intuition precise: AI's value is not in the draft, which is cheap. It is in the review, which is the entire job now. An analyst who treats AI output as finished work has not saved 6 hours; they have borrowed them at a high interest rate.

There is a second, subtler cost. The Brynjolfsson result — novices gain most — cuts both ways. If juniors lean on AI for every first draft, they may never build the muscle that the tool is imitating. The model learned from experts' patterns; if the next generation of experts never practices the patterns, the quality of what gets imitated decays. Senior bankers already worry about this out loud: the analyst years were never really about the pages produced, but about the judgment built while producing them. Automate the practice and you may automate away the training. That is a hypothesis, not a measured fact — the studies above run for months, not careers — but it is the right worry to carry into your own habits: use the tool to go faster, not to skip learning.

## 5. What Doesn't Change

After all that, here is the part the hype usually skips. Several things about banking are untouched by AI, because they were never information-processing problems in the first place.

**Liability.** Someone signs the fairness opinion. Someone tells the board a price is fair. Someone's name is on the CIM. AI does not take liability, so it cannot take responsibility, and the work that carries liability will always be done — and priced — by humans. Article 10's point about fairness opinions stands: the opinion is valuable precisely because a reputable human stands behind it.

**Trust.** Clients hire bankers they trust with the most consequential decision in their company's life. Trust is built in rooms, on calls, and through a track record of judgment under pressure. No model, however fluent, has sat across a table from a founder who is scared to sell the company their father built.

**Private information.** The most valuable inputs in a deal — the real reason a seller is selling, the buyer's walk-away price, the board's internal split — are never written down anywhere a model could train on. AI is trained on the public past; deals are decided on the private present. That gap is structural, not a temporary limitation waiting for a bigger model.

**The fee logic.** Recall article 01: banks are paid for advice and execution, largely on success. Clients do not pay a success fee for a document; they pay for an outcome. If AI commoditizes document production, the fee migrates even further toward judgment, access, and execution — the parts that cannot be generated. Paradoxically, the better AI gets at drafts, the more valuable the non-draft skills become.

**Regulation and conflicts.** Clearance, confidentiality walls, insider information rules — these are institutional, not technical, constraints. AI does not resolve a conflict; it can only be operated inside the system that does.

## 6. A Practical Workflow

So what does a sensible analyst actually do on Monday morning? Something like this:

1. **Draft with AI, from your outline.** Never ask for a finished product from a vague prompt. Write the structure yourself — the argument, the sections, the numbers you already know — and let the tool fill in prose. If you can't write the outline, you don't understand the task well enough to check the output.
2. **Verify every number to its source.** Open the filing, the price feed, the precedent article. Re-tie, don't re-read. If a number cannot be traced to a source, delete it.
3. **Keep the audit trail.** Save the prompt, the draft, and the sources you checked. When a VP asks "where did this come from?" — and they will — you want an answer that isn't "the model said so."
4. **Red-team the draft.** Ask: if this is wrong, where would it be wrong? The BCG study's outside-the-frontier task is a warning: the most dangerous output is the one you agree with too quickly. Argue against your own draft before you send it.
5. **Keep confidential material inside approved tools only.** If your bank hasn't approved a tool for deal material, the answer is no, however convenient the alternative.
6. **Protect your own training.** At least sometimes, do the task by hand — build the comps table from scratch, write the CIM section yourself. The point of the analyst years is becoming the person whose patterns are worth imitating.

None of this is glamorous, and none of it will appear in a vendor's pitch deck. It is also, as far as I can tell, the whole game: AI moves the frontier of what is cheap, and the banker's job moves with it, toward verification, judgment, and trust.

## 7. Common Misconceptions

**"AI will replace analysts."** It replaces *tasks*, not jobs — and the tasks it replaces are the most mechanical slice of the analyst's week. The job then reconstitutes around the remaining tasks: verification, judgment, client work. The headcount question is real and worth watching, but "replaced" is the wrong verb for what the evidence shows. Both field studies found augmentation, with humans still in the loop and still responsible.

**"If the output reads well, it's probably right."** Fluency is not evidence. The model is optimized for plausible text, and a wrong number in a clean table is more dangerous than a wrong number in a messy one, because it disarms your skepticism. Treat polish as a reason to check harder, not less.

**"Checking AI output is faster than doing it yourself, so the saving is the whole draft time."** Section 4 shows why this is wrong: proper review is a large, irreducible chunk of the work. The honest saving is draft time minus review time, and review time grows as output volume grows. Anyone quoting a 90% time saving has silently assumed review away.

**"AI is bad at finance because it can't do math."** It is bad at *unchecked* math, but paired with a calculator, a spreadsheet, or a code interpreter it can be perfectly accurate — because then it is not doing the arithmetic at all. The failure mode is not "AI can't add"; it is "AI adds confidently without showing its work, and nobody checks." Put the arithmetic where arithmetic belongs: in Excel, not in prose.

**"Using AI means I'm not really learning."** Only if you let it. Used as a first draft that you then verify line by line, it can actually teach faster — you see more examples, more phrasings, more structures per week. Used as an answer machine, it teaches nothing. The difference is not the tool; it is whether you do the verification step yourself.

## 8. Test Yourself

**1. A VP asks you to "just run the comps through the AI" and send the output to a client. Using the framework in this article, what is wrong with that instruction, and what do you do instead?**
*Answer: It skips the entire job. Comps numbers are outside the safe zone unless verified: a wrong EBITDA or share price looks identical to a right one in a clean table. You use the AI for a first draft if helpful, then re-tie every input to its filing or market source, check the multiple arithmetic in Excel, and only then send it. If the VP pushes back, the honest sentence is: "I'll verify the numbers first — an unverified table is worse than a slow one."*

**2. An AI draft of a CIM market section saves you 4 hours of writing but takes 3 hours to verify properly. A colleague skims it in 30 minutes and claims a 3.5-hour saving. Who is right about the saving, and what risk is your colleague carrying?**
*Answer: You are right about the honest saving: 4 − 3 = 1 hour, not 3.5. Your colleague's "saving" assumes review away, and carries the residual error probability from section 4 — with skim-level review catching only a fraction of errors, a material mistake reaching the client becomes a live possibility, and its cost (rework, credibility) dwarfs the 2.5 hours "saved."*

**3. In the BCG experiment, consultants using AI did worse on a task outside the frontier. Give a banking example of an outside-the-frontier task, and explain why AI hurts rather than merely failing to help there.**
*Answer: Example: recommending a walk-away price in a negotiation, or judging whether a CEO genuinely wants to sell. These need private, unwritten context and novel judgment. AI hurts rather than merely not helping because its fluent, confident answer anchors the human: the consultant (or banker) stops thinking independently and defers to a plausible-sounding answer, performing worse than they would have on their own. That is the 19-percentage-point effect.*

**4. The Brynjolfsson study found novices gained ~34% while experts gained little. Does that mean a bank should give AI only to juniors? Argue both sides in two sentences each.**
*Answer: For giving it to juniors: they gain most because the tool supplies expert patterns they haven't internalized yet, so it compresses their learning curve. Against juniors-only: experts gain little on routine output but are exactly the people who can spot the model's errors, so restricting it to those least able to verify it maximizes the risk; and juniors who never practice the underlying task may never become the experts the tool imitates.*

---

*Sources cited in this article, verified before publication: Brynjolfsson, E., Li, D., & Raymond, L. R. (2023). "Generative AI at Work." NBER Working Paper 31161 (published 2025 in the Quarterly Journal of Economics, 140(2), 889–942). Dell'Acqua, F., McFowland, E., Mollick, E., Lifshitz-Assaf, H., Kellogg, K. C., Rajendran, S., Krayer, L., Candelon, F., & Lakhani, K. R. (2023). "Navigating the Jagged Technological Frontier: Field Experimental Evidence of the Effects of AI on Knowledge Worker Productivity and Quality." Harvard Business School Working Paper.*

*Next up: ECM and IPO Pricing — How a Bookbuild Really Works.*
