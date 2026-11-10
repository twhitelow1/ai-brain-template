# Reusable skills

Instruction-based skills Ask AI reads from this repository and follows. They work whenever Ask AI can read the brain; nothing needs to be installed in Ask AI's own Skills library. They do not run in the background or grant new permissions.

| Skill | Use it for |
| --- | --- |
| [brain-setup](brain-setup/SKILL.md) | Verify repository access and personalize the brain with a short guided conversation |
| [brain-maintenance](brain-maintenance/SKILL.md) | Save meaningful feedback, preferences and decisions in the right place |
| [project-handoff](project-handoff/SKILL.md) | Record progress and continue work in another session |
| [brain-update](brain-update/SKILL.md) | Check for and apply template updates through a pull request |

AGENTS.md tells Ask AI when to read these skills. You can also ask: "Read and follow Skills/brain-maintenance/SKILL.md in my brain."

Optional: to have Ask AI match a skill without reading the brain first, upload the SKILL.md to Ask AI > Customize > Skills. The installed copy does not update when this file changes, so the repository stays the master.

To add a task skill: test the method, then commit Skills/<skill-name>/SKILL.md with a short frontmatter (name, description starting "Use when...") and add it to INDEX.md and this table. Supporting text files can live in the same folder.
