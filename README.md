<h1 align="center">Platon Korolev</h1>

<p align="center">
  fullstack developer • react / vue / node.js / python
</p>

<p align="center">
  <a href="https://t.me/manethes">
    <img src="https://img.shields.io/badge/Telegram-@manethes-09090b?style=flat-square&logo=telegram&logoColor=26A5E4" />
  </a>
  <a href="mailto:kplatonglfc@gmail.com">
    <img src="https://img.shields.io/badge/Email-contact-09090b?style=flat-square&logo=gmail&logoColor=EA4335" />
  </a>
  <img src="https://img.shields.io/badge/Location-Moscow-09090b?style=flat-square&logo=googlemaps&logoColor=white" />
</p>

---

## about

i'm a fullstack developer focused on building clean, usable and maintainable web applications — from the interface down to the database.

my main interests are:

- product interfaces
- react / vue applications
- frontend architecture
- backend logic, api design & sql / nosql databases
- ai integration (llm routing, mcp, rag)
- refactoring and improving existing code
- writing code that is easy to read and extend

i like working with real product logic, understanding how data flows through the whole system — from the database to the UI — and turning messy requirements into clear user experiences.

---

## tech stack

**frontend**<br>
<a href="https://skillicons.dev">
  <img src="https://skillicons.dev/icons?i=react,vue,nextjs,ts,js,tailwind,html,css&theme=dark" alt="frontend stack" />
</a>
<br><br>

**backend & databases**<br>
<a href="https://skillicons.dev">
  <img src="https://skillicons.dev/icons?i=nodejs,python,express,postgres,sqlite&theme=dark" alt="backend stack" />
</a>
<br>
<sup>*also working with nosql/vector databases (qdrant) and jwt auth*</sup>
<br><br>

**tools & workflow**<br>
<a href="https://skillicons.dev">
  <img src="https://skillicons.dev/icons?i=git,docker,linux,vscode&theme=dark" alt="tools" />
</a>

---

## featured projects

### [TelegramHelper](https://github.com/M00N77/tg-helper)

ai-powered assistant for pm / dev teams built in a hackathon sprint.

evolved from a personal assistant into a full team pm tool running in telegram groups.

**stack:** `python` `aiogram 3` `telethon` `sqlalchemy async` `postgresql` `qdrant` `openai` `gemini` `groq` `docker`

key features:

- natural language interface — write to the bot like a human, the llm agent understands intent
- meeting transcription → summary → kanban tasks in YouGile (one flow)
- burnout analysis based on outgoing message tone
- daily standups, blocker escalation, anonymous pulse surveys
- real-time message mirroring via MTProto userbot
- 9 background tasks running in a single asyncio event loop
- fernet/aes encryption for all api keys and session data
- rbac with director / member roles and approval flow

> finalist project — Цифровой прорыв (national hackathon, competed with middle/senior teams)

---

### [MCP Telegram Server](https://github.com/M00N77/mcp_telegram)

model context protocol (mcp) server connecting llm agents (like claude) directly to the telegram bot api. turns a stateless push-api into a stateful, discoverable context for ai.

**stack:** `python 3.12` `fastmcp` `aiosqlite` `httpx`

key features:
- architectural workaround for api constraints — background listener continuously syncs updates to a local db, allowing mcp tools to perform discovery and history reads that telegram natively lacks
- concurrency-safe storage — sqlite in wal mode prevents locks between the async listener (writes) and mcp tools (reads)
- idempotent operations — composite keys (`chat_id`, `message_id`) and offset tracking ensure at-least-once delivery without duplicate records after network restarts
- human-in-the-loop — built-in approval gate for the `send_message` tool to prevent unverified ai actions
- token-optimized parsing — plain text history formatting natively understood by llms, avoiding json escaping issues

> designed as a robust local adapter to give llms persistent memory over stateless platforms

---

### [Mini CRM](https://github.com/M00N77/mini-crm/tree/main)

fullstack CRM for managing contacts, tasks and notes. next.js frontend connected to a raw express + postgresql backend — no ORM.

**stack:** `next.js 16` `react 19` `typescript` `tailwind css v4` `express 5` `postgresql 17` `jwt`

key features:

- JWT auth — access token (15 min, bearer) + refresh token in httpOnly cookie, with rotation and race-condition-safe refresh (concurrent 401s share a single in-flight refresh, no duplicate token issuance)
- kanban board with drag-and-drop status changes (@hello-pangea/dnd)
- strict separation of transport / auth / features / types layers — DTO ≠ domain, every feature has its own mapper normalizing snake_case/camelCase server responses into clean domain types
- in-memory token store (not React context) — access token available synchronously outside React, zero unnecessary re-renders
- logout via event-bus — failed refresh clears token and emits logout, AuthProvider resets user + cache
- raw SQL, no ORM — full control over queries, explicit understanding of what happens under the hood

---

### [IRS Dashboard](https://github.com/M00N77/dashboard-irs)

modern SPA reimagining a heavy government-style case management portal (based on ППК РЭО) as a fast, responsive dashboard.

[Live demo](https://dashboard-irs.vercel.app)

**stack:** `react 19` `vite 6` `typescript` `mui 9` `tanstack query 5` `tanstack table 8` `react hook form + zod` `recharts` `msw` `faker`

key features:

- master-detail interface — registry list + person card with tabs (general info, family, education, housing, appeals)
- server-side pagination, filtering and sorting — even on mocked data, via MSW handlers
- PersonSummary vs PersonDetails — list endpoint returns only table fields, full profile loads on demand, mirroring real REST API practice
- Feature-Sliced Design — strict layer hierarchy (app / pages / widgets / features / entities / shared)
- measured Core Web Vitals: **LCP 1.71s / 1.92s, CLS 0** — optimized via priority routing, explicit skeleton dimensions, deferred mock data loading after initial render

![Registry performance](https://dashboard-irs.vercel.app/preview/lighthouse-registry.png)
![Dashboard performance](https://dashboard-irs.vercel.app/preview/lighthouse-dashboard.png)

---

## current focus

currently building:

- ai-assisted development workflow (claude code, opencode cli)
- deeper backend architecture — race conditions, token rotation, raw SQL performance
- frontend architecture & design patterns

---

## looking for

i'm open to fullstack / frontend opportunities where i can work on:

- react / vue applications with real backend logic
- product interfaces with real business logic
- api-driven, database-backed systems
- refactoring and code quality
- growing inside a strong engineering team

---

## contact

- telegram: [@manethes](https://t.me/manethes)
- email: **kplatonglfc@gmail.com**
- 
