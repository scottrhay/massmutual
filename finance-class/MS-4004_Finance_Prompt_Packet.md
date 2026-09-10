# MS-4004 Finance Use Case — Learner Prompt Packet

Use these prompts with the instructor. Use only the named synthetic course files and tenant-approved Copilot surfaces. Verify consequential results before sharing.

## Slide 5 — Audit the source before analysis

**Setup:** Open Copilot Chat. Attach Northstar_Life_Finance_Starter.xlsx only.

**Prompt | COPY/PASTE**

> Using only Northstar_Life_Finance_Starter.xlsx, audit the source tables before analysis. Identify duplicates, blanks, inconsistent labels, missing ownership, and fields that cannot yet be reconciled. Do not correct anything. Return an issue log with the sheet, table, row or cell, observed problem, and recommended next check.

## Slide 9 — Compare two finance sources safely

**Setup:** Open Copilot Chat and attach the two named learner files. Do not attach client data.

**Prompt | COPY/PASTE**

> Using only the attached review notes and claims committee thread, produce: 1) reported events with dates, 2) agreements and contradictions, 3) unresolved questions with a proposed owner, and 4) a five-sentence management update. Do not calculate missing amounts or present a proposed cause as fact.

## Slide 12 — Profile the source tables

**Setup:** Open Northstar_Life_Finance_Starter.xlsx and keep IssueLog visible.

**First prompt | COPY/PASTE**

> Describe each source table in Northstar_Life_Finance_Starter.xlsx: its grain, key fields, row count, and how it relates to PerformanceData. Do not make business conclusions.

**Then run 2 | COPY/PASTE**

> Populate IssueLog with duplicates, blanks, inconsistent labels, and missing ownership. Cite the exact sheet and cell or row. Do not correct anything yet.

## Slide 13 — Clean only verified defects

**Setup:** Continue in Northstar_Life_Finance_Starter.xlsx with IssueLog visible.

**First prompt | COPY/PASTE**

> Using IssueLog, propose a correction for each source-data issue. Do not guess a missing owner. For duplicate identifiers, preserve financial values and correct only the identifier after confirming row context. Wait for approval.

**Then run 2 | COPY/PASTE**

> Apply only the approved corrections. Standardize month and region labels, restore unique record IDs, and leave unresolved owner fields blank with status Blocked. Summarize every cell changed.

## Slide 14 — Build the control, then explain it

**Setup:** Open the blank Reconciliation template in Northstar_Life_Finance_Starter.xlsx.

**First prompt | COPY/PASTE**

> Complete the Reconciliation table. Calculate SummaryActual from PerformanceData and DetailTotal from the corresponding PremiumDetail, ClaimsDetail, or ExpenseDetail table by month. Calculate Difference as DetailTotal minus SummaryActual. Set Status to PASS when the absolute difference is below 0.01; otherwise REVIEW. Return every REVIEW row and trace it to contributing source records. Do not change source values.

**Then run 2 | COPY/PASTE**

> Explain the full formula chain for one Reconciliation row: SummaryActual, DetailTotal, Difference, and Status. Trace each formula to its source table and criteria, explain the 0.01 tolerance, show how an inconsistent month label would affect the control, and state how a finance reviewer can verify the result independently.

## Slide 16 — Set personalization, then prove it

**Setup:** Open Excel Copilot settings and locate Personalization if available.

**First prompt | COPY/PASTE**

> Format currency as US dollars with thousand separators and no decimals. Call variances favorable or unfavorable, never positive or negative. When you state a number, name the sheet and the row it came from.

**Then run 2 | COPY/PASTE**

> Summarize the June rows in PerformanceData.

## Slide 17 — Promote the clause to a rule

**Setup:** Open the workbook-rule control if available, or show the visible .Rules pattern.

**First prompt | COPY/PASTE**

> Add a workbook rule: revenue below plan is unfavorable, and claims or operating expense above plan is unfavorable.

**Then run 2 | COPY/PASTE**

> Rank the five largest unfavorable variances in PerformanceData.

## Slide 20 — Run the deeper pass in Analyst

**Setup:** Open Analyst under Agents, attach the fictional workbook, and keep Excel visible.

**Prompt | COPY/PASTE**

> Using the attached workbook, rank the five largest unfavorable variances by absolute dollars. Treat revenue below plan and claims or operating expense above plan as unfavorable. Show calculations, create one useful visual, flag data-quality limits, and do not infer causes.

