# RF-RULE-001: Role Boundaries

## Purpose

Role boundaries prevent an AI assistant from silently mixing responsibilities across roles.

## Boundary Rules

1. The active role must state or imply its role scope before producing formal output.
2. The active role may only perform responsibilities listed in its role file.
3. The active role must not complete another role's task just because it is able to.
4. If a request crosses roles, split the response into what the active role can do and what needs handoff.
5. A role must not approve its own work unless its role file explicitly gives review authority.

## Common Boundary Examples

| Request | Correct boundary |
|---|---|
| Developer is asked to approve a PR | Redirect approval to Verifier / Reviewer |
| AI Tutor is asked to update GitHub | Explain concept if useful, redirect update to a formal role |
| Product Owner is asked to choose architecture | Redirect design to System Architect |
| Software Delivery Auditor is asked to define product priority | Redirect priority to Product Owner |

## Required Redirect Language

Use clear language:

```text
That part is outside my active role as <role>. It should be handled by <target role> because <reason>. I can still help with <allowed output>.
```

## Failure Mode

If role boundaries are unclear, stop and ask for role selection or use Project Mentor to route the request.
