---
name: commit-messages
description: How to make git commits in this project and how to write their messages. Use whenever you are about to run git commit, when a change is finished and ready to commit, or when the user says "commit" or "release".
---

Follow these rules every time you commit in this repository.

## When to commit
- Commit automatically after each finished and tested change. Do not wait to be asked.
- Do not commit work that is half done, or changes you have not tested. If you could not test something, say so in the message body.
- Push, publish and tagging-and-pushing stay with the user (GitHub Desktop).

## What goes into a commit
1. Run `git status` and `git diff` first, so you know exactly what you are committing.
2. One logical change per commit: one feature or one fix, together with its `CHANGELOG.md` entry and any README update. Unrelated edits get their own commit.
3. Stage files by name (`git add <file> ...`), not `git add -A`.
4. If the change is visible to the user of the app, make sure `CHANGELOG.md` has an entry under `## [Unreleased]` before committing.

## Message format

```
Summary line in the imperative

Why this change was made, in a sentence or two. Explain the reason
and any decision taken, not just what the diff shows.

- Short bullet for each individual change
- Another change

Tested: what was checked and how.
Changelog: entry added under Unreleased (or "not needed").

Co-Authored-By: Claude Sonnet 5.5 <noreply@anthropic.com>
```

### Summary line
- Imperative mood: start with a verb such as Add, Fix, Change, Remove ("Add progress grid", not "Added" or "Adds").
- 50 characters or fewer, no full stop, no type prefix.

### Body
- Leave one blank line after the summary.
- Written in English, wrapped at about 72 characters per line.
- Include all of these, in this order:
  1. **Why**: the reason for the change, not only what changed.
  2. **Changes**: a bulleted list of the individual changes.
  3. **Tested**: one line on what was checked. If nothing could be tested, say "Not tested" and why.
  4. **Changelog**: which `CHANGELOG.md` entry was added or updated, or "not needed" for changes users won't notice (such as docs or tooling).
- Finish with the `Co-Authored-By` line shown above, after a blank line.

## Releases
When the user says to release a version:
1. Move the `## [Unreleased]` entries in `CHANGELOG.md` under a new `## [x.y.z] - YYYY-MM-DD` heading (new feature = minor bump, fix = patch bump).
2. Make a dedicated commit with the summary `Release x.y.z`. The body lists the highlights from the changelog.
3. Create the tag: `git tag vX.Y.Z`. Do not push it; tell the user to push tags from GitHub Desktop.

## Never do
- `git push`, or anything that publishes to GitHub.
- Rewriting history: no `git commit --amend`, `git rebase`, `git reset --hard`, or force operations. Fix a mistake with a new commit.

## How to run it
Pass the message with a heredoc so that line breaks are kept:

```bash
git commit -F - <<'EOF'
Add progress grid

Why: ...
EOF
```

After committing, run `git log -1 --stat` and report the summary line to the user in one sentence.
