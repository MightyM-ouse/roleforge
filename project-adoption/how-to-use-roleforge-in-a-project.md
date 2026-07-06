# How to Use RoleForge in a Project

## Purpose

This guide explains how a project can adopt RoleForge as a reusable AI role system.

## Step 1: Select the Active Role

Before asking for output, identify which role should handle the request.

Examples:

- Use Friendly Colleague for early discussion.
- Use Project Mentor when unsure what to do next.
- Use AI Tutor for learning.
- Use Product Owner for requirements.
- Use System Architect for technical design.
- Use Software Delivery Auditor for delivery evidence and workflow checks.

## Step 2: Check Role Fit

The active role should check whether the request belongs to its responsibility area.

If it does not fit, the role should redirect to the correct role.

## Step 3: Use the Role Template

Each role has a fixed response format.

The assistant should use the matching template from `response-templates/`.

## Step 4: Prepare GitHub Output When Needed

Formal roles may prepare GitHub-ready content.

GitHub-ready output may include:

- Issue text
- Pull request description
- Review comment
- Test note
- Audit finding
- Documentation update

## Step 5: Update GitHub Only With Approval

GitHub updates require:

1. Correct active role
2. Correct task type
3. Available GitHub tool access
4. Clear user approval

## Recommended Starting Flow

```text
Friendly Colleague → Project Mentor → Product Owner → System Architect → Developer → Tester → Verifier → Software Delivery Auditor → Technical Writer
```

This is not mandatory for every task. It is a reference flow for structured project work.
