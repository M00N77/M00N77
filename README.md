<h1 align="center">Platon Korolev</h1>

<p align="center">
  fullstack developer • vue / react / node.js / typescript
</p>

<p align="center">
  <a href="https://t.me/manethes">
    <img src="https://img.shields.io/badge/Telegram-@manethes-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" />
  </a>
  <a href="mailto:kplatonglfc@gmail.com">
    <img src="https://img.shields.io/badge/Email-contact-EA4335?style=for-the-badge&logo=gmail&logoColor=white" />
  </a>
  <img src="https://img.shields.io/badge/Location-Moscow-111827?style=for-the-badge" />
</p>

---

## about

i'm a fullstack developer focused on building clean, usable and maintainable web applications — from the interface down to the database.

my main interests are:

- product interfaces
- vue / react applications
- frontend architecture
- backend logic and REST API design
- api integration
- refactoring and improving existing code
- writing code that is easy to read and extend

i like working with real product logic, understanding how data flows through the whole system — from the database to the UI — and turning messy requirements into clear user experiences.

---

## tech stack

**frontend**

![Vue.js](https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D)
![React](https://img.shields.io/badge/React-111827?style=for-the-badge&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-1f2937?style=for-the-badge&logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-1f2937?style=for-the-badge&logo=typescript&logoColor=3178C6)
![JavaScript](https://img.shields.io/badge/JavaScript-1f2937?style=for-the-badge&logo=javascript&logoColor=F7DF1E)
![HTML5](https://img.shields.io/badge/HTML5-1f2937?style=for-the-badge&logo=html5&logoColor=E34F26)
![CSS3](https://img.shields.io/badge/CSS3-1f2937?style=for-the-badge&logo=css3&logoColor=1572B6)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-1f2937?style=for-the-badge&logo=tailwindcss&logoColor=38B2AC)

**backend**

![Node.js](https://img.shields.io/badge/Node.js-1f2937?style=for-the-badge&logo=nodedotjs&logoColor=339933)
![Express](https://img.shields.io/badge/Express-1f2937?style=for-the-badge&logo=express&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-1f2937?style=for-the-badge&logo=postgresql&logoColor=4169E1)
![JWT](https://img.shields.io/badge/JWT-1f2937?style=for-the-badge&logo=jsonwebtokens&logoColor=white)

**tools & workflow**

![Git](https://img.shields.io/badge/Git-1f2937?style=for-the-badge&logo=git&logoColor=F05032)
![REST API](https://img.shields.io/badge/REST_API-1f2937?style=for-the-badge)
![Docker](https://img.shields.io/badge/Docker-1f2937?style=for-the-badge&logo=docker&logoColor=2496ED)
![Linux](https://img.shields.io/badge/Linux-1f2937?style=for-the-badge&logo=linux&logoColor=FCC624)
![VS Code](https://img.shields.io/badge/VS_Code-1f2937?style=for-the-badge&logo=visualstudiocode&logoColor=007ACC)

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

- vue / react applications with real backend logic
- product interfaces with real business logic
- api-driven, database-backed systems
- refactoring and code quality
- growing inside a strong engineering team

---

## contact

- telegram: [@manethes](https://t.me/manethes)
- email: **kplatonglfc@gmail.com**
