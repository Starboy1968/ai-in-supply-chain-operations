# Honest limits of AI in supply chain work

AI is useful in supply chain operations, and it fails in predictable ways. A manager who knows these limits gets most of the benefit with fewer surprises.

| Limit | What it means in practice | What to do |
|---|---|---|
| **Data quality** | Wrong item codes, missing receipts, promised (not actual) lead times, unmarked stockouts. The model learns from whatever is there. | Clean one area before piloting there. Mark unusual periods. |
| **Cold start / new products** | No history means nothing to learn from. Forecasting texts note judgment is often the only option for new products [S2]. | Use structured judgment and similar products; switch to the model once history builds up. |
| **Black-swan demand** | Sudden shocks (a pandemic-style disruption, a major customer win or loss) break patterns the model relies on. | Override with documented reasons; don't let the model learn the shock as normal. |
| **Model drift** | The world changes; a model trained on last year slowly gets worse and nobody notices. | Track accuracy and bias over time with a named owner and a threshold that triggers review. ([R06](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R06-forecast-model-drift-over-automation.md)) |
| **Over-trust and automation bias** | People accept the AI's answer, or miss its errors, especially when busy. Research finds this affects experts as well as novices and isn't fixed by training alone [S4]. | Design the review step in: require a reason to accept big or unusual recommendations, and sample-check routine ones. The NIST AI RMF expects human oversight processes to be defined and documented (MAP 3.5) [S8]. |
| **Hallucinations in contract and document review** | An LLM can invent or misquote clauses [S9]. | Require quoted text and section numbers; check every field that matters. ([R07](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R07-hallucinated-biased-supplier-decisions.md)) |
| **Data leakage** | Pasting pricing, contracts or customer data into unapproved AI tools. | Approved tools only; strip confidential fields; clear rules. ([R02](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R02-data-leakage-genai-shadow-ai.md)) |
| **Integration with ERP** | Insights that live in a separate tool or spreadsheet don't change orders. Integrations take time and create new access risks. | Start with exports and reviews; integrate after the pilot proves value. Give integrations the least access they need. |
| **Vendor dependency** | Features depend on the vendor and often on its own AI provider. Outages and silent model changes happen. | Keep a practiced manual fallback; ask about model changes in contracts. ([R03](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R03-ai-vendor-concentration-fourth-party.md)) |
| **Change management** | Planners who feel replaced either ignore the tool or stop thinking. | Involve them in the side-by-side pilot; make overrides with reasons part of the job. |
| **Cost** | Licenses, data cleanup and people's time add up; the benefit depends on acting on the output. | Pilot on one use case with a clear before-and-after measure before scaling. |
| **Explainability to stakeholders** | "The model said so" won't convince a CFO, auditor or supplier. | Prefer methods and tools that show *why*; keep the decision log. |
| **Correlated signals** | Many companies using similar tools may react to the same alert at the same time. | Verify fast and act early; see the [case study](04-case-study/dual-sourcing-decision.md). |

---
[Back to README](README.md)
