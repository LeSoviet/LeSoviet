<div align="center">

# Daniel Khadour

**Forward Deployed Engineer · Full-Stack · Applied AI & Cloud**

Vicente López, Buenos Aires, Argentina

[LinkedIn](https://linkedin.com/in/daniel-khadour) · [daniel.w8@outlook.com](mailto:daniel.w8@outlook.com) · [npm](https://www.npmjs.com/package/ghextractor)

</div>

---

Forward Deployed Engineer at **AutarkIA**. I take custom software from the client's ask to production and keep it there: CRM and WhatsApp/Instagram conversational agents, a quoting ERP, public-data dashboards, and the migration of a multitenant messaging transport onto owned infrastructure.

Before that I built **VolApp** end to end — an offline-first fleet management platform with an on-device GPS telemetry pipeline — and worked remotely as a contractor for a Japanese startup (OCR + LLM product matching, Stripe payments).

I'm at my best in inherited systems: I step in, stabilize them, document them, and leave them deployable.

**Open to** Forward Deployed / Solutions Engineer, Full-Stack and Backend roles — remote worldwide, or hybrid in Buenos Aires.

## What I'm working on

**AutarkIA** — client products, all in production · `Python` `TypeScript` `React` `Cloudflare` `PostgreSQL`

- **Gralf · CRM + conversational agent (WhatsApp and Instagram).** Agent loop with tools and hard guardrails, multi-tenant through a YAML file, official Meta WhatsApp (via Faraday) plus Instagram DMs, comments and feed. Modules that replace spreadsheets: price lists imported from `.xlsx`, costing, margins, scenarios, finance and taxes, distribution and coverage. Meta's 24-hour window and a 6-hour takeover cooldown implemented in the engine. The in-app feedback inbox — short code per type, screenshot, JS errors, failed server responses, CSV/Markdown/PDF export — is reused across every AutarkIA product.
- **Faraday · stabilization and infrastructure migration.** Multitenant WhatsApp and Instagram transport: 7 services in Python/Flask, a PHP portal and MariaDB. Moved it off DigitalOcean onto an owned VPS with nginx/TLS, systemd and immutable releases (build → validation → promote → rollback), keeping git history. Own outbox with dedupe, strict per-contract field allowlists and reconciliation of ambiguous deliveries without blind resends.
- **Bitelec · quoting ERP.** TanStack Start + React 19 on Cloudflare Workers with D1. Quotes with materials, tools, UOCRA labor, fees and VAT, live totals and price snapshots — changing a supplier price list never moves old quotes. Depot management with soft-delete and restore, and server-side auth with an HMAC-signed cookie plus a middleware guard.
- **Argydata · public-data dashboard.** INDEC and ArgentinaDatos cross-sections (inflation, poverty, labor, activity, foreign trade, population) behind a proxy that validates datasets, columns, operators and limits, with a KV cache with last-good fallback. Every chart carries a one-line reading and the full table, and values suppressed by statistical secrecy show as `s/d` and are never summed. Plus AutarkIA's SSR landing on Cloudflare Pages with a D1 inbox behind Cloudflare Access.

## VolApp — Founder & Full-Stack Developer

`Java` `React` `Capacitor` `Supabase` `SQLite` `Cloudflare`

Fleet management and dispatch for dumpster rental, shipped as an Android APK and a PWA. Offline-first: a native Java geolocation engine, a local SQLite queue and automatic sync for areas with frequent signal loss.

- **GPS pipeline that runs entirely on the phone** — gates, Kalman filter, validation, output — modeled from academic papers and five frontier LLMs. Filtered distances land within **~5% of ground truth**, the practical limit of phone sensors.
- Validated over **40 real trips** (walking, train, bus, truck and car) against three independent ground truths: routes hand-drawn in Google Maps measured with Haversine, computed Haversine distance, and the vehicle dashboard. A replay harness re-runs recorded tracks and A/B tests the Java engine before every release.
- Multi-tenant with four roles (admin, owner, driver, customer), a unique track ID per delivery or pickup, live tracking and internal chat between owner, driver and customer.
- Serverless routing combining Haversine and Mapbox with dumpster capacity rules; voice-based task creation with Whisper STT + Llama 8B and fuzzy matching against a canonical street database of the Buenos Aires metro area.
- Production on self-hosted Supabase on a droplet: Caddy/Envoy, a Cloudflare Access tunnel for Studio, Prometheus + Grafana + cAdvisor, backups and 65 migrations. Migrating the backend to Cloudflare Workers + D1 + Durable Objects.
- Presented to the CABA and Vicente López governments and at the Vicente López AI competition.

## Kaitomo — Software Engineer, Contractor (Osaka, Japan)

`React Native` `Node.js` `Fastify` `MongoDB` `Stripe`

AI price comparison app. Built the mobile price-tag scanning flow: pick the nearest store from Google Places, scan a product, get it compared against other stores within 3 km.

- OCR + LLM pipeline (Google Cloud Vision, DeepSeek) over **1.4M+ products**, with image preprocessing, prompt refinement and fuzzy matching against canonical tables.
- Moved the catalog from scraped snapshots to live Google Shopping queries through SerpAPI, returning 15–20 store-filtered results.
- Stripe subscriptions, credits and webhooks end to end, plus profiles, follows and bug reporting.
- Zod validation, Swagger docs, Postman E2E covering every endpoint, Vitest and Maestro, Prometheus + Grafana.

## Open source

**[ghextractor](https://github.com/LeSoviet/GithubCLIExtractor)** — CLI and GUI to extract commits, PRs, issues and releases from GitHub repositories with user and date-range filters. Incremental exports 80–95% faster than a full fetch.

![npm](https://img.shields.io/badge/npm-2.9k%2B%20downloads-CB3837?style=flat-square)
![tests](https://img.shields.io/badge/tests-206-brightgreen?style=flat-square)
![stars](https://img.shields.io/github/stars/LeSoviet/GithubCLIExtractor?style=flat-square&color=yellow)

GitHub Actions CI/CD with automatic versioning on merge.

## Toolbox

| Area | Stack |
|---|---|
| **Languages** | TypeScript, Python, Java, Kotlin, JavaScript, PHP, SQL |
| **Frontend** | React 19, TanStack Start, Next.js, Vite, Tailwind CSS, Electron, Capacitor |
| **Mobile** | Native Android (Java/Kotlin), React Native |
| **Backend** | Flask, Django, Node.js, Fastify, REST APIs, Supabase (Edge Functions, self-hosted PostgreSQL), Cloudflare Workers |
| **Data** | PostgreSQL, SQLite, Cloudflare D1, MariaDB, MongoDB, Prisma |
| **Cloud & infra** | Cloudflare Workers/Pages/D1/KV/Access, VPS with nginx/TLS and systemd, immutable releases, Docker, DigitalOcean, Vercel, GitHub Actions |
| **AI / LLM** | tool-using agents with hard guardrails, multi-provider (OpenAI, Gemini, Anthropic, Groq, OpenRouter), Whisper, DeepSeek, Google Cloud Vision |
| **Observability** | Prometheus, Grafana, cAdvisor |

## Selected repositories

- **[GithubCLIExtractor](https://github.com/LeSoviet/GithubCLIExtractor)** — ghextractor: GitHub data to Markdown/JSON, published on npm. `TypeScript`
- **[hos-trip-planner](https://github.com/LeSoviet/hos-trip-planner)** — trip planner with FMCSA hours-of-service compliance and ELD daily log sheets. `Django` `React`
- **[ElHalcon](https://github.com/LeSoviet/ElHalcon)** — auto body shop site with a full quote generator, PDF export and parts management. `Next.js` `TypeScript`
- **[MyRadio](https://github.com/LeSoviet/MyRadio)** — personal radio streaming platform with Icecast, live listeners and an audio visualizer. `Next.js`
- **[hot-and-cold-kotlin](https://github.com/LeSoviet/hot-and-cold-kotlin)** — Android word game with Levenshtein similarity and MVVM. `Kotlin` `Jetpack Compose`
- **[APM-Counter](https://github.com/LeSoviet/APM-Counter)** — Windows overlay that tracks actions per minute in real time. `Tauri` `TypeScript`

Most of my day-to-day work — VolApp, Bitelec, Argydata, Faraday and the AutarkIA products — lives in private repositories because it belongs to clients. Happy to walk through any of it.

## Background

Self-taught, with a high school diploma in Economics. Continuous study of system design, offline-first architecture and LLM integration. Certifications: *React Native — The Practical Guide* and *MongoDB — The Complete Developer's Guide* (Udemy, 2025).

Spanish (native) · English (conversational, B1–B2).
