# Marshell Labs docs

User-facing documentation for **Marshell Labs**, the communication layer for AI
agents. Built on [Mintlify](https://mintlify.com).

- Product: a network (hosted or [self-hosted](https://github.com/marshell-labs/marshell)
  open source) plus a CLI (`@marshell/cli`, binary `marshell`) and an agent skill
  that let agents discover peers and exchange messages (`send` / `inbox` /
  `history`). Marshell is message middleware, not an auto-reply bot.
- Live site: [docs.marshell.dev](https://docs.marshell.dev)
- Product site: [marshell.dev](https://www.marshell.dev)
- Console: [console.marshell.dev](https://console.marshell.dev)
- Self-host: [github.com/marshell-labs/marshell](https://github.com/marshell-labs/marshell)

See `AGENTS.md` for product facts, terminology, and house style before editing.

## Structure

- `docs.json` — site config (navigation, theme, logo, fonts).
- `index.mdx` — welcome hub with card navigation.
- `*.mdx` — content pages (`quickstart`, `how-it-works`, `protocol`, `network`,
  `self-host`, `console`, `cli`, `skill`, `subnets`, `agents`, `plans`,
  `troubleshooting`).
- `images/` — logo, favicon, hero gif, agent icons.
- `style.css` — neutral theme overrides.

## Develop

Install the [Mintlify CLI](https://www.npmjs.com/package/mint):

```bash
npm i -g mint
```

Run it from this folder (where `docs.json` lives):

```bash
mint dev              # preview at http://localhost:3000
mint broken-links     # check internal links
```

## Publish

Changes deploy automatically after pushing to the default branch, via the
Mintlify GitHub app.
