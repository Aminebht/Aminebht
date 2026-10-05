# Med Amine Belhadj Taher

**Founder & CTO of [Demarky](https://demarky.ai)** , an AI website generator with a built-in CRM, now at **2,731 users** and **4,599 generated sites**. Third-year Computer Engineering student at the Faculty of Sciences of Tunis.

I build on the platform side: multi-tenant edge hosting, partner-facing APIs, and LLM agent runtimes.

**Open to a 6-month final-year internship (PFE) from February 2027** . Full-stack, cloud/DevOps, or applied AI.

---

### A note on what's public here

Demarky is a commercial product, so its codebase is private. The running product is the artefact — **[demarky.ai](https://demarky.ai)** — and what follows is a description of what I built and why. Happy to walk through any of it in detail.

---

## Selected work

**AI Builder Agent** — conversational control of the entire builder
Every action in the product is reachable through chat: adding and restyling components, generating copy and images, routing, SEO, checkout, domains. I built the runtime behind it — **39 typed tools** over a streaming multi-turn loop on server-sent events, with server-side tool resolution, loop detection on repeated calls, and confirmation gates before anything destructive runs.
`Deno` · `Supabase Edge Functions` · `LLM tool calling` · `SSE`

**Edge deployment infrastructure** — Vercel to Cloudflare migration
Replaced Vercel with a purpose-built architecture on Cloudflare R2, Workers and KV, and **cut hosting cost by 60%**. Multi-tenant edge routing resolves customer custom domains through KV-backed hostname lookup via Cloudflare for SaaS, with a headless renderer Worker producing static HTML server-side.
`Cloudflare Workers` · `R2` · `KV` · `Cloudflare for SaaS` · `Wrangler`

**Partner integration API** — a public REST surface for third-party apps
OAuth 2.0 installation flow with scoped tokens, at-least-once webhook delivery over a transactional outbox with HMAC-SHA256 signed payloads, per-tenant rate limiting on Durable Objects, and DNS-level SSRF validation on partner-supplied webhook URLs — all against a CI-verified OpenAPI contract.
`Cloudflare Workers` · `Durable Objects` · `OpenAPI` · `PostgreSQL` · `OAuth 2.0`

**AI-augmented development pipeline**
Moved first-pass code review into CI to clear the bottleneck created by the volume of AI-generated code. Path-scoped review rules — migration idempotency, pinned imports, secret detection — run alongside lint, type-check, OpenAPI contract verification and 37 test suites, each PR against an ephemeral database branch.
`GitHub Actions` · `Vitest` · `Playwright` · `Supabase CLI`

---

## Stack

**Languages** TypeScript · JavaScript · SQL (PL/pgSQL)
**Backend & web** Node.js · Deno · React · REST · OpenAPI · webhooks · idempotency
**Data** PostgreSQL · row-level security · schema migrations · concurrency control · Redis · Supabase
**Cloud & DevOps** Cloudflare (Workers, Durable Objects, R2, KV) · AWS (EC2, RDS, CloudFront, CloudWatch) · Docker · GitHub Actions · CI/CD
**AI engineering** agent orchestration · tool/function calling · MCP · streaming inference · guardrails and human oversight · multi-provider fallback
**Security** OAuth 2.0 · HMAC request signing · encrypted secrets with key rotation · SSRF validation · rate limiting

Arabic (native) · French (C1) · English (B2)

---

## Reach me

[LinkedIn](https://www.linkedin.com/in/medaminebht/) · medaminebht7@gmail.com · [demarky.ai](https://demarky.ai)
