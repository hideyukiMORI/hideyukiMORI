<picture>
  <source media="(prefers-color-scheme: dark)"  srcset="assets/hero-dark.webp">
  <source media="(prefers-color-scheme: light)" srcset="assets/hero-light.webp">
  <img alt="Hideyuki Mori — Engineering you can verify" src="assets/hero-light.webp" width="100%">
</picture>

# Hideyuki Mori

### Software engineer. I build small Windows desktop tools and self-hosted business software in the open, and I put the proof next to every claim.

These days most of my open-source time goes into **native Windows applications** — small, frameless, single-purpose tools written without a UI library. Alongside them I maintain the **NENE2 series**: MIT-licensed, self-hosted business software on one design language across PHP, Python, and TypeScript. Everything below is public and checkable: the code, the tests, the releases, and the architecture decisions.

<sub>日本語: ソフトウェアエンジニア。いまは Windows 向けの小さなネイティブアプリ（UI ライブラリを使わない、枠なし・単機能の道具）を中心に公開開発しています。あわせて、MIT ライセンスの自己ホスト型業務ツール群「NENE2 シリーズ」を保守しています。このページの数字はすべてリンク先で確かめられます。</sub>

---

## Windows apps

Small tools I use every day. No UI library, no runtime to install, one executable where the platform allows it. Snapshot: October 2026.

<p align="center">
  <a href="https://apps.microsoft.com/detail/9N6HZB1SXKBM"><img alt="NeNe Loupe — a magnified grid of screen pixels with the centre pixel outlined, and its colour shown as #33E699" src="assets/nene-loupe.webp" width="49%"></a>
  &nbsp;
  <a href="https://github.com/hideyukiMORI/nene-clock"><img alt="NeNe Clock — twelve frameless desktop clocks in different typefaces and colours" src="assets/nene-clock.webp" width="49%"></a>
</p>

