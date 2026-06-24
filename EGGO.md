# EGGO.md — mascot reference for image generation

> visual spec distilled from maggie appleton's original eggo asset library (71 files, dropbox archive).
> purpose: drop into context for image-gen agents (midjourney / flux / qwen / nano banana) + humans art-directing them.
> companion files: SOUL.md (personality), newegghead-research.md (brand context).

---

## 0. reference images (local, in this repo)

- **canonical logomark:** `references/official-egghead-eggo-logomark.png` — the official egghead eggo mark (cream egg, dark outline, thick rectangular browline glasses, no eyes/mouth). this is the ground truth for silhouette + glasses-as-face. feed it as the primary image ref / `--cref` for character consistency.
- **expression sketch sheet:** `references/eggo-character-sketch-sheet-test.jpeg` — John Lindquist's Images 2.0 character sketch sheet test. use this as the strongest reference for expressive hands + eyebrow marks while preserving no eyes/mouth/ears.
- **full asset library:** `references/all-the-eggos-from-maggie-appleton/` — local copy of the dropbox archive (maggie appleton's original eggo library). all canon filenames cited below (`Highfive_Eggos.png`, `variety_eggos.png`, `Eggodex_Bits/`, `Solo_Eggos/`, `Team_Eggos/`, `Warning_Eggo/`, `basic_eggo.ai`, …) live in this directory. pull style refs per render mode from here.

---

## 1. identity tl;dr

eggo is an egg wearing glasses. that's the whole logo and the whole character. the **glasses ARE the face** — thick dark frames, no eyes drawn behind them, no mouth, no ears. emotion is carried by glasses angle, eyebrow marks, body tilt, hands, props, and motion lines. in 3/4 view the two lenses render as different sizes — the asymmetric **"Oo"** that mirrors the egghead logomark.

---

## 2. anatomy spec (hard rules)

- **body:** smooth egg, roughly 2:3 width-to-height, slightly bottom-heavy. sits on its fat end. soft drop shadow ellipse underneath.
- **face = glasses only.** no eyeballs, no mouth, no nose, no ears. frame thickness ≈ 1/8 of body width. default: round black/dark-slate frames.
- **eyebrows are expression marks, not facial features.** short dark strokes above the glasses are allowed and useful for anger, worry, delight, focus, confusion, and surprise. keep them simple; never add eyes beneath them.
- **hair tuft (optional):** one soft swoosh/curl on the crown. signals individuality in groups.
- **limbs: none by default; hands are allowed when expressive or functional.** white cartoon gloves (mickey-style, 4 fingers) manifest for gestures, emotion, or props — typing, high-fiving, holding a wand, clutching glasses, pointing, celebrating. avoid long stick arms; hands should float or connect with tiny unobtrusive stubs. same for feet. → "you can manifest hands if needed" (SOUL.md)
- **the egg does not crack.** ever. no yolk, no shell fragments, no hatching.
- **scale play is canon:** eggo is often tiny against a huge subject (planet, cloud, mountain) — wonder through scale.

## 3. the eggodex system (modular kit)

the original library literally ships as parts (`Eggodex_Bits/`): egg bodies in multiple shell colors (cream, black, pink, sky blue, brown, alien green w/ saturn ring) × a glasses wardrobe (classic round, browline, hexagonal, cat-eye, aviators, pink rounds, safety goggles, orange "8" frames). 

→ **identity = body color + glasses choice + one prop.** this is how you generate infinite distinct eggos (community members, team, instructors) while staying on-model. diversity of shell colors in group scenes is canon (High Five, Team Climbers).

## 4. render modes (three, pick one per asset)

| mode | look | use for | canon refs |
|---|---|---|---|
| **A. flat vector** | clean shapes, subtle linear gradients, soft drop shadows, no outlines | logo, UI states, stickers, og-cards, error pages | `Highfive_Eggos.png`, `Team_Climbers/*`, `Warning_Eggo/*`, `tamagotchi_eggo.png` |
| **B. painterly sketch** | visible pencil linework + loose soft digital color, blob-swatch backgrounds, unfinished edges | editorial spots, blog illustrations, "wip energy" | `variety_eggos.png`, `gardener_eggo.png`, `thinking_eggo_1.png`, `astronomy_eggo.png` |
| **C. textured cosmic** | rich digital painting, grain/noise texture, glow, deep navy space | hero images, course covers, big-moment scenes | `Solo_Eggos/Planets_Eggo/*`, `marioworld_eggo.png`, `HP_eggo_1.png` |

## 5. palette (extracted from assets, approx)

- **deep space navy / slate:** `#102030` – `#304050` (backgrounds, frames, rocks)
- **shell cream:** `#f0f0f0` / warm off-white (default egg)
- **sun yellow:** `#f0d050` – `#f0e080` (the JS-sun, glows, halos)
- **terracotta / rust:** `#904040` – `#a05040` (planets, alt shells, warmth)
- **sky blue:** `#a0d0e0` (clouds, secondary)
- **confetti accents:** teal, coral, orange, lime — tiny doses only (celebration, floating symbols)

rule: dark navy + cream do the heavy lifting; yellow is the light source; everything else is seasoning.

## 6. storytelling devices (canon, reuse freely)

- **floating code confetti:** `{ }`, `;`, `( )`, λ, atoms, "A", "JS" drifting around eggo like sparks
- **framework celestial bodies:** technologies as planets/suns (red "A" angular planet, yellow JS sun) — eggo voyages between them
- **props define role:** wand = magic/codegen, telescope = exploration, jetpack = speed, watering can = growing skills, pickaxe+flag = mastery summit, wrench = maintenance
- **the swarm:** many eggos = teamwork/subagents (climbers roped together, repair crew, high-fives)
- **game-world logic:** floating item blocks, +1000 score popups, level platforms (`marioworld_eggo.png`)
- **eggo cosplays things:** tamagotchi shell, twitter bird, ice-cream scoops, gingerbread — the egg silhouette survives any costume

## 7. prompt recipes

### base character block (prepend to everything)
```
eggo: a smooth egg-shaped mascot character wearing large thick round
black glasses, the glasses are the face, no eyes no mouth no ears,
simple eyebrow marks allowed for expression, small hair tuft on top,
cream-white shell, no long stick arms, white cartoon gloves may
manifest for gestures or props, soft drop shadow, charming and curious
posture
```

### mode A — flat vector (logo/UI/sticker)
```
[base block], flat vector illustration, clean geometric shapes, subtle
gradients, soft shadows, no outlines, solid background, sticker design,
minimal, in the style of modern saas mascot illustration
```

### mode B — painterly sketch (editorial)
```
[base block], loose pencil sketch with soft digital painting, visible
construction lines, muted watercolor blob background, hand-drawn
imperfect charm, editorial spot illustration, floating code symbols
{ } ; λ around the character
```

### mode C — textured cosmic (hero)
```
[base block] as a tiny astronaut with headphones, floating in deep navy
space toward a huge glowing [terracotta planet marked "A" / yellow sun
marked "JS"], rich painterly texture, film grain, soft rim light,
sense of wonder and scale, asteroid debris, sparse code-symbol particles
```

### scene seeds (swap into any mode)
- eggo conjuring code symbols with a magic wand, orange glow
- swarm of five eggos in different shell colors roped together climbing a navy rock face, yellow JS sun behind the summit, one plants a `{ };` flag
- eggo with jetpack manifesting white gloves, speed lines, trailing brackets
- eggo watering tiny sprouting framework trees with a watering can
- two eggos with wrenches repairing a server rack, "we're updating egghead" scene
- eggo on a floating game platform collecting a glowing JS cube, +1000 popup
- eggo peeking through a telescope at a night sky of constellation-shaped code

### negative prompt (all modes)
```
realistic egg, cracked shell, yolk, human face, eyeballs, mouth, teeth,
nose, ears, full human body, long stick arms, realistic arms, arms
attached without gloves, 3d render, photorealism, corporate
gradient-on-black AI aesthetic, neon cyberpunk
```

### model-specific notes
- **image refs:** always anchor character identity on `references/official-egghead-eggo-logomark.png`; add `references/eggo-character-sketch-sheet-test.jpeg` when generating expressive poses, hands, or character sheets; add per-mode style refs from `references/all-the-eggos-from-maggie-appleton/`.
- **midjourney:** use canon pngs as image refs / `--sref` (best: `Highfive_Eggos.png` for vector, `variety_eggos.png` for sketch, `EGH_PlanetEggo_1.png` for cosmic). character consistency via `--cref` on the official logomark or a clean solo eggo.
- **flux.1 dev / qwen-image (local + fal.ai):** these follow long prose prompts well — paste base block + mode block + scene verbatim. for production consistency, **train a LoRA per render mode** (not one mixed LoRA): ~20–30 curated images each from the folders above. mode A is the easiest win (cleanest, most consistent data).
- **vision-rank loop:** generate n variants → vision model scores against sections 2 + 5 of this file (glasses-as-face? eyebrows but no eyes? no mouth/ears? no stick arms? palette?) → top pick ships. same pattern as the ffmpeg cover pipeline.

## 8. do / don't

**do:** keep the silhouette readable at 16px · let glasses, eyebrows, tilt, and hands carry emotion · manifest gloves with expressive or functional purpose · use scale for wonder · multiply eggos for teamwork · costume freely (silhouette survives)

**don't:** crack the egg · add eyes/mouth/ears "for expressiveness" · draw long stick arms · attach realistic arms · go neon/cyberpunk/terminator · photoreal render · shrink the glasses (they're ~60% of the face read)

## 9. source asset map (`references/all-the-eggos-from-maggie-appleton/`)

all paths below are relative to `references/all-the-eggos-from-maggie-appleton/` in this repo (originally a dropbox archive).

- `Eggodex_Bits/` — modular kit: shells + glasses wardrobe (13 parts)
- `Solo_Eggos/` — Planets (4 cosmic comps + psd), HighFive (+psd), Microphone (good/bad mic svg)
- `Team_Eggos/` — sketch sheets + Climbers set (light/dark bg, psd)
- `Warning_Eggo/` — error/warning state (svg + ai + UI comp)
- root — ~30 named solo eggos (gardener, astronomy, tamagotchi, twitter, birthday, marioworld, rocket booster, code magic, cloud ladder, gingerbread, ice cream stack, award medal, thinking, 500-repair…)
- source files: `.ai` (basic_eggo, microphones, warning) + `.psd` (planets, highfive, climbers) — **vector source of truth for the base character lives in `basic_eggo.ai`**