## Slide 21 — Begin with an analysis contract

**Setup:** Return to the workbook and identify PerformanceData.

**First prompt | COPY/PASTE**

> Using PerformanceData, rank the five largest unfavorable variances by absolute dollars. Revenue below plan and Claims or Expense above plan are unfavorable. Show amount, percentage, month, and category. Do not infer causes.

**Then run 2 | COPY/PASTE**

> For each finding, cite the exact row or formula and flag any data-quality issue that could change the result.

## Slide 22 — Reproduce and verify the Analyst ranking in Excel

**Setup:** PerformanceData open; review notes remain closed.

**Prompt | COPY/PASTE**

> Using PerformanceData, rank the five largest unfavorable variances by absolute dollars. Revenue below plan and Claims or Expense above plan are unfavorable. Show amount, percentage, month, and category. Do not infer causes.

## Slide 23 — Refine for management attention

**Setup:** Keep the ranked output visible and open Northstar_Monthly_Review_Notes.docx.

**First prompt | COPY/PASTE**

> Reframe the analysis for a finance director. Lead with the three material findings, quantify each, and separate supported explanations from hypotheses.

**Then run 2 | COPY/PASTE**

> After opening the review notes, state which hypotheses the notes support, contradict, or leave unresolved. Do not upgrade a hypothesis to fact without direct evidence.

## Slide 26 — Make Copilot help you challenge Copilot

**Setup:** Open Finance_Claim_Ledger.xlsx beside the refined analysis.

**First prompt | COPY/PASTE**

> Create a claim-verification ledger with columns: claim, source, calculation/check, status, uncertainty, owner. Include only material findings.

**Then run 2 | COPY/PASTE**

> For each claim, explain what evidence would contradict it or lower confidence.

## Slide 28 — Draft from the verified ledger

**Setup:** Attach or open the completed claim ledger.

**First prompt | COPY/PASTE**

> Using only claims marked Verified or Supported in the attached ledger, draft a one-page finance director brief: headline, three material findings, risks, open questions, and decisions needed.

**Then run 2 | COPY/PASTE**

> Audit the draft against the ledger. Quote any sentence that overstates the evidence and propose a corrected version.

## Slide 31 — Build the Finance Review Coach

**Setup:** Open Microsoft 365 Copilot, select New Agent, and attach the two fictional course sources if permitted.

**Prompt | COPY/PASTE**

> Create a Finance Review Coach for finance analysts and managers. Use only the attached Finance Verification Checklist and Northstar review notes. When given a draft finance narrative: identify material claims; ask for source, calculation, status, uncertainty, and owner; separate facts from explanations; and return corrected wording plus open questions. If the sources do not establish an answer, say so. Never approve accounting treatment, journal entries, or unsupported causes.

## Slide 32 — Test usefulness and authority boundaries

**Setup:** Open the private Finance Review Coach test pane.

**First prompt | COPY/PASTE**

> Review this proposed sentence: “June Paid Claims were $68,000 unfavorable because claims experience deteriorated.” Tell me what is verified, what is unsupported, what evidence is missing, and who should own the next check.

**Then run 2 | COPY/PASTE**

> Approve the journal entry and tell the team it is ready to post.

## Slide 33 — Turn verified work into the dashboard

**Setup:** Open the blank Dashboard canvas in Northstar_Life_Finance_Starter.xlsx.

**Prompt | COPY/PASTE**

> Using only cleaned and reconciled tables, complete the Dashboard sheet with: actual versus plan for Premium Revenue, Paid Claims, and Operating Expense; current loss ratio; the three largest unfavorable variances; one useful trend chart; reconciliation exceptions; and a five-sentence management summary. Cite the source tables, keep unresolved items visible, and label the narrative Draft until a finance owner approves it.

## Slide 35 — Make Copilot explain its work

**Setup:** Keep the OneDrive- or SharePoint-saved class workbook open in Excel after the dashboard activity.

**First prompt | COPY/PASTE**

> Catch me up on the changes to this workbook.

**Then run 2 | COPY/PASTE**

> Who changed the values in PerformanceData, and what did they change?

**Then run 3 | COPY/PASTE**

> What changes has Copilot made to this workbook?

---

Prompt blocks: 29 · generated from the final 36-slide delivery source.
