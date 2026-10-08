# Times Tables Trainer

Web app (`index.html` holds all the app code, no build step) for practising times tables. Opened by double-click in Safari, or hosted and added to the iPhone Home Screen. `manifest.webmanifest`, `sw.js` and `icons/` provide the Home Screen icon and offline support.

## Language
- The app is German only (the player is a native German speaker): all on-screen text, the page title and the Home Screen name are in German, addressing him with "du". New text must be German too.
- Code, comments, CHANGELOG, README and commit messages stay in English.

## Commits
- Claude commits after each finished and tested change.
- Before every commit, follow the `commit-messages` skill (`.claude/skills/commit-messages/SKILL.md`): message format, what to stage, and what never to do.
- Claude never pushes or publishes. The user does that in GitHub Desktop.

## Release notes
- Keep `CHANGELOG.md` up to date with every user-visible change, in the same working session as the change.
- Add entries under `## [Unreleased]` while working. When the user says to release, move them under a new `## [x.y.z] - YYYY-MM-DD` heading (details in the `commit-messages` skill).
- Use the sections Added / Changed / Fixed / Removed, and write for a non-technical reader.
- Version numbers: new feature = minor bump, bug fix = patch bump.
- When releasing, also bump the `CACHE` name in `sw.js` to the new version so installed copies update.
