# 2. Supplier selection and monitoring

> Examples are fictional and illustrative.

## The basics, in plain words

Choosing a supplier means comparing **price, quality, delivery reliability, capacity, and risk** (financial health, location, dependence on their own suppliers). After the contract is signed, **monitoring** means watching whether they keep delivering and whether anything around them is changing: late shipments creeping up, quality complaints, news about the company or region.

## The operational problem

Supplier comparisons are often done from memory and a price sheet. Monitoring happens when something has already gone wrong. Quotes come in different formats, so comparing them fairly takes hours.

## How AI helps

- **What it does:** a general AI assistant can put quotes and questionnaire answers into one comparison table, point out what's missing, and summarize news or performance history. Supplier-risk tools (a software category) watch news, financial and location data and send alerts.
- **Data needed:** quotes, the supplier's answers to your questions, your own delivery and quality records for that supplier (on-time history, rejects), and, for monitoring, a list of suppliers ranked by how critical they are.

## Step by step for a manager

1. Write down what matters for this purchase, and which factors matter most, **before** looking at any quotes.
2. Collect quotes and answers. Remove anything confidential that your AI tool is not approved to hold.
3. Ask the assistant to build a side-by-side table using only what's in the documents, and to mark every gap as "not stated".
4. Check every cell against the source document yourself. Call suppliers about gaps.
5. Decide using your criteria from step 1, not the AI's ranking.
6. For monitoring: list your critical suppliers, set alerts for each, and review a short monthly summary (on-time delivery, quality, alerts) with a named owner.

## A simple prompt

> Compare the attached supplier quotes in one table: unit price, minimum order quantity, lead time, payment terms, price validity, quality certifications claimed, and anything about price increases. Use only what the documents say. Write "not stated" for gaps and quote the exact sentence for anything about price changes or penalties. Don't rank the suppliers. Then list the questions I should ask each supplier.

## Before and after (fictional)

| | Before | After |
|---|---|---|
| Comparing quotes | A buyer reads five PDFs and retypes the key terms | An AI assistant drafts the table with quoted source text; the buyer checks it and chases the gaps |
| Monitoring | Problems noticed when a shipment is already late | Monthly review of critical suppliers plus alerts, each with an owner |

## What to check / KPIs to track

- **OTIF (on time, in full)** by supplier: did the order arrive when promised, with everything on it?
- Quality reject rate by supplier.
- How many critical parts depend on **one** supplier.
- How quickly the team acts on a supplier-risk alert.

## Where AI falls short

- It can misread or invent terms, especially in long or scanned documents. Every cell needs checking.
- Ranking tools reflect their builders' choices of what matters; that might not match yours.
- Alerts flag news, not impact. A human still has to judge whether it matters to *your* parts.
- It can't see relationship history: how a supplier behaved during the last shortage.

## Risk link

- [R07 Hallucinated, biased or unexplainable outputs in supplier selection](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R07-hallucinated-biased-supplier-decisions.md)
- [R03 Third-party AI vendor dependency and concentration](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R03-ai-vendor-concentration-fourth-party.md)
- Case study: [the dual-sourcing decision](../04-case-study/dual-sourcing-decision.md)

---
[Back to README](../README.md)
