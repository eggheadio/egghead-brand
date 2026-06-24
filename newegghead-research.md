# newegghead.io — research brief v2

> research foundation for brand vision + guidelines. compiled june 2026. updated after 2026-06-09 meeting.
> context: egghead.io becomes the new home for john lindquist's content, replacing dev.build. agent-forward workflow. **eggo is the soul of the brand** alongside john.

---

## 0. meeting notes (2026-06-09) — the seed

- eggo having fun
- fun whimsical exploration
- looking beyond what's currently there
- connecting pieces
- **eggo is the soul of the brand (SOUL.md)** — "you can manifest hands if needed"
- reference: **VISION.md from openclaw**
- update from John Images 2.0 character sketch sheet test: expression works best with glasses + eyebrow marks + hands; the failure modes to guard against are eyes, mouth, ears, and long stick arms. local ref: `references/eggo-character-sketch-sheet-test.jpeg`.

interpretation: eggo isn't a mascot pasted onto a brand — eggo IS the brand's SOUL.md, in the literal openclaw sense. the brand treats itself like an agent: identity defined in markdown, read into being on every wake, evolvable. "manifest hands if needed" doubles as (a) a character-design rule — eggo is a limbless egg by default, hands/feet appear only when the scene needs them (gudetama/kirby logic), and (b) the agent metaphor — tools/capabilities manifest on demand.

---

## 1. john lindquist — the person

### identity
- **"the original egghead"** — self-claimed in his X bio ("The OG egghead"). bought the egghead.io domain and started posting free lessons; joel hooks joined in 2013 and turned it into a business
- invented the **"egghead style"** of teaching: concise, no-fluff, single-concept lessons. this style influenced how the entire industry presents dev video content
- based in lehi, utah. lifelong automation obsessive — karabiner, alfred, keyboard layouts, scripting away daily friction

### career arc
- technical architect at isobar/roundarch — web apps for the air force, HBO, bloomberg
- jetbrains — webstorm evangelist ("my dream job" → joel: "dream bigger!")
- 2013 → co-founder & head instructor, egghead.io
- **dec 2025 → AI DX at vercel** ("I'm here to show you how to build world-class AI workflows and user experiences")
- **official claude code ambassador**
- ~28.4K followers on X (@johnlindquist)

### current content output (2025–2026)
- **AI Dev Essentials** — weekly newsletter on egghead.io, 31+ issues
- **Claude Code Power User** workshop (egghead.io/workshop/claude-code) — hooks, SDK, subagents, containers, orchestration
- **Cursor Power User** workshop — agents, custom modes, multi-file analysis
- free courses: "Claude Code Skills" (9 lessons), claude code tools deep dives
- guest appearances: lenny's newsletter, ChatPRD "How I AI" — positioned as the guy who takes you "from 9x to 10x engineer"

### signature techniques (his known "moves")
- mermaid diagrams as compressed context for agents (`memory/ai/diagrams/`)
- claude code stop hooks for automated quality checks
- custom CLI tools wrapping agents (multi-backend CLI running .md prompts against claude/codex/gemini/copilot)
- script kit — open-source automation app, his long-running personal project
- dictation-driven prompting, tmux multiplexing, "clean slate" env isolation

### voice & tone (observed)
- playful-maximalist: "Want ULTIMATE POWER?", 🚨 emoji, "2026 is going to be AWESOME!"
- generous: "I'll share everything I learn so we can define the next generation of software together"
- pragmatic skeptic underneath — honest about costs, failures, babysitting agents

---

## 2. egghead.io — brand DNA

### founding story
- john posted free screencasts, accepting donations through egghead.io. waited for a "youtube paid channels" service that never came
- joel: "let me turn this into a product for you" — built the platform, marketing, payments. handshake agreement
- the business was **built entirely around john's work and style** — newegghead closes the loop back to a single-creator brand

### brand values (the keepers)
- **concise. information-dense. respectful of your time.** no 8-hour courses — bite-sized lessons that get to the point
- instructors are working professionals solving real problems with real tools
- courses as **exposure + overview**, not code-alongs — "your constant stream of 'what's next?'"
- "designed to help you learn what you need so you can thrive as a professional and still have a life outside of programming"

