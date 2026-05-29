# Brand Identity

Primary reference for all positioning, messaging, and visual decisions on timbaird.com. Creative choices that conflict with this document should either update it (with rationale) or defer to it.

---

## Purpose of This Site

The site exists to support Tim's transition from education back into active software development. It is a professional credibility document aimed at a single audience: technology hiring managers.

Education and instructional design are part of Tim's history. They are not the destination. The site must not read as the portfolio of an educator who also codes — it must read as the portfolio of a developer who can communicate clearly and has deep, demonstrable technical depth.

---

## Target Audience

**One audience: technology hiring managers.**

### Primary Targets — XRPL and AI/LLM Roles

Companies operating in the XRPL ecosystem (wallets, DEX integrations, token platforms, NFT infrastructure) or building AI/LLM-powered products (agents, RAG pipelines, LLM integrations, AI tooling).

**Who they are.** Often small, remote-friendly, highly technical organisations. The hiring manager is frequently a founding engineer or CTO. They make decisions fast and weight evidence heavily over credentials.

**What they care about.**
- Have you shipped something real in this space — not a tutorial project?
- Do you understand the domain, not just the API surface? (For XRPL: ledger mechanics, multisig, NFT/XLS-20, trustlines. For LLM: embeddings, vector retrieval, prompt architecture, evaluation.)
- Are you active in the ecosystem? Do you have a GitHub that shows it?

**Tim's credibility signals for this audience.**
- XRPL: production integration in FCM — multisig transactions, NFT metadata, wallet management interface. Not a demo; running on fcmud.world.
- AI/LLM: OpenRouter and OpenAI API integration in FCM, embeddings stored in vector databases, LLM test-bot harness for automated game dialogue testing.
- Architecture: horizontal scaling of Evennia's single-threaded Twisted Reactor across multiple instances — a non-trivial distributed systems problem solved from first principles.
- All of it is live, ongoing, and on GitHub.

---

### Secondary Targets — Stepping-Stone Roles

**Solidity / EVM / broader crypto.** Tim has Solidity experience (smart contracts) from personal projects. Not as deep as XRPL, but genuine. Relevant for Web3 generalist roles.

**Senior development / architecture roles.** Python-focused or stack-agnostic senior developer positions at companies that value decoupled architecture, clean library design, and technical depth. The 10+ years of teaching programming (Swinburne, Kangan) is reframed here as evidence of mastery — you truly understand something when you can teach it rigorously, over years, to students who will probe every assumption.

---

### How Visitors Arrive

Primarily via a direct link in a cover letter or resume. They know Tim's name. They are checking whether the site confirms or complicates the impression formed from the resume. They are not landing from a Google search.

First impression window: **under 30 seconds**. In that time they need to see: real technical work, specific technologies, live evidence. Then they will decide whether to keep reading or click away.

---

## Core Message

**Tim is a senior developer with production experience in XRPL and AI/LLM systems, strong Python and architecture depth, and the communication skills of a decade-long educator.**

The teaching history is not a detour — it is evidence of mastery and a differentiator. A developer who can explain layered architecture clearly, write documentation that actually works, and mentor juniors without hand-holding is rare. The decade in education is what produces that.

But the teaching is supporting evidence. The lead is the technical work.

**Expressed directly:** *"I build real, production systems — currently in XRPL and AI/LLM. I've been doing it since 2022, and the code is live."*

---

## Communication Principles

1. **Lead with the work, not the bio.** FCM and its live URL (fcmud.world) should appear early. Links to GitHub repos before lengthy prose.
2. **Specifics over generics.** "Engineered horizontal scaling of Evennia's single-threaded Twisted Reactor across multiple instances" is better than "experienced in distributed systems."
3. **The teaching is framed for a developer audience.** Not "I was a VET teacher." More like: "I spent seven years teaching database design and software architecture at Swinburne — which is where you really learn whether you understand something."
4. **The 2022–present period is a strength.** FCM has been running since 2022. The fact that teaching work continued alongside it is context; the FCM work is the story.
5. **Short, scannable prose.** Hiring managers in crypto/AI move fast. No walls of text.
6. **Australian English.** Colour, licence, practitioner. Melbourne professional.

---

## Visual Identity

### Typography

**Recommendation: Inter + JetBrains Mono**

- **Body and UI: Inter** — humanist sans-serif, highly legible at all sizes, standard in developer and technical product contexts. Zero friction.
- **Code and technical accents: JetBrains Mono** — used sparingly for role titles, skill tags, or inline technical references. Signals developer identity without being heavy-handed.
- **Type scale:** Large, confident heading hierarchy. The design is typographic — this is not a photography portfolio. Whitespace and type scale carry the visual weight.

---

### Colour

**Dark palette — decided.**

| Role | Value |
|---|---|
| Background | `#0f1117` |
| Surface | `#18191f` |
| Body text | `#e8eaed` |
| Accent | `#14b8a6` (teal) — decided |
| Accent hover | `#2dd4bf` |
| Muted | `#6b7280` |

