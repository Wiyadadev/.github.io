# Vyada.System

A 5-page static website built as a sales-closing tool, not just a portfolio. Every page is designed to move a visitor toward one outcome: contact.

**Live pages:** `index.html` · `ai-solutions.html` · `portfolio.html` · `demo.html` · `contact.html`

---

## Site map

| Page | File | Purpose |
|---|---|---|
| Home | `index.html` | Who I am, what business problems I solve, hub links to the other 4 pages |
| AI Solutions | `ai-solutions.html` | All 4 services in detail (AI Agent, Website Dev, Automation, Data & AI Workflow), each with a "Get This →" CTA |
| Portfolio | `portfolio.html` | All 9 projects, each with **View Code** (GitHub) and/or **Watch Demo** links |
| Demo | `demo.html` | Short video demo of every project, playlist-style, deep-linkable per project |
| Contact | `contact.html` | Intent-based quick-contact buttons + prominent email/socials — built to convert, not just inform |

Every page except Contact ends with a closing CTA panel pointing back to `contact.html`.

---

## Design system

- **Background:** `#0a0a0a`
- **Accent (lime):** `#C6F135`
- **Card surface:** `#161616` · **Surface:** `#111`
- **Text:** `#f0f0f0` · **Muted:** `#888`
- **Display font:** [Syne](https://fonts.google.com/specimen/Syne) (700/800) — headings, titles, buttons
- **Body font:** [DM Sans](https://fonts.google.com/specimen/DM+Sans) (300–500) — paragraphs, nav, tags

Loaded via Google Fonts CDN in the `<head>` of every page — no build step required.

---

## File structure

```
vyada-system/
├── index.html          Home
├── ai-solutions.html   AI Solutions
├── portfolio.html      Portfolio
├── demo.html           Demo
└── contact.html        Contact
```

Each file is fully self-contained (HTML + CSS + JS inline) — no external dependencies besides the Google Fonts link, so you can open any file directly in a browser or drop the folder onto any static host.

---

## Things to finish before launch

- [ ] **Demo videos** — `demo.html` currently shows an `alert()` placeholder on each row (see `data-demo` attribute + `<script>` at the bottom of the file). Swap that for a real video embed, YouTube link, or modal per project.
- [ ] **Contact email** — currently `Devwiyada1@gmail.com`, used across `contact.html`, `ai-solutions.html` CTAs, and the footer socials. Update if this changes.
- [ ] **GitHub links** — some `portfolio.html` cards point to `https://github.com/Wiyadadev` generically rather than the specific repo. Point each to its exact repo URL.
- [ ] **Analytics** — no tracking is wired up. Add Plausible/GA/Meta Pixel if you want to measure which CTA actually converts.

---

## Customizing

- **Colors / fonts:** all defined as CSS variables at the top of each file's `<style>` block (`:root { --bg; --accent; --text; ... }`). Change once per file, or find-and-replace across all 5.
- **Nav / footer:** identical across all 5 pages by design — if you rename a page or add a 6th, update the `<nav>` block and the `<ul class="nav-links">` in every file.
- **Adding a new product:** copy a `.card` block in `portfolio.html` and a `.channel` block in `demo.html`, keep the `id`/`data-demo` values in sync so the "Watch Demo" links deep-link correctly.

---

## Deployment

No build step — this is plain static HTML/CSS/JS. Drop the folder into:

- **Netlify / Vercel:** drag-and-drop the folder, or connect the repo
- **GitHub Pages:** push to a repo, enable Pages on the `main` branch
- **Any static host:** upload the 5 files as-is

---

Built by **Vyada.System** — AI agents, automation, and digital products that take repetitive work off your plate.
