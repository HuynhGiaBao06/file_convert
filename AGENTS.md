# Project instructions

## Scope and language

Write project documentation, checkpoints and skills in English. Respond to the user in their preferred language.

Determine task, work mode, read scope, write scope, target, objective, constraints and validation before substantial work. Supported modes are READ_ONLY, REVIEW, PLAN_ONLY, AUTO_IMPLEMENT and VERIFY_ONLY. Missing work mode defaults to READ_ONLY. Apply the user's explicit task authorization and declared write scope. Findings alone do not authorize changes.

The user creates and connects the Git repository. Git initialization, commits, remote changes and pushes require task-specific authorization.

## Context loading

Read this file at session start. Read only the architecture sections and source files relevant to the current task. Use the session-handoff skill when resuming from a checkpoint or preparing a handoff. Read the selected task record rather than the whole handoff directory.

The architecture source is [docs/architecture.md](docs/architecture.md). The shared handoff procedure is [.agent/workflow.md](.agent/workflow.md). Skills are entry points to that procedure.

## Implementation boundaries

Keep extract and compose independent. External SDKs belong in adapters. Application services accept typed options and injected dependencies. Keep Document and PagePlan separate. Add shared code only for demonstrated shared requirements.

Make changes within the current write scope. Preserve unrelated edits. Review shared contract changes before dependent work proceeds. Use scoped branches or worktrees once the user has established Git.

## Evidence and completion

Record actual commands and outcomes. Distinguish implemented, planned, failed and unverified work. Check changed files, relevant tests, documentation consistency and scope before claiming completion. Never mark a task complete solely because code or output files exist.

For substantial tasks, report Task, Work Mode, Files Read, Files Modified, Work Performed, Validation Performed, Review Findings, Hallucination / Overclaim Check, Scope Check, Unverified Items and Final Status. Use PASS, ISSUES FOUND or INCOMPLETE for the overclaim check, and PASS or SCOPE DEVIATION DETECTED for scope. Final Status is COMPLETE, PARTIAL, BLOCKED or REVIEW ONLY.