Appropriate for the primary target audience (XRPL / AI / crypto). Execution quality is the differentiator.

---

### Layout Principles

1. **Single column, content width ~720–760px.** Scannable on laptops and phones.
2. **Typography-led.** No hero photography, no decorative illustration. Whitespace and hierarchy are the design.
3. **Mobile-first.** Recruiter and hiring manager links frequently opened on phones.
4. **Hierarchy through scale and weight, not colour.** Accent used for one or two emphasis points per section — not decoration.
5. **No unnecessary motion.** No parallax, hero animations, scroll-triggered theatrics. Subtle hover states acceptable. Speed and clarity over visual interest.
6. **Accessible contrast.** WCAG AA minimum. Fast load — static output, minimal JS.

---

### Imagery

**No decorative imagery on the page itself.** No hero photography, no project screenshots, no illustration. Visual interest comes from type scale, weight, and whitespace.

Functional exceptions:

- **OG image — included.** A typographic Open Graph image (name + tagline rendered in Inter / JetBrains Mono on the brand-dark background) so link previews in Slack, email, and LinkedIn render coherently. Does not appear on the page itself; only in shared link previews.
- **Headshot — excluded.** Conflicts with the typography-led aesthetic. LinkedIn already serves the "face to the name" function for this audience.
- **Project screenshots — excluded.** FCM is text-based and would not visualise well at portfolio scale. Prose description plus the live link to `fcmud.world` is the stronger evidence.
- **Hero code block — optional.** A small JetBrains Mono snippet (e.g., a 4-line Python function) is on-brand and reads as confident rather than decorative. Use only if it strengthens the hero. Final call deferred to the build phase.

---

## Voice and Tone

- **Confident, not boastful.** Let specifics do the work. Evidence before claims.
- **Technical vocabulary used naturally.** Not a keyword list — vocabulary in context.
- **Direct.** First person, active voice. "I built" not "was responsible for building."
- **Not apologetic about the career arc.** The Navy → Mac support → education → FCM trajectory signals: disciplined, varied, self-directed. Not a liability.

---

## Content Scope

*(Pending decisions — to be captured in a separate content-plan document once agreed.)*

- **Structure: single-scroll page with sticky anchor-linked nav — decided.** One URL, controlled reading order, right-sized for the content. Multi-page can be added later if a blog is introduced (individual post URLs require it). Not a JS SPA — static HTML with sections and anchor links.
- Education history: one sentence in the bio, framed as mastery evidence — e.g. "Seven years teaching architecture and databases at Swinburne" signals depth to a developer audience. Full history lives in the resume PDF only.
- Blog / writing section — only if Tim will actively maintain it. A neglected blog hurts more than it helps.
- **Contact method — decided (reversed 2026-05-29).** GHL-embedded contact form in the Contact section; no public email, no public resume download. The primary website visitor already has the resume (and Tim's direct email and phone) from a job application — the form serves only cold inbound. Tim sends the resume in response to legitimate enquiries via the form. Public resume download was removed because the PDF contains referees' direct phone/email — a third-party privacy issue beyond Tim's own scraping concern. Schema.org `Person` `email` field also removed from the page JSON-LD to close the same leak. Framing on the page: "Resume and referees available on request. Direct details stay off the public page — Nigerian princes don't fill out forms."

---

## Client Portal Link

A second visitor type exists alongside hiring managers: Tim's existing clients, who arrive at timbaird.com to access the GHL (Go High Level) instance at `app.timbaird.com`.

They are **not** a design target — the site is not built for them. But the site must not confuse or block them.

**Decision:** A persistent link to `app.timbaird.com` in the top-right of the sticky nav bar. Visually distinct from the primary nav links — a small, muted pill or bordered button labelled **"Client Login"** (or similar). Clients who know it's there will find it immediately. Hiring managers will register it as a "login" affordance and ignore it — a signal that Tim has active clients, not a distraction.

This link must survive any redesign. It is a functional requirement, not a design flourish.

---

## Hosting and DNS

**Cloudflare — decided.** Both DNS and static hosting via Cloudflare Pages (free tier). Implications:

- **Stack: Astro — decided.** Outputs pure static HTML by default, first-class Cloudflare Pages support, Tim has prior experience with it.
- `app.timbaird.com` is already a subdomain on Cloudflare DNS — no additional DNS config needed for the client portal link.
- Cloudflare Pages provides free SSL, global CDN, and preview deployments on push — no additional infrastructure needed.

---

## SEO and Discoverability

Goal is branded search only — "Tim Baird developer", "Tim Baird XRPL", "Timothy Baird Melbourne." Minimum required:

- `<title>` and `<meta description>` tuned to developer / XRPL / AI identity.
- Schema.org `Person` structured data.
- Open Graph tags for link previews in Slack / email.
- Canonical URL: `https://timbaird.com`.

## Analytics

Recommendation: none, or privacy-respecting minimal analytics (Plausible — no cookies, no GDPR complexity). Knowing visitor counts adds no actionable information for a job-application site.
