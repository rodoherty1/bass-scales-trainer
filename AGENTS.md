# Architecture
The entire application is a single `index.html` — inline CSS, HTML, and JS with no build step and no external dependencies. Do not split into multiple files.

# Scale Images
Images live under `<universe-folder>/pngs/` (primary) and `<universe-folder>/jpgs/` (fallback).
Stem format: `<key-slug>-<type-slug>-<variation-slug>` — e.g. `a-major-1231`.
Currently only `major-scales/` images exist. Natural Minor images are forthcoming; when they arrive, `showScaleImage()` will need a universe-aware stem — it currently hardcodes `-major-` on line 1152.

# Git
Commits may take place on the `main` branch.
Commits must always preserve the current git history.  Never use `git push -f`.
