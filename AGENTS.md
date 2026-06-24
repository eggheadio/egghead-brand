# egghead-brand — agent notes

This directory holds egghead brand assets and references (see `EGGO.md` for the
mascot spec, `SOUL.md` for personality, `newegghead-research.md` for brand context).

## Related repos

These are expected to be cloned as siblings of this directory (Claude Code
sessions started here get them as additional working directories via
`.claude/settings.json`):

- **`../egghead`** — pnpm/turbo monorepo behind beta.egghead.io. The web app is
  `../egghead/apps/web` (Next.js, runs locally on `http://localhost:3008` via
  `pnpm dev`).
- **`../ui`** — separate design-system exploration turborepo (see below).

## Design system — current stage

The egghead design system flows in one direction:

**1. This repo (source of truth for design):** paired light/dark HTML mockups
define the visual language — `components.html` / `components-dark.html` (tokens,
buttons, cards), `layout.html`, `navigation.html`, `footer.html` (+ `-dark`
variants), and `brand.html`. `EGGO.md` (mascot spec) and `SOUL.md` (personality)
govern illustration and voice.

**2. `@egghead/ui` (shipped implementation):** `../egghead/packages/ui` —
`src/styles/tokens.css` mirrors the mockups as semantic light/dark CSS variables
plus a fluid type scale; its header names this repo's HTML files as the source of
truth. Component set is intentionally small so far: `button`, `container`,
`eggo-mark`, `structure`. Consumed by `../egghead/apps/web` (beta.egghead.io).

**Workflow:** design changes land in the HTML mockups here first (both light and
dark variants), then get ported to `tokens.css` / components in `@egghead/ui`.
Don't edit `tokens.css` values that diverge from the mockups without updating the
mockups too.

**Not canon:** `../ui` is a separate exploration turborepo (gremlin design
system, uxspec page specs, ai-hero). It is upstream R&D, not what the egghead app
ships — don't copy patterns from it into `@egghead/ui` unless explicitly asked.
