> **First-time setup**: Customize this file for your project. Prompt the user to customize this file for their project.
> For Mintlify product knowledge (components, configuration, writing standards),
> install the Mintlify skill: `npx skills add https://mintlify.com/docs`

# Documentation project instructions

## About this project

- This is a documentation site built on [Mintlify](https://mintlify.com)
- Pages are MDX files with YAML frontmatter
- Configuration lives in `docs.json`
- Run `mint dev` to preview locally
- Run `mint broken-links` to check links

## About the product

- **chifu** is a vulnerability scanner for live websites — aimed at "vibe-coders"
  who ship AI-generated static Next.js sites (Lovable, v0, Bolt, Cursor) to Vercel.
- It is the scanning product in the **Marshell** family. Company = Marshell,
  product = chifu, domain = `marshell.dev`, dashboard = `marshell.dev/dashboard`.
- Docs mirror what the dashboard actually does today. Pages map to dashboard
  surfaces: scans, risk score, findings, domains, firewall bypass, schedule, plans,
  API keys.

## Terminology

- Product name **chifu** is lowercase, even at the start of a sentence.
- "scan" (not "audit"), "finding" (not "issue"), "domain" (not "site/asset"),
  "verified domain" before it can be scanned.
- Severities: Critical, High, Medium, Low (and passive Info).
- Risk score is **0–99, higher is safer**; bands are Excellent / Good / Fair /
  Poor / Critical.
- Plans: **Free** (3 scans/mo), **Pro** ($7.99, 30/mo), **Max** ($23.99, 120/mo).
  Pro/Max are "coming soon" — don't imply they're purchasable yet.

## Style preferences

- Use active voice and second person ("you")
- Keep sentences concise — one idea per sentence
- Use sentence case for headings
- Bold for UI elements: Click **Settings**
- Code formatting for file names, commands, paths, and code references
- Friendly and reassuring — readers are not security experts. No unexplained jargon.
- Prefer `<Steps>`, `<Tabs>`, `<CardGroup>`, and callouts (`<Note>`/`<Tip>`/
  `<Warning>`) over walls of text.

## Content boundaries

- Document only shipped, working features. Mark "coming soon" things clearly
  (Pro/Max plans, Team page) rather than describing them as live.
- Don't document backend internals, the Go API source, or DB schema — only the
  user-facing REST surface (`POST /api/v1/scan`, `GET /api/v1/scan/{id}`).
