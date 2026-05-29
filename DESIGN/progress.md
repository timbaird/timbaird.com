# Progress

Running log of project milestones with links to supporting evidence where appropriate. Coarse-grained — meaningful project state changes, not commit-level detail. Most recent entries at the top.

## 2026-05-29 — Repo history scrubbed of resume `.docx`

Surgically removed `DESIGN/archive/RESUME_2026_05_28.docx` from all git history via `git filter-repo`, then force-pushed. The file carried referees' direct contact details (third-party privacy concern); removing it only from current HEAD would have left it reachable via GitHub raw URLs at older commit SHAs. After this rewrite, the file is gone from every commit in the public repo. Tim retains a working copy outside the repo. CLAUDE.md §9 (Repository layout) updated to reflect the empty `archive/`.

## 2026-05-29 — Pre-launch polish: OG image, doc consistency, CLAUDE.md fill-ins

Generated the typographic OG image (`public/og-image.png`) by rendering `og-template.html` via headless Chrome at 1200×630. Wired `og:image`, dimensions, alt text, and `twitter:image` meta tags in `index.astro` so link previews in Slack, email, and LinkedIn render coherently. Filled in CLAUDE.md §9 (Repository layout) and updated §10 (Tools and environment) — both had been minimal/stale since the doc skeleton was first laid down. Reconciled brand-identity.md with the site copy: three lingering "since 2022" / "software architecture" framings updated to match the honest framing we landed on for the live page.

## 2026-05-29 — Site live at timbaird.com

Deployed to Cloudflare Pages (project `timbaird-com`) and DNS pointed at the production URL via the Pages "Custom domains" UI (apex `timbaird.com`, CF handles the CNAME flattening and SSL automatically). DNS propagated quickly. First public-facing version of the site is live.

## 2026-05-29 — Resume files cleared from repo

Closes out the open follow-up from the resume-on-request decision: `public/tim-baird-resume.pdf` deleted, and the verbatim markdown transcription `archive/RESUME_2026_05_28.md` also deleted. Both files carried the same third-party privacy exposure (referees' direct phone and email). The `.docx` source remains in `archive/` as Tim's working copy — never linked from the site and never served by Astro. INDEX.md updated to drop the stale transcription entry.

## 2026-05-29 — Custom favicon added

Replaced the default Astro favicon (`favicon.ico` + `favicon.svg`) with Tim's branded version.

## 2026-05-29 — Footer year made dynamic

Footer copyright year now computed at build time via `new Date().getFullYear()` rather than hardcoded. Each fresh build picks up the current year.

## 2026-05-29 — Public resume download removed; resume + referees on request

Removed the "Download resume (PDF)" button from the Contact section. The PDF contains Tim's direct phone, full work history detail, *and* two referees' direct contact details (phone, email) — publishing it on a public page exposed third-party contact details, a privacy breach beyond Tim's own information. New framing: "Resume and referees available on request" — Tim sends the PDF in response to legitimate form enquiries. Schema.org `Person.email` field also removed from the JSON-LD in the page head (same scraper leak). [brand-identity.md](brand-identity.md) updated to document the rationale.

**Open follow-up:** the file `public/tim-baird-resume.pdf` is still served at `https://timbaird.com/tim-baird-resume.pdf` even though it's no longer linked. Needs to be moved out of `public/` (to `DESIGN/archive/` alongside the `.docx`, or `.gitignore`'d entirely if the GitHub repo is public) before deployment.

## 2026-05-29 — Contact strategy reversed; GHL form integrated

Public mailto link removed; replaced by a GHL-embedded contact form in the Contact section. Rationale: the primary website visitor is someone who has received the resume from a job application and *already has* Tim's direct email and phone — the form serves only cold/unsolicited inbound. Privacy from scraping + automated acknowledgement outweigh the original "mailto only" stance. Contact section restructured: lede → resume-first intro → resume download button → form embed → humour note. Hero "Get in touch" CTA now scrolls to `#contact` instead of opening mailto. Both [CLAUDE.md §6](../CLAUDE.md) (Out of scope) and [brand-identity.md](brand-identity.md) updated to document the reversal.

## 2026-05-28 — Site v1 built

