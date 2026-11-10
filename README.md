# AI Brain (GitHub Edition for Lead Alchemist Ask AI)

DubLow Digital | Version 2.0.0 | November 10, 2026
Adapted from the AI Employee Course starter (ContentCreator.com, v1.0).

This repository is a template for an AI employee's brain. Copy it into your own GitHub account, connect it to Lead Alchemist's Ask AI, and manage it in GitHub. Ask AI reads it for context, rules and procedures and commits updates back. You can edit it on GitHub yourself at any time. The commit history is the version archive.

## Get your own copy

Pick one:

- **Use this template (easiest):** click "Use this template" > "Create a new repository" at the top of this page. Choose your account, name it (for example `ai-brain-yourname`), select **Private**, and create it.
- **Clone and push:**
  ```
  git clone https://github.com/DubLow-Digital/ai-brain-template.git ai-brain-yourname
  cd ai-brain-yourname
  git remote rename origin template
  gh repo create YOUR-ACCOUNT/ai-brain-yourname --private --source . --push
  ```

Keep your copy private.

## Connect it to Ask AI

1. Connect GitHub in Ask AI and give it access to your new repository: [docs/CONNECTOR-SETUP.md](docs/CONNECTOR-SETUP.md).
2. Create an Ask AI project. Paste [docs/PROJECT-INSTRUCTIONS.md](docs/PROJECT-INSTRUCTIONS.md) into its instructions, replacing OWNER/REPO with your repository. Upload docs/CONNECTOR-SETUP.md as a project file.
3. Start a chat in the project and say: "Set up my brain." Ask AI tests read and write access, records the install, and runs a short personalization interview.

## How it is organized

| Path | What it holds | Who owns it |
| --- | --- | --- |
| AGENTS.md | Working rules, including how Ask AI reads and commits | Template (managed) |
| INDEX.md | One line per file: what it holds and when to read it | You (Ask AI maintains it) |
| brain.json | Version, template source, managed vs owner files | Template, plus your install fields |
| Context/ | Facts, goals and preferences about you and your work | You |
| Employees/ | Personalized AI employee profiles | You (README and template are managed) |
| Skills/ | Procedures Ask AI follows (setup, maintenance, handoff, update) | Template; you can add your own |
| Projects/ | Briefs, handoffs and working files for specific work | You (template folder is managed) |
| docs/ | Ask AI project instructions and connector setup | Template (managed) |
| CHANGELOG.md | Template release notes | Template (managed) |

## Making additions and updates in GitHub

You can work two ways, and they mix freely:

- **Through Ask AI:** "Save that preference to my brain," "Create an employee profile from this setup file," "Save the handoff for this project." Ask AI commits the change and tells you what it changed.
- **Directly on GitHub:** edit any file in the browser (pencil icon) or locally, then commit. If you add, rename or remove a file, update its line in INDEX.md so Ask AI can find it.

Conventions: Markdown files, names with letters, numbers and hyphens, one file per subject. New skills go in `Skills/<skill-name>/SKILL.md`. New projects go in `Projects/<Project-Name>/` with a BRIEF.md and HANDOFF.md copied from `_Project-Template`. Files starting with an underscore are templates. If you deliberately customize a managed file, add its path to the `customized` list in brain.json so template updates ask before replacing it.

## Getting template updates

- **Through Ask AI:** say "Check my brain for an update." Ask AI follows Skills/brain-update/SKILL.md and opens a pull request that changes only managed files. You review and merge it.
- **By hand:** if you cloned with the `template` remote, run `git fetch template`, then `git checkout template/main -- <managed paths from brain.json>`, review, commit and push. Do not merge the template wholesale; it would reset your Context and other owner files.

## Staying in control

Every Ask AI change is a commit you can review, compare and revert. Larger changes (deletions, reorganizations, rule changes, template updates) arrive as pull requests. Never store passwords, API keys, login codes, payment details or regulated client data (such as health information) in the brain, even in a private repository: git history keeps deleted content.
