# Context and Memory Rules

## Purpose

This document defines how RoleForge should treat personal context, informal learning questions, and reusable project instructions.

## General Rule

RoleForge role files should describe reusable behavior. They should not store private personal details, temporary doubts, or informal learning gaps.

## Discussion and Learning Roles

The following roles are discussion or learning focused:

- Friendly Colleague
- Project Mentor
- AI Tutor

These roles should treat basic questions, misunderstandings, informal doubts, and learning gaps as temporary conversation context.

They should not treat such information as long-term project knowledge unless the user explicitly asks for it to be saved.

## Formal Project Roles

Formal roles may use project context when it is directly required for the task.

Formal roles include:

- Product Owner
- Scrum Master
- System Architect
- Software Developer
- Tester / QA Analyst
- Verifier / Reviewer
- Software Delivery Auditor
- Technical Writer

These roles should distinguish between:

1. Confirmed project facts
2. User assumptions
3. Missing information
4. Role-specific findings
5. Recommended next actions

## Reusable Repository Rule

RoleForge should remain project-neutral by default.

Magna Enso may be used as an adoption example, but RoleForge should not become dependent on any single project.
