# Case study: Should we dual-source a critical part? One decision, three lenses

> **Fictional and illustrative.** "Ridgeline Controls" and Suppliers A and B are made up. No real company, event or number is described. Payoffs are **ranked in plain words** (best, second, third...), not calculated.

## 1. The situation

Ridgeline Controls is a mid-size distributor that assembles and ships industrial control panels. One part, a controller board, comes from a **single supplier, Supplier A**. Ridgeline has bought from A for years, A's board is designed into most of Ridgeline's panels, and switching would mean testing and approving (qualifying) a new board, which takes months.

On the same Monday, two AI outputs land:
- **The AI demand forecast** shows orders for panels using A's board rising over the next two quarters.
- **A supplier-risk tool** raises an alert on Supplier A: news about strain at A's main plant and signs of financial stress. The alert does not say how serious it is.

The operations director has until Friday's leadership meeting to recommend what to do.

## 2. The options

| # | Option | In plain words |
|---|---|---|
| 1 | Stay single-source | Keep buying from A only; ask A for a written supply commitment |
| 2 | Buffer only | Order extra boards from A now and hold them |
| 3 | Dual-source | Qualify Supplier B and move part of the volume there |
| 4 | Staged mix | Small buffer for the most critical panels now, start qualifying B with a trial order, and share the real forecast with A |

## 3. Lens one: game theory (who wants what)

Game theory here just means: **each player acts on their own incentives, and each one's best move depends on what the others do.**

### The players and what they want

| Player | What they want most | What they fear |
|---|---|---|
| Ridgeline (buyer) | Steady supply at a fair price | A stockout that stops panel shipments |
| Supplier A (incumbent) | Keep all of Ridgeline's volume and pricing power | Losing share to B for good |
| Supplier B (challenger) | Win a foothold with a new customer | Spending on qualification and getting only a token order |
| Carriers | Full, well-paying, predictable loads | Small, irregular shipments when trucks are scarce |
| Ridgeline's sales team | Never tell a key customer "no" | Being blamed for a missed delivery |

### How each player ranks the options (1 = best for them)

Ridgeline's ranking depends on whether the alert turns out to be real, so it is shown both ways.

| Option | Ridgeline if alert is real | Ridgeline if alert is a false alarm | Supplier A | Supplier B | Sales team |
|---|---|---|---|---|---|
| 1 Stay single-source | 4th (most exposed) | 1st (cheapest, least effort) | 2nd | last (tie) | 4th |
| 2 Buffer only | 3rd (helps short term, cash tied up) | 3rd | 1st (more orders now, keeps all volume) | last (tie) | 1st |
| 3 Dual-source | 2nd | 4th (cost and effort for nothing) | 4th | 1st | 3rd |
| 4 Staged mix | 1st | 2nd (small cost, keeps options open) | 3rd | 2nd | 2nd |

**Reading the table:** no option is first for everyone. For Ridgeline, option 4 is the only one that ranks first or second in both futures, which is what makes it attractive when you don't know whether the alert is real.

### Four game-theory ideas at work

1. **A single source has leverage.** Because switching takes months, A knows Ridgeline can't walk away quickly. In a shortage, A can decide who gets boards first or raise prices. A threat to dual-source only changes A's behavior if it is **credible**: B actually being qualified, not just mentioned.
2. **Trust in a repeated game.** Ridgeline and A have worked together for years. Cooperation in repeated relationships is held together by the value of future business: each side behaves well because there will be a next order [S7]. Dual-sourcing can look like breaking that trust. Framing matters: "we're adding resilience, you keep most of the volume" signals the relationship continues; "we're replacing you" invites A to put Ridgeline last in line.
3. **Shortage gaming and the bullwhip effect.** When buyers fear a shortage, they order more than they need to get a bigger share of whatever is available. Everyone doing this sends the supplier a false demand signal that grows as it moves up the chain. Research on supply chains calls this the bullwhip effect and names this "rationing game" as one of its causes [S3]. If Ridgeline reacts to the AI forecast *and* the alert by placing a huge buffer order (option 2 at full size), it becomes part of the problem. **Sharing real demand with A** is the coordination fix.
4. **Carriers respond to tight capacity.** When trucks are scarce, carriers favor shippers with steady, full loads and contract rates. A new lane from Supplier B with small, irregular shipments is the kind of freight they turn down first. Securing that capacity early is part of the decision, not an afterthought.

## 4. Lens two: psychology (how people actually decide)

The people in Friday's meeting are under deadline pressure, with incomplete information, and with history. These are the traps that show up:

