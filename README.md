# Bass Scales Trainer

An offline, single-file bass guitar scale practice app with spaced repetition scheduling.

## Features

- **Four universes of material:** Major scales, Modes (key-derived), with Pentatonic and Arpeggios planned
- **12 keys** across the circle of fifths (C, F, Bb, Eb, Ab, Db, Gb, B, E, A, D, G)
- **8 playing variations** per scale (2 Octaves, Fretboard, 4-Note Seq, 3-Note Seq, Sequential Seconds, Lower/Upper Neighbour, 1231)
- **4 rhythmic variations** per slot (Quarter, Eighth, Triplet, 16th)
- **SM-2 spaced repetition** — each of the 384 slots is scheduled independently; due slots pulse in the grid
- **Comfort ratings** — 1 (Hard), 2 (Getting there), 3 (Comfortable) — with undo support
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
| `[` / `]` | BPM ±5 |
| `,` / `.` | BPM ±1 |

## Photos

Scale fingering photos are served from `pngs/` (with `jpgs/` fallback). Files follow the naming convention `<key>-major-<slug>.png`, e.g. `c-major-2-octaves.png`.
