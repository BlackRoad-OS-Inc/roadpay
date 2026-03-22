# RoadPay

Billing and subscription management. Stripe handles the cards. Your data stays in your database.

**Live at [pay.blackroad.io](https://pay.blackroad.io)**

## What It Does

RoadPay manages plans, subscriptions, invoices, and customer records. Stripe is used only for card processing. All billing logic and data live in D1.

## Plans

| Plan | Price | For |
|------|-------|-----|
| **Starter** | Free | Getting started, 1 agent, 100 req/day |
| **Pro** | $29/mo | Individuals, 5 agents, 10K req/day |
| **Team** | $99/mo | Small teams, 25 agents, 100K req/day |
| **Enterprise** | Custom | Unlimited agents and requests, SLA |

## API

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/api/checkout` | POST | Create a checkout session for a plan |
| `/api/subscription` | GET | Check current subscription status |
| `/plans` | GET | List available plans and pricing |
| `/customers` | GET/POST | Manage customer records |
| `/invoices` | GET | View invoice history |
| `/webhook` | POST | Stripe event receiver |

## Stack

- **Runtime**: Cloudflare Worker
- **Database**: D1 (customers, invoices, subscriptions)
- **Payments**: Stripe (card processing only)
- **Auth**: JWT tokens

## Deploy

```bash
npm install
npm run dev        # Local dev server
npm run deploy     # Deploy to production
```

Set Stripe keys:

```bash
wrangler secret put STRIPE_SECRET_KEY
wrangler secret put STRIPE_WEBHOOK_SECRET
```

## How It Works

1. Customer picks a plan and checks out
2. RoadPay creates the Stripe subscription
3. Invoice and subscription state is stored locally in D1
4. Webhooks keep D1 in sync with Stripe events
5. All queries (plan changes, invoices, status) hit your database, not Stripe

Your customer records. Your invoice history. Your database. Stripe only touches the card.

## License

Proprietary. Copyright (c) 2024-2026 BlackRoad OS, Inc. All rights reserved.

---

*Remember the Road. Pave Tomorrow.*
