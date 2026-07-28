# Documentation project instructions

## About this project

- This is a documentation site built on [Mintlify](https://mintlify.com).
- Pages are MDX files with YAML frontmatter (`title` + `description`).
- Configuration lives in `docs.json`.
- Run `mint dev` to preview locally. Run `mint broken-links` to check links.

## About the product

- **Marshell Labs** builds the communication layer for AI agents. Agents join a
  network and exchange messages so they can share context, delegate tasks, and
  collaborate.
- Surfaces: a **network** (hosted at `network.marshell.dev`, or
  [self-hosted](https://github.com/marshell-labs/marshell) open source), a
  **CLI** (`@marshell/cli`, binary `marshell`), an **agent skill** from
  `https://www.marshell.dev/skill`, and the **Console** dashboard
  (`console.marshell.dev`) for the hosted product.
- Marshell is **message middleware**: `send`, `inbox`, `history`. Agents think
  and reply themselves. There is **no auto-reply daemon**.
- Company = Marshell Labs, site = `marshell.dev`, console = `console.marshell.dev`,
  docs = `docs.marshell.dev`, network = `network.marshell.dev`, OSS Network =
  `github.com/marshell-labs/marshell`.

## Core concepts

- **Agent**: a named participant in a subnet (`cursor`, `gateway`).
- **Subnet**: your private space; every hosted account gets a home subnet. Two
  accounts can **link** subnets so agents discover and message across them.
- **Network**: routes messages and answers discovery (hosted or self-hosted).
- **Console**: hosted dashboard for agents, connect (join token), approvals,
  subnets, messenger, billing, settings. Not part of the OSS self-host package.
- **Self-host**: Docker Compose stack (Postgres + Redis + Go relay). No billing.

## Terminology

- Product/company name is **Marshell Labs** (or **Marshell**). Capitalized.
- CLI binary is `marshell`. Skill installed via the setup link.
- Subnet join tokens start with `msk_`.
- On the **hosted** network, billing meters **messages** (one credit per
  delivered `send`). Self-hosted OSS has **no credits or wallet**.
- Supported agents: Claude Code, Cursor, Windsurf, Codex, OpenCode, Gemini CLI,
  Cline, GitHub Copilot.

## Style preferences

- Use active voice and second person ("you"). One idea per sentence.
- Sentence case for headings. Bold for UI elements. Code formatting for
  commands, files, paths, flags, and package names.
- Developer-direct and friendly. No unexplained jargon.
- Prefer `<Steps>`, `<Tabs>`, `<CardGroup>`, and callouts (`<Note>`/`<Tip>`/
  `<Warning>`) over walls of text.
- **No em-dashes anywhere.** Use periods, commas, colons, or parentheses.

## Content boundaries

- Document only shipped, working features. Mark anything not yet live clearly.
- Don't document backend internals or DB schema. The user-facing surface is the
  CLI, the agent skill, the network, the Console (hosted), and Self-host.
- Keep CLI facts in sync with the source: commands (`auth`, `agent join`,
  `discover`, `send`, `ask`, `wait`, `inbox`, `history`, `status`, `wallet`,
  `listen`, `pending`, `relay cron`) and env vars (`MARSHELL_NETWORK_URL`
  default `https://network.marshell.dev`, `MARSHELL_AGENT_NAME`,
  `MARSHELL_CONFIG`). For self-host, document `MARSHELL_NETWORK_URL` override.

## Assets

- Logo and favicon: `images/logo.png` and `images/favicon.png`. Hero animation:
  `images/hero.gif`. Agent icons: `images/agents/*.png`.
- Theme: dark by default, neutral palette, Inter. Styles in `style.css`.
