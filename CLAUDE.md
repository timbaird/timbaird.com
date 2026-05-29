# CLAUDE.md

Instructions for Claude (and other LLM agents) working in this repository.

## What this project is

`timbaird.com` is the personal website of Tim Baird, built to accompany his recently-updated resume and support job applications. Tagline: **"Resume-aligned personal website for job applications."**

The site exists downstream of the resume: the resume is the canonical statement of Tim's professional positioning, and the site presents that material — and any supporting context — to visitors, primarily hiring managers and recruiters who arrive via job applications, and secondarily anyone landing on the domain organically.

Specifics on stack, hosting, content scope, audience beyond hiring managers, and tone are open decisions and will be captured in `DESIGN/` as they're made.

For the big-picture overview, read [README.md](README.md).
For the design wiki, read [DESIGN/INDEX.md](DESIGN/INDEX.md).

## Project status

For the current state of the project — milestones reached, what's pending — see [DESIGN/progress.md](DESIGN/progress.md), the running log of milestones with links to evidence.

## Where to read first

For any non-trivial task, start by reading in this order:

1. [README.md](README.md) — what the project is, status, quick start.
2. [DESIGN/INDEX.md](DESIGN/INDEX.md) — map of all design docs.
3. [DESIGN/documentation-structure.md](DESIGN/documentation-structure.md) — what goes in CLAUDE.md vs README.md vs DESIGN/, and naming conventions.

## Load-bearing architectural principles

These are the principles every implementation decision must respect. Getting them wrong is expensive to undo.

[TBD — principles will be captured here as architectural decisions are made and agreed.]

## Out of scope

Scope boundaries below reflect decisions already made. Do not add features in these categories without an explicit conversation and a update to this file.

- **Server-side code and APIs.** The site is static Astro output deployed to Cloudflare Pages. Any dynamic backend behaviour lives at `app.timbaird.com`, not here.
- ~~**Contact form with backend.**~~ **Reversed 2026-05-29** — GHL-embedded contact form now lives in the Contact section. Privacy from public email scraping + automated acknowledgement outweighed the simplicity of mailto, particularly given the primary visitor already has Tim's direct details on the resume PDF. See [DESIGN/brand-identity.md](DESIGN/brand-identity.md) for full rationale.
- **Authentication or gated content.** The client portal is at `app.timbaird.com`. Nothing on `timbaird.com` requires a login.
- **Dark/light mode toggle.** Dark palette is the decided visual identity. A toggle adds complexity and dilutes it.
- **JS-heavy animations and effects.** Parallax, canvas, three.js, scroll-triggered theatrics — all excluded. Conflicts with the layout principle of speed and no unnecessary motion.

**Deferred (not permanently excluded):**

- **Blog.** Out of scope for this build. Astro's content collections pattern means it can be added later without touching the existing site structure. Add it when there is a concrete plan to maintain it — a neglected blog is worse than no blog.

## Working conventions

- **Editing design docs.** Update or add design documents whenever an architectural decision is made or refined. Capture the *why*, not just the *what*. Index new docs in [DESIGN/INDEX.md](DESIGN/INDEX.md).
- **CLAUDE.md vs README.md vs DESIGN/.** See [DESIGN/documentation-structure.md](DESIGN/documentation-structure.md) for the split. CLAUDE.md is for Claude-facing instructions; README.md is for humans landing on the repo; DESIGN/ is the technical wiki.
- **Don't put implementation detail in this file or README.** Link out to DESIGN/ instead. Keep CLAUDE.md and README.md stable; let DESIGN/ churn.
- **Licence.** All rights reserved. © Tim Baird. No `LICENSE` file is shipped — the absence is intentional, not an oversight. No permission is granted to copy, modify, redistribute, or reuse any code or content from this repository without explicit written consent. Source files do not carry SPDX headers.

## Documentation discipline (load-bearing)

Design documents in `DESIGN/` must reflect decisions **actually discussed and agreed on with the project owner**. They are not a place to forward-design the system from first principles or extrapolate "reasonable defaults" from a starting point.

**Rules:**

1. **Only capture what was discussed and agreed.** If the conversation establishes a principle, do not extrapolate it into specifics that were not raised.
2. **Flag open questions explicitly.** Where a topic has been raised but not resolved, write `[TBD — needs discussion: <what is open>]` in the doc. Future sessions then pick the topic up deliberately rather than inheriting unagreed assumptions.
3. **Distinguish archived material from in-conversation decisions.** Material in `DESIGN/archive/` is preserved historical context, not authoritative. Restating archived content in new docs is acceptable when it provides necessary context, but mark it as such rather than presenting it as a decision freshly made or as canonical project intent.
4. **Smaller is better.** A doc that captures three discussed points faithfully is more useful than one that captures three discussed points plus seven invented ones. Resist the urge to fill out sections "for completeness."

If a session catches itself writing content that goes beyond what was discussed, stop and either remove the extrapolation or convert it to a `[TBD]` marker. Documentation that puts unagreed decisions in the project's mouth is worse than documentation that has gaps.

## Repository layout

```
timbaird.com/
├── CLAUDE.md
├── README.md
├── .gitignore
├── astro.config.mjs        # Astro build configuration
├── package.json
├── package-lock.json
├── tsconfig.json
├── DESIGN/                 # technical wiki (humans + agents)
│   ├── INDEX.md
│   ├── brand-identity.md
│   ├── documentation-structure.md
│   ├── progress.md
│   └── archive/            # substrate material and historical context
│       ├── RESUME_2026_05_28.docx
│       └── RESUME_2026_05_28.md
├── public/                 # static assets copied verbatim to dist/
│   └── favicon.svg
└── src/
    └── pages/
        └── index.astro     # single-scroll home page — the entire site
```

## Tools and environment

- **Node.js 22+** — required by Astro 6. Managed via nvm. Before running any npm commands in a new shell: `source ~/.nvm/nvm.sh && nvm use 22`.
- **npm** — package manager. No pnpm or yarn.
- **Astro 6** — static site framework. Outputs pure static HTML to `dist/`.
- **TypeScript** — strict mode. Frontmatter in `.astro` files and any `.ts` files are type-checked.
- **Dev server:** `npm run dev` — starts at `http://localhost:4321`. Hot-reload on save.
- **Build:** `npm run build` — outputs static site to `dist/`.
- **Preview:** `npm run preview` — serves the built `dist/` locally for pre-deploy testing.
- **Deployment:** Cloudflare Pages. Build command: `npm run build`. Output directory: `dist`. Deploys on push to the production branch.
