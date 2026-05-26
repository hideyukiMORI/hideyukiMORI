# Hideyuki Mori — OSS

**Convention-visible JSON API frameworks** readable by humans and AI agents — one design language across PHP, Python, and Node, without Laravel/Symfony/Django weight.

**Hub:** [nene2.dev](https://nene2.dev) · **Strategy:** [publication-strategy](https://github.com/hideyukiMORI/publication-strategy) · **Contact:** [ayane.co.jp](https://ayane.co.jp/)

---

## Runtimes — pick your stack

Same architecture. Same OpenAPI contract. Same field-trial discipline.

| Runtime | Stack | Status | Install |
|---|---|---|---|
| **[NeNe](https://github.com/hideyukiMORI/NeNe)** | PHP 8.4 · Smarty · URL routing · renovation story | active | [Demo](https://nene-php.com/) · [v0.2+](https://github.com/hideyukiMORI/NeNe/releases) |
| **[NENE2](https://github.com/hideyukiMORI/NENE2)** | PHP 8.4 · OpenAPI contract author · MCP catalog · **179 howtos** | active | `composer require hideyukimori/nene2` |
| **[nene2-python](https://github.com/hideyukiMORI/nene2-python)** | FastAPI · mypy strict · Pydantic v2 · **v1.8.97 · 466 tests** | active | `uv add nene2-python` |
| **[nene2-node](https://github.com/hideyukiMORI/nene2-node)** | Hono · TypeScript strict · Redis · **v0.1.23** | active | `npm i @hideyukimori/nene2-framework` |

---

## Showcase products

### NeNe Records — Headless CMS

> Typed, API-first headless CMS on NENE2. Lighter where WordPress is heavy and meta-chaotic.

```
docker compose up --build
```

→ **[hideyukiMORI/nene-records](https://github.com/hideyukiMORI/nene-records)**

**M4 complete** — full-stack headless CMS platform:

| Layer | What's in |
|---|---|
| **Data** | Typed entity fields · multi-locale content · tag filtering · sort/filter |
| **API** | OpenAPI-first · full-text search · CSV/JSON export · rate limiting (120 req/60s) |
| **Publishing** | Scheduled publish · draft preview tokens · permalink patterns · public `Cache-Control` / ETag |
| **Admin UI** | React + TypeScript · dark theme · Markdown editor · theme selector · toast notifications |
| **Auth & Users** | JWT · roles · user invite / password management |
| **Webhooks** | HMAC-SHA256 signed · `entity.created` / `.updated` / `.deleted` |
| **Docker** | `docker compose up` → API + React admin + cron scheduler |

Next: M5 — plugin/extension system.

---

### NeNe Corpus — Self-hosted Knowledge Chat

> Ingest your documents. Chat with citations. Keep everything on your stack.

```
docker compose up --build   # Docker / VPS
# or: shared-hosting ZIP + web installer
```

→ **[hideyukiMORI/nene-corpus](https://github.com/hideyukiMORI/nene-corpus)**

A self-hosted RAG platform built on NENE2 — no SaaS lock-in, no data leaving your server.

| Layer | What's in |
|---|---|
| **Ingestion** | PDF / CSV upload · chunk pipeline · column-mapping preview |
| **Chat** | Claude tool_use orchestration · cited answers · session rate limiting |
| **Embed** | One `<script>` tag on any existing homepage (same origin) |
| **Deployment** | Dual-track: shared hosting ZIP installer (Japan SMB) + Docker Compose (developers / VPS) |
| **Admin** | JWT auth · upload management · audit logs · OpenAPI |

---

## Ecosystem packages

| Package | Role | Version |
|---|---|---|
| **[nene2-js](https://github.com/hideyukimori/nene2-js)** | Typed HTTP client (Node / browser) | **v1.0.0** 🎉 · `@hideyukimori/nene2-client` |
| **[nene-mcp](https://github.com/hideyukimori/nene-mcp)** | stdio MCP bridge → any HTTP API · Bearer hardening (FT750+) | `hideyukimori/nene-mcp` |
| **[NENE2-examples-repo](https://github.com/hideyukimori/NENE2-examples-repo)** | 93 runnable field-trial apps — each proves one NENE2 howto pattern | — |

---

## Why this stack

- **AI-readable by design** — conventions over magic; Cursor, Claude Desktop, and CI agents navigate the code without extra documentation
- **MCP-native** — `nene-mcp` wires any NENE2-compatible API to AI agents in minutes; NeNe Records ships 60+ MCP tools out of the box
- **Multi-language parity** — PHP, Python, Node share the same OpenAPI contract and field-trial validation, so you can adopt incrementally
- **Security-first** — rate limiting, Bearer token auth, HMAC webhooks, RFC 9457 error responses, `mypy --strict` / PHPStan level 8

---

## Start here

| You want… | Go to |
|---|---|
| Old-school PHP MVC + renovation story | [NeNe](https://github.com/hideyukiMORI/NeNe) |
| New JSON API in PHP | [NENE2](https://github.com/hideyukiMORI/NENE2) |
| Same architecture in Python | [nene2-python](https://github.com/hideyukiMORI/nene2-python) |
| Same architecture in Node / TypeScript | [nene2-node](https://github.com/hideyukiMORI/nene2-node) |
| Typed client to call any NENE2 API | [nene2-js](https://github.com/hideyukimori/nene2-js) — **v1.0.0 stable** |
| Wire Cursor / Claude Desktop to your API | [nene-mcp](https://github.com/hideyukimori/nene-mcp) |
| Full headless CMS demo on NENE2 | [NeNe Records](https://github.com/hideyukiMORI/nene-records) — M4 |
| Self-hosted RAG chat with citations | [NeNe Corpus](https://github.com/hideyukiMORI/nene-corpus) |
| See 93 real API patterns in action | [NENE2-examples-repo](https://github.com/hideyukimori/NENE2-examples-repo) |

Proof sandbox: [sakura-exhibition-nene2-field-trial](https://github.com/hideyukimori/sakura-exhibition-nene2-field-trial)

---

## Articles (Japanese)

- NeNe renovation (Zenn): [source](https://github.com/hideyukiMORI/NeNe/blob/main/docs/articles/zenn-renovating-legacy-php-framework.md) · [published](https://zenn.dev/xioncc/articles/a2709df3e0de3b)
- NeNe hands-on (Qiita) — coming soon
