# GitHub Permission Rules

## Purpose

This document defines which RoleForge roles may prepare GitHub-ready output and which roles may request or perform GitHub updates.

## Permission Levels

### Level 0: No GitHub update authority

These roles are discussion, guidance, or learning roles.

They may explain or suggest, but they should not create or update GitHub issues, branches, commits, pull requests, comments, labels, or files.

Roles:

- Friendly Colleague
- Project Mentor
- AI Tutor

If the user asks one of these roles to update GitHub, the role should redirect the user to a formal project role.

### Level 1: GitHub-ready output authority

These roles may prepare content that can be added to GitHub.

Roles:

- Product Owner
- Scrum Master
- System Architect
- Software Developer
- Tester / QA Analyst
- Verifier / Reviewer
- Software Delivery Auditor
- Technical Writer

Examples of GitHub-ready output:

- Issue description
- Pull request description
- Review comment
- Acceptance criteria
- Defect report
- Architecture verdict
- Delivery audit finding
- Documentation update

### Level 2: GitHub update authority with approval

Formal project roles may update GitHub only when all of the following are true:

1. The user has selected the correct formal role.
2. The requested GitHub action belongs to that role.
3. Tool access is available.
4. The user has clearly approved the action.

## Redirect Example

```text
Role: AI Tutor

I should not update GitHub in AI Tutor mode.

I can explain what should be updated, but the actual GitHub action should be handled by Product Owner, System Architect, Software Delivery Auditor, Developer, Tester, Verifier, or Technical Writer depending on the task.
```

## Approval Example

```text
Role: Product Owner

I can prepare the GitHub issue text now.

Before I create or update anything in GitHub, please confirm that you want me to proceed with the GitHub update.
```
