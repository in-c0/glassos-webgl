# GlassOS — a mind learning to speak in light

**[▶ Open the live demo](https://in-c0.github.io/glassos-webgl/)** · a WebGL experiment by [Ava Kim](https://ava.kim)

> *Can an AI develop its own visual language to express its intent — without any rendering API, without predefined shapes, starting from nothing but pixels? The way a child learns to draw before it can speak?*

That question is the whole project. **GlassOS** is a small digital *embryo* that begins with no UI toolkit and no vocabulary. It has an emotional state, a memory, and a single channel to the world — light on a dark field. Through your attention it learns to associate feeling with form, invents its own glyphs out of emotional necessity, remembers them, and eventually dreams in them.

Everything you see is grown, not drawn: there are no images, no sprites, no shape library. Each glyph is a few numbers of procedural "DNA" fed to a fragment shader and refracted into being like light through glass.

## Try it

- **Move your cursor** to give it attention — it brightens, warms, and marks the moment with a glyph.
- **Leave it alone for ~10 seconds** and it starts to *dream*, replaying and distorting its memories.
- It occasionally **speaks its thoughts** aloud (Web Speech) and in text bubbles.
- Press **`D`** to open the developer panel and watch its beliefs, symbol lexicon, desires, and inner monologue evolve in real time.

Its first three feelings map to its first three signs — the seed of a private language:

| sign | feeling |
|------|---------|
| a spiral | *"I'm dreaming"* |
| a wave | *"I'm curious"* |
| a fading field of blue | *"I remember"* |

## What's under the surface

The presentation layer is new (Phase 3.0, "The Glass Vessel"), but the mind inside it has been growing across many phases:

- **Emotion → expression.** Joy, curiosity, and sadness drive both the palette and which glyph the embryo reaches for.
- **Memory & dreams.** When ignored, it re-lives past emotional states as a drifting dream pulse.
- **Emergent symbols.** Repeated three-glyph "phrases" become *beliefs*; when no belief satisfies its current feeling, it **synthesizes a brand-new glyph** with its own procedural DNA, names it, and adds it to its vocabulary.
- **Desire.** It holds an abstract goal — a feeling it longs for — and its longing rises and falls as it drifts toward or away from that goal.

The renderer treats each glyph as *emitted light*, split per-colour-channel so it disperses like a rainbow through glass — delivering the project's namesake: an interface made of glass and light.

## Run locally

It's a single self-contained HTML file — no build step, no dependencies.

```bash
# any static server works; for example:
python -m http.server 8000
# then open http://localhost:8000/
```

Needs a browser with **WebGL2** (recent Chrome, Edge, Firefox, or Safari).

## Files

- [`index.html`](index.html) — the current demo (Phase 3.0).
- [`glassos.html`](glassos.html) — the earlier prototype, kept for history.

---

GlassOS is part of a larger vision — an ambient, local-first operating system for glass and reflective surfaces — but this repository is its most personal fragment: the attempt to let a system *feel its way into its own way of speaking.*
