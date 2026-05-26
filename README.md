👋 Hi, I'm Daniel Khadour — Full-Stack & AI Engineer

> Full-stack developer building end-to-end AI-powered products and shipping them to real users.
> Based in Vicente López, Buenos Aires 🇦🇷

---

## 🚀 About me

- Building **VolApp** — a production fleet GPS tracking platform for dump truck companies in Buenos Aires
- Contractor at **Kaitomo** (Japan 1y) — OCR + LLM scanning pipeline + price comparison (1M+ scraped products)
- Published **ghextractor** on npm — 2,900+ downloads, open source CLI + Electron GUI
- Heavy agentic coding user — used every major model in every harness. Currently: Claude Code + GLM, Codex + GPT-5.5, Kilo + Ollama cloud
- I break things, test, break again, test again — until it feels right. If it doesn't feel perfect I keep pushing

---

## 🛠 Tech Stack

**Languages:** TypeScript · JavaScript · Java · SQL  
**Frontend:** React 18 · Next.js · React Native (Expo) · Tailwind CSS · Electron · Vite  
**Backend:** Node.js · Fastify · Supabase (PostgreSQL · Auth · Realtime · RPC · Edge Functions)  
**AI / ML:** Prompt engineering · Llama 8B · DeepSeek · GPT-4 · Claude · Whisper STT · Google Cloud Vision · OCR pipelines  
**Mobile:** Capacitor · Android Foreground Service (Java/Kotlin) · SQLite offline queues  
**Databases:** PostgreSQL · MongoDB (Prisma ORM) · SQLite · Redis  
**DevOps:** GitHub Actions CI/CD · Docker · Google Cloud · Prometheus · Grafana · Vercel  
**Testing:** Vitest · Jest · Maestro (E2E mobile)  

---

## 📦 Featured Projects (Private)

### 🚛 VolApp — Fleet GPS Tracking Platform

Full-stack fleet management for dump truck companies. React + Capacitor mobile app, multi-tenant dashboard, Supabase backend with 55+ tables, 80+ RPC functions, 30+ triggers.

- 7-filter GPS quality pipeline in a PostgreSQL BEFORE INSERT trigger
- Native Android foreground service (Java) with SQLite offline queue
- 9-stage offline recovery system with watchdog timers
- Voice-to-task: Whisper STT → Llama 3.1-8b → 5-tier geocoding fallback with the full AMBA street dictionary

`React` `TypeScript` `Supabase` `Capacitor` `Android (Java)` `Mapbox` `Groq API`

> 3 companies using it in production. I walk the streets weekly collecting feedback.  
> Walked ~50km on foot to tune GPS at low velocity simulating truck speed.  
> 30+ hours testing voice input until fuzzy + canonical matching on AMBA streets actually worked.  
> Each truck: ~3% CPU, 5 DB pools. Heavy lifting on the frontend + batching keeps it cheap even with realtime.  
> Ships as Web + PWA + APK (with OTA versioning) + Java native. Missing iOS — no Mac, no iPhone, but Capacitor can handle it.

---

### 📱 Kaitomo — Price Scanner App

Full-stack mobile app: barcode/receipt scanning, price comparison via Google Shopping, price history tracking, social features, Stripe payments. Built as contractor, end-to-end.

- OCR + LLM pipeline (Google Cloud Vision + DeepSeek) over 1.4M scraped products
- 285+ tests (Vitest unit/integration + Maestro E2E on physical Android device)
- GitHub Actions CI/CD with nightly test pipelines

`React Native` `Expo` `Fastify` `MongoDB` `Prisma` `Stripe` `Docker` `GitHub Actions`

> 3-person startup: Juan (PM), Cami (Sr), me (everything else).  
> Started doing small UI buttons, ended up owning the full pipeline: Docker, Prometheus/Grafana monitoring, CI/CD, Vitest suite, OCR pipeline, and most of the frontend.  
> Stack from mid-2025: Windsurf + Claude Code. Early stage: GPT + GLM.

---

### 🔍 [ghextractor](https://www.npmjs.com/package/ghextractor) — Open Source CLI + GUI · ![npm](https://img.shields.io/npm/v/ghextractor.svg) ![downloads](https://img.shields.io/npm/dt/ghextractor.svg)

Cross-platform GitHub data extraction tool. Interactive CLI (Ink terminal UI) + Electron GUI sharing the same engine. Exports PRs, commits, issues, branches, releases → Markdown / JSON / PDF.

- Incremental export engine: 80–95% faster on repeated exports
- Offline analytics engine (trends, predictions, velocity charts — zero API calls)
- 206 tests, semantic versioning CI/CD, published on npm

`TypeScript` `Node.js` `Electron` `Ink` `pdfkit` `GitHub CLI` `Vitest`

> Works well — useful for PMs doing repo reporting. Hard to have open repos these days but roughly 1k real downloads (tracked via Reddit traffic). Rest might be bots. It is what it is.

---

## 📫 Contact

- 📧 daniel.w8@outlook.com
- 💼 [linkedin.com/in/daniel-khadour](https://linkedin.com/in/daniel-khadour)
- 🐙 [github.com/LeSoviet](https://github.com/LeSoviet)

*"Último Commit"* — that's a lie.
