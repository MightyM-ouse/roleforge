# RoleForge

**Reusable AI Role System for Project Work**

RoleForge defines how an AI assistant should behave when acting as a specific project role. It is intended for project work where the user may need support from different role perspectives such as Friendly Colleague, Project Mentor, AI Tutor, Product Owner, System Architect, Developer, Tester, Reviewer, Auditor, and Technical Writer.

RoleForge is not a generic prompt collection. It is a role-based operating model for AI-assisted project work.

## Purpose

RoleForge exists to make AI role behavior clear, strict, reusable, and reviewable.

When a role is selected, the assistant should:

1. Understand which role is active.
2. Stay within that role's responsibilities.
3. Use the response format defined for that role.
4. Redirect the request if it belongs to another role.
5. Avoid silently mixing responsibilities from another role.
6. Respect GitHub and context rules.
7. Produce clear, professional, reusable output.

## Role Index

| ID | Role | Primary Purpose |
|---|---|---|
| RF-ROLE-001 | Friendly Colleague | Informal discussion, simple clarification, early thinking |
| RF-ROLE-002 | Project Mentor | Guidance on what to do next and which role to use |
| RF-ROLE-003 | AI Tutor | Step-by-step learning and explanation |
| RF-ROLE-004 | Product Owner | Requirement value, scope, priority, acceptance readiness |
| RF-ROLE-005 | Scrum Master | Process health, sprint flow, blockers, team working model |
| RF-ROLE-006 | System Architect | System design, structure, integrations, technical risk |
| RF-ROLE-007 | Software Developer | Implementation of approved work |
| RF-ROLE-008 | Tester / QA Analyst | Test design, validation, defects, quality risk |
| RF-ROLE-009 | Verifier / Reviewer | Check completed work against approved requirement |
| RF-ROLE-010 | Software Delivery Auditor | Delivery process, GitHub evidence, workflow correctness |
| RF-ROLE-011 | Technical Writer | Documentation clarity, structure, and publishable content |

## Repository Structure

```text
roleforge/
├── README.md
├── roles/
├── role-rules/
├── response-templates/
├── examples/
└── project-adoption/
```

## Current Status

This repository contains the initial RoleForge baseline. It is intended to be reviewed, refined, and reused across projects.
