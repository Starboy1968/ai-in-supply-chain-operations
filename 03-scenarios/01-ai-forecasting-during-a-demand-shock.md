# Scenario 1: Rolling out AI forecasting during a demand shock

> **Fictional and illustrative.** "Harlow Industrial Supply" is made up. No numbers or results are claimed.

**Setting.** Harlow, a mid-size distributor of maintenance parts, is three weeks into a pilot of a machine-learning forecast for one product family (pumps and seals). The old weekly spreadsheet still runs alongside it.

**What happens.**
1. A large customer announces a plant expansion and places several unusually big orders. Orders across the family jump.
2. The new model sees the jump in history and starts raising the forecast for the *following* weeks, as if the spike were a new normal.
3. The planner, who knows the orders are one-off project buys, has two pressures: trust the new tool the company just paid for, or override it.
4. Following the pilot's rule, the planner overrides the forecast for the affected items **and writes down the reason** ("one-time project orders, customer confirmed no repeat"). Research on forecasting recommends exactly this: adjust only for information the model can't see, and document it [S2].
5. In the weekly review, the team marks those weeks as one-time events in the history so the model doesn't learn from them.
6. Two weeks later, a supplier warns of longer lead times on seals. The model has no way to know this; the planner raises the reorder point manually and logs it.

**Where AI helped.** It forecast every item consistently, freeing the planner to spend time on the few items that mattered this week.

**Where people had to step in.** Spotting that the spike was one-off; feeding back the supplier warning; resisting both extremes ("the model is always right" and "the model is useless").

**Lessons.**
- Run the old and new methods side by side before a shock, not after.
- An override with a written reason is a feature, not a failure.
- Mark unusual weeks so the model doesn't learn the wrong lesson.
- Watch **bias**, not only accuracy: a forecast that stays too high after a spike builds excess stock.

Related: [demand forecasting how-to](../02-use-cases/01-demand-forecasting.md), [R06 forecast drift](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R06-forecast-model-drift-over-automation.md), [limits](../05-limits.md)

---
[Back to README](../README.md)
