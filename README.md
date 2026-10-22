# AI in Supply Chain Operations: A Strategist's Field Guide

**How a supply chain manager can put AI to work in six everyday jobs, what to check before trusting it, and how one sourcing decision changes when you look at incentives, human behavior and AI together.**

## Summary

This is a practical guide written from a strategist's point of view, not a data scientist's. It covers six common supply chain jobs (forecasting, supplier selection and monitoring, inventory, routing, invoice and shipment anomalies, contract review). For each one it explains the basics in plain words, gives a step-by-step way to use AI with a sample prompt, lists what to check and which KPIs to watch, and says where AI falls short. Each use case links to the matching risk in a companion risk assessment. A case study then follows one decision, whether to dual-source a critical part after an AI alert, through three lenses: game theory (who wants what), psychology (how people really decide), and strategy (what AI changes). There are no formulas; everything is in words, and every example is fictional and labeled.

> **About the author's angle.** Rashon Alsberry comes from risk and strategy (CompTIA Security+), Army IT service desk work, and years running restaurant kitchens, where vendors, stock counts and missed deliveries were weekly problems. They are **learning supply chain operations** and bring the risk and decision-making side to it. This guide is that learning, made usable.

## What's inside

1. **[How-to guide](02-use-cases/):** six use cases, each with basics, steps, a prompt, checks, KPIs, limits and a risk link.
2. **[Case study](04-case-study/dual-sourcing-decision.md):** one dual-sourcing decision through game theory, behavioral and strategic lenses, with ranked (not calculated) payoffs.
3. **[Scenarios](03-scenarios/), [limits](05-limits.md), [getting started](06-getting-started.md):** three short end-to-end stories, an honest list of what goes wrong, and a 30/60/90-day low-cost path.

## Use cases at a glance

| Use case | What AI does | Before → after (fictional, one line) | Where it falls short | Risk link |
|---|---|---|---|---|
| [Demand forecasting](02-use-cases/01-demand-forecasting.md) | Finds patterns in order history; forecasts every item the same way each cycle | Gut-feel spreadsheet → model forecast with logged human overrides | New products, sudden shocks, quiet drift | [R06 forecast drift](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R06-forecast-model-drift-over-automation.md) |
| [Supplier selection and monitoring](02-use-cases/02-supplier-selection-and-monitoring.md) | Puts quotes into one table; watches news and performance | Retyping PDFs → checked comparison table with quoted terms | Misread terms; alerts without context | [R07 hallucinated decisions](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R07-hallucinated-biased-supplier-decisions.md) |
| [Inventory](02-use-cases/03-inventory-optimization.md) | Suggests safety stock and reorder settings; flags slow movers | Settings set once and forgotten → reviewed by item group | Bad lead-time data; unknown future plans | [R06 over-automation](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R06-forecast-model-drift-over-automation.md) |
| [Routing and load planning](02-use-cases/04-logistics-routing-and-load-planning.md) | Tests many load and route combinations against your rules | Planner-dependent loads → AI plans approved by planners | Unwritten rules; vendor outages | [R03 vendor dependency](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R03-ai-vendor-concentration-fourth-party.md) |
| [Invoice and shipment anomalies](02-use-cases/05-anomaly-detection-invoices-and-shipments.md) | Flags duplicates, split bills, off-rate charges, late loads | Random sampling → every invoice checked, odd ones reviewed | False alarms; fraud that looks normal | [R01 payment fraud](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R01-supplier-impersonation-payment-fraud.md) |
| [Contract review](02-use-cases/06-contract-review.md) | Pulls renewal, notice and price-change clauses with quotes | Missed renewal dates → dates on a calendar with an owner | Invented or misquoted clauses | [R07](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R07-hallucinated-biased-supplier-decisions.md), [R02 data leakage](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R02-data-leakage-genai-shadow-ai.md) |

## Teaser: the dual-sourcing decision

