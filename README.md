<h1 align="center">Platon Korolev</h1>

<p align="center">
  <b>Fullstack Engineer</b> • React / Next.js / Node.js / Python / High-Density Systems
</p>

<p align="center">
  <a href="https://t.me/manethes"><img src="https://img.shields.io/badge/Telegram-@manethes-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" /></a>
  <a href="mailto:kplatonglfc@gmail.com"><img src="https://img.shields.io/badge/Email-kplatonglfc%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /></a>
  <img src="https://img.shields.io/badge/Location-Moscow-09090b?style=for-the-badge&logo=googlemaps&logoColor=white" />
  <img src="https://img.shields.io/badge/Status-Open_to_Offers-22c55e?style=for-the-badge" />
</p>

---

## ⚡ About Me

Fullstack developer focused on building clean, high-performance, and resilient web applications — from low-level database transactions to zero-latency user interfaces.

- **Product Interfaces & Design Engineering:** Zero-layout-shift (CLS = 0), high data density, keyboard-first terminal workflows.
- **Scalable Frontend Architecture:** Feature-Sliced Design (FSD), optimistic UI mutations, client cache layer isolation.
- **Backend & Data Integrity:** Concurrency-safe auth (token rotation, grace periods), zero-ORM raw SQL performance (`pg.Pool`), SQLite WAL state stores.
- **AI Tooling & Agentic Protocols:** Model Context Protocol (MCP), multi-provider LLM fallback routing, vector embeddings (Qdrant RAG).
- **Code Quality & Typing:** Strict runtime validation (TypeScript, Zod), pure domain models, decoupled transport layers.

---

## 🛠️ Tech Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=ts,js,react,nextjs,vue,vite,nodejs,express,python,postgres,sqlite,docker,linux,git,github,vscode&theme=dark" alt="Tech Stack Icons" />
</p>

<p align="center">
  <code>TanStack Query v5</code> • <code>Zustand</code> • <code>Qdrant Vector DB</code> • <code>FastMCP</code> • <code>raw pg.Pool</code> • <code>OAuth 2.0 / JWT</code> • <code>MSW</code> • <code>Vitest</code>
</p>

---

## 🚀 Featured Projects

### 1. Nexus CRM (Mini-CRM)
> Production-ready fullstack CRM with Kanban task management, relation notes, token reuse detection, and Swiss 90° industrial terminal UI.

<p align="left">
  <a href="https://mini-crm-web-swart.vercel.app"><img src="https://img.shields.io/badge/🚀_Live_Demo-0070F3?style=for-the-badge&logo=vercel&logoColor=white" /></a>
  <a href="https://mini-crm-api-ms.vercel.app/api-docs"><img src="https://img.shields.io/badge/📖_Swagger_API-85EA2D?style=for-the-badge&logo=swagger&logoColor=black" /></a>
  <a href="https://github.com/M00N77/mini-crm"><img src="https://img.shields.io/badge/💻_Repository-181717?style=for-the-badge&logo=github&logoColor=white" /></a>
</p>

<img width="100%" alt="Nexus CRM Interface Preview" src="https://github.com/user-attachments/assets/0a7ed7f1-0bb8-4346-b216-ac6b93abbbf6" />

**Stack:** Next.js 16 • React 19 • TypeScript • Tailwind CSS v4 • TanStack Query v5 • Zustand v5 • Express 5 • PostgreSQL 17 (pg.Pool) • Docker

* **Security & Token Rotation:** Dual-token JWT (in-memory access + HttpOnly refresh cookie) with server-side rotation in PostgreSQL. Implements a 15-second **Grace Period** to resolve concurrent browser tab races (`409 Concurrent Refresh`) and instant session purges on replay attacks.
* **Single-Flight Refresh Queue:** Network interceptor coalesces parallel `401 Unauthorized` requests into a single refresh promise, eliminating refresh storming.
* **Zero-ORM Data Layer:** Direct parameterized queries via `pg.Pool` with strict DDL constraints (`CHECK (hashed_password IS NOT NULL OR google_sub IS NOT NULL)`), cascaded deletions, and custom transactional migrations.
* **Algorithmic UI Sorting:** Custom stable **Merge Sort** Theta(n log n) implementation for data tables, preventing row flickering and worst-case O(n^2) degradations of naive quicksort.
* **Measured Web Vitals:** **LCP < 0.8s, CLS = 0.000, INP < 30ms**. Zero layout shift via Turbopack font metric overrides and optimistic mutations.

---

### 2. TelegramHelper
> AI-powered team assistant for automated meeting transcription, sentiment analysis, and project management sync.

<p align="left">
  <a href="https://github.com/M00N77/tg-helper"><img src="https://img.shields.io/badge/💻_Repository-181717?style=for-the-badge&logo=github&logoColor=white" /></a>
  <img src="https://img.shields.io/badge/🏆_Hackathon-4th_Place_Finalist-8A2BE2?style=for-the-badge" />