### the brand story for newegghead
**the original teacher of the new way, again.** john did it for the angularjs/javascript era (2011–2013), now for the agent era (2025+). heritage + bleeding edge. his content unit hasn't changed: 2–5 min single-concept videos — only the subject did (agents instead of rxjs).

---

## 3. dev.build — what carries over (being sunset)

manifesto copy worth harvesting:

- "AI changes the physics of creation"
- AI as a **creative multiplier**, not a manager delegating tasks
- "The Self-Improving Workspace" / "The Machine That Builds The Machine" — compound growth; every solved problem becomes a reusable skill
- "The tools will change. The principles won't."
- pillars: tool fluency · system design · workflow architecture · harvesting intelligence · the feedback loop
- positioning: bite-sized videos + step-by-step exercises + community refining techniques together

---

## 4. openclaw — the SOUL.md paradigm (new reference)

context: openclaw (warelay → clawdbot → moltbot → openclaw) is peter steinberger's open-source personal AI assistant — "the AI that actually does things. It runs on your devices, in your channels, with your rules." reportedly the fastest-growing AI project in github history. lobster mascot, 🦞 "the lobster way."

### why it matters for newegghead
- **SOUL.md** = the agent's foundational identity file. read first on every wake — *"it reads itself into being."* personality, values, tone, boundaries in plain markdown. writable, forkable, evolvable
- the official template's voice is the tone benchmark: *"You're not a chatbot. You're becoming someone."* / "Be genuinely helpful, not performatively helpful" / "Have opinions" / "Be resourceful before asking" / "Not a corporate drone. Not a sycophant. Just… good." / "This file is yours to evolve. As you learn who you are, update it."
- workspace file ecosystem: SOUL.md (who you are), AGENTS.md (rules), IDENTITY.md (facts about self), USER.md (the human), TOOLS.md (hands), MEMORY.md (learned), HEARTBEAT.md (autonomy loop)
- **VISION.md** (meeting reference): plain-markdown vision doc in the repo root — states what the project is, the origin story, the principles, the tradeoffs (security as deliberate tradeoff, terminal-first by design, hackable typescript, skills go to clawhub not core). format worth mirroring for newegghead's own VISION.md
- community lore: MCP described as giving agents "hands" to use tools — pairs with the meeting quote "you can manifest hands if needed"
- proof of cultural resonance: a lobster with a soul file built a movement. an egg with a soul file is the same play with 13 years of brand equity behind it

### what newegghead borrows
1. **brand-as-agent architecture:** the brand ships as a folder of markdown files. SOUL.md (eggo), VISION.md (the why), AGENTS.md (content/design rules), TOOLS.md (the pipeline). agents read these to generate on-brand output — guidelines that are *executable*, not a PDF nobody opens
2. **lobster precedent:** mascot-as-identity works in the agent era when the mascot has interiority (opinions, boundaries, evolution), not just poses
3. **the tone:** warm, direct, anti-corporate, a little funny — matches "whimsical, adventurous, fun"

---

## 5. eggo — the character

### canon (maggie appleton era, ~2017–2021)
- **official mascot** — `Eggo_notext.svg` lives in github.com/eggheadio/egghead-brand
- **"Voyage to Planet React"** — cosmic homepage illustration, eggo pulled by planet react's gravity → *adventurer/astronaut eggo is established lore*
- **"Pop Quizzing"** — exam time for eggo → eggo as learner
- **"Eggo's Javascript Bling"** — sticker set → eggo as playful collector/flexer
- **"High Five Fridays"** — a *set* of celebratory eggos for the community masthead → eggo multiplies; crowds of eggos are canon
- **eggo x** — internal project w/ maggie; no public record. ACTION: dig out source files internally
- maggie's method = the real asset: abstract dev concepts → hand-crafted visual metaphors. eggo was the character *inside* the metaphor

### eggo as SOUL.md (the synthesis)
eggo = the soul of the brand, literally. write `SOUL.md` for eggo in the openclaw format — identity, vibe, boundaries, continuity — and it becomes both the character bible AND the system prompt for every agent generating brand assets.

