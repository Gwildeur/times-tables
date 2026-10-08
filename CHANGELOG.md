# Changelog

All notable changes to Times Tables Trainer are listed here, newest first.
Versions follow [Semantic Versioning](https://semver.org/): new features bump the minor number, fixes bump the patch number.

## [Unreleased]

## [0.3.0] - 2026-10-09

### Added
- On-screen number keypad with a Check button, so answers can be entered on an iPhone (the phone's own number pad has no Return key). Typing on a computer keyboard still works.
- Can be added to the iPhone Home Screen as an app, with its own icon and name, opening full-screen.
- Works offline once opened from a web address (for example GitHub Pages).
- Tap a square in the progress grid to see that fact and how often it was right or wrong.

### Changed
- The whole app is now in German (it is called "Einmaleins-Trainer"), including the Home Screen name and the praise and result messages. English is no longer available.
- On phones the app now uses the whole screen, with the keypad at the bottom and room for the notch and the Home bar.
- The progress grid fits the width of a phone screen.
- Buttons are bigger and easier to hit with a finger, and double-tap zoom is switched off.
- The layout also fits when the phone is held sideways.

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
