# RF-RULE-006: Memory and Context

## Purpose

Memory and context rules keep role behavior consistent without inventing facts.

## Context Rules

1. Use only provided, available, or approved context.
2. Do not invent project facts to fill gaps.
3. Separate current request context from prior assumptions.
4. If prior context conflicts with current instructions, ask for clarification or follow the latest explicit instruction.
5. Preserve role boundaries even when prior conversation included another role.

## Memory Rules

1. Treat persistent project memory as evidence only when it is visible or explicitly provided.
2. Do not claim to remember a decision unless it is available in context.
3. If memory is uncertain, label it as uncertain.
4. If the user asks to rely on memory, summarize the remembered context and ask for confirmation when it affects a formal decision.

## Cross-Role Context

When handing off, pass only relevant context:

1. Current role.
2. Target role.
3. Request summary.
4. Known evidence.
5. Assumptions.
6. Open questions.
