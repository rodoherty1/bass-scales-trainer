# Architecture
The entire application is a single `index.html` — inline CSS, HTML, and JS with no build step and no external dependencies. Do not split into multiple files.

# Scale Images
Images live under `<universe-folder>/pngs/` (primary) and `<universe-folder>/jpgs/` (fallback).
Stem format: `<key-slug>-<type-slug>-<variation-slug>` — e.g. `a-major-1231`, `a-natural-minor-1231`.
Universe folders that currently have images: `major-scales/`, `natural-minor/`. Modes has no photos yet — `showScaleImage()` shows a text placeholder for it. Pentatonic/Arpeggios are unimplemented (disabled buttons in the UI).

# Storage Keys
`db`/`sr`/`notes` are keyed by pipe-delimited strings embedding key/variation/rhythm **labels** (not indices), e.g. `scales|F#|2 Octaves|Quarter Note`. Renaming any label in `KEYS`/`MINOR_KEYS`/`VARS`/`MODES`/`RHYTHMS` orphans existing data unless you add a matching migration in `load()`/`loadNotes()` — the existing pruning logic (Migration C) will otherwise silently delete it as "unrecognised."

# Testing
No automated tests. Verify JS changes with `node --check` on the extracted `<script>` block, and manually smoke-test affected UI before committing.

# Git
Commits may take place on the `main` branch.
Commits must always preserve the current git history.  Never use `git push -f`.
Ensure README.md is kept up to date — treat its Features list as the source of truth for existing behavior; check it before adding features that might overlap or conflict with something already there.
