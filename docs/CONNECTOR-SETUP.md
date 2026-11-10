# CONNECTOR SETUP: GitHub in Ask AI

Ask AI uses this (also shipped as a project context file) when the GitHub connector is missing, cannot read the brain repository, or a commit fails. Give the user the matching steps and wait for their result.

## Connect GitHub

1. In Ask AI, open Customize > Connectors > Manage Connectors.
2. Search for GitHub and click Connect. Sign in to GitHub and approve access.
3. When GitHub asks which repositories to allow, choose "Only select repositories" and pick your brain repository (and DubLow-Digital/ai-brain-template if you will pull template updates through Ask AI). "All repositories" works but gives Ask AI more access than it needs.
4. Back in Ask AI, make sure the GitHub connector toggle is Enabled. It can also be toggled from the + menu in the chat composer.

The connector is tied to the user's own login, not the sub-account. Every person who uses the brain connects their own GitHub account, and that account needs access to the repository (owner or collaborator).

## Tools to enable

Open the GitHub connector in Connected apps and switch off "All tools" to choose individually. Enable the tools for:

- Reading: get file contents, list repository contents or tree, search code, list commits, get pull request.
- Writing: create or update file, push multiple files (if offered), create branch, create pull request.

Leave off anything that deletes repositories or branches, changes repository settings, manages collaborators or secrets, or merges pull requests (the user merges on GitHub). Tool names vary by connector version; match by what the tool does.

## Troubleshooting

| Symptom | Likely cause | Fix |
| --- | --- | --- |
| Repository not found | Repo not in the GitHub app's selected repositories, or wrong OWNER/REPO in project instructions | Add it in GitHub > Settings > Applications > the connector app > Repository access; check the spelling |
| Can read, cannot commit | Write tools switched off, or the account has read-only access | Enable the write tools; give the account write access |
| Commit to main rejected | Branch protection requires pull requests | Expected for protected repos: Ask AI commits to a brain/ branch and opens a pull request instead |
| "SHA does not match" or conflict | File changed since it was read | Ask AI rereads, merges and retries once |
| New file not found by search | Code search index lags | Read the file by path; INDEX.md is the primary map |
| Connector worked yesterday, fails today | Token revoked or account reconnected | Reconnect in Manage Connectors |

## Security reminders

- Keep the brain repository private.
- Turn on GitHub secret scanning and push protection for the repository if available.
- Revoke access any time from Customize > Connectors or from GitHub's application settings.
