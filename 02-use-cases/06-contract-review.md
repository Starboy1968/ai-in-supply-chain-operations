# 6. Contract review

> Examples are fictional and illustrative. AI clause extraction is not legal advice; contracts still go to legal.

## The basics, in plain words

Supply contracts hide the terms that cost money later: **automatic renewals** (the contract quietly rolls over unless you give notice by a date), **price escalation** (the supplier can raise prices when an index or their costs go up), minimum volumes, penalties, liability caps, termination rights, and who owns data.

## The operational problem

Contracts sit in shared drives. Nobody tracks notice dates. Price increases arrive and nobody remembers agreeing to them.

## How AI helps

- **What it does:** a large language model (LLM), the kind behind general AI assistants, can read a contract and pull out specific clauses into a table: renewal date, notice period, price-change terms, termination rights. Contract management tools (a software category) do this across many contracts and set reminders.
- **Data needed:** the contracts themselves, ideally as readable text rather than poor scans, and a list of the fields you want pulled out.

## Step by step for a manager

1. Decide the fields you need (renewal date, notice period, price escalation, minimums, termination, liability, data use).
2. Use only an AI tool approved for confidential documents. Contract terms and pricing are confidential.
3. Ask for each field **with the exact quoted text and page or section**, and "not found" if absent.
4. Check every extracted field against the quoted text yourself. Send anything about liability, indemnity or data to legal.
5. Put renewal and notice dates in a shared calendar with an owner, set early enough to renegotiate.
6. Review price-escalation terms before each renewal.

## A simple prompt

> From the attached supply agreement, extract into a table: start date, end date, auto-renewal (yes/no), notice period to stop renewal, price increase or escalation terms, minimum purchase commitments, termination rights, liability cap. For each, quote the exact text and give the section number. If something isn't in the document, write "not found". Don't summarize or interpret beyond the quote.

## Before and after (fictional)

| | Before | After |
|---|---|---|
| Notice dates | Discovered after the contract has already renewed | Dates on a shared calendar with an owner, set early |
| Price increases | Accepted because nobody can find the clause | Clause quoted and checked before renewal talks |
| Review time | Full read of every contract | Targeted check of quoted clauses, legal review of risky ones |

## What to check / KPIs to track

- Contracts with renewal and notice dates recorded.
- Renewals that happened without a decision (target: none).
- Extracted fields that turned out wrong when checked (tells you how far to trust the tool).

## Where AI falls short

- It can **invent or misquote** clauses (hallucination) [S9], especially in long or scanned documents. That's why every field needs a quote and a check.
- It may miss terms that sit in a separate document the contract refers to (schedules, terms posted on a website).
- It doesn't know your negotiating history or what "market" terms look like.
- Uploading contracts to an unapproved tool can leak confidential terms.

## Risk link

- [R07 Hallucinated, biased or unexplainable outputs](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R07-hallucinated-biased-supplier-decisions.md)
- [R02 Data leakage through generative AI tools](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R02-data-leakage-genai-shadow-ai.md)
- [R09 Intellectual property exposure through AI vendor terms](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R09-ip-exposure-ai-vendor-terms.md)
- [R05 Regulatory, privacy and contractual non-compliance](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R05-regulatory-privacy-contract-compliance.md)

---
[Back to README](../README.md)
