# Task and session workflow

## Start or resume

1. Identify the task and current authorization from the user's request. Use the [task template](templates/task.md) for substantial implementation work.
2. When a task ID or checkpoint is supplied, read only its record under `handoffs/`. If several records could apply, list their names and resolve the intended task before using their state.
3. Check the actual workspace. With Git, inspect branch, HEAD, status and the task-relevant diff. Without Git, record that fact and inspect the named files.
4. Treat checkpoint evidence as historical. Reconcile changed files or revisions before relying on earlier test results.
5. Read the relevant architecture section and the minimum source needed for the next action. A checkpoint never grants additional write authority.

## Save a checkpoint

Use the [handoff template](templates/handoff.md). Save one current snapshot per task at `.agent/handoffs/<task-id>.md` when pausing, transferring work, or reaching a meaningful milestone that needs persistence. Include this path in the task's write scope.

Update the snapshot in place. Git can retain earlier versions once available. Keep durable design decisions in architecture documentation when authorized and link their section. Keep checkpoint content focused on the next action, actual evidence and unresolved decisions.

A target of roughly 500 words per checkpoint is a local guideline. Include additional evidence when required for safe continuation. Preserve failure details and incomplete work. If checkpoint writes are outside scope, provide the checkpoint text in the response.

## Context use

Use targeted search, section reads and scoped diffs. Preserve full logs in an authorized output location when needed, and return a concise result with a retrieval path. Re-read files after relevant edits or revision changes. Load templates when authoring their corresponding artifact.

Use the host's resume or compaction features where supported. The skill guides retrieval and checkpoint writing; the host controls context compaction. Save checkpoints at meaningful milestones because session termination can occur before an end-of-session save.

## Collaboration

Assign one writer to each task record. Use separate task IDs and branches or worktrees for independent work. Record shared contract dependencies before implementation. Resolve changes to package metadata, CLI registration and public data contracts through an integration owner assigned for the task.

## Handoff acceptance

Test a Codex-to-Claude transfer and a Claude-to-Codex transfer on a small authorized task. Give the receiving session only the task ID or checkpoint path and the normal project instructions. Confirm that it identifies scope, actual code state, validation gaps and the next step.

Measure initial files and output volume read, clarification turns and usage reported by the host where available. Record results before claiming token or quota savings.