| Trap | How it sounds in the room | What to do |
|---|---|---|
| **Loyalty / status quo** | "A has never let us down." | Separate the relationship (good) from the exposure (real). Both can be true. |
| **Anchoring** [S5] | B's quote looks "expensive" because everyone compares it with A's price from years ago | Compare B with the cost of a stockout, not only with A's price |
| **Sunk cost** [S6] | "We spent years and a lot of money qualifying A's board." | That money is spent either way. Ask only: what's best from here? |
| **Overconfidence** | "We're a big customer; A will look after us." | Ask A in writing. Check what share of A's business Ridgeline really is. |
| **Automation bias** [S4] | "The tool flagged it, so it's real", or the opposite: "these tools always cry wolf" | Treat the alert as a question to verify, not an answer |
| **Group optimism** | The meeting talks itself into the easiest option | Ask each person to write their recommendation before discussion; forecasting research notes group settings can push people toward optimism [S2] |
| **Deadline pressure** | Pick the first option that sounds workable | Choose a **first step** by Friday, not a final answer; set dates to revisit |

## 5. Lens three: strategy (what changes when AI enters)

- **Faster signals, not better certainty.** AI saw the demand rise and the supplier strain earlier than a person scanning news would. It did not tell anyone *how serious* the strain is. Speed buys time to verify, if the team uses it that way.
- **Everyone sees the same alert.** Competitors using similar supplier-risk tools may get the same alert on A at the same time. If they all rush to Supplier B, B's capacity becomes the new bottleneck. Being early to verify and start qualification matters more than being certain.
- **The information gap moves.** Before, Supplier A knew much more about its own health than Ridgeline did. AI narrows that gap a little, and A knows it. That makes an honest conversation with A more likely to work than a bluff.
- **New dependencies.** The decision now leans on an AI forecast and a risk tool from outside vendors. If they are wrong, drift, or go down, so does the signal (see [R03](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R03-ai-vendor-concentration-fourth-party.md) and [R06](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R06-forecast-model-drift-over-automation.md)).
- **Who captures the value.** The value of an early warning goes to whoever **acts** on it well, not whoever receives it. Some also goes to the AI vendors whose tools everyone now relies on, and to Supplier B, whose bargaining position improves when many buyers want a second source.

## 6. The role of AI vs the human decision

| | AI did | People did |
|---|---|---|
| Spotting | Flagged rising demand and supplier strain early | Decided the alert was worth a Monday phone call |
| Verifying | Nothing; the alert gave no evidence of severity | Called A, asked for a written capacity and supply statement, checked the forecast against confirmed customer orders |
| Choosing | Nothing | Weighed the options against two possible futures (alert real / not real) |
| Relationships | Nothing | Framed the change to A, approached B, booked carrier capacity |

## 7. The decision (fictional)

The director recommends **option 4, the staged mix**:
1. **Verify first:** call Supplier A this week; ask for a written supply commitment and a plain account of the plant issue.
2. **Buffer narrowly:** extra boards only for panels going to the most critical customers, not the whole range, to avoid feeding the bullwhip.
3. **Start qualifying B:** a small trial order and testing plan, with a named engineer and a target date.
4. **Talk to A openly:** share the real forecast; say clearly that a second source is about resilience and A keeps most of the volume.
5. **Lock in freight:** agree contract capacity with a carrier for B's lane before it's needed.
6. **Set revisit triggers:** if A's answer is vague, the alert gets worse, or the trial goes well, move more volume to B. If the alert proves false, keep B qualified at a small share. That is the price of the option.

## 8. Lessons

- An AI alert starts a decision; it doesn't make one.
- Rank options under more than one possible future. The best choice is often the one that is never the worst.
- Supplier leverage is about how long it takes you to switch. Shortening that time is the real risk control.
- Over-ordering in a scare makes the shortage worse for everyone, including you.
- Name the behavioral traps out loud in the meeting; it's cheaper than learning them the hard way.
- AI shifts who knows what, and when. The advantage goes to the team that verifies fastest and acts sensibly, not the one with the most alerts.

## Related reading in this portfolio

- [two-suppliers-one-factory](https://github.com/Starboy1968/two-suppliers-one-factory): finding hidden tier-2 single points of failure
- [behavioral-supply-chain-risk-audit-ai](https://github.com/Starboy1968/behavioral-supply-chain-risk-audit-ai): how bias and pressure create supply chain risk, and how AI triage, audit evidence and human review help catch it
- [supply-chain-ai-governance-strategy](https://github.com/Starboy1968/supply-chain-ai-governance-strategy): plain-language game theory that explains why supply chain and AI risks persist, and which incentives to change
- [supply-web-audit](https://github.com/Starboy1968/supply-web-audit): mapping who holds the money and power in a supply web
- [power-behavior-risk-indicators](https://github.com/Starboy1968/power-behavior-risk-indicators): spotting power and behavior signals in risk decisions
- [ai-supply-chain-risk-assessment](https://github.com/Starboy1968/ai-supply-chain-risk-assessment): the risk side of AI in the supply chain

---
[Back to README](../README.md)
