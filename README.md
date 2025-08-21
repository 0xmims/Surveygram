# Telegram CRM + Surveys

MVP: Telegram bot + lightweight CRM (contacts/tags) that dispatches surveys to opted-in segments and tracks responses.

**Docs:** See /docs for architecture, flows, API, DB, rate limiting, deployment.  
**Start here:** 1) copy `.env.example` → `.env` 2) `pnpm i` 3) `pnpm dev`.

## Monorepo layout
- apps/bot – Telegraf webhook + handlers
- apps/admin – Next.js admin dashboard (placeholder scaffold)
- packages/db – Prisma schema & client
- packages/queue – BullMQ sender with rate limiting

## Scripts
- `pnpm dev` – run bot, worker, admin locally
- `pnpm db:migrate` – Prisma migrate
- `pnpm test` – vitest unit tests
