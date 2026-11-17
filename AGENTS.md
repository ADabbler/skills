# AGENTS.md

## Skill layout

- Keep each skill under `skills/<name>/` with an English `SKILL.md`. The frontmatter `name` must match the directory name.
- Keep each skill independently installable by storing its required resources within its own directory and linking to them with relative paths.

## Documentation

- Keep existing English and Chinese versions of the same document in sync.
- Keep private working context out of the [maintenance notes](notes/README.md).

## Verification

- After adding, removing, renaming, or moving a skill, run `npx skills add . --list` from the repository root to check discovery.

## Commits

Follow the style of recent commits. Use `<type>(<scope>): <description>` by default.
