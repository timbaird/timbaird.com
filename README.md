# timbaird.com

Personal website of Tim Baird — software developer working in XRPL and AI/LLM. Live at [timbaird.com](https://timbaird.com) (once deployed).

## What this is

A single-scroll personal portfolio site built to support job applications. The resume is canonical; the site presents technical work and positioning to hiring managers — primarily for remote XRPL and AI/LLM engineering roles.

## Status

In active development. Initial single-page build complete; Cloudflare Pages deployment pending. Content and visual polish still in progress.

## Built with

- [Astro](https://astro.build/) — static site framework
- TypeScript (strict mode)
- Inter and JetBrains Mono via Google Fonts
- Cloudflare Pages (hosting) + Cloudflare DNS

## Running locally

Requires Node.js 22+ (managed via nvm):

```bash
nvm use 22
npm install
npm run dev
```

Dev server runs at `http://localhost:4321`. Hot reload on save.

## Project structure

- [`src/pages/index.astro`](src/pages/index.astro) — the entire single-scroll page
- [`public/`](public/) — static assets copied verbatim to the build output (favicon, resume PDF)
- [`DESIGN/`](DESIGN/INDEX.md) — design wiki: brand identity, documentation conventions, progress log, archived substrate

For design decisions and rationale, start at [`DESIGN/INDEX.md`](DESIGN/INDEX.md). For LLM-agent context when working in this repo, see [`CLAUDE.md`](CLAUDE.md).

## Licence

All rights reserved. © Tim Baird. No permission is granted to copy, modify, redistribute, or reuse any code or content from this repository without explicit written consent. See [`CLAUDE.md`](CLAUDE.md) §7.4 for the full statement.
