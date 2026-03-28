<p align="center">
  <img src="https://reffo.ai/gitLogo.png" alt="Reffo" width="280" />
</p>

<p align="center">
  The open-source protocol for decentralized commerce.
</p>

<p align="center">
  <a href="https://reffo.ai">Website</a> &middot;
  <a href="https://reffo.ai/about">About</a> &middot;
  <a href="https://github.com/ReffoAI/reffo-beacon/releases">Download Beacon</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/protocol-CC0--1.0-green" alt="Protocol License" />
  <img src="https://img.shields.io/github/license/ReffoAI/reffo-beacon" alt="Beacon License" />
  <img src="https://img.shields.io/github/stars/ReffoAI/reffo-beacon?style=flat" alt="GitHub Stars" />
</p>

---

## What is Reffo?

Today's online marketplaces charge sellers 10-20% in fees, harvest your data, and dictate what you can sell. Reffo is the alternative: an **open protocol** that lets anyone trade directly with anyone else — no platform taking a cut.

Think of it like email for commerce. Anyone can run a node, anyone can trade with anyone, regardless of provider.

<img width="1057" height="780" alt="image" src="https://github.com/user-attachments/assets/fd46c1a9-ec88-42cc-bf51-aedd12e42cad" />


## How it works

1. **Run a beacon** — Download the app or run `npx create-reffo-beacon`. Your beacon is your personal storefront on the open network.
2. **List your items** — Products, rentals, services, things to trade. Your inventory, your rules.
3. **Trade directly** — Buyers discover your items through search, send offers, and you negotiate peer-to-peer.

## Repositories

| Repo | Description | License |
|------|-------------|---------|
| [reffo-protocol](https://github.com/ReffoAI/reffo-protocol) | Shared type system, Schema.org extensions, and category schemas that let beacons speak the same language. | CC0-1.0 |
| [reffo-beacon](https://github.com/ReffoAI/reffo-beacon) | Self-hosted inventory server. SQLite database, Express API, Hyperswarm DHT peer discovery. | AGPL-3.0 |
| [reffo-webapp](https://github.com/ReffoAI/reffo-webapp) | Search and discovery layer at [reffo.ai](https://reffo.ai). Next.js, React, Supabase. | Proprietary |
| [create-reffo-beacon](https://github.com/ReffoAI/create-reffo-beacon) | One-command scaffold: `npx create-reffo-beacon` — sets up a beacon project in seconds. | AGPL-3.0 |

## Get started

### Set up with npm

```bash
npx create-reffo-beacon
cd my-reffo-beacon
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) — your beacon is live.

### Download a prebuilt bundle

Grab the latest release from [reffo-beacon/releases](https://github.com/ReffoAI/reffo-beacon/releases) — extract, double-click, done. Includes an embedded Node.js runtime so nothing else is needed.

### Connect to Reffo.ai (optional)

Generate an API key at [reffo.ai/account](https://reffo.ai/account) and paste it into your beacon's Settings page. This syncs your listings to the Reffo.ai discovery network. It's entirely optional — your beacon works independently without it.

## Architecture

```
┌──────────────────────────────────────────────┐
│           @reffo/protocol (CC0)              │
│        Shared types, schemas, utilities       │
└────────────┬─────────────────┬───────────────┘
             │                 │
     ┌───────▼───────┐ ┌──────▼──────┐
     │  reffo-beacon │ │ reffo-webapp │
     │  Self-hosted  │ │  Discovery   │
     │  Express +    │ │  Next.js +   │
     │  SQLite +     │ │  Supabase    │
     │  Hyperswarm   │ │              │
     └───────┬───────┘ └──────────────┘
             │
             ▼
     Hyperswarm DHT
     (peer-to-peer network)
```

## Principles

- The protocol, beacon, and core tooling are **free and open source** — always.
- Peer-to-peer trading will **never** require a Reffo.ai account or fee.
- Optional Reffo.ai services (API, managed integrations, enhanced search) are **always opt-in**.
- We will never insert ourselves into transactions between independent beacons.

## Status

Reffo is in early alpha. Star the repos to follow progress.

## Contributing

We welcome contributions to all Reffo projects. See our [Contributing Guide](https://github.com/ReffoAI/.github/blob/main/CONTRIBUTING.md) and [Code of Conduct](https://github.com/ReffoAI/.github/blob/main/CODE_OF_CONDUCT.md).

## License

Each project is licensed independently — see the table above. The protocol is CC0 (public domain). The beacon and CLI are AGPL-3.0. The webapp is proprietary.
