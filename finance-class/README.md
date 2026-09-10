# Finance Class Download Checklist

Download all files in this folder before class.

## Required

- `Verified_Finance_Review_Pack_Lab.pdf`
- `Northstar_Life_Monthly_Performance.xlsx` — advanced synthetic workbook with detailed schedules, reconciliation controls, scenarios, and challenge prompts
- `Northstar_Monthly_Review_Notes.docx`
- `Finance_Claim_Ledger.xlsx`
- `Northstar_Finance_Fallback_Outputs.pdf`
- `Finance_Verification_Checklist.pdf`
- `Northstar_Finance_Review_Skill.zip` — instruction-only custom skill used during the Excel exercise

## Custom skill exercise

1. Unzip `Northstar_Finance_Review_Skill.zip`.
2. In Copilot in Excel, open **Settings > Manage skills > Custom skills**.
3. Copy the complete `northstar-finance-review` folder into the skills folder, then select **Refresh**.
4. Invoke `@northstar-finance-review` and verify the resulting `SkillReview` sheet against the source tables.

If Custom skills is unavailable in your tenant, paste [`skills/northstar-finance-review/SKILL.md`](skills/northstar-finance-review/SKILL.md), followed by: `Run the complete review on this workbook and create the SkillReview sheet. Include every required section, and do not present a causal explanation as fact.`

Keep `Northstar_Monthly_Review_Notes.docx` closed until the instructor tells you to open it; first freeze the cause-free variance ranking from the workbook.

Use only approved company data and tenant-approved Copilot surfaces. The Northstar Life files are synthetic and contain no MassMutual business data.
