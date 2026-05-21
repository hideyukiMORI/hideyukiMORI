# Hideyuki Mori — OSS

Small, explicit web frameworks for **reviewable services** and **JSON APIs** — readable by humans and AI agents alike.

Promotion strategy and experiment logs: [publication-strategy](https://github.com/hideyukiMORI/publication-strategy)

---

## Frameworks

| | Stack | Best for | Start here |
|---|---|---|---|
| **[NeNe](https://github.com/hideyukiMORI/NeNe)** | Renovated legacy PHP · Smarty · URL routing · OpenAPI | Small services, legacy-friendly PHP, lower review cost | [Demo](https://nene-php.com/) · [Release v0.2.0](https://github.com/hideyukiMORI/NeNe/releases/tag/v0.2.0) · `git clone` + Docker |
| **[NENE2](https://github.com/hideyukiMORI/NENE2)** | PHP 8.4 · JSON API first · OpenAPI · MCP · Packagist | New JSON APIs, thin HTML, AI tool boundaries | [Quick Start](https://github.com/hideyukiMORI/NENE2#quick-start) · `composer require hideyukimori/nene2` |
| **[nene2-python](https://github.com/hideyukiMORI/nene2-python)** | FastAPI · Pydantic v2 · mypy strict · MCP | Same design as NENE2 in Python | [README](https://github.com/hideyukiMORI/nene2-python#installation) · `uv add nene2-python` |

**Not** Laravel/Symfony/Django replacements — intentionally small, convention-visible frameworks.

---

## Which one?

- **Old-school PHP MVC, renovation story** → NeNe  
- **Modern PHP API + OpenAPI + MCP** → NENE2  
- **Python, clean architecture, strict typing** → nene2-python  

---

## Field trials & proof

External sandboxes that exercise each framework outside its main repo:

- [sakura-exhibition-nene2-field-trial](https://github.com/hideyukiMORI/sakura-exhibition-nene2-field-trial) — NENE2 client-style demo (OpenAPI, tests, MCP)

---

## Articles (Japanese)

- NeNe renovation story (Zenn): [source in NeNe repo](https://github.com/hideyukiMORI/NeNe/blob/main/docs/articles/zenn-renovating-legacy-php-framework.md)  
- Qiita hands-on tutorial — coming soon (NeNe)

---

## Elsewhere

- Website: [ayane.co.jp](https://ayane.co.jp/)
