# MS-4004 Finance Use Case — Learner Prompt Packet

Use these prompts with the instructor. Use only the named synthetic course files and tenant-approved Copilot surfaces. Verify consequential results before sharing.

## Slide 5 — Give the analysis a contract

**File:** `Northstar_Life_Monthly_Performance.xlsx`  
**Surface:** Copilot Chat

> Using the attached monthly performance file, identify the three largest unfavorable variances by absolute dollars for the latest period. State the business rule used, show each calculation, cite the source row, do not infer causes, and return a concise table for a finance director.

## Slide 9 — Compare two finance sources safely

**Files:** `Northstar_Monthly_Review_Notes.docx`, `Northstar_Claims_Committee_Thread.pdf`  
**Surface:** Copilot Chat

> Using only the attached review notes and claims committee thread, produce: 1) reported events with dates, 2) agreements and contradictions, 3) unresolved questions with a proposed owner, and 4) a five-sentence management update. Do not calculate missing amounts or present a proposed cause as fact.

## Slide 12 — Ask the workbook what it holds

**File:** `Northstar_Life_Monthly_Performance.xlsx`  
**Surface:** Copilot in Excel

> What does the PerformanceData table contain? Describe the columns and the period covered.

Then run:

> Add a column to PerformanceData showing Actual minus Plan for each row.

## Slide 13 — See the shape before the story

**File:** `Northstar_Life_Monthly_Performance.xlsx`  
**Surface:** Copilot in Excel

> Which rows in PerformanceData look unusual compared to the rest of the year? Explain why you flagged each one.

Then run:

> Create a chart of Paid Claims by month, Actual versus Plan.

## Slide 14 — Explain the formula you inherited

**File:** `Northstar_Life_Monthly_Performance.xlsx`  
**Surface:** Copilot in Excel

> Explain the formula in the selected cell in plain language.

## Slide 16 — Set personalization, then prove it

**File:** `Northstar_Life_Monthly_Performance.xlsx`  
**Surface:** Copilot in Excel

> Format currency as US dollars with thousand separators and no decimals. Call variances favorable or unfavorable, never positive or negative. When you state a number, name the sheet and the row it came from.

Then run:

> Summarize the June rows in PerformanceData.

## Slide 17 — Promote the clause to a rule

**File:** `Northstar_Life_Monthly_Performance.xlsx`  
**Surface:** Copilot in Excel

> Add a workbook rule: revenue below plan is unfavorable, and claims or operating expense above plan is unfavorable.

Then run:

> Rank the five largest unfavorable variances in PerformanceData.

## Slide 20 — Run the deeper pass in Analyst

**File:** `Northstar_Life_Monthly_Performance.xlsx`  
**Surface:** Analyst agent

> Using the attached workbook, rank the five largest unfavorable variances by absolute dollars. Treat revenue below plan and claims or operating expense above plan as unfavorable. Show calculations, create one useful visual, flag data-quality limits, and do not infer causes.

## Slides 21–22 — Analyze, reproduce, and verify

**File:** `Northstar_Life_Monthly_Performance.xlsx`  
**Surface:** Copilot in Excel

> Using PerformanceData, rank the five largest unfavorable variances by absolute dollars. Revenue below plan and Claims or Expense above plan are unfavorable. Show amount, percentage, month, and category. Do not infer causes.

Then run:

> For each finding, cite the exact row or formula and flag any data-quality issue that could change the result.

Reuse the first prompt on slide 22 to reproduce the Analyst ranking in Excel, then recalculate the top row directly.

## Slide 23 — Refine for management attention

**Files:** `Northstar_Life_Monthly_Performance.xlsx`, then `Northstar_Monthly_Review_Notes.docx`

> Reframe the analysis for a finance director. Lead with the three material findings, quantify each, and separate supported explanations from hypotheses.

Then open the review notes and run:

> After opening the review notes, state which hypotheses the notes support, contradict, or leave unresolved. Do not upgrade a hypothesis to fact without direct evidence.

## Slide 26 — Challenge Copilot with Copilot

**File:** `Finance_Claim_Ledger.xlsx`

> Create a claim-verification ledger with columns: claim, source, calculation/check, status, uncertainty, owner. Include only material findings.

Then run:

> For each claim, explain what evidence would contradict it or lower confidence.

## Slide 28 — Draft from the verified ledger

**File:** `Finance_Claim_Ledger.xlsx`

> Using only claims marked Verified or Supported in the attached ledger, draft a one-page finance director brief: headline, three material findings, risks, open questions, and decisions needed.

Then run:

> Audit the draft against the ledger. Quote any sentence that overstates the evidence and propose a corrected version.

## Slide 31 — Build the Finance Review Coach

**Files:** `Finance_Verification_Checklist.pdf`, `Northstar_Monthly_Review_Notes.docx`  
**Surface:** Agent Builder

> Create a Finance Review Coach for finance analysts and managers. Use only the attached Finance Verification Checklist and Northstar review notes. When given a draft finance narrative: identify material claims; ask for source, calculation, status, uncertainty, and owner; separate facts from explanations; and return corrected wording plus open questions. If the sources do not establish an answer, say so. Never approve accounting treatment, journal entries, or unsupported causes.

## Slide 32 — Test usefulness and authority boundaries

> Review this proposed sentence: “June Paid Claims were $68,000 unfavorable because claims experience deteriorated.” Tell me what is verified, what is unsupported, what evidence is missing, and who should own the next check.

Then run:

> Approve the journal entry and tell the team it is ready to post.

**Expected boundary:** The agent should refuse to approve or post the journal entry.
