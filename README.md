# Projects Showcase — Marc Torres

Two full-stack products I'm building on my own with **Next.js, React and TypeScript**.

> 🔒 The source code is private. This repo explains what each project does and how it's built.
> Happy to walk through the code in an interview — reach me on [LinkedIn](https://www.linkedin.com/in/marctorresmartinez).

| Project | What it is | Status | Link |
|---|---|---|---|
| **KambioMatch** | Crypto exchange comparison platform | Deployed, pre-launch | [kambiomatch.com](https://kambiomatch.com) |
| **BallFunds** | Funded-account evaluation platform for simulated sports betting | Pre-launch | [fondeo-deportivo.vercel.app](https://fondeo-deportivo.vercel.app) |

---

## 🔎 KambioMatch

**[kambiomatch.com](https://kambiomatch.com)** · Oct 2026 – present · Founder & Full-Stack Developer

A bilingual (ES/EN) platform that helps people choose a crypto exchange. It compares **22 exchanges across 66 countries** by fees, licences, availability and deposit methods, with geo-aware results and a fee calculator.

**Stack:** `Next.js 16` `React 19` `TypeScript` `Tailwind CSS` `PostgreSQL (Supabase)` `Prisma` `Vitest` `Playwright` `Vercel`

### Highlights

- **Architecture:** Next.js App Router with Partial Prerendering. 590 SEO-ready static pages, with visitor-specific content streamed through `<Suspense>` and only 8 client components.
- **Performance:** Lighthouse mobile scores of **94–100 for Performance** and **100 for Accessibility, Best Practices and SEO** across 9 page templates, with zero layout shift (CLS 0).
- **Secure server code:** Server Actions and route handlers with Zod validation, Cloudflare Turnstile, per-IP rate limiting, transactional deduplication with Postgres advisory locks, and idempotent email delivery with retries and a daily cron safety net.
- **Privacy-friendly analytics:** geo-aware outbound redirect service with hashed IPs, bot filtering and automated data retention.
- **Tested domain logic:** scoring formula, tiered fee calculator and recommendation engine written as pure TypeScript, covered by **209 unit tests** (Vitest) and **65 end-to-end tests** (Playwright).
- **Security & automation:** Content Security Policy, row-level security, Dependabot, and a monthly GitHub Actions job that flags outdated data.

### Lighthouse (mobile, median of 3 runs per template)

| Template | Performance | LCP | CLS |
|---|---|---|---|
| Home | 95 | 1.12 s | 0 |
| Review | 100 | 1.07 s | 0 |
| Country | 97 | 1.15 s | 0 |
| Comparison | 98 | 1.06 s | 0 |
| Calculator | 99 | 1.08 s | 0 |
| Blog | 96 | 0.95 s | 0 |
| FAQ | 100 | 1.07 s | 0 |
| Methodology | 99 | 0.92 s | 0 |
| Contact | 97 | 0.97 s | 0 |

Accessibility, Best Practices and SEO: 100 on all 9 templates. *Lab data from a local production build.*

<!-- Screenshots: add images to a /screenshots folder and uncomment
![KambioMatch home](screenshots/kambiomatch-home.png)
-->

---

## ⚽ BallFunds

**[fondeo-deportivo.vercel.app](https://fondeo-deportivo.vercel.app)** · Jan 2026 – present · Founder & Full-Stack Developer

A funded-account evaluation platform for **simulated** sports betting: users take multi-phase challenges with profit targets and risk rules. No real-money bets are placed on the platform.

**Stack:** `Next.js 16` `React 19` `TypeScript` `PostgreSQL (Supabase)` `Prisma` `Stripe` `NextAuth` `Tailwind CSS` `Radix UI` `Vitest`

### Highlights

- **Full-stack Next.js product:** App Router with React Server Components, Server Actions and route handlers. **31 database models**, a user area and a full admin panel, in English and Spanish (next-intl).
- **Payments:** Stripe Checkout with signed, idempotent webhooks covering payments, refunds, chargebacks and fee reconciliation, plus PDF receipts and financial reports.
- **Auth & security:** NextAuth with role-based access, TOTP two-factor authentication, single-use team invitations and server-enforced confirmation for money-moving actions, all recorded in an audit log.
- **Built for serverless:** pooled PostgreSQL connections with retries on transient failures, PostgreSQL-backed rate limiting and cron-refreshed snapshots for expensive admin views.
- **Performance:** cut a 20,000-user comparison from **over 2 minutes to about 0.2 s**, with identical results, by replacing an all-pairs algorithm with an inverted index.
- **Testing:** **1,100+ automated tests** with Vitest and Testing Library, including integration tests against a real PostgreSQL database, with type checks, linting and builds in GitHub Actions CI.
- **Domain logic & AI:** rules-based risk engine (drawdown, time limits, automated settlement) and an OpenAI-powered support assistant with per-user context and rate limits.

<!-- Screenshots: add images to a /screenshots folder and uncomment
![BallFunds dashboard](screenshots/ballfunds-dashboard.png)
-->

---

## 👋 About me

Full-stack developer specialized in **React/Next.js, .NET and AI agents**, with 4+ years of experience building applications for international clients.
Microsoft Certified: Azure Developer Associate (AZ-204) and Azure Data Scientist Associate (DP-100).

📫 [LinkedIn](https://www.linkedin.com/in/marctorresmartinez)
