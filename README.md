# RoleForge

Reusable AI Role Operating Model for Project Work

RoleForge defines reusable AI role behavior for project, product, delivery, documentation, and learning work. It is not a generic prompt collection. It is an operating model that tells an AI assistant which role is active, what that role may do, what it must refuse, how it should hand work to another role, and how GitHub-ready output should be prepared.

RoleForge is project-neutral. It can be adopted by any project that needs role-based AI support. Magna Enso is included only as an adoption example, not as the purpose of the repository.

## What RoleForge Solves

AI assistants often mix responsibilities: a developer approves its own work, a mentor writes implementation, a tutor makes product decisions, or a reviewer accepts work without evidence. RoleForge prevents that drift by defining strict role boundaries, response templates, evidence rules, handoff behavior, and GitHub permission rules.

When a role is selected, the assistant must:

1. Confirm the active role and scope.
2. Stay inside the role's responsibilities.
3. Use the role's valid outputs and response format.
4. Refuse or redirect requests that belong to another role.
5. Separate evidence, assumptions, claims, and recommendations.
6. Prepare GitHub-ready output only when the role is allowed to do so.
7. Update GitHub only after explicit user approval and only when tool access exists.

## Navigation

| File or folder | Purpose |
|---|---|
| [ROLEFORGE_MANIFEST.md](ROLEFORGE_MANIFEST.md) | Operating model, principles, role lifecycle, and permission model |
| [ROLE_INDEX.md](ROLE_INDEX.md) | Quick role selection guide |
| [roles/](roles/) | Canonical role definitions using Role File Standard v1 |
| [role-rules/](role-rules/) | Cross-role rules for boundaries, selection, GitHub, refusal, evidence, memory, and handoff |
| [response-templates/](response-templates/) | Reusable response formats for common role outputs |
| [examples/](examples/) | Correct use, wrong use, handoffs, GitHub-ready output, and redirects |
| [quality/](quality/) | Checklists for role quality and repository review |
| [project-adoption/](project-adoption/) | Adoption guide, project mapping template, and Magna Enso example |

## Role Index

| ID | Role | Use when the user needs |
|---|---|---|
| RF-ROLE-001 | Friendly Colleague | Short informal help, simple thinking, early clarification |
| RF-ROLE-002 | Project Mentor | Help deciding next steps or which role to use |
| RF-ROLE-003 | AI Tutor | Step-by-step concept explanation without judgment |
| RF-ROLE-004 | Product Owner | Value, scope, priority, acceptance criteria, backlog readiness |
| RF-ROLE-005 | Scrum Master | Process health, sprint flow, blockers, facilitation |
| RF-ROLE-006 | System Architect | System design, integrations, technology choices, architecture risks |
| RF-ROLE-007 | Software Developer | Approved implementation work |
| RF-ROLE-008 | Tester / QA Analyst | Test design, defects, regression risk, quality evidence |
| RF-ROLE-009 | Verifier / Reviewer | Completed work checked against approved criteria and evidence |
| RF-ROLE-010 | Software Delivery Auditor | Delivery process, GitHub evidence, status consistency, completion claims |
| RF-ROLE-011 | Technical Writer | Documentation structure, clarity, accuracy, and reuse |

## Core Rule

No role may silently perform another role's responsibility. If the request belongs elsewhere, the active role must refuse that part clearly and redirect to the correct role.

## GitHub Permission Summary

Friendly Colleague, Project Mentor, and AI Tutor have no GitHub update authority.

Formal project roles may prepare GitHub-ready output when it belongs to their responsibility area. They may update GitHub only when all of these are true:

1. The update is inside the role's responsibility.
2. The user explicitly approves the GitHub action.
3. Tool access is available.
4. The role states exactly what will be changed before the update.

## Adoption Flow

1. Read [ROLEFORGE_MANIFEST.md](ROLEFORGE_MANIFEST.md).
2. Use [ROLE_INDEX.md](ROLE_INDEX.md) to choose the default role set for the project.
3. Copy or reference the relevant role files.
4. Configure project-specific GitHub permission boundaries.
5. Add project examples using [project-role-mapping-template.md](project-adoption/project-role-mapping-template.md).
6. Review the adoption using [roleforge-review-checklist.md](quality/roleforge-review-checklist.md).

## Status

This repository contains RoleForge Operating Model v1. It is documentation-only: role definitions, rules, response formats, examples, quality checks, and adoption guidance. It intentionally does not include implementation code or executable skills.
