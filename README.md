# claude-skills

Canonical home of Forrest's personal Claude Code skills. This repo is cloned as
`~/.claude/skills/`, the directory Claude Code auto-discovers personal skills
from — the GitHub repo is the source of truth and changelog; the local clone is
what the tooling actually loads.

## Skills

- **`dev-workflow/`** — my development-session methodology: the
  plan → build → review → remediate → live-test → close loop and its approval
  gates (`SKILL.md`), the new-project design-stage process
  (`design-methodology.md`), and production cutover / live-data migration
  discipline (`launch-and-cutover.md`). **This repo is the upstream.** Project
  repos (e.g. [pbe-address-book](https://github.com/fthiess/pbe-address-book))
  carry vendored snapshots at `.claude/skills/dev-workflow/` so the methodology
  travels with each project; when the methodology changes, the change lands
  here and propagates to project copies at their next methodology-touching
  session.

- **`obsidian-tandem-comments/`** — NOT mine. Generated at runtime by the
  [obsidian-tandem-comments](https://github.com/leonpawelzik/obsidian-tandem-comments)
  Obsidian plugin, which writes its skill directly into the user's personal
  skills directory. Tracked here so plugin-driven changes show up as diffs
  instead of silent overwrites; if `git status` shows this folder modified, the
  plugin updated itself — review and commit.

## Conventions

- Methodology changes are commits with reasoning in the message — this repo's
  log is the skill's changelog.
- Skill format: each skill is a folder with a `SKILL.md` (frontmatter `name` +
  `description` drive discovery); supporting docs load on demand.
