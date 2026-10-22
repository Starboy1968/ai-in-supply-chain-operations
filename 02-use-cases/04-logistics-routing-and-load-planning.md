# 4. Logistics routing and load planning

> Examples are fictional and illustrative.

## The basics, in plain words

**Load planning** decides which orders go on which truck. **Routing** decides the order of stops and the path. **Carrier selection** decides who hauls it. Good planning fills trucks, meets delivery windows, and avoids paying for empty space or rush shipments.

## The operational problem

Planners build loads by hand or in spreadsheets, under time pressure, using rules of thumb. Late orders, special customer requirements and carrier availability all change during the day.

## How AI helps

- **What it does:** optimization software (often built into a transportation management system, or TMS) tries a very large number of combinations and suggests loads, stop sequences and carriers that meet the rules at lower cost. Some tools use AI to predict arrival times or which carrier will accept a load.
- **Data needed:** orders with weights, sizes and delivery windows; addresses; customer rules (dock hours, appointment needs); carrier rates and capacity; truck types.

## Step by step for a manager

1. Write down the hard rules (delivery windows, truck limits, customer requirements) and the soft preferences.
2. Check that the data is right: wrong weights or addresses ruin any plan.
3. Run the tool's plan next to the planner's plan for a few weeks without switching over.
4. Review where they differ. Often the tool is missing a rule people know but never wrote down ("this customer won't take deliveries on Mondays").
5. Add the missing rules, then let planners approve AI plans, starting with the simplest lanes.
6. Keep the manual method ready and practiced as a fallback for outages.

## A simple prompt

> Here are today's orders (order, ship-to city, weight, pallets, delivery window) and our truck limits. Suggest how to group them into loads, show your reasoning for each load, and list any order that can't meet its window. Flag any assumption you made about drive times. I will check this against our planning tool; don't present it as final.

## Before and after (fictional)

| | Before | After |
|---|---|---|
| Building loads | Planner builds loads from experience; quality depends on who is working | Tool proposes loads; planner approves, especially for priority customers |
| Unwritten rules | Live in planners' heads | Written into the tool during the side-by-side period |
| Outage | No plan B | Practiced manual fallback |

## What to check / KPIs to track

- **Freight cost per unit** shipped (or per pallet).
- **OTIF** to customers.
- How full trucks are.
- How often planners reject or change AI plans, and why (this is your early warning that something drifted).

## Where AI falls short

- It only knows the rules you've entered.
- Real-world events (weather, a closed dock, a driver shortage) move faster than the data.
- The plan depends on the vendor's system; an outage at the wrong time stops shipping.
- Carriers respond to their own incentives (rates, backhauls), not just to your optimized plan; see the [case study](../04-case-study/dual-sourcing-decision.md).

## Risk link

- [R03 Third-party AI vendor dependency and concentration](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R03-ai-vendor-concentration-fourth-party.md)
- Worked example of a TMS with AI features: [ai-assisted-risk-analysis](https://github.com/Starboy1968/ai-assisted-risk-analysis/blob/main/worked-example/04-final-risk-register.md) (R5 poor AI load plans, R7 TMS outage)

---
[Back to README](../README.md)
