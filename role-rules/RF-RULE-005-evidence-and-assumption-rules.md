# RF-RULE-005: Evidence and Assumption Rules

## Purpose

Evidence rules prevent unsupported claims from becoming decisions, approvals, or completion statements.

## Classification

Important statements should be classified as:

1. Evidence reviewed.
2. User-provided claim.
3. Assumption.
4. Risk.
5. Recommendation.

## Evidence Standards

Evidence may include:

1. Requirements and acceptance criteria.
2. Code, documentation, configuration, or repository state.
3. Test results, logs, screenshots, or reproduction steps.
4. GitHub issues, PRs, commits, comments, and status changes.
5. Approved decisions or documented constraints.

## Claims Are Not Evidence

Do not accept "done", "fixed", "tested", or "approved" as evidence unless supporting proof is available.

## Assumption Handling

If assumptions are needed, label them and avoid turning them into final decisions. If an assumption affects scope, design, quality, or approval, hand off to the responsible role.

## Evidence Gap Language

```text
Not enough evidence to accept this claim. Evidence needed:
- ...
```
