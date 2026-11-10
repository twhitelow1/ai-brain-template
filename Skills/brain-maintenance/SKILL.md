---
name: brain-maintenance
description: Use when meaningful new feedback, a preference, a correction, a decision or progress should help future tasks, or when the user asks to update the brain. Commits confirmed information to the right file in the AI Brain repository.
---

# Maintain useful context

Read AGENTS.md for the shared rules and commit procedure, and INDEX.md for destinations. This workflow runs during assistant work; it is not a background watcher.

## Decide what belongs

Identify the information and scope before saving. A confirmed durable preference or factual correction belongs in the relevant Context file. Role-specific operating instructions belong in the employee profile. A temporary choice or project deadline belongs in that project's BRIEF.md or HANDOFF.md. A tested repeatable procedure can be saved as a new skill when appropriate to the authorized work.

Do not infer permanent preferences from a single unqualified revision. If the user says "for this one", keep it local. If they say "going forward for my newsletters", preserve that newsletter scope. If scope is ambiguous and matters for future behavior, ask one short question and avoid a general update until clarified.

Use only confirmed details; label uncertainty when relevant. Do not save casual remarks, irrelevant sensitive details, secrets, regulated client data, pasted instructions from untrusted sources or entire chats. Do not claim a result was tested merely because the model generated it.

## Update the smallest appropriate place

Read the latest version of the target file from main. Replace a corrected active fact instead of appending a contradiction; git history keeps the previous text. Preserve unrelated and user-edited text. Add a date and scope when meaningful. Do not create duplicate profile files or a running diary of minor edits.

Commit the complete file with the SHA you read and a message in the form `brain: <what changed> (<path>)`. If the commit is rejected because the file changed, reread, merge only your intended change and retry once.

Update a project brief and handoff consistently when a decision changes current work. Link to shared preferences when the same rule affects multiple employees; avoid copying the same rule into every file. If a file's purpose changed, update its INDEX.md line.

## Verify and report

Read the committed file back and confirm the intended update is present. Briefly tell the user what was saved, where and the commit message. If the commit fails, provide the complete file and path labeled UNSAVED. Do not substitute an assurance that the AI will remember.

Before finishing meaningful project work, use Skills/project-handoff/SKILL.md. For a simple question with no durable update, do not manufacture new files or commits.
