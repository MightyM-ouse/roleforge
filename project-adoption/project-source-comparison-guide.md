# Project Source Comparison Guide

## Purpose

This guide explains how to decide the minimum useful ChatGPT Project source pack when adopting RoleForge into another GitHub project.

The goal is to compare the target project with RoleForge and recommend only the files that help ChatGPT understand project authority, workflow, governance, and assistant role behavior.

This guide does not instruct users to copy the full RoleForge repository into every project.

## When to use this guide

Use this guide when:

1. Adopting RoleForge into an existing GitHub project.
2. Creating a ChatGPT Project for a specific repository.
3. Deciding which RoleForge role files are needed.
4. Comparing project-native governance with RoleForge role behavior.
5. Avoiding bloated project source.

## Inputs required

Prepare these inputs before the review:

1. Target GitHub repository URL.
2. RoleForge repository URL.
3. Target project README.
4. Project instruction files, if any.
5. Project governance files, if any.
6. Role or agent routing files, if any.
7. Workflow files, if any.
8. Evidence or state files, if any.

## Review principles

1. Project authority remains with the target project.
2. RoleForge controls assistant role behavior, not project state.
3. Do not replace project governance with RoleForge.
4. Do not add the full RoleForge repo unless justified.
5. Prefer minimum source packs.
6. Do not add frequently changing state files as static project source.
7. Add dynamic files only when needed for a specific review, then refresh from GitHub.
8. Explain every recommended file with a reason.

## Step 1: Inspect the target project

Inspect the target repository before recommending source files. Identify whether the project contains:

1. `README.md`.
2. `AGENTS.md` or equivalent instruction files.
3. ChatGPT, Codex, Claude, or agent adapter files.
4. Governance folder.
5. Workflow folder.
6. Role registry or agent registry.
7. Routing index.
8. Current-state or status files.
9. Task packets.
10. Evidence folders.
11. Archive or vendor folders.
12. Source code folders.

The goal is to understand which files are authoritative, which files are operational context, and which files are too dynamic or implementation-specific for permanent ChatGPT Project source.

## Step 2: Identify project authority files

Project authority files usually define:

1. Who owns decisions.
2. What branch is accepted.
3. What current state means.
4. Who can update GitHub.
5. How work is approved.
6. What must be verified before current-state claims.

These files are usually good candidates for ChatGPT Project source because they tell the assistant how the target project governs work.

## Step 3: Identify project workflow and governance files

Workflow and governance files are good candidates when they are stable and define how work happens.

Examples include:

1. Agent routing.
2. Workflow rules.
3. Permission boundaries.
4. Review process.
5. Evidence rules.
6. Merge rules.
7. Handoff rules.

Prefer files that define durable process. Avoid files that are only snapshots of current progress.

## Step 4: Identify dynamic files that should not be added as static source

Dynamic files often should not be permanently added as ChatGPT Project source because they become stale.

Examples include:

1. Current status maps.
2. Active work registries.
3. Task folders.
4. Issue evidence.
5. PR evidence.
6. Test logs.
7. Archive folders.
8. Vendor folders.
9. Generated outputs.
10. Full source code.

These files should be checked live from GitHub when a current-state claim or review is needed.

## Step 5: Map the target project to RoleForge

Compare the target project's existing role or agent model with RoleForge roles.

Use these mapping questions:

1. Does the project already define ChatGPT's role?
2. Does it distinguish Product Owner, Architect, Developer, Tester, Reviewer, Auditor, and Writer responsibilities?
3. Does it define GitHub permissions?
4. Does it define refusal behavior?
5. Does it define evidence classification?
6. Does it define handoffs?
7. Does it define role selection rules?
8. Does it define informal roles such as tutor, mentor, or colleague?

If the target project already defines a rule, RoleForge should complement it unless the project owner explicitly adopts RoleForge as the assistant-role authority.

## Step 6: Select the minimum RoleForge source pack

Start with a minimum RoleForge core pack instead of the full repository:

| RoleForge file | Reason |
|---|---|
| `ROLEFORGE_MANIFEST.md` | Defines the operating model and core authority boundaries. |
| `ROLE_INDEX.md` | Provides quick role selection and links to role files. |
| `role-rules/RF-RULE-001-role-boundaries.md` | Prevents roles from silently performing the wrong work. |
| `role-rules/RF-RULE-002-role-selection.md` | Helps choose the right RoleForge role for the target project task. |
| `role-rules/RF-RULE-003-github-permissions.md` | Defines GitHub authority and approval boundaries. |
| `role-rules/RF-RULE-004-refusal-and-redirect.md` | Defines how wrong-role requests should stop and redirect. |
| `role-rules/RF-RULE-005-evidence-and-assumption-rules.md` | Separates evidence, claims, assumptions, risks, and recommendations. |
| `role-rules/RF-RULE-007-handoff-rules.md` | Defines role-to-role handoff behavior. |
| `role-rules/RF-RULE-008-role-lifecycle.md` | Defines the lifecycle for selecting, validating, performing, and closing role work. |
| `response-templates/RF-TEMPLATE-004-formal-role.md` | Provides a reusable formal-role output structure. |
| `response-templates/RF-TEMPLATE-007-role-redirect.md` | Provides the standard wrong-role redirect pattern. |

