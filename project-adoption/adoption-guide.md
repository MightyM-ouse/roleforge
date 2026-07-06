# RoleForge Adoption Guide

Use this guide to adopt RoleForge in a project without making RoleForge project-specific.

## Adoption Steps

1. Read the [RoleForge Manifest](../ROLEFORGE_MANIFEST.md).
2. Choose the roles the project needs from the [Role Index](../ROLE_INDEX.md).
3. Compare the target project with RoleForge using the [Project Source Comparison Guide](project-source-comparison-guide.md).
4. Copy or reference only the relevant role files.
5. Define project-specific examples, not new role responsibilities.
6. Set GitHub permission expectations for the project.
7. Add role handoff examples for common workflows.
8. Review the adoption with the [RoleForge Review Checklist](../quality/roleforge-review-checklist.md).

## What May Be Customized

1. Project examples.
2. Local terminology.
3. Repository links or issue templates.
4. Workflow names.
5. Domain-specific acceptance criteria examples.

## What Must Not Be Weakened

1. Role boundaries.
2. Refusal and redirect behavior.
3. Evidence and assumption rules.
4. GitHub approval requirements.
5. Handoff rules.
6. The separation between GitHub-ready output and GitHub updates.

## Recommended Project Setup

```text
project/
├── roleforge/
│   ├── selected-roles.md
│   ├── project-role-map.md
│   ├── github-permissions.md
│   └── examples/
```

## Adoption Review Questions

1. Which role is the default when the user does not specify one?
2. Which roles may prepare GitHub-ready output?
3. Who can approve GitHub updates?
4. How are handoffs recorded?
5. What counts as evidence for completion?
6. What role handles unclear requirements?
7. What role handles architecture risks?
8. What role checks completion claims?
