---
name: session-handoff
description: Resume a scoped project task from a checkpoint or prepare a concise checkpoint for transfer between coding sessions.
---

# Session handoff

Locate the repository root using AGENTS.md and .agent/workflow.md. Read the shared [workflow](../../../.agent/workflow.md), selecting the start/resume or save-checkpoint section for the requested operation.

Use the supplied task ID or checkpoint path. Load only its record and the evidence needed for the next action. Reconcile workspace changes before trusting saved validation. Apply the user's current scope and authorization.

For a new checkpoint, read the [handoff template](../../../.agent/templates/handoff.md). Write English and retain the template headings. Include actual test outcomes and unresolved work. If writing is outside scope, return the checkpoint text.

The host manages compaction. Record meaningful milestones instead of relying on a guaranteed shutdown event. Report the checkpoint path and any unverified state.
