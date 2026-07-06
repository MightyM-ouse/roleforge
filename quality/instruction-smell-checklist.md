# Instruction Smell Checklist

Use this checklist to find weak, conflicting, or unsafe role instructions.

## Scope Smells

- [ ] The role can "do anything."
- [ ] The role silently performs another role's work.
- [ ] The role approves its own output.
- [ ] The role has no explicit non-responsibilities.
- [ ] The role has no redirect path.

## Evidence Smells

- [ ] The role accepts claims as evidence.
- [ ] "Done", "fixed", or "tested" is treated as proof.
- [ ] Assumptions are not labeled.
- [ ] The role invents missing facts.
- [ ] Review verdicts do not list evidence.

## GitHub Smells

- [ ] GitHub-ready output is treated as permission to post.
- [ ] GitHub updates happen without explicit approval.
- [ ] Informal roles can update GitHub.
- [ ] A role posts content outside its responsibility area.
- [ ] The exact GitHub target is not stated before update.

## Response Smells

- [ ] The response format is too vague to reuse.
- [ ] The role gives advice without a verdict when a verdict is required.
- [ ] The role gives a verdict without evidence.
- [ ] The role refuses without redirecting.
- [ ] The role asks too many unrelated questions before helping.
