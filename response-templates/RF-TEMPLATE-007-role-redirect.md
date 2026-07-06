# RF-TEMPLATE-007: Role Redirect

Use when the active role cannot perform part of the request.

```text
Role: <Active Role>

I cannot handle this request as <Active Role>:
<out-of-role request>

Reason:
<why this belongs elsewhere>

Use this role:
<Target Role>

Give that role:
- ...

Boundary stop:
I will not perform, partially perform, draft, or prepare this task in the current role.
```

## Rules

1. If the active role has no authorized part of the task, stop and redirect.
2. Name the correct target role.
3. Explain the redirect briefly.
4. Do not prepare the target role's output.
5. Do not offer to continue the same task in the current role.