This pack includes the RoleForge operating model, selection rules, boundary controls, evidence handling, lifecycle behavior, and the main output templates.

Do not include every RoleForge file by default.

## Step 7: Select role files based on actual project usage

Add RoleForge role files only for roles ChatGPT is expected to perform in the target project.

| Project need | Add RoleForge role file |
|---|---|
| Informal discussion / early thinking | `RF-ROLE-001-friendly-colleague.md` |
| Decide what role or next step is needed | `RF-ROLE-002-project-mentor.md` |
| Learn concepts step by step | `RF-ROLE-003-ai-tutor.md` |
| Scope, value, priority, acceptance criteria | `RF-ROLE-004-product-owner.md` |
| Sprint flow, blockers, process health | `RF-ROLE-005-scrum-master.md` |
| Architecture review and technical risk | `RF-ROLE-006-system-architect.md` |
| Implementation by ChatGPT | `RF-ROLE-007-software-developer.md` |
| Test design and QA risk | `RF-ROLE-008-tester-qa-analyst.md` |
| Verify completed work against criteria | `RF-ROLE-009-verifier-reviewer.md` |
| Audit delivery records, GitHub evidence, worker status | `RF-ROLE-010-software-delivery-auditor.md` |
| Documentation from approved facts | `RF-ROLE-011-technical-writer.md` |

Do not add Developer or Tester role files unless ChatGPT is expected to perform those roles in that project.

## Step 8: Produce the final recommendation

The final recommendation should include:

1. Files to add from the target project.
2. Files to add from RoleForge.
3. Files not to add.
4. Reason for each group.
5. Risks if omitted.
6. Follow-up tests to run.

Every recommended file should have a specific reason. If the reason is only "might be useful," do not add it.

## Output template

```markdown
# RoleForge Project Source Recommendation: <Target Project>

## Review summary

...

## Target project files to add

| File | Reason |
|---|---|
| | |

## RoleForge core files to add

| File | Reason |
|---|---|
| | |

## RoleForge role files to add

| File | Reason |
|---|---|
| | |

## Files not recommended as static source

| File or folder | Reason |
|---|---|
| | |

## Risks and conditions

...

## Recommended validation tests

...

## Final verdict

...
```

## Example output format

# RoleForge Project Source Recommendation: example-ai-project

## Review summary

`example-ai-project` has its own project instructions and release workflow, but it does not define assistant role boundaries. Use the project files for authority and RoleForge for assistant role behavior.

## Target project files to add

| File | Reason |
|---|---|
| `README.md` | Defines project purpose and user-facing scope. |
| `AGENTS.md` | Defines project-specific assistant instructions. |
| `docs/workflow.md` | Defines stable work and review process. |

## RoleForge core files to add

| File | Reason |
|---|---|
| `ROLEFORGE_MANIFEST.md` | Defines the reusable role operating model. |
| `ROLE_INDEX.md` | Helps select the correct assistant role. |
| `role-rules/RF-RULE-001-role-boundaries.md` | Prevents wrong-role task completion. |
| `role-rules/RF-RULE-003-github-permissions.md` | Defines GitHub permission boundaries. |
| `response-templates/RF-TEMPLATE-007-role-redirect.md` | Gives a standard refusal and redirect pattern. |

## RoleForge role files to add

| File | Reason |
|---|---|
| `roles/RF-ROLE-004-product-owner.md` | ChatGPT will help write requirements and acceptance criteria. |
| `roles/RF-ROLE-006-system-architect.md` | ChatGPT will review architecture tradeoffs. |
| `roles/RF-ROLE-009-verifier-reviewer.md` | ChatGPT will review completed work against criteria. |

## Files not recommended as static source

| File or folder | Reason |
|---|---|
| `status/current-state.md` | Dynamic status should be checked live from GitHub. |
| `tasks/` | Active task files change frequently. |
| `vendor/` | Too large and not project-governance authority. |

## Risks and conditions

If `docs/workflow.md` is omitted, ChatGPT may not understand how the project expects reviews and handoffs to happen.

## Recommended validation tests

1. Ask ChatGPT to refuse a wrong-role GitHub request.
2. Ask ChatGPT to select the correct role for a requirement task.
3. Ask ChatGPT to distinguish project authority from RoleForge role behavior.

## Final verdict

Use a small RoleForge source pack plus three role files. Do not add the full RoleForge repository.

## Anti-patterns

1. Adding the whole RoleForge repo without need.
2. Replacing project governance with RoleForge.
3. Adding stale current-state files as permanent project source.
4. Adding role files for roles ChatGPT will not perform.
5. Ignoring target-project authority files.
6. Using archived or vendor files as authority.
7. Treating README links as enough when exact role behavior is required.
8. Mixing Product Owner, Architect, Developer, Verifier, and Auditor responsibilities.

## Acceptance checklist

- [ ] Target project authority files identified.
- [ ] Target project workflow files identified.
- [ ] Dynamic files excluded or marked as live-check only.
- [ ] RoleForge core pack selected.
- [ ] Only relevant RoleForge role files selected.
- [ ] Each recommended file has a reason.
- [ ] Project governance remains authoritative.
- [ ] RoleForge is used only for assistant role behavior.
- [ ] Follow-up validation tests are listed.
