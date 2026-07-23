# GlassOS — a mind learning to speak in light

**[▶ Open the live demo](https://in-c0.github.io/glassos-webgl/)** · a WebGL experiment by [Ava Kim](https://ava.kim)

> *Can an AI develop its own visual language to express its intent — without any rendering API, without predefined shapes, starting from nothing but pixels? The way a child learns to draw before it can speak?*

That question is the whole project. **GlassOS** is a small digital *embryo* whose signs are **alive**: each one is a genome, your attention is its food, and the language you see on screen is the result of real selection — not a script pretending to learn.

## How it actually works

There are no sprites, no shape library, no hand-drawn glyphs.

- **Every sign is a genome.** A small CPPN-style function network — composed `sin` / `gauss` / `tanh` / `triangle` nodes over local space and time. The network's zero-contour, rendered as refracted light with chromatic dispersion, *is* the sign. The expressive space is the network's function space: open-ended, evolvable, unowned.
- **Attention is the fitness function.** Cursor dwell near a sign feeds *that sign* (per-artifact credit assignment). Fed signs hold energy; energy-weighted parents breed the next generation, with mutation and crossover. Ignored signs starve, fade, and die. Touching a sign directly is a feast.
- **Left alone, it dreams — by novelty search.** After ~12 seconds without attention, selection changes regime: instead of chasing reward, the system breeds candidates from its archive and keeps whichever is most *unfamiliar* (distance in phenotype space against everything it has ever kept). Awake, it learns what you like; asleep, it imagines. When you return, its dreams face selection.
- **It remembers.** The living population, the hall-of-fame archive, and the generation count persist in `localStorage`. Close the tab, come back tomorrow — same creature, older, shaped by everyone who has visited that browser.

The two meters in the HUD are honest: **Vitality** is smoothed attention income; **Restlessness** rises when income has been scarce, and drives up mutation.

## Try it

- **Move your cursor** near a sign to feed it. Watch it brighten and swell.
- **Click a sign** to feast it.
- **Stop moving** for ~12 seconds and it starts to dream — new, stranger forms replace the dim ones.
- Press **`D`** for the developer panel: per-sign energy, lineage, activation genes, the archive, and the generation log — selection happening in real numbers.
- `GlassEmbryo.reset()` in the console wipes its memory and starts a new genesis.

## Run locally

A single self-contained HTML file — no build step, no dependencies.

```bash
# any static server works; for example:
python -m http.server 8000
# then open http://localhost:8000/
```

Needs a browser with **WebGL2** (recent Chrome, Edge, Firefox, or Safari).

## History

Earlier phases (1.0–3.0) explored the same question with a scripted cognition engine — templated glyphs, counted "beliefs," randomized "synthesis." Phase 4.0 replaced that theater with the real thing: genomes, selection, novelty search, persistence. The old prototypes live in git history.

---

GlassOS is part of a larger vision — an ambient, local-first operating system for glass and reflective surfaces — but this repository is its most personal fragment: the attempt to let a system *feel its way into its own way of speaking.*
