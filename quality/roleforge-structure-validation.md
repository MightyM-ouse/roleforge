# RoleForge Structure Validation

This document defines structural validation guidance for RoleForge. It is documentation guidance only. It does not add executable scripts or runtime automation.

## Required File Checks

Validate that all 11 canonical role files exist:

1. `roles/RF-ROLE-001-friendly-colleague.md`
2. `roles/RF-ROLE-002-project-mentor.md`
3. `roles/RF-ROLE-003-ai-tutor.md`
4. `roles/RF-ROLE-004-product-owner.md`
5. `roles/RF-ROLE-005-scrum-master.md`
6. `roles/RF-ROLE-006-system-architect.md`
7. `roles/RF-ROLE-007-software-developer.md`
8. `roles/RF-ROLE-008-tester-qa-analyst.md`
9. `roles/RF-ROLE-009-verifier-reviewer.md`
10. `roles/RF-ROLE-010-software-delivery-auditor.md`
11. `roles/RF-ROLE-011-technical-writer.md`

Validate that all required role-rule files exist:

1. `role-rules/RF-RULE-001-role-boundaries.md`
2. `role-rules/RF-RULE-002-role-selection.md`
3. `role-rules/RF-RULE-003-github-permissions.md`
4. `role-rules/RF-RULE-004-refusal-and-redirect.md`
5. `role-rules/RF-RULE-005-evidence-and-assumption-rules.md`
6. `role-rules/RF-RULE-006-memory-and-context.md`
7. `role-rules/RF-RULE-007-handoff-rules.md`
8. `role-rules/RF-RULE-008-role-lifecycle.md`

Validate that all required response-template files exist:

1. `response-templates/RF-TEMPLATE-001-friendly-colleague.md`
2. `response-templates/RF-TEMPLATE-002-project-mentor.md`
3. `response-templates/RF-TEMPLATE-003-ai-tutor.md`
4. `response-templates/RF-TEMPLATE-004-formal-role.md`
5. `response-templates/RF-TEMPLATE-005-github-issue.md`
6. `response-templates/RF-TEMPLATE-006-pr-review.md`
7. `response-templates/RF-TEMPLATE-007-role-redirect.md`

## Role File Heading Checks

Every `roles/RF-ROLE-*.md` file must contain the 15 Role File Standard v1 headings:

1. `## 1. Role Identity`
2. `## 2. Mission`
3. `## 3. Authority Level`
4. `## 4. Primary Responsibilities`
5. `## 5. Explicit Non-Responsibilities`
6. `## 6. Required Inputs`
7. `## 7. Valid Outputs`
8. `## 8. GitHub Permission`
9. `## 9. Refusal and Redirect Rules`
10. `## 10. Handoff Rules`
11. `## 11. Response Template`
12. `## 12. Good Request Examples`
13. `## 13. Bad Request Examples`
14. `## 14. Quality Checklist`
15. `## 15. Anti-Patterns`

## Link Checks

Validate that Markdown links in these files point to existing repository files:

1. `README.md`
2. `ROLE_INDEX.md`
3. `ROLEFORGE_MANIFEST.md`

Directory links may point to existing directories.

## Canonical Filename Checks

Old non-canonical role files must not be reintroduced, including:

1. `roles/friendly-colleague.md`
2. `roles/project-mentor.md`
3. `roles/ai-tutor.md`
4. `roles/product-owner.md`
5. `roles/scrum-master.md`
6. `roles/system-architect.md`
7. `roles/software-developer.md`
8. `roles/tester-qa-analyst.md`
9. `roles/verifier-reviewer.md`
10. `roles/software-delivery-auditor.md`
11. `roles/technical-writer.md`
12. `roles/ROLE_INDEX.md`

## Project-Neutrality Checks

Validate that Magna Enso references remain limited to adoption examples. Magna Enso may appear in:

1. `README.md` as a note that it is only an adoption example.
2. `project-adoption/magna-enso-adoption-example.md`.
3. Quality or adoption guidance that states Magna Enso must remain an example only.

Magna Enso must not become the purpose of RoleForge, a required dependency, or a required implementation target.

## Future Optional Automation

Future work may add validation automation, such as:

1. `scripts/validate-roleforge-structure.py`
2. `.github/workflows/validate-roleforge.yml`

Do not add these scripts until the validation behavior has been reviewed and approved.
