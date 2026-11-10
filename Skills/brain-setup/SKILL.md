---
name: brain-setup
description: Use for first-time setup of the AI Brain repository or when the user asks to reconfigure it. Verifies read and write access through the GitHub connector and personalizes the brain through a short guided interview. Not for ordinary tasks.
---

# Set up this AI Brain

Read AGENTS.md and INDEX.md. Follow the owner's permissions. Apply the commit procedure in AGENTS.md rather than duplicating it here. If the repository is still the template itself (DubLow-Digital/ai-brain-template), stop and point the user to "Get your own copy" in README.md; personal context never goes in the template.

## Check access first

Confirm the GitHub connector is enabled in this chat and which repository and branch you are using. Read brain.json and report its version.

If installed_on is empty, record the install: set installed_from_version to the current version and installed_on to today's date (YYYY-MM-DD), and commit with `brain: record install (brain.json)`.

If the user requested a write test, commit a file named access-test.md at the root containing a neutral test line and today's date, with the message `brain: access test (access-test.md)`. Read it back and report the actual outcome, including the commit link if available. Keep the test file until the user chooses to remove it. Do not claim write access based on reading alone.

If writing fails, report the error. The usual causes are covered in docs/CONNECTOR-SETUP.md (also a project file) (connector tool toggles, repository access granted to the GitHub app, branch protection). Continue useful conversation if the user wants, labeling unsaved output.

## Ask only what is useful

Read the existing Context files before asking questions. Do not restart a completed interview. Ask up to three related questions at a time, then wait. Begin with:

1. What would you like the AI to call you?
2. Is this brain for personal tasks, work, or both? What is the first task you want help with?
3. What would make that first task useful, and are there any preferences you already want it to follow?

Skip answers already known from confirmed context. Ask more only as required by the first task. Do not request a full life history, financial details, logins or all future employee plans. For work, ask role and audience only when relevant. For scheduling, clarify timezone. Do not pressure the user to fill unused files.

## Save while you learn

Summarize the useful answers briefly and commit confirmed details to Context/About-Me.md, Context/Work.md or Context/Preferences.md. Use scoped updates with dates. Update the matching INDEX.md lines so they describe what the files now hold (for example "Owner's name and business..." instead of "Starter fields only"). Report the actual changed files and commit messages.

Ask whether the user is ready to start the first useful task or wants to add anything essential. If they supplied an employee setup file, follow its process and commit the result to Employees following AGENTS.md. If they are starting a substantial project, create Projects/<Project-Name>/ from _Project-Template and replace placeholders with confirmed facts, leaving unknowns explicit.

## Demonstrate continuity when wanted

Ask the user for one real lasting preference. Commit it, show the changed section, and give this prompt for a fresh chat in the same Ask AI project:

"Read my brain. Tell me my saved preference for [topic] and apply it to [small task]."

Do not label the fresh-chat test passed until it actually happens. Setup is complete enough to begin work once access is verified and the first useful context is committed; extra fields can stay blank. Distinguish repository setup, employee configuration, tool connections and schedules.