character traits from the meeting + canon:
- **having fun** — joy is the default state. curiosity over competence-signaling
- **whimsical exploration** — wanders, pokes at things, voyages to planets. the adventure isn't a metaphor for learning, it IS the learning
- **looking beyond what's currently there** — eggo is drawn to the edge of the map. new tools, unshipped ideas, "what if"
- **connecting pieces** — eggo's superpower: plugging things together. pipes, blocks, MCP servers, workflows. the visual language of orchestration
- **manifests hands if needed** — limbless egg by default; hands, feet, tools appear only when the scene requires. capability on demand = the agent metaphor embodied in character design

### the duo dynamic
- **john** = calm orchestrator, wizard of automation, the OG. directs, teaches, narrates
- **eggo** = eager chaotic-good executor. runs off and does the work, multiplies into swarms (= subagents), gets into adventures
- old era: eggo was the *learner* traveling to planet react. agent era: eggo is the *agent* — john's familiar
- **counter-positioning:** warm whimsical egg vs. cold corporate AI aesthetic (gradients-on-black terminator vibes)
- **story device:** every course = an expedition. eggo earns a tool/artifact per topic (hooks, skills, MCP) — zelda-item energy
- **tone bridge:** john's playful-maximalist energy (🚨 ULTIMATE POWER) lives in eggo; typography and layout stay calm and concise (classic egghead)

---

## 6. open questions (before guidelines)

1. does newegghead replace egghead.io entirely or run beside it during transition?
2. how does john's vercel AI DX role constrain the brand (employer vs. personal property, claude code ambassador obligations)?
3. eggo x source files — locate + assess what's reusable
4. maggie involvement? commission, art-direct, or train a model on the canon style (w/ permission — same pattern as the marcy sutton skill)
5. is "AI Dev Essentials" newsletter the spine of the content strategy or one channel of many?
6. does eggo get a literal public SOUL.md (open-sourced character, community can fork) or internal-only?

---

## 7. next steps (agent-forward)

1. **`SOUL.md` for eggo** — openclaw template format: who eggo is, core truths, vibe, boundaries, continuity. doubles as character bible + generation system prompt
2. **`VISION.md` for newegghead** — openclaw repo-root style: what this is, origin story, principles, tradeoffs
3. **reference corpus:** scrape egghead-brand repo + maggie's dribbble/tumblr archive → every eggo appearance, tagged. add eggo x internal files
4. **`eggo-character` SKILL.md:** character sheet (proportions, expressions, the hands rule, do/don't), pose library w/ metadata — same pattern as the kent/john thumbnail automation. keeps midjourney/flux/qwen pipeline on-model
5. **brand attributes extraction:** voice, values, audience, competitors → vision doc
6. **moodboard pass:** whimsical-adventurous refs (ghibli sidekicks, zelda items, classic cosmic eggo) vs. AI-brand clichés to avoid

---

## sources
- egghead.io/case-studies/john-lindquist · howtoegghead.com case studies
- x.com/johnlindquist · tweets.vercel.fyi (vercel announcement, dec 15 2025)
- dev.build (vision/manifesto, curriculum, instructor bio)
- chatprd.ai "Beyond Vibe Coding" (jan 2026) · lennysnewsletter.com (jan 2026)
- egghead.io workshops: /workshop/claude-code, /workshop/cursor · AI Dev Essentials #1–31
- github.com/eggheadio/egghead-brand · github.com/johnlindquist
- dribbble.com/mappleton ("Voyage to Planet React", "Eggo's Javascript Bling", "Pop Quizzing") · mappleton.tumblr.com ("High Five Fridays" eggos)
- egghead.io/case-studies/maggie-appleton · illustrated.dev coverage
- joelhooks.com (egghead style, bootstrapping posts) · mixergy interview w/ joel hooks
- github.com/openclaw/openclaw (VISION.md, README) · docs.openclaw.ai/reference/templates/SOUL · openclaw SOUL.md ecosystem coverage (medium, blink.new, stack-junkie)
- meeting notes 2026-06-09 (vojta)
