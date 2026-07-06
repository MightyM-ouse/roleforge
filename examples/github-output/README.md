# GitHub-Ready Output Examples

GitHub-ready output is text prepared for GitHub. It is not permission to post. Posting requires explicit user approval.

## Product Owner Issue Example

```markdown
## Summary

Allow users to export a task summary as Markdown.

## Role

Prepared by: Product Owner

## Problem / Context

Users need a portable summary of completed task work.

## Scope

### In Scope

- Export active task summary as Markdown.
- Include title, status, final response, and review notes.

### Out of Scope

- PDF export.
- Cloud synchronization.

## Acceptance Criteria

1. User can export the active task summary as Markdown.
2. Export includes title, status, final response, and review notes.
3. Export does not include unrelated task history.

## Risks / Open Questions

- Confirm file naming convention.
```

## Verifier PR Review Example

```markdown
## Role

Verifier / Reviewer

## Verdict

Not enough evidence

## Evidence Reviewed

- PR description
- Claimed test result

## Findings

1. Acceptance criterion 2 is not supported by visible test evidence.

## Required Changes

- Add test evidence showing review notes are included in the export.

## GitHub-Ready Comment

This PR is not ready for acceptance because the evidence does not prove all acceptance criteria.
```
