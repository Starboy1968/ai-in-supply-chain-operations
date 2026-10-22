# 5. Anomaly detection in invoices and shipments

> Examples are fictional and illustrative.

## The basics, in plain words

An **anomaly** is something that doesn't look like the usual pattern. In supply chain money and freight, the common ones are:
- **Duplicate invoices:** the same charge billed twice, sometimes with a slightly different invoice number.
- **Split invoices:** one charge broken into several smaller ones, often to stay under an approval limit.
- **Freight audit issues:** charges that don't match the agreed rate, extra fees nobody approved, or bills for shipments that didn't happen.
- **ETA deviations:** shipments running later (or earlier) than expected.
- **Bank-detail changes:** a supplier or carrier "updating" where to send payment, a common fraud pattern.

## The operational problem

AP and freight teams check invoices by hand or by sampling. Volume is high, most invoices are fine, and the odd ones hide in the crowd. Late shipments are noticed when the customer calls.

## How AI helps

- **What it does:** rules plus pattern-spotting models compare each invoice with the purchase order, the shipment record, the agreed rate and past invoices, then flag the odd ones for a person to review. Shipment tracking tools predict arrival times and flag loads that are drifting late.
- **Data needed:** invoices, purchase orders, receiving records, shipment records with reference numbers, rate agreements, vendor master data (including bank-detail change history), tracking events.

## Step by step for a manager

1. Start with simple, explainable checks: same vendor + same amount + close dates; several invoices for one shipment; charges above the agreed rate.
2. Run them on the last few months of paid invoices first. This shows what's already slipped through and tunes the checks.
3. Route flags to a named reviewer with a target time to clear them.
4. Record the outcome of every flag (real problem / false alarm) so the checks get better.
5. Treat **any bank-detail change** as high risk: confirm it by calling a number you already have on file, never one from the request.
6. For shipments: agree what counts as "late enough to act", and who calls the customer.

## A simple prompt

> Below is an anonymized export of last quarter's freight invoices (carrier, invoice number, shipment/PRO reference, date, amount, agreed rate). Find: possible duplicates (same carrier and amount within 30 days, or same shipment reference), groups of invoices for one shipment that look split, and amounts above the agreed rate. Show each finding with the rows involved and why it was flagged. Don't conclude fraud; label everything "for review".

## Before and after (fictional)

| | Before | After |
|---|---|---|
| Checking | Random sample checked by hand | Every invoice checked against simple rules; odd ones go to a reviewer |
| Split and duplicate bills | Found by chance, if at all | Flagged before payment |
| Late shipments | Customer calls first | Team gets an alert and calls the customer first |

## What to check / KPIs to track

- **Invoice exception rate:** share of invoices flagged, and how many of those were real problems.
- Time to clear a flag.
- Money recovered or prevented (actual, from your own records).
- Bank-detail changes verified by callback (target: all of them).
- Shipments arriving outside the promised window.

## Where AI falls short

- Too many false alarms and people stop looking (alert fatigue).
- A clever fraud that looks normal won't be flagged; callbacks and approvals still matter.
- If the system that flags invoices can also **approve** them, a mistake flows straight to payment.
- Tracking predictions depend on carriers sending timely updates.

## Risk link

- [R01 AI-enabled supplier impersonation and payment fraud](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R01-supplier-impersonation-payment-fraud.md)
- Worked example: AI freight audit that auto-approves small invoices, in [ai-assisted-risk-analysis](https://github.com/Starboy1968/ai-assisted-risk-analysis/blob/main/worked-example/04-final-risk-register.md) (R1 carrier bank-change fraud, R2 invoice auto-approval)

---
[Back to README](../README.md)
