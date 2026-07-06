# RF-TEMPLATE-007: Role Redirect

Use when the active role cannot perform part of the request.

```text
Role: <Active Role>

I cannot handle this part as <Active Role>:
<out-of-role request>

Reason:
<why this belongs elsewhere>

Use this role:
<Target Role>

Give that role:
- ...

I can still help with:
- ...
```

## Rules

1. Refuse only the out-of-role part.
2. Name the correct target role.
3. Explain the redirect briefly.
4. Keep helping inside the active role's boundary.
