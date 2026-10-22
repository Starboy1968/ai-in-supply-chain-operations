# 3. Inventory: safety stock, reorder points, slow movers

> Examples are fictional and illustrative. No formulas: the ideas are explained in words.

## The basics, in plain words

- **Safety stock** is the extra you keep "just in case": demand comes in higher than forecast, or the supplier is late. More uncertainty, or a longer and less reliable supplier, means more safety stock.
- **Reorder point** is the stock level that triggers a new order. It needs to cover what you expect to use while you wait for the delivery, plus the safety stock.
- **Slow movers** are items that sit on the shelf. They tie up cash and space and may expire or become obsolete.

In a kitchen, this is the difference between running out of a menu staple on a Friday night and throwing out a case of something nobody ordered. Same trade-off, bigger scale.

## The operational problem

Settings are often made once and never revisited. Some items carry far too much stock, others run out, and nobody has time to review thousands of items one by one.

## How AI helps

- **What it does:** tools look at how much each item's demand and supplier lead times vary, then suggest safety stock and reorder settings item by item. They also sort items by how fast they move and flag the ones that have stopped moving. A general AI assistant can summarize an inventory export and draft the list of items to review.
- **Data needed:** on-hand stock by item and location, usage or sales history, supplier lead times (promised and **actual**), cost, and the service target for each item group (how often you're willing to run out).

## Step by step for a manager

1. Agree on service targets by item group first. Not every item deserves the same protection.
2. Pull an inventory export: item, location, on hand, recent usage, last movement date, lead time.
3. Ask the assistant (or tool) to group items: fast, slow, not moving, and items whose stock looks too high or too low compared with recent usage.
4. Review the top items in each group with the planner. Check *why* before changing anything (an item may be slow because of a planned project).
5. Change settings for a small batch, write down what you changed and why, and check the effect after a few cycles.
6. For slow movers, decide with sales and finance: return, discount, use elsewhere, or write off.

## A simple prompt

> Below is an anonymized inventory export (item, location, on hand, average monthly usage over the last 6 months, last movement date, supplier lead time). Group the items into: (a) no movement in 6 months, (b) stock much higher than recent usage, (c) stock that looks too low to cover the lead time, (d) everything else. Explain each grouping in one line. Don't recommend write-offs; list the questions I should ask before deciding.

## Before and after (fictional)

| | Before | After |
|---|---|---|
| Settings | Reorder points set years ago, rarely changed | Settings reviewed by item group on a schedule, with tool suggestions and human sign-off |
| Slow movers | Found during the annual count | Flagged monthly with a decision owner |
| Trade-off | Run out of some items while others pile up | Protection matched to how important and how unpredictable each item is |

## What to check / KPIs to track

- **Fill rate:** share of orders shipped complete from stock.
- **Inventory turns:** how many times stock sells through in a year (higher usually means less cash tied up).
- Stockouts on critical items.
- Value of stock with no movement in the last 6 or 12 months.

## Where AI falls short

- Suggestions are only as good as the lead-time data. If the system holds *promised* lead times rather than *actual* ones, the settings will be wrong.
- It doesn't know about planned events (a new contract, a product being discontinued) unless someone tells it.
- It can tell you an item is slow; it can't tell you whether a key customer still needs it.

## Risk link

- [R06 Forecast model drift and over-automation](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R06-forecast-model-drift-over-automation.md): auto-ordering on bad settings is the over-automation case.

---
[Back to README](../README.md)
