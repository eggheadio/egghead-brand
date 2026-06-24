---
name: eggo-generator
description: "Generate on-brand egghead Eggo mascot prompts and bitmap artwork from this repo's local brand references. Use when the user asks for eggos, Eggo illustrations, egghead mascot art, course covers, stickers, social images, thumbnails, UI states, or any image/prompt featuring the egg-shaped egghead character."
---

# Eggo Generator

## Purpose

Create on-brand Eggo prompts and image assets using this repository's source-of-truth brand files.

Use this skill for:
- Writing prompts for image models.
- Generating or editing bitmap Eggo art.
- Art-directing course covers, stickers, thumbnails, OG images, UI empty/error states, or editorial spots.
- Reviewing generated Eggos for brand fit.

If the user asks for an actual image asset, use the available image generation/editing workflow. If they ask for a prompt, deliver the prompt only.

## Required Local References

Read these repo-local files before generating or reviewing Eggo artwork:

- `EGGO.md`: canonical anatomy, render modes, palette, prompt blocks, negative prompt, and source asset map.
- `SOUL.md`: Eggo's personality, tone, boundaries, and continuity.

Use these local visual references when image tools support references:

- `references/official-egghead-eggo-logomark.png`: primary character identity reference.
- `references/eggo-character-sketch-sheet-test.jpeg`: primary expression/hands reference; use for character sheets, emotional poses, and laptop/workflow scenes.
- `references/all-the-eggos-from-maggie-appleton/Highfive_Eggos.png`: flat vector/group reference.
- `references/all-the-eggos-from-maggie-appleton/variety_eggos.png`: painterly sketch reference.
- `references/all-the-eggos-from-maggie-appleton/HP_eggo_1.png`: textured cosmic reference.
- `references/all-the-eggos-from-maggie-appleton/`: full source artwork library.

Do not copy the asset library into the skill. Reference the files in place.

## Workflow

1. Identify the output type: prompt only, generated bitmap, edit of an existing image, or critique.
2. Pick one render mode from `EGGO.md`: flat vector, painterly sketch, or textured cosmic.
3. Preserve the hard identity rules:
   - Eggo is an egg wearing large dark glasses.
   - The glasses are the face. Do not add eyes, mouth, nose, teeth, or ears.
   - Simple eyebrow marks are allowed and useful for expression; never draw eyes beneath them.
   - No cracking, yolk, shell fragments, hatching, photorealism, or full human body.
   - Hands/feet appear when required for expression, gesture, or props, usually as white cartoon gloves or small stylized feet.
   - Avoid long stick arms; hands should float or connect with tiny unobtrusive stubs.
4. Build the prompt from the `EGGO.md` base character block, selected render-mode block, user scene, palette guidance, and negative prompt.
5. If generating an image, use `references/official-egghead-eggo-logomark.png` as the strongest identity reference where the tool supports image references.
6. Save or move generated image files into this repo's `generated/` directory. Create it if needed. Use descriptive filenames such as `generated/eggo-agent-grid.png`.
7. Validate the result against: readable egg silhouette, glasses-only face, eyebrows but no eyes, no mouth/ears, no cracks/yolk, no stick arms, correct mode, dark navy/cream/yellow-led palette, and scene clarity.

## Prompt Shape

For prompt-only requests, return a compact, ready-to-paste prompt:

```text
[base character], [mode styling], [scene], [palette/light], [composition/output details]

Negative prompt: [negative prompt]
Reference images: [repo-local reference paths to use]
```

Do not over-explain unless the user asks for art direction notes.

## Default Art Direction

Favor whimsical, curious, concise compositions over corporate AI gloss. Eggo should feel capable and playful, never dark-edgy, cyberpunk, or photoreal.
