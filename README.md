# Tasbih · Dzikir

A premium, minimalist **Tasbih & Dzikir** counter — a mobile-first prototype with a skeuomorphic *falling-beads* counting mechanic. Tap anywhere and the lowest bead detaches from the top string, falls under simulated gravity, and settles into a growing reservoir at the bottom.

Single self-contained `index.html` — no build step. Open it in any modern browser.

## Features

- **Falling-beads physics** — a 60fps `<canvas>` loop (gravity, damped bounce, settling) decoupled from React renders.
- **Counting** — the count increments the instant a bead detaches; the top reservoir empties exactly at the target.
- **Targets** — 33, 99, or continuous (∞) mode.
- **Dhikr selector** — Subhanallah · Alhamdulillah · Allahu Akbar · Custom, each with Arabic, transliteration and translation.
- **Completion** — golden particle burst + an *Alhamdulillah / Completed* card when the target is reached.
- **Light & dark mode** — cream/emerald/charcoal palette; deep slate/gold in dark.
- **Sound & haptics** — synthesised wooden "clink" (WebAudio, no asset files) and `navigator.vibrate` feedback, both toggleable.
- **Long-press reset** — a 750ms hold (with fill ring) refills the bead pool, preventing accidental resets.
- Accessibility: `prefers-reduced-motion` aware, `aria-label`s on icon controls, safe-area padding.

## Tech

React 18 · Tailwind CSS · inline Babel (classic JSX runtime) · HTML5 Canvas · WebAudio. Lucide icons are inlined as SVG path data to keep the project a single dependency-light file.

## Run

```bash
# any static server works, e.g.
npx serve .
# then open the printed URL
```

Or simply open `index.html` directly in a browser.
