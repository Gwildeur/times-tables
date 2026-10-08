# Times Tables Trainer

Single-file web app (`index.html`, no build step) for practising times tables. Opened by double-click in Safari.

## Commits
- Claude commits after each finished and tested change.
- Before every commit, follow the `commit-messages` skill (`.claude/skills/commit-messages/SKILL.md`): message format, what to stage, and what never to do.
- Claude never pushes or publishes. The user does that in GitHub Desktop.

## Release notes
- Keep `CHANGELOG.md` up to date with every user-visible change, in the same working session as the change.
- Add entries under `## [Unreleased]` while working. When the user says to release, move them under a new `## [x.y.z] - YYYY-MM-DD` heading (details in the `commit-messages` skill).
- Use the sections Added / Changed / Fixed / Removed, and write for a non-technical reader.
- Version numbers: new feature = minor bump, bug fix = patch bump.
