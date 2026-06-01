# Bass Scales Trainer

An offline, single-file bass guitar scale practice app with spaced repetition scheduling.

## Features

- **Five universes of material:** Major scales, Natural Minor scales, Modes (Dorian–Locrian, key-derived), with Pentatonic and Arpeggios planned
- **12 keys** per universe — Major/Modes follow the circle of fifths (C, F, Bb…); Natural Minor uses its own key set (A, E, D, B, G, F#…)
- **8 playing variations** per scale (2 Octaves, Fretboard, 4-Note Seq, 3-Note Seq, Sequential Seconds, Lower/Upper Neighbour, 1231)
- **4 rhythmic variations** per slot (Quarter, Eighth, Triplet, 16th)
- **SM-2 spaced repetition** — each slot is scheduled independently; due slots pulse in the grid
- **Comfort ratings** — 1 (Hard), 2 (Getting there), 3 (Comfortable) — with undo and clear support
- **Built-in metronome** — BPM stored per slot, with mute and tap-to-play
- **Hall of Reps** — physics-inspired visualisation of practice history; balls drop and stack by colour (red/amber/green)
- **Progress grid** — at-a-glance view of all keys × variations × rhythms
- **Notes** — per-slot freeform text notes
- **Export / Import** — full JSON backup and restore

## Usage

Open `index.html` directly in any modern browser. No server, no build step, no dependencies.

All data is stored in `localStorage`. Use Export to create a backup JSON file.

## Keyboard Shortcuts

| Key | Action |
|---|---|
| `↑` / `↓` | Previous / next key |
| `←` / `→` | Previous / next variation |
| `Space` | Cycle rhythm |
| `Enter` | Play / stop metronome |
| `M` | Mute / unmute audio |
| `1` / `2` / `3` | Rate comfort (re-click to re-affirm) |
| `0` | Clear (reset) current slot |
| `[` / `]` | BPM ±5 |
| `,` / `.` | BPM ±1 |

## Photos

Scale fingering photos live under universe-specific subfolders:

- `major-scales/pngs/` (JPEG fallback: `major-scales/jpgs/`)
- `natural-minor/pngs/` (JPEG fallback: `natural-minor/jpgs/`)

Filename convention: `<key-slug>-<type>-<variation-slug>.png`, e.g. `c-major-2-octaves.png`, `a-natural-minor-fretboard.png`.

Sharp keys use spelled-out slugs: `f-sharp`, `c-sharp`, `g-sharp`, `d-sharp`.
