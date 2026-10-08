# Changelog

All notable changes to Times Tables Trainer are listed here, newest first.
Versions follow [Semantic Versioning](https://semver.org/): new features bump the minor number, fixes bump the patch number.

## [Unreleased]

## [0.2.0] - 2026-10-08

### Added
- Progress tracking saved in the browser (`localStorage`), per fact (7×8 and 8×7 count as the same fact).
- A fact counts as learned after 3 correct answers in a row.
- "My progress" screen with a 12×12 colour grid (learned, getting there, needs work, not tried) and a learned-facts count.
- "Reset progress" button with a confirmation step.
- Missed questions return a few questions later in the same round.

### Changed
- Rounds still have 10 questions, but about half now come from facts that aren't learned yet, weighted towards the weak ones.
- Score and stars count first attempts only; retries don't add to the score.
- The "pick at least one table" warning is now shown on the page instead of in a pop-up.

## [0.1.0] - 2026-10-08

### Added
- First version: pick tables 1–12, 10 random questions per round, score, streaks, and a list of tricky questions at the end.
