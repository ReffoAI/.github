<p align="center">
  <img src="https://reffo.ai/favicon.ico" width="64" height="64" alt="Reffo" />
</p>

<h1 align="center">Reffo</h1>

<p align="center">
  <strong>Open-source protocol for decentralized commerce.</strong><br />
  Buy, sell, trade, rent, and share — peer-to-peer, no middleman, no predatory fees.
</p>

<p align="center">
  <a href="https://reffo.ai">Website</a> &nbsp;&middot;&nbsp;
  <a href="https://reffo.ai/about">About</a> &nbsp;&middot;&nbsp;
  <a href="https://reffo.ai/download">Download Beacon</a>
</p>

---

## What is Reffo?

Today's online marketplaces charge sellers 10–20% in fees, harvest your data, and dictate what you can and can't sell. Reffo is the alternative: an **open protocol** that lets anyone trade directly with anyone else — no platform taking a cut.

Think of it like email for commerce. Anyone can run a node, anyone can trade with anyone, regardless of provider.

### How it works

1. **Run a beacon** — Download the app or run `npx create-reffo-beacon`. Your beacon is your personal storefront on the open network.
2. **List your items** — Products, rentals, services, things to trade. Your inventory, your rules.
3. **Trade directly** — Buyers discover your items through search, send offers, and you negotiate peer-to-peer.

## Repositories

| Repo | Description | License |
|------|-------------|---------|
| [`reffo-protocol`](https://github.com/ReffoAI/reffo-protocol) | Shared type system, Schema.org extensions, and category schemas that let beacons speak the same language. | CC0-1.0 |
| [`reffo-beacon`](https://github.com/ReffoAI/reffo-beacon) | Self-hosted inventory server. SQLite database, Express API, Hyperswarm DHT peer discovery. | MIT |
| [`reffo-webapp`](https://github.com/ReffoAI/reffo-webapp) | Search and discovery layer at [reffo.ai](https://reffo.ai). Next.js, React, Supabase. | MIT |
| [`create-reffo-beacon`](https://github.com/ReffoAI/create-reffo-beacon) | One-command scaffold: `npx create-reffo-beacon` — sets up a beacon project in seconds. | MIT |

## Get Started

### Run a beacon locally (no install required)

Download a prebuilt bundle from the [latest release](https://github.com/ReffoAI/reffo-beacon/releases) — extract, double-click, done. Includes an embedded Node.js runtime so nothing else is needed.

### Set up with npm

```bash
npx create-reffo-beacon
cd my-reffo-beacon
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) — your beacon is live.

### Connect to Reffo.ai (optional)

Generate an API key at [reffo.ai/account](https://reffo.ai/account) and add it to your beacon's `.env` file. This syncs your listings to the Reffo.ai discovery network. It's entirely optional — your beacon works independently without it.

## Architecture

```
┌──────────────────────────────────────────────┐
│        @reffo/protocol (CC0 — public domain) │
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

## Our Promise

- The protocol, beacon, and core tooling are **free and open source** — always.
- Peer-to-peer trading will **never** require a Reffo.ai account or fee.
- Optional Reffo.ai services (API, managed integrations, enhanced search) are **always opt-in**.
- We will never insert ourselves into transactions between independent beacons.

## Contributing

We welcome contributions to all Reffo projects. See our [Contributing Guide](https://github.com/ReffoAI/.github/blob/main/CONTRIBUTING.md) and [Code of Conduct](https://github.com/ReffoAI/.github/blob/main/CODE_OF_CONDUCT.md).

## License

Each project is licensed independently — see the table above. The protocol is CC0 (public domain). Application code is MIT.
