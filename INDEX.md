# Brain index

One line per file: path, what it holds, when to read it. Ask AI reads this first and keeps it current. Files beginning with an underscore are templates.

## Core
- AGENTS.md — Working rules: retrieval, commit procedure, routing, safety. Read at the start of brain work.
- README.md — Human overview of the repository and useful requests.
- brain.json — Version, template source, managed vs owner files. Read for updates or installs.
- CHANGELOG.md — Template release notes. Read when checking for updates.

## Docs
- docs/PROJECT-INSTRUCTIONS.md — Text to paste into the Ask AI project instructions. Read when setting up or after updates.
- docs/CONNECTOR-SETUP.md — GitHub connector setup, tool permissions, troubleshooting. Read when access fails.

## Context
- Context/About-Me.md — Owner's name, relevant background, personal goals, constraints. Starter fields only.
- Context/Work.md — Owner's role or business, audience, services, work goals, brand references. Starter fields only.
- Context/Preferences.md — Lasting communication and delivery preferences with scope. Starter fields only.

## Employees
- Employees/README.md — How employee profiles are created; list of configured employees (none yet).
- Employees/_Employee-Profile-Template.md — Template for a new employee profile. Not an active employee.

## Skills
- Skills/README.md — List of brain skills and how to add one.
- Skills/brain-setup/SKILL.md — First-time setup: verify repository access, personalization interview.
- Skills/brain-maintenance/SKILL.md — Saving feedback, preferences and decisions to the right file.
- Skills/project-handoff/SKILL.md — Saving project milestones and resuming projects.
- Skills/brain-update/SKILL.md — Checking for and applying template updates via pull request.

## Projects
- Projects/README.md — How projects are created; list of active projects (none yet).
- Projects/_Project-Template/BRIEF.md — Template project brief. Not an active project.
- Projects/_Project-Template/HANDOFF.md — Template project handoff. Not an active project.
