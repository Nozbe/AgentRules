# AgentRules

This repository holds the rules for how AI works with Nozbe, in English and Polish.

## Files

- `rules.md`: the rules in English. **This is the source of truth.**
- `rules.pl.md`: the Polish translation, generated from `rules.md`.
- `setup.md`: a prompt that connects a repository to Nozbe and writes the team, director, agent and project to its CLAUDE.md. **The English version is the source of truth.**
- `setup.pl.md`: the Polish translation, generated from `setup.md`.
- `README.md`: a short description of the repository for GitHub.
- `LICENSE`: the repository's license.
- `AGENTS.md`: this file, with working agreements for this repository. `CLAUDE.md` only imports it, so Claude Code loads it too.
- Everything stays in the repository root, with no folders.

## Working agreements

- **English first.** Make every change in the English file (`rules.md`, `setup.md`) first. Then update its Polish file (`rules.pl.md`, `setup.pl.md`) to match. Never change only the Polish file.
- **Translate using the glossary.** When updating a Polish file (`rules.pl.md`, `setup.pl.md`), use the glossary at the end of `rules.md` for Nozbe terms. Section and project names stay as they are unless the glossary gives a translation (for example "To be reviewed" → „Do sprawdzenia”).
- **Keep both files in step.** Each English file and its Polish file (`rules.md` and `rules.pl.md`, `setup.md` and `setup.pl.md`) always have the same sections, rules and numbering.
- **General rules only.** `rules.md` holds rules that apply everywhere. Team, project and user names and IDs belong in each repository's own CLAUDE.md, not in the rules.
- **Mark your own additions.** When a change includes something I didn't ask for, say so, so I can remove it.

## Keeping files current

- **New agreement about how we work in this repository:** propose adding it to this file (`AGENTS.md`). Quote the exact wording and add it once I agree.
- **New agreement about how to work in Nozbe:** propose adding it to `rules.md`, and to `rules.pl.md` with it. Quote the exact wording and add it once I agree.
- Do the same when an existing agreement or rule changes or no longer applies.
