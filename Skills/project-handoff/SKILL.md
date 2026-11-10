---
name: project-handoff
description: Use at meaningful project milestones, before ending ongoing work, or when continuing an existing project. Commits progress to the project's HANDOFF.md in the AI Brain repository and resumes from those files.
---

# Save or resume a project

Read AGENTS.md, INDEX.md and the relevant project's BRIEF.md and HANDOFF.md. Resolve ambiguous project identity before modifying files. Projects/_Project-Template is empty scaffolding, never an actual project to resume.

## Save a milestone

Update the existing HANDOFF.md with:

- Actual update date and current status.
- Completed work and real output locations (repository path, or where it lives in Lead Alchemist or another connected app).
- Confirmed decisions and task-specific feedback.
- Pending work, unresolved questions, blockers and next step.
- What was reviewed, tested, committed or delivered and what remains unverified.

Preserve user edits and useful prior decisions. Keep the current summary short and accurate; git history holds older states. Distinguish planned, drafted, reviewed, approved, tested and delivered work. A draft is not an approval or publication. Link to context and source files instead of repeating them in full. Do not invent locations, test outcomes or timestamps.

Commit with a message like `brain: handoff for <project> (Projects/<Project-Name>/HANDOFF.md)`. If a significant decision changes requirements, update BRIEF.md in the same commit when possible. Verify the commit and tell the user where the handoff lives.

## Resume safely

Read the handoff and inspect relevant current files before saying where the project stands. You can check recent commits on the project folder to see what changed since the handoff. Check that external sources and connectors are available in this session. A handoff's recorded access does not establish current access.

Summarize the current state and identify the next step. Continue the user's requested work when authorized. If the user only asks for status, give status instead of running all pending tasks. Missing data, approval checkpoints or changed requirements may require a focused question.

When another person picks up the work, they need their own Ask AI GitHub connector with access to this repository and the Ask AI project instructions. Chat history, connector settings and schedules do not move with the repository.
