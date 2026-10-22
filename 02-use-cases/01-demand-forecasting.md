# 1. Demand forecasting

> Examples are fictional and illustrative. No real company or result is described.

## The basics, in plain words

A **forecast** is a best guess of how much customers will order, by item, by week or month. Everything downstream depends on it: what to buy, what to make, how many trucks to book. A forecast is always somewhat wrong. The useful questions are **how wrong, in which direction, and does anyone notice in time**.

Two ideas matter more than any formula:
- **Accuracy:** how close the forecast was to what really happened.
- **Bias:** whether it is wrong in the *same direction* again and again (always too high, or always too low). A forecast can be roughly accurate on average and still be biased, which quietly builds up too much or too little stock.

## The operational problem

Many teams still forecast in a weekly spreadsheet: last year's numbers, a few manual tweaks, and the sales team's opinion. It is slow, it depends on one or two people, and nobody tracks whether past tweaks helped or hurt.

## How AI helps

- **What it does:** a statistical or machine learning model looks at order history and spots patterns people miss or don't have time for: seasonality, trends, the effect of promotions or price changes. It produces a forecast for every item, every cycle, the same way each time.
- **Data needed:** at least a couple of years of order history by item and week (or month), with promotions, stockouts and one-off events marked. Clean item codes. Optional: prices, customer signals, open orders.
- **Where a general AI assistant fits:** it does not replace a forecasting tool, but it can help a manager clean and summarize history, explain why a forecast changed, and draft the questions to ask in the planning meeting.

## Step by step for a manager

1. Pick one product family with steady history. Don't start with new products.
2. Export order history to a spreadsheet. **Remove customer names and prices** before using any AI tool that is not approved for confidential data.
3. Mark the weeks that were not normal (stockouts, a big one-time order, a plant shutdown).
4. Run the forecast (forecasting module, planning tool, or a simple spreadsheet forecast) and keep the old method running alongside it.
5. Hold a short weekly review: where does the new forecast disagree with the old one, and why?
6. **Override only with new information the model can't see** (a confirmed customer launch, a lost account), and write down the reason each time. Forecasting research recommends adjusting sparingly and documenting every adjustment [S2].
7. After a few cycles, compare both methods on accuracy and bias, and check whether the overrides helped.

## A simple prompt

> I'm a supply chain manager reviewing a demand forecast. Below is anonymized weekly order history for one product family and this week's forecast. In plain language: (1) describe the pattern you see (trend, seasonality, unusual weeks), (2) list the weeks that look like outliers and why, (3) tell me which forecast numbers look out of line with the history, and (4) list questions I should ask sales before I accept it. Do not invent causes; if you are guessing, say so.

## Before and after (fictional)

| | Before | After |
|---|---|---|
| Process | A planner updates a weekly spreadsheet from last year plus gut feel | A model forecasts every item each week; planners review exceptions and log the reason for each override |
| Who notices errors | Usually the warehouse, when stock runs out or piles up | The weekly review flags items where the forecast keeps missing in one direction |
| Knowledge | Lives in one planner's head | Overrides and reasons are written down and can be checked later |

## What to check / KPIs to track

- **Forecast accuracy** by item family, compared with the old method, not in isolation. Judge it on weeks the model had not already seen, not on how well it fits the past [S1].
- **Forecast bias:** is it consistently high or low?
- **Override log:** how often people override, and whether overrides made it better or worse.
- Downstream: **fill rate** (share of orders shipped complete from stock) and **inventory turns** (how fast stock sells through).

## Where AI falls short

- New products, new customers or a sudden shock (no history to learn from).
- A model trained on "normal" years can drift quietly when the market changes.
- It can't know what sales hasn't told anyone yet.
- Good-looking charts make people trust it more than they should (automation bias, see [05-limits.md](../05-limits.md)).

## Risk link

- [R06 Forecast model drift and over-automation](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R06-forecast-model-drift-over-automation.md)
- [R02 Data leakage through generative AI tools](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R02-data-leakage-genai-shadow-ai.md) if order data is pasted into unapproved tools

---
[Back to README](../README.md)
