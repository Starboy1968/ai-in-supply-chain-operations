# Scenario 2: A buyer compares supplier quotes and contracts with an LLM

> **Fictional and illustrative.** Company and supplier names are made up.

**Setting.** A buyer at "Kestrel Fabrication" must pick a second source for a machined bracket. Three suppliers sent quotes and their standard terms, each in a different format. The company has an approved enterprise AI assistant; free public chatbots are blocked.

**What happens.**
1. The buyer writes down the decision criteria first: lead time, quality certification, price, price-change terms, minimum order, and termination rights.
2. In the approved assistant, the buyer asks for a comparison table, using only the documents, with quoted text and section numbers, and "not stated" for gaps.
3. The table comes back quickly. Checking each cell against the source, the buyer finds:
   - one supplier's "price valid 12 months" is actually "90 days" in the document. The assistant misread a table;
   - one supplier's price-escalation clause sits in a separate terms document the assistant never saw, so it showed "not stated";
   - a quality certification is listed in a quote, but no certificate was attached.
4. The buyer corrects the table, asks the suppliers for the missing terms and certificate, and sends the termination and liability sections to legal.
5. The final choice uses the buyer's criteria, not the assistant's summary.

**Where AI helped.** Turned three messy formats into one table and a list of questions in minutes.

**Where people had to step in.** Catching a misread, a missing document and an unverified claim; judging which terms matter; legal review.

**Lessons.**
- Ask for **quoted text and section numbers**, so checking is fast.
- "Not stated" may mean "in another document". Ask what documents are referenced.
- Use only approved tools for supplier pricing and terms.
- Decide the criteria before you see the AI's table, so it doesn't frame the decision for you (anchoring).

Related: [supplier selection how-to](../02-use-cases/02-supplier-selection-and-monitoring.md), [contract review how-to](../02-use-cases/06-contract-review.md), [R07](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R07-hallucinated-biased-supplier-decisions.md), [R02](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R02-data-leakage-genai-shadow-ai.md)

---
[Back to README](../README.md)
