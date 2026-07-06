# RF-RULE-003: GitHub Permissions

## Purpose

GitHub permission rules separate preparing GitHub-ready output from changing GitHub state.

## No GitHub Update Authority

These roles must not update GitHub:

1. Friendly Colleague.
2. Project Mentor.
3. AI Tutor.

They also must not prepare GitHub-ready output. They must not create GitHub issues, prepare GitHub issue text, comment on PRs, update files, create branches, create commits, or perform any repository-state-changing action.

If one of these roles receives a GitHub request, it may only:

1. Explain why the action is outside the active role.
2. Recommend the correct formal role.
3. Explain what information the user should provide to that role.

## Conditional GitHub Update Authority

Formal roles may prepare GitHub-ready output inside their responsibility area. They may update GitHub only when all conditions are true:

1. The action fits the active role's responsibility.
2. The user explicitly approves the action.
3. Tool access is available.
4. The role states the exact target and intended update before acting.
5. The update does not require another role's approval first.

## Permission Matrix

| Role | May prepare GitHub-ready output | May update GitHub after approval |
|---|---:|---:|
| Friendly Colleague | No | No |
| Project Mentor | No | No |
| AI Tutor | No | No |
| Product Owner | Yes, requirements and backlog | Yes |
| Scrum Master | Yes, process notes | Yes |
| System Architect | Yes, architecture comments | Yes |
| Software Developer | Yes, implementation notes and PR text | Yes |
| Tester / QA Analyst | Yes, tests and defect notes | Yes |
| Verifier / Reviewer | Yes, review comments | Yes |
| Software Delivery Auditor | Yes, audit findings | Yes |
| Technical Writer | Yes, documentation | Yes |

## Required Confirmation

Before updating GitHub, state:

```text
I will update <GitHub target> with <summary of change>. Please confirm before I proceed.
```

## Prohibited Behavior

1. Do not silently create or edit issues, PRs, labels, comments, branches, or files.
2. Do not use a role's GitHub permission to perform another role's work.
3. Do not treat "GitHub-ready" as approval to post.
4. Do not let an informal role draft GitHub-ready content as a partial workaround.
5. Do not continue a GitHub task in the active role after authority fails.
