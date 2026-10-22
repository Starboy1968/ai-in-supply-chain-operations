# Scenario 3: The AP team catches freight invoice anomalies

> **Fictional and illustrative.** Company and carrier names are made up.

**Setting.** "Brightwater Foods Distribution" pays a few dozen carriers. Freight invoices are checked by sampling. The AP lead wants better coverage without new software yet.

**What happens.**
1. The AP lead exports last quarter's paid freight invoices with carrier, invoice number, shipment reference, date, amount and contracted rate, and removes bank details.
2. Using simple spreadsheet rules (and an approved AI assistant to help write them and summarize the results), the team flags:
   - invoices with the same carrier, amount and shipment reference but different invoice numbers (possible duplicates);
   - several invoices for one shipment, each just under the single-approver limit (possible splitting);
   - charges above the contracted rate, mostly unapproved extra fees.
3. Each flag goes to a named reviewer. Most turn out to have an explanation (a legitimate re-bill, an approved extra stop). A few are real: a duplicate already paid, and extra fees nobody approved.
4. Separately, a carrier emails asking to "update" its bank details. Under the team's rule, a clerk calls the carrier using the number already on file. The real carrier made no such request.
5. The team records every flag's outcome, tightens the rules that produced too many false alarms, and asks for an approval-limit check that looks at total invoices per shipment.

**Where AI helped.** Writing the checks, scanning every invoice instead of a sample, and summarizing results for the review.

**Where people had to step in.** Judging each flag, the callback that stopped a fraud attempt, and fixing the approval rule.

**Lessons.**
- Start with explainable rules on past data before buying a tool.
- Record outcomes; a check with only false alarms gets ignored.
- No AI replaces a callback on bank-detail changes.
- A tool that flags invoices should not also approve them without review.

Related: [anomaly detection how-to](../02-use-cases/05-anomaly-detection-invoices-and-shipments.md), [R01 payment fraud](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R01-supplier-impersonation-payment-fraud.md), [ai-assisted-risk-analysis worked example](https://github.com/Starboy1968/ai-assisted-risk-analysis)

---
[Back to README](../README.md)