An AI forecast says demand for a key part is rising. On the same day, a supplier-risk tool flags strain at the only company that makes it. The tempting moves are "trust the long-time supplier" or "order a mountain of stock". The case study shows why the second one feeds the **bullwhip effect** (everyone over-ordering in a scare, which distorts demand up the chain), why a threat to switch only works if a second supplier is actually qualified, and which biases (loyalty, anchoring, sunk cost, automation bias) show up in the meeting. The recommended path is the option that is **first or second in both futures**, whether the alert turns out real or not: verify, buffer narrowly, start qualifying a second source, and talk openly with the incumbent. [Read the case study →](04-case-study/dual-sourcing-decision.md)

## How operations and risk connect

Every operational gain from AI comes with a matching risk, and the controls are usually simple:

| Operational use | The risk it brings | The simple control |
|---|---|---|
| Faster forecasts | Quiet drift; people stop checking | Track bias; log every override with a reason |
| Quicker quote and contract review | Invented clauses; confidential data leaving | Quoted text and section numbers; approved tools only |
| Automated invoice checks | A tool that flags *and* approves | Keep approval separate; callback on bank changes |
| AI-planned freight | Dependence on one vendor | Practiced manual fallback; model-change notice in contracts |

The full risk analysis lives in [ai-supply-chain-risk-assessment](https://github.com/Starboy1968/ai-supply-chain-risk-assessment) and [ai-assisted-risk-analysis](https://github.com/Starboy1968/ai-assisted-risk-analysis).

## Skills demonstrated

- Translating supply chain operations into plain-language, step-by-step practice for managers
- Practical use of AI assistants: prompts that demand quoted evidence and flag gaps
- Strategic analysis: incentives between buyers, suppliers and carriers; repeated-game trust; bullwhip as a coordination problem
- Behavioral insight: anchoring, sunk cost, overconfidence, automation bias, and how deadlines shape decisions
- Bridging operations and risk: each use case tied to a scored risk and a control
- Honest scoping: fictional labeled examples, verified sources, no invented numbers

## Repo map

| Path | What's inside |
|---|---|
| [01-project-brief.md](01-project-brief.md) | Angle, objective, audience, scope, conventions |
| [02-use-cases/](02-use-cases/) | How-to guide: [forecasting](02-use-cases/01-demand-forecasting.md), [suppliers](02-use-cases/02-supplier-selection-and-monitoring.md), [inventory](02-use-cases/03-inventory-optimization.md), [routing](02-use-cases/04-logistics-routing-and-load-planning.md), [anomalies](02-use-cases/05-anomaly-detection-invoices-and-shipments.md), [contracts](02-use-cases/06-contract-review.md) |
| [03-scenarios/](03-scenarios/) | [AI forecasting in a demand shock](03-scenarios/01-ai-forecasting-during-a-demand-shock.md), [LLM quote and contract comparison](03-scenarios/02-buyer-compares-quotes-and-contracts-with-an-llm.md), [AP catches freight invoice anomalies](03-scenarios/03-ap-team-catches-freight-invoice-anomalies.md) |
| [04-case-study/](04-case-study/dual-sourcing-decision.md) | One decision, three lenses: game theory, psychology, strategy |
| [05-limits.md](05-limits.md) | Where AI falls short, and what to do about it |
| [06-getting-started.md](06-getting-started.md) | Free or low-cost 30/60/90-day path |
| [sources.md](sources.md) | Checked references |

## Related projects

- [ai-supply-chain-risk-assessment](https://github.com/Starboy1968/ai-supply-chain-risk-assessment): nine scored AI risks across the supply chain, with controls and a 30/60/90 plan
- [ai-assisted-risk-analysis](https://github.com/Starboy1968/ai-assisted-risk-analysis): a reusable GRC prompt and a worked TMS vendor example, from AI draft to human review
- [power-behavior-risk-indicators](https://github.com/Starboy1968/power-behavior-risk-indicators): reading power and behavior signals in risk decisions
- [supply-web-audit](https://github.com/Starboy1968/supply-web-audit): plain-English audit of who you depend on and who holds the money and power
- [two-suppliers-one-factory](https://github.com/Starboy1968/two-suppliers-one-factory): finding hidden tier-2 single points of failure

## Author

Rashon Alsberry, supply chain and third-party risk analyst - [starboy1968.github.io](https://starboy1968.github.io)
