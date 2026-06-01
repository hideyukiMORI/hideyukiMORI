# Hideyuki Mori — OSS

**Convention-visible JSON APIs** for humans and AI agents — one design language across PHP, Python, and Node, plus self-hosted products you can ship on shared hosting or Docker.

**Hub:** [nene2.dev](https://nene2.dev) · **Strategy:** [publication-strategy](https://github.com/hideyukiMORI/publication-strategy) · **Contact:** [ayane.co.jp](https://ayane.co.jp/)

*Last updated: 2026-06-02 — profile README synced to public repo state.*

---

## What shipped recently (June 2026)

| Area | Highlight |
| --- | --- |
| **NENE2** | [v1.5.329](https://github.com/hideyukiMORI/NENE2/releases) — 349 field trials covered; OpenAPI author + howto library |
| **NeNe Invoice** | Phases 1–3 complete — quote-to-cash admin UI, qualified-invoice PDF, Tier A installer, Clear upstream `/api/*` |
| **NeNe Vault** | Phases 0–4 complete — 電子帳簿保存法 archive, admin UI, Tier A ZIP, 9 MCP tools; compliance gate approved |
| **NeNe Profile** | Normalization API + admin SPA + Playwright E2E — bank CSV → standard output for Clear |
| **NeNe Clear** | Reconciliation + dunning API + admin UI; Invoice upstream contract wired |
| **NeNe Concierge** | Scenario engine, admin SPA, embed widget, action engine (email / Slack / Chatwork), 22 MCP tools |
| **NeNe Corpus** | Cited knowledge chat — ingest, embed widget, Tier A installer, 157 Playwright specs |
| **NeNe Suite** | Phase 1 installer API + apex shell — multi-app orchestrator with professional sign-off on record |
| **NeNe Records** | [v0.4.0](https://github.com/hideyukiMORI/nene-records/releases) — M9 multi-tenant complete; 545 PHPUnit + 157 Playwright E2E |

---

## Runtimes — pick your stack

Same architecture · OpenAPI contract · RFC 9457 Problem Details · MCP-ready boundaries.

| Runtime | Stack | Latest | Start |
| --- | --- | --- | --- |
| **[NeNe](https://github.com/hideyukiMORI/NeNe)** | PHP 8.4 · Smarty · URL routing · renovation story | [v0.3.0](https://github.com/hideyukiMORI/NeNe/releases) | [Demo](https://nene-php.com/) · `composer require` |
| **[NENE2](https://github.com/hideyukiMORI/NENE2)** | PHP 8.4 · OpenAPI author · MCP catalog · howto library | [v1.5.329](https://github.com/hideyukiMORI/NENE2/releases) | `composer require hideyukimori/nene2` |
| **[nene2-python](https://github.com/hideyukiMORI/nene2-python)** | FastAPI · mypy strict · Pydantic v2 | [v1.8.164](https://github.com/hideyukiMORI/nene2-python/releases) | `uv add nene2-python` |
| **[nene2-node](https://github.com/hideyukiMORI/nene2-node)** | Hono · TypeScript strict | [v0.3.0](https://github.com/hideyukiMORI/nene2-node/releases) | `npm i @hideyukimori/nene2-framework` |

---

## Platform products — content & conversion

Real products, not demo endpoints. MIT · self-hosted · OpenAPI-first · MCP for ops.

| Product | One line | Status | Try it |
| --- | --- | --- | --- |
| **[NeNe Records](https://github.com/hideyukiMORI/nene-records)** | Headless CMS — typed entities, React admin, 60+ MCP tools, multi-tenant JWT | M9 complete · [v0.4.0](https://github.com/hideyukiMORI/nene-records/releases) | [`docker compose up --build`](https://github.com/hideyukiMORI/nene-records#quick-start) |
| **[NeNe Corpus](https://github.com/hideyukiMORI/nene-corpus)** | Knowledge chat with citations — PDF/CSV ingest, embed widget, Tier A ZIP | Phases 1–3 core ✅ | [Quick start](https://github.com/hideyukiMORI/nene-corpus#quick-start) · [nene-corpus.com](https://nene-corpus.com) |
| **[NeNe Concierge](https://github.com/hideyukiMORI/nene-concierge)** | Visual chat scenarios — embed on product pages; actions (email / Slack / Chatwork) | Engine + admin + widget + 22 MCP tools ✅ | [`docker compose up --build`](https://github.com/hideyukiMORI/nene-concierge#quick-start) |

**Records** — 545 backend tests · 157 Playwright E2E · superadmin / admin / editor · org-scoped JWT  
**Corpus** — sync cited chat · 6-locale admin · analytics dashboard · shared-hosting path  
**Concierge** — condition nodes · session analytics · scenario import/export · AI authoring via MCP

Optional upstream: Corpus and Concierge can read from Records over HTTP — repos stay separate.

---

## Japan SMB back-office — sibling apps, one stack

Separate repos · separate databases · HTTP contracts only. Install what you need.

```
NeNe Profile          NeNe Invoice          NeNe Clear           NeNe Vault
(bank CSV normalize)  (quote · invoice ·     (reconcile ·         (received docs ·
                       payment SoR)          dunning)              電子帳簿保存法)
        │                     ▲                     ▲
        └──── normalized CSV ─┴──── Invoice API ────┘
```

| Product | Domain | Status | Repo |
| --- | --- | --- | --- |
| **[NeNe Invoice](https://github.com/hideyukiMORI/nene-invoice)** | 見積・請求・入金 — 適格請求書 PDF, multi-tenant admin | Phases 1–3 ✅ · security review ✅ | [Quick start](https://github.com/hideyukiMORI/nene-invoice#quick-start) |
| **[NeNe Clear](https://github.com/hideyukiMORI/nene-clear)** | 入金消込・督促 — consumes Invoice `/api/*`, not a billing app | Phase 1–2 ✅ · pentest remediated | [README](https://github.com/hideyukiMORI/nene-clear) |
| **[NeNe Profile](https://github.com/hideyukiMORI/nene-profile)** | Bank CSV column mapping → standard transaction export | Phase 1–2 ✅ | [README](https://github.com/hideyukiMORI/nene-profile) |
| **[NeNe Vault](https://github.com/hideyukiMORI/nene-vault)** | Received-document archive — search, retention, audit | Phases 0–4 ✅ · CPA sign-off 🟢 | [`docker compose up`](https://github.com/hideyukiMORI/nene-vault) → `:8600` |
| **[NeNe Deal](https://github.com/hideyukiMORI/nene-deal)** | Ultra-light B2B pipeline — kanban, forecast, won → Invoice handoff | MVP backend + admin ✅ | [README](https://github.com/hideyukiMORI/nene-deal) |

**Not one monolith.** Invoice issues bills; Clear clears deposits; Profile normalizes CSV; Vault archives received PDFs. See each repo's ADR 0009 boundary docs.

---

## NeNe Suite — multi-app installer

**[nene-suite](https://github.com/hideyukiMORI/nene-suite)** orchestrates sibling products: catalog-driven install wizard, apex login shell, suite env contract, audit trail on every mutation.

| | |
| --- | --- |
| **Role** | Installer + orchestrator only — no billing/CMS domain logic in Suite |
| **Status** | Phase 1 OpenAPI (13 ops) + frontend wizard ✅ · Tier B Docker MVP ✅ |
| **Local** | `docker compose up suite` → `:8800` |

---

## Ecosystem packages

| Package | Role | Latest |
| --- | --- | --- |
| **[nene2-js](https://github.com/hideyukiMORI/nene2-js)** | Typed HTTP client — `@hideyukimori/nene2-client` · multi-backend verify | [v1.0.0](https://github.com/hideyukiMORI/nene2-js/releases) |
| **[nene-mcp](https://github.com/hideyukiMORI/nene-mcp)** | stdio MCP bridge → any OpenAPI-backed HTTP API | [v0.1.8](https://github.com/hideyukiMORI/nene-mcp/releases) |
| **[NENE2-examples](https://github.com/hideyukiMORI/NENE2-examples)** | 130+ runnable field-trial apps — one pattern per howto | active |

Wire Cursor / Claude Desktop to your API: `composer require hideyukimori/nene-mcp` → point MCP host at `vendor/bin/nene-mcp`.

---

## Why this stack

- **AI-readable** — Handler → UseCase → Repository; agents and CI navigate without hidden magic
- **MCP-native** — catalog-driven tools; Records 60+ · Concierge 22 · Vault 9 · Deal 7 read tools
- **Multi-language parity** — PHP, Python, Node share OpenAPI-shaped boundaries
- **Security-first** — RFC 9457 errors, JWT org isolation, PHPStan L8 / `mypy --strict` / Vitest
- **Japan SMB path** — Tier A shared-hosting ZIP installers alongside Docker Compose (Tier B)

---

## Start here

| You want… | Go to |
| --- | --- |
| Old-school PHP MVC + renovation story | [NeNe](https://github.com/hideyukiMORI/NeNe) |
| New JSON API in PHP | [NENE2](https://github.com/hideyukiMORI/NENE2) |
| Same architecture in Python / Node | [nene2-python](https://github.com/hideyukiMORI/nene2-python) · [nene2-node](https://github.com/hideyukiMORI/nene2-node) |
| Typed client for any NENE2 API | [nene2-js](https://github.com/hideyukiMORI/nene2-js) |
| Wire Cursor / Claude Desktop to your API | [nene-mcp](https://github.com/hideyukiMORI/nene-mcp) |
| Headless CMS + MCP | [NeNe Records](https://github.com/hideyukiMORI/nene-records) |
| Self-hosted RAG chat with citations | [NeNe Corpus](https://github.com/hideyukiMORI/nene-corpus) |
| Conversion-focused embed chat scenarios | [NeNe Concierge](https://github.com/hideyukiMORI/nene-concierge) |
| Quote · invoice · payment (Japan) | [NeNe Invoice](https://github.com/hideyukiMORI/nene-invoice) |
| Bank deposit reconciliation & dunning | [NeNe Clear](https://github.com/hideyukiMORI/nene-clear) |
| Bank CSV normalization | [NeNe Profile](https://github.com/hideyukiMORI/nene-profile) |
| Received-document archive (電子帳簿保存法) | [NeNe Vault](https://github.com/hideyukiMORI/nene-vault) |
| B2B deal pipeline → Invoice handoff | [NeNe Deal](https://github.com/hideyukiMORI/nene-deal) |
| Install multiple NeNe apps together | [NeNe Suite](https://github.com/hideyukiMORI/nene-suite) |
| Browse 130+ API patterns | [NENE2-examples](https://github.com/hideyukiMORI/NENE2-examples) |
| Publication experiments & schedule | [publication-strategy](https://github.com/hideyukiMORI/publication-strategy) |

---

## Articles

### Japanese

- NeNe renovation — [Zenn](https://zenn.dev/xioncc/articles/a2709df3e0de3b) · [source](https://github.com/hideyukiMORI/NeNe/blob/main/docs/articles/zenn-renovating-legacy-php-framework.md)
- NeNe hands-on (fixed page + REST) — [Qiita](https://qiita.com/xioncc/items/bc18adedd8c5f5a84336) · [source](https://github.com/hideyukiMORI/NeNe/blob/main/docs/articles/qiita-fixed-page-and-rest-api.md)

### English (planned / in flight)

NENE2 OpenAPI + MCP wedge and sibling port articles: [publication-strategy schedule](https://github.com/hideyukiMORI/publication-strategy/blob/main/docs/schedules/2026-publication-schedule.md) (EXP-003 DEV, Jun 2026).
