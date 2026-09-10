---
name: northstar-finance-review
description: Use when reviewing the Northstar Life workbook or when asked to turn its finance tables into a checkable variance review.
---

# Northstar finance review

Use the workbook as the only source of truth. Complete the controls before writing a narrative.

Northstar Life is synthetic and contains no MassMutual business data.

## Scope

- Work only with the visible tables in the open workbook.
- Do not search the web or use other files unless the user explicitly adds an approved source.
- Never infer a business cause from a variance, trend, contributor, or data-quality flag.
- Do not modify `Dashboard`, `PerformanceData`, `PremiumDetail`, `ClaimsDetail`, `ExpenseDetail`, `MonthlyContext`, `Reconciliation`, or `ScenarioModel`.

## Workflow

1. Confirm that `PerformanceData`, `Reconciliation`, `PremiumDetail`, `ClaimsDetail`, and `ExpenseDetail` are present. If a required table or sheet is missing, stop and name it.
2. Read every row in `Reconciliation`. If any status is not `PASS` or any difference is nonzero, stop the review and list only the failed controls.
3. Rank the five largest unfavorable variances in `PerformanceData` by absolute dollars:
   - Premium Revenue below plan is unfavorable.
   - Paid Claims above plan is unfavorable.
   - Operating Expense above plan is unfavorable.
4. For each ranked finding, show month, category, plan, actual, dollar variance, percentage variance, and the exact source row or formula.
5. Use the relevant detail table to identify the largest contributing records. Describe what the rows show, not why the result occurred.
6. Read the data-quality warning for each finding. Label every explanation as `Supported`, `Hypothesis`, or `Blocked`. Workbook arithmetic alone can support what happened, not an external cause.
7. Recalculate the largest finding independently and show the arithmetic.
8. If the user asks about `ScenarioModel`, describe it as an illustrative sensitivity exercise, never a forecast. State every assumption before comparing outputs.

## Workbook output

Unless the user requests chat-only output, create or refresh a worksheet named `SkillReview` containing:

1. `CONTROL STATUS` — reconciliation result and any failures.
2. `TOP FIVE UNFAVORABLE VARIANCES` — the ranked table with source references.
3. `DETAIL CONTRIBUTORS` — largest records from the relevant detail schedules.
4. `CLAIM BOUNDARIES` — claim, status, supporting evidence, missing evidence, and owner needed.
5. `INDEPENDENT CHECK` — the arithmetic for the largest finding.
6. `OPEN QUESTIONS` — evidence needed before any cause can be presented.

Use editable Excel tables, US-dollar formatting with thousand separators and no decimals, percentages with one decimal, banded rows, frozen headers, and clear section labels. Preserve all source sheets and formulas.

## Completion check

Before reporting completion:

- confirm every reconciliation control passed;
- confirm the top finding was independently recalculated;
- confirm no causal explanation is presented as fact;
- name the new or refreshed `SkillReview` sheet;
- state what still requires a finance owner or additional source.

## Common pitfalls to avoid

- Do not rank solely by percentage when the request specifies absolute dollars.
- Do not treat a detail contributor as a proven cause.
- Do not hide data-quality warnings.
- Do not call scenario outputs forecasts.
- Do not change source data to make a reconciliation pass.

After class, keep this skill only if your organization's policy allows it; otherwise remove the `northstar-finance-review` folder from your custom-skills folder.
