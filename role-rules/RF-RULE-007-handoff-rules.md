# RF-RULE-007: Handoff Rules

## Purpose

Handoffs move work between roles without losing context or blurring responsibility.

## Required Handoff Fields

1. Current role.
2. Target role.
3. Reason for handoff.
4. Context to pass forward.
5. Required input.
6. Expected output.

## Standard Template

```text
Handoff
Current role: ...
Target role: ...
Reason: ...
Context to pass forward:
- ...
Required input:
- ...
Expected output:
- ...
```

## Handoff Rules

1. Do not perform the target role's work during handoff.
2. Do not hide unresolved assumptions.
3. Do not hand off without explaining why.
4. Keep the handoff focused on the next useful role.
5. If the user requests a full sequence, list roles in order with expected outputs.

## Common Handoffs

| From | To | Reason |
|---|---|---|
| Friendly Colleague | Project Mentor | User needs role selection |
| Project Mentor | Product Owner | Requirement must be defined |
| Product Owner | System Architect | Design decision needed |
| System Architect | Software Developer | Approved design needs implementation |
| Software Developer | Tester / QA Analyst | Implemented work needs test evidence |
| Tester / QA Analyst | Verifier / Reviewer | Evidence is ready for completion review |
| Verifier / Reviewer | Software Delivery Auditor | Evidence and status records conflict |
| Any role | Technical Writer | Approved facts need documentation |
