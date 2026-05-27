# Hideyuki Mori — OSS

**Convention-visible JSON APIs** for humans and AI agents — one design language across PHP, Python, and Node, plus self-hosted products you can ship on shared hosting or Docker.

**Hub:** [nene2.dev](https://nene2.dev) · **Strategy:** [publication-strategy](https://github.com/hideyukiMORI/publication-strategy) · **Contact:** [ayane.co.jp](https://ayane.co.jp/)

---

## Runtimes — pick your stack

Same architecture · OpenAPI contract · field-trial discipline.

| Runtime | Stack | Status | Start |
| --- | --- | --- | --- |
| **[NeNe](https://github.com/hideyukiMORI/NeNe)** | PHP 8.4 · Smarty · URL routing · renovation story | active | [Demo](https://nene-php.com/) · [releases](https://github.com/hideyukiMORI/NeNe/releases) |
| **[NENE2](https://github.com/hideyukiMORI/NENE2)** | PHP 8.4 · OpenAPI author · MCP catalog · howto library | active | `composer require hideyukimori/nene2` |
| **[nene2-python](https://github.com/hideyukiMORI/nene2-python)** | FastAPI · mypy strict · Pydantic v2 | active | `uv add nene2-python` |
| **[nene2-node](https://github.com/hideyukiMORI/nene2-node)** | Hono · TypeScript strict | active | `npm i @hideyukimori/nene2-framework` |

---

## Applications — built on NENE2

Real products, not demo endpoints. MIT · self-hosted · OpenAPI-first.

| Product | One line | Try it |
| --- | --- | --- |
| **[NeNe Records](https://github.com/hideyukiMORI/nene-records)** | Headless CMS — typed entities, React admin, 60+ MCP tools, multi-tenant | `docker compose up --build` → `:8080` |
| **[NeNe Corpus](https://github.com/hideyukiMORI/nene-corpus)** | Knowledge chat with citations — PDF/CSV ingest, embed widget, Tier A ZIP installer | [Docker](https://github.com/hideyukiMORI/nene-corpus#quick-start) or shared hosting |
| **[NeNe Concierge](https://github.com/hideyukiMORI/nene-concierge)** | Visual chat scenarios — embed on product pages, actions (email / Slack / Chatwork), AI via MCP | `docker compose up --build` → `:8080` |

**Records** — M9 complete · 545 backend tests · Playwright E2E · JWT org isolation  
**Corpus** — ingestion + cited chat + admin UI + embed widget · Japan SMB Tier A path  
**Concierge** — scenario engine + embed widget + admin SPA + MCP (20 tools)

Optional upstream link: Corpus and Concierge can read from Records over HTTP — repos stay separate.

---

## Ecosystem packages

| Package | Role |
| --- | --- |
| **[nene2-js](https://github.com/hideyukimori/nene2-js)** | Typed HTTP client — `@hideyukimori/nene2-client` · multi-backend verify |
| **[nene-mcp](https://github.com/hideyukimori/nene-mcp)** | stdio MCP bridge → any OpenAPI-backed HTTP API |
| **[NENE2-examples](https://github.com/hideyukimori/NENE2-examples)** | 130+ runnable field-trial apps — one pattern per howto |

---

## Why this stack

- **AI-readable** — explicit layers; agents and CI navigate without hidden magic
- **MCP-native** — catalog-driven tools; Records ships 60+; Concierge exposes scenario ops
- **Multi-language parity** — PHP, Python, Node share the same API contract
- **Security-first** — RFC 9457 errors, JWT boundaries, PHPStan L8 / `mypy --strict`

---

## Start here

| You want… | Go to |
| --- | --- |
| Old-school PHP MVC + renovation story | [NeNe](https://github.com/hideyukiMORI/NeNe) |
| New JSON API in PHP | [NENE2](https://github.com/hideyukiMORI/NENE2) |
| Same architecture in Python / Node | [nene2-python](https://github.com/hideyukiMORI/nene2-python) · [nene2-node](https://github.com/hideyukiMORI/nene2-node) |
| Typed client for any NENE2 API | [nene2-js](https://github.com/hideyukimori/nene2-js) |
| Wire Cursor / Claude Desktop to your API | [nene-mcp](https://github.com/hideyukimori/nene-mcp) |
| Headless CMS + MCP | [NeNe Records](https://github.com/hideyukiMORI/nene-records) |
| Self-hosted RAG chat with citations | [NeNe Corpus](https://github.com/hideyukiMORI/nene-corpus) |
| Conversion-focused embed chat scenarios | [NeNe Concierge](https://github.com/hideyukiMORI/nene-concierge) |
| Browse 130+ API patterns | [NENE2-examples](https://github.com/hideyukimori/NENE2-examples) |

---

## Articles (Japanese)

- NeNe renovation — [Zenn](https://zenn.dev/xioncc/articles/a2709df3e0de3b) · [source](https://github.com/hideyukiMORI/NeNe/blob/main/docs/articles/zenn-renovating-legacy-php-framework.md)
- NeNe hands-on (fixed page + REST) — [Qiita](https://qiita.com/xioncc/items/bc18adedd8c5f5a84336) · [source](https://github.com/hideyukiMORI/NeNe/blob/main/docs/articles/qiita-fixed-page-and-rest-api.md)

English DEV articles for NENE2 and ports: see [publication-strategy schedule](https://github.com/hideyukiMORI/publication-strategy/blob/main/docs/schedules/2026-publication-schedule.md).