Full single-scroll page implemented in [src/pages/index.astro](../src/pages/index.astro): hero, about, featured FCM, other work, tech stack, contact. Sticky nav with Client Login button (top-right). Dark palette, Inter + JetBrains Mono via Google Fonts. Content iterated across the session for honest framing — FCM tagged "Ongoing" rather than "2022 – Present"; teaching framed as concurrent ("in addition to technical work") rather than chronological; "software engineering" terminology; remote-only + globally mobile positioning; Solidity work credited as OpenZeppelin-based contracts deployed on Polygon. Tech Stack section opens with a first-principles framing line. Resume PDF placed at [public/tim-baird-resume.pdf](../public/tim-baird-resume.pdf).

## 2026-05-28 — Accent colour: teal

`#14b8a6` selected as the brand accent. May be revisited during build. Recorded in [brand-identity.md](brand-identity.md).

## 2026-05-28 — Imagery decisions captured

`Visual Identity → Imagery` subsection added to [brand-identity.md](brand-identity.md). Decisions: typographic OG image included; headshot, project screenshots excluded; hero code block optional (build-phase call).

## 2026-05-28 — Project scaffolded

Astro 6 minimal template scaffolded into project root. TypeScript strict mode. Node 22 required (nvm). Dev server: `npm run dev` → `localhost:4321`. CLAUDE.md §9 (repo layout) and §10 (tools/env) populated with real structure. `package.json` name corrected from scaffolder default to `timbaird-com`.

## 2026-05-28 — Stack confirmed: Astro

Astro selected as the build framework. Static output, first-class Cloudflare Pages support, prior familiarity. Unlocks: CLAUDE.md §9 (repo layout) and §10 (tools/env), and project scaffolding.

## 2026-05-28 — Architecture and hosting decisions confirmed

- **Structure:** single-scroll page, sticky anchor-linked nav (not a JS SPA).
- **Hosting/DNS:** Cloudflare Pages (free) + Cloudflare DNS. `app.timbaird.com` already on CF DNS.
- **Client portal link:** persistent link to `app.timbaird.com` top-right of nav, muted "Client Login" button — functional requirement, not optional.
- **Colour:** dark palette (`#0f1117`) confirmed. Accent (blue vs teal) still TBD.
- **Education on site:** one sentence in bio as mastery evidence; full history in resume PDF only.

## 2026-05-28 — Brand identity drafted

[brand-identity.md](brand-identity.md) created. Single audience (tech hiring managers), primary targets XRPL and AI/LLM roles, secondary stepping-stone targets (Solidity/EVM, general architecture). Teaching history reframed as evidence of depth, not lead identity. Colour palette pending Tim's decision (two options presented). Indexed in INDEX.md.

## 2026-05-28 — Resume transcribed to markdown

[archive/RESUME_2026_05_28.md](archive/RESUME_2026_05_28.md) created as a verbatim pandoc conversion of the `.docx` resume. All content preserved; header and referees sections render as HTML tables (Word two-column layout — not auto-convertible to pipe tables). No word changes made.

## 2026-05-28 — Licence decided

All rights reserved (proprietary stance; no `LICENSE` file shipped — the absence is intentional). Captured in [CLAUDE.md §7.4](../CLAUDE.md). Template's SPDX-header convention dropped, as SPDX is for open-source identification.

## 2026-05-28 — Project initialised

Repository skeleton in place under `timbaird.com/`:

- `README.md` stub.
- `DESIGN/` with `INDEX.md`, `documentation-structure.md`, and `archive/RESUME_2026_05_28.docx` (substrate material — the updated resume the site must stay consistent with).

[CLAUDE.md](../CLAUDE.md), [INDEX.md](INDEX.md), and [documentation-structure.md](documentation-structure.md) drafted iteratively from the `evennia-mob-spawner` project template:

- CLAUDE.md sections 1 (title), 2 (What this project is), 3 (Project status), 4 (Where to read first), and 7 (Working conventions — less the licence sub-bullet) populated. Section 5 retained as a header + preamble only, awaiting principles to be derived from actual design decisions. Remaining sections marked `[TBD]` and pending discussion.
- INDEX.md rewritten to reflect actual contents (process docs only, empty architecture/design section, the archived resume).
- documentation-structure.md lightly scrubbed of library-flavoured phrasings (status terminology, "install or try it", "supported deployment shapes").