| App | What it is | Built with | Status |
| --- | --- | --- | --- |
| **[NeNe Loupe](https://github.com/hideyukiMORI/nene-loupe)** | A tiny frameless screen loupe and colour picker. See the pixels behind the lens, copy the colour in the centre. | C++23 · Win32 | **On the [Microsoft Store](https://apps.microsoft.com/detail/9N6HZB1SXKBM)** · [v1.0.0](https://github.com/hideyukiMORI/nene-loupe/releases/latest) · portable ZIP also available |
| **[NeNe Clock](https://github.com/hideyukiMORI/nene-clock)** | A quiet desktop clock. No frame, no buttons, no tray icon — just the time, in the typeface and colours you choose. | Java 21 · Swing | [v0.2.6](https://github.com/hideyukiMORI/nene-clock/releases/latest) — Windows installer, portable ZIP, Ubuntu `.deb` · Microsoft Store listing in preparation |
| **[NeNe Nib](https://github.com/hideyukiMORI/nene-nib)** | A fast single-executable text editor that toggles between ordinary editing and Vim editing. Japanese IME, tabs that come back on the next start, 95 built-in themes. | C++23 · Win32 · Direct2D / DirectWrite | **Beta** · [v0.1.0-beta.2](https://github.com/hideyukiMORI/nene-nib/releases/tag/v0.1.0-beta.2) for Windows 11 x64 |
| **[NeNe Folio](https://github.com/hideyukiMORI/nene-folio)** | A frameless Markdown notebook with a category drawer. View and edit, a short history of every save, search and regex replace, Vim-like keys; UI in 日本語 / English / 简体中文. | C23 · Win32 | v0.1.0 — usable from source · no packaged download yet |
| **[NeNe Commander](https://github.com/hideyukiMORI/NeNeCommander)** | A keyboard-first dual-pane file manager; Windows, UNC, and WSL paths as typed, explicit boundaries. | C# · .NET 10 · WinUI 3 | In development — most of the MVP scope is on `main`: Vim-first dual panes, fail-closed copy / move / rename / delete on Windows local paths and inside a WSL distribution, UNC directory reads, copy from Windows into WSL · no download yet |

**How they are built.** Each repository starts from a specification, an architecture constitution, and a test strategy before the first feature. The rule is the same in every one: *every meaning has exactly one canonical implementation path, and the compiler, the build graph, static analysis, and CI enforce that — not memory.* NeNe Nib's Vim mode, for example, is replayed against real Vim 9.1 through 1,853 oracle-generated fixtures. The documents and the measurements are in each repo (`SPECIFICATION.md`, `docs/adr/`, `docs/quality/gate-proofs.md`).

### Also outside the web stack

| Repo | Ecosystem | What it is |
| --- | --- | --- |
| **[NENE-PIXEL](https://github.com/hideyukiMORI/NENE-PIXEL)** | Kotlin · Android | Pixel drawing tool for Android 8.0+ — indexed palettes, up to 16 layers, PNG import/export, reference underlay; single-frame, in development |
| **[xi-tools](https://github.com/hideyukiMORI/xi-tools)** | Rust | Tools for a many-repo workflow — `scopegrep` (grep that reports *where in the structure* a hit lives), `fleet-top` (dozens of repos on one screen) |
| **[nene-recall](https://github.com/hideyukiMORI/nene-recall)** | Go · PostgreSQL · pgvector | Hybrid vector + lexical retrieval API, fully local |

---

## At a glance

Numbers are **measured, not claimed** — each links to where you can check it yourself. Snapshot: October 2026.

| | |
| --- | --- |
| **Shipped** | [NeNe Loupe on the Microsoft Store](https://apps.microsoft.com/detail/9N6HZB1SXKBM) · [NeNe Clock installers](https://github.com/hideyukiMORI/nene-clock/releases/latest) · [NeNe Nib beta](https://github.com/hideyukiMORI/nene-nib/releases/tag/v0.1.0-beta.2) |
| **Scale** | **10,900+ merged PRs** across my own repositories ([verify](https://github.com/search?q=is%3Apr+is%3Amerged+author%3AhideyukiMORI+owner%3AhideyukiMORI&type=pullrequests)) · **42 public repos** |
| **Languages** | C++23 · C23 · Java 21 · C# · Kotlin · Rust · Go · PHP 8.4 · Python 3.14 · TypeScript |
| **Background** | 25 years of JavaScript and 20 years of PHP as a working engineer, from customer hearings through design, implementation, and operation |

---

## NENE2 series — status

MIT · self-hosted · OpenAPI-first JSON APIs · RFC 9457 Problem Details · MCP-ready boundaries. Separate repos, separate databases, HTTP contracts only.

Running: [nene-records.com](https://nene-records.com) · [nene-corpus.com](https://nene-corpus.com) · [NeNe Invoice demo](https://invoice.ayane.co.jp/demo/kensetsu) (a fresh disposable environment per click).

### Frameworks

| Runtime | Stack | Latest | Install |
| --- | --- | --- | --- |
| **[NENE2](https://github.com/hideyukiMORI/NENE2)** | PHP 8.4 · OpenAPI · MCP catalog | [v1.12.0](https://github.com/hideyukiMORI/NENE2/releases) | `composer require hideyukimori/nene2` |
| **[nene2-python](https://github.com/hideyukiMORI/nene2-python)** | FastAPI · `mypy --strict` · Pydantic v2 | [v1.8.164](https://github.com/hideyukiMORI/nene2-python/releases) | `uv add nene2-python` |
| **[nene2-node](https://github.com/hideyukiMORI/nene2-node)** | Hono · TypeScript strict | [v0.3.0](https://github.com/hideyukiMORI/nene2-node/releases) | `npm i @hideyukimori/nene2-framework` |
| **[NeNe](https://github.com/hideyukiMORI/NeNe)** | PHP 8.4 · Smarty · a legacy framework renovated in the open | [v0.3.0](https://github.com/hideyukiMORI/NeNe/releases) | [Demo](https://nene-php.com/) |

Frontend standards on npm ([nene2-fleet-tooling](https://github.com/hideyukiMORI/nene2-fleet-tooling)): [`nene2-tokens`](https://www.npmjs.com/package/@hideyukimori/nene2-tokens) v1.3.0 · [`nene2-standards`](https://www.npmjs.com/package/@hideyukimori/nene2-standards) v2.4.0 · [`nene2-ui`](https://www.npmjs.com/package/@hideyukimori/nene2-ui) v0.21.0 · [`nene2-i18n`](https://www.npmjs.com/package/@hideyukimori/nene2-i18n) v0.3.2

### Products

| Product | One line | Status |
| --- | --- | --- |
| **[NeNe Records](https://github.com/hideyukiMORI/nene-records)** | Headless CMS — typed entities, React admin, multi-tenant | Production SaaS · [v0.5.4](https://github.com/hideyukiMORI/nene-records/releases) |
| **[NeNe Invoice](https://github.com/hideyukiMORI/nene-invoice)** | 見積・請求・入金 — 適格請求書 PDF | [v1.0.0](https://github.com/hideyukiMORI/nene-invoice/releases) · live demo |
| **[NeNe Corpus](https://github.com/hideyukiMORI/nene-corpus)** | Knowledge chat with citations | Live |
| **[NeNe Contact](https://github.com/hideyukiMORI/nene-contact)** | Embeddable contact forms | In production |
| **[NeNe Concierge](https://github.com/hideyukiMORI/nene-concierge)** | Visual chat scenarios, embeddable | Working |
| **[NeNe Serve](https://github.com/hideyukiMORI/nene-serve)** | Self-hosted ad serving | Working |
| **[NeNe Clear](https://github.com/hideyukiMORI/nene-clear)** | 入金消込・督促 — consumes the Invoice API | Working |
| **[NeNe Vault](https://github.com/hideyukiMORI/nene-vault)** | 受領文書アーカイブ（電子帳簿保存法） | Working |
| **[NeNe Profile](https://github.com/hideyukiMORI/nene-profile)** | Bank-CSV normalization | Working |
| **[NeNe Deal](https://github.com/hideyukiMORI/nene-deal)** | Light B2B pipeline — won → Invoice handoff | Working |
| **[NeNe Payout](https://github.com/hideyukiMORI/nene-payout)** | Pay received vendor invoices by card | Working |
| **[NeNe Field](https://github.com/hideyukiMORI/nene-field)** | Daily reports from field workers' phones | Working |
| **[NeNe Suite](https://github.com/hideyukiMORI/nene-suite)** | Multi-app installer + orchestrator | Working |

Tooling: [nene2-js](https://github.com/hideyukiMORI/nene2-js) (typed HTTP client, [v1.4.0](https://github.com/hideyukiMORI/nene2-js/releases)) · [nene-mcp](https://github.com/hideyukiMORI/nene-mcp) (stdio MCP bridge for any OpenAPI-backed API, [v0.1.8](https://github.com/hideyukiMORI/nene-mcp/releases)) · [NENE2-examples](https://github.com/hideyukiMORI/NENE2-examples) (runnable field-trial apps)

### Quality and security practice

- **Static analysis as a gate** — PHPStan level 8 on the PHP repos, `mypy --strict` on nene2-python, conformance linting across products, dependency audits in CI.
- **JWT is fail-closed by default** — org isolation denies on any resolver ambiguity rather than falling open.
- **Security testing is maintainer-run self-assessment** against isolated environments. **It is not a third-party penetration test.** Deepest coverage: NENE2, NeNe Invoice, NeNe Clear.

---

## Articles

I write about what actually broke and what fixed it — [DEV](https://dev.to/hideyukimori) · [Zenn](https://zenn.dev/xioncc) · [Qiita](https://qiita.com/xioncc).

**Featured**

*English*
- [I built a tiny PHP framework for AI-readable business APIs](https://dev.to/hideyukimori/i-built-a-tiny-php-framework-for-ai-readable-business-apis-48eo) — DEV
- [MCP should not mean letting AI touch your database](https://dev.to/hideyukimori/mcp-should-not-mean-letting-ai-touch-your-database-57p1) — DEV
- [A todo.txt shared by a human and AI agents](https://dev.to/hideyukimori/a-todotxt-shared-by-a-human-and-ai-agents-why-plain-text-beat-a-saas-board-for-my-workflow-5dbh) — DEV

*日本語*
- [テストが全部緑でも壊せる｜リリース前アドバーサリアルレビューを常設する](https://zenn.dev/xioncc/articles/349a739826288b) — Zenn
- [コンテキストが溢れる AI 協働を multi-session で回す｜指揮×担当を指示書と報告書で受け渡す](https://zenn.dev/xioncc/articles/4445ac86600d28) — Zenn
- [レガシー PHP フレームワークの改修（NeNe）](https://zenn.dev/xioncc/articles/a2709df3e0de3b) — Zenn

**Latest** <!-- auto-updated from the nene-articles pipeline · do NOT hand-edit between the markers below -->
<!-- ARTICLES:START -->
- [Two AI Agents Shared a Todo File and a Line Vanished](https://dev.to/hideyukimori/two-ai-agents-shared-a-todo-file-and-a-line-vanished-22jd) — DEV (en) · 2026-08-08
- [適用ゼロで codemod の非冪等バグを見つけた──撃つ前の机上 dry-run](https://zenn.dev/xioncc/articles/codemod-desk-check-idempotence) — Zenn (ja) · 2026-08-07
- [target="_blank"がハイドレーション後だけ消える｜SSR/SPA二重sanitizerの罠](https://qiita.com/xioncc/items/32c9220145e116263023) — Qiita (ja) · 2026-08-06
- [AI への作業指示書は4日で腐る──着手前の再実測が空撃ちを防いだ](https://zenn.dev/xioncc/articles/stale-orders-subordinate-verifies) — Zenn (ja) · 2026-08-05
- [緑の PR を 11 秒差でマージしたら main が赤になった話｜PR CI は統合後の main を検証しない](https://qiita.com/xioncc/items/d26f17c566a6139f4aff) — Qiita (ja) · 2026-08-05
<!-- ARTICLES:END -->

<sub>Featured = hand-picked · Latest = newest 5 (max 2 per platform).</sub>

---

<sub>Issues are open on every repository above.</sub>
