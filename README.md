<h1 align="center">Platon Korolev</h1>

<p align="center">
  frontend developer • vue / react / typescript
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

i'm a frontend developer focused on building clean, usable and maintainable web interfaces.

my main interests are:

- product interfaces
- vue / react applications
- frontend architecture
- api integration
- refactoring and improving existing code
- writing code that is easy to read and extend

i like working with real product logic, understanding how data flows through the interface, and turning messy requirements into clear user experiences.

---

## tech stack

**frontend**

![Vue.js](https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D)
![React](https://img.shields.io/badge/React-111827?style=for-the-badge&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-1f2937?style=for-the-badge&logo=typescript&logoColor=3178C6)
![JavaScript](https://img.shields.io/badge/JavaScript-1f2937?style=for-the-badge&logo=javascript&logoColor=F7DF1E)
![HTML5](https://img.shields.io/badge/HTML5-1f2937?style=for-the-badge&logo=html5&logoColor=E34F26)
![CSS3](https://img.shields.io/badge/CSS3-1f2937?style=for-the-badge&logo=css3&logoColor=1572B6)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-1f2937?style=for-the-badge&logo=tailwindcss&logoColor=38B2AC)

**tools & workflow**

![Git](https://img.shields.io/badge/Git-1f2937?style=for-the-badge&logo=git&logoColor=F05032)
![REST API](https://img.shields.io/badge/REST_API-1f2937?style=for-the-badge)
![Linux](https://img.shields.io/badge/Linux-1f2937?style=for-the-badge&logo=linux&logoColor=FCC624)
![VS Code](https://img.shields.io/badge/VS_Code-1f2937?style=for-the-badge&logo=visualstudiocode&logoColor=007ACC)

**familiar with**

![Node.js](https://img.shields.io/badge/Node.js-1f2937?style=for-the-badge&logo=nodedotjs&logoColor=339933)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-1f2937?style=for-the-badge&logo=postgresql&logoColor=4169E1)
![Docker](https://img.shields.io/badge/Docker-1f2937?style=for-the-badge&logo=docker&logoColor=2496ED)
![Next.js](https://img.shields.io/badge/Next.js-1f2937?style=for-the-badge&logo=nextdotjs&logoColor=white)

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

### [Saveur - Table Booking](https://github.com/M00N77/saveur-table-booking)

restaurant table booking page built with **Next.js 16 / React 19 / TypeScript / Tailwind CSS 4 / Vitest**.

[Live demo](https://saveur-table-booking.vercel.app)

technical decisions worth noting:

- **pure utility layer** — `generateTimeSlots` and `formatPhoneNumber` are framework-agnostic pure functions in `utils/`, not hooks. portable, independently testable, zero React coupling
- **form management** — React Hook Form + Zod with schema declared at module level (not inside component), avoiding unnecessary recreation on each render
- **`useWatch` over `watch`** — subscribes only to the `time` field, no cascading re-renders across the whole form
- **`React.memo` on Select** — compares `value`, `error`, `disabled`, `options`. sibling field input does not trigger Select re-render
- **dynamic import for react-day-picker** — calendar chunk loads only on date input click, not in the initial bundle
- **`AbortController` in click-outside effects** — guarantees listener cleanup on unmount, no memory leaks
- **57 tests** covering all edge cases including partial phone input, international prefixes, and malformed strings

---

### [admin-panel](https://github.com/M00N77/admin-panel)

admin panel test task built with **React / TypeScript / Vite / Consta UI**.

[Live demo](https://admin-panel-seven-lac.vercel.app/)

focus:

- GoREST API integration
- users and posts lists with pagination from response headers
- details pages with comments
- access token flow
- loading / error / empty states

---

## current focus

currently building:

- fullstack pet project — next.js + express + postgresql (raw, no orm) in a monorepo
- ai-assisted development workflow (opencode cli + deepseek)
- frontend architecture & design patterns

---

## looking for

i'm open to frontend opportunities where i can work on:

- vue / react applications
- product interfaces with real business logic
- api-driven frontend
- refactoring and code quality
- growing inside a strong engineering team

---

## contact

- telegram: [@manethes](https://t.me/manethes)
- email: **kplatonglfc@gmail.com**
