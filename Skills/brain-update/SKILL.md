---
name: brain-update
description: Use when the user asks to update the brain, check for a template update, or when the template's brain.json version is newer than this repository's. Updates managed files from the template through a pull request, never touching owner files.
---

# Update this brain from the template

Updates change managed system files only (the managed_paths list in brain.json). Owner files (Context, real employees, real projects, owner entries in INDEX.md) are never overwritten.

## 1. Check versions

1. Read brain.json in this repository and in the template repository named in template_repo (default DubLow-Digital/ai-brain-template).
2. Compare versions. If they match, tell the user the brain is current and stop. If the template cannot be read, say so; the user may need read access to it (see docs/CONNECTOR-SETUP.md).
3. Read the template's CHANGELOG.md and summarize the releases between the two versions in plain language.

## 2. Build the change list

For each path in the template's managed_paths:

- Missing here: plan to add it.
- Different from the template: plan to replace it, unless the path is in this repository's brain.json "customized" list. For a customized file, show what the template changed and ask whether to replace it, merge the template's changes into the owner's version, or keep the owner's version.
- Same: no change.

New template files that are not managed (for example an optional example skill) are offered, not added without a yes. If the template dropped a managed path this repository still has, do not delete the file; tell the user and let them decide.

## 3. Show the plan

Tell the user the version jump, the release summary, and the files to add, replace or review. Ask for approval before committing.

## 4. Apply as a pull request

1. Create a branch named `brain/update-<new-version>` from main.
2. Commit the approved changes on that branch. Copy managed files from the template exactly, except for merges the user approved.
3. Update brain.json on the branch: take version, released, managed_paths and template_repo from the template; keep installed_from_version, installed_on and the customized list; set updated_on to today's date (YYYY-MM-DD).
4. Add entries for any new managed file to INDEX.md on the branch, keeping every existing owner entry.
5. Open a pull request titled `AI Brain update <old> → <new>` with the release summary and file list in the description.
6. Give the user the pull request link. Merge only when the user says to, or let them merge on GitHub.

## 5. After the merge

Read AGENTS.md and INDEX.md again from main, since the rules may have changed. If the CHANGELOG says the Ask AI project instructions changed, tell the user to replace them from the template's docs folder, keeping their own Repository line. Ask AI cannot edit its own project instructions.

## Rules

- Never update directly on main.
- Never overwrite owner files to match the template.
- If any step fails, stop, report what was committed on the branch, and leave main untouched.

## Doing it by hand instead

Owners comfortable with git can pull template updates themselves; see the "Getting template updates" section of README.md.