</p>

<img width="100%" alt="TelegramHelper Interface Preview" src="https://github.com/user-attachments/assets/5b23cb16-5681-4207-9cf2-9634463ed931" />

**Stack:** Python 3.12 • aiogram 3 • Telethon • SQLAlchemy 2 (asyncpg) • Qdrant • OpenAI • Gemini • Groq • Docker Compose

* **Dual-Bot Architecture:** Unified process combining a Telethon MTProto userbot (message mirroring, group listening) with an aiogram Control Bot for natural language agent execution.
* **Supervised Lifecycle:** 9 concurrent background tasks running in a single `asyncio` event loop under active supervision with deterministic shutdown.
* **Heuristic LLM Routing:** Multi-tier request classifier dynamically routing requests across Groq, Gemini, OpenAI, and GigaChat with automatic exponential-backoff fallback.
* **Audio Pipeline & PM Sync:** Webhook server (`aiohttp`) handling MTS Link meeting recordings with background `ffmpeg` conversion, Whisper transcription, and automatic YouGile Kanban task generation.
* **Security & RBAC:** Fernet (AES-128-CBC) encryption for sensitive API keys and session tokens with granular role-based access control.

---

### 3. IRS Dashboard
> High-density master-detail registry and analytics dashboard reimagining heavy enterprise case management portals.

<p align="left">
  <a href="https://dashboard-irs.vercel.app"><img src="https://img.shields.io/badge/🚀_Live_Demo-0070F3?style=for-the-badge&logo=vercel&logoColor=white" /></a>
  <a href="https://github.com/M00N77/dashboard-irs"><img src="https://img.shields.io/badge/💻_Repository-181717?style=for-the-badge&logo=github&logoColor=white" /></a>
  <img src="https://img.shields.io/badge/CLS-0.000-22c55e?style=for-the-badge" />
  <img src="https://img.shields.io/badge/LCP-1.71s-22c55e?style=for-the-badge" />
</p>

<img width="100%" alt="IRS Dashboard Interface Preview" src="https://github.com/user-attachments/assets/942cca62-dcc4-4736-a937-d04a8af0c473" />

**Stack:** React 19 • Vite 6 • TypeScript • Material UI 9 • TanStack Query 5 • TanStack Table 8 • React Hook Form + Zod 4 • Recharts • MSW 2

* **Decoupled Data Architecture:** Strict separation between lightweight table records (`PersonSummary`) and deep nested profile entities (`PersonDetails`), cutting initial payload transfer.
* **Server-Side Simulation:** Client-side mock engine powered by Mock Service Worker (MSW) intercepting network calls at the Service Worker level with full pagination, search, and sorting.
* **Cache Invalidation Mesh:** Coordinated TanStack Query invalidation graph where mutations automatically flush dependent profile details and aggregated analytical widgets simultaneously.
* **Strict Performance Budget:** **LCP ~1.71s, CLS = 0.000**. Achieved via explicit skeleton dimensions matching typography and column min-widths.

---

### 4. MCP Telegram Server
> Model Context Protocol (MCP) server connecting LLM agents (Claude Code, OpenCode) directly to the Telegram Bot API.

<p align="left">
  <a href="https://github.com/M00N77/mcp_telegram"><img src="https://img.shields.io/badge/💻_Repository-181717?style=for-the-badge&logo=github&logoColor=white" /></a>
  <img src="https://img.shields.io/badge/Storage-SQLite_WAL-003B57?style=for-the-badge&logo=sqlite&logoColor=white" />
</p>

<img width="100%" alt="MCP Telegram Server Inspector Preview" src="https://github.com/user-attachments/assets/b13d940e-be9b-41ed-9373-006a03852f64" />

**Stack:** Python 3.12 • FastMCP • SQLite (WAL) • aiosqlite • httpx • asyncio

* **Platform Constraint Bypass:** Background listener + watchdog continuously captures incoming updates into a local state store, enabling discovery and history reads impossible via bare stateless Bot API endpoints.
* **Lock-Free Concurrency:** SQLite in WAL mode prevents lock contention between async listener writes and concurrent tool reads by LLM agents.
* **Idempotency & Delivery:** Composite primary keys (`chat_id`, `message_id`) and offset tracking ensure at-least-once delivery without record duplication.

---

## 🎯 Current Focus

- Agentic engineering workflows (Claude Code, OpenCode CLI, custom MCP tooling)
- High-concurrency backend patterns, distributed caching, and lock-free data structures
- Advanced UI engineering: zero-CLS rendering, canvas visualizers, optimistic data sync

---

## 📬 Contact

<p align="left">
  <a href="https://t.me/manethes"><img src="https://img.shields.io/badge/Telegram-@manethes-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" /></a>
  <a href="mailto:kplatonglfc@gmail.com"><img src="https://img.shields.io/badge/Email-kplatonglfc%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /></a>
</p>
