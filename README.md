<div align="center">
<img src="https://images.blackroad.io/pixel-art/road-logo.png" alt="BlackRoad OS" width="80" />

# RoadPay

**Own your billing. D1 subscriptions, plans, invoices. Stripe is the card charger — you are the bank.**

[![BlackRoad OS](https://img.shields.io/badge/BlackRoad_OS-Pave_Tomorrow-FF2255?style=for-the-badge&labelColor=000000)](https://blackroad.io)
[![License](https://img.shields.io/badge/License-Proprietary-FF6B2B?style=for-the-badge&labelColor=000000)](./LICENSE)
</div>

---

## Architecture

```
User → RoadPay (D1) → Stripe (card processing only)
         ↓
    Plans, Invoices, Subscriptions
    stored in YOUR database
```

RoadPay is BlackRoad's own billing system. Stripe handles card charging — nothing else. All subscription logic, plan management, invoicing, and metering lives in D1 (Cloudflare's serverless SQL).

## Plans

| Plan | Price | Agents | Requests/Day | Support |
|------|-------|--------|-------------|---------|
| Starter | Free | 1 | 100 | Community |
| Pro | $29/mo | 5 | 10K | Priority |
| Team | $99/mo | 25 | 100K | Dedicated |
| Enterprise | Custom | Unlimited | Unlimited | SLA |

## Add-ons

| Add-on | Price | Description |
|--------|-------|-------------|
| Extra TOPS | $19/mo | Additional AI compute |
| Custom Models | $49/mo | Fine-tune your own |
| Priority Inference | $9/mo | Skip the queue |
| Dedicated Node | $149/mo | Your own Pi 5 |

## API

```bash
# Create checkout session
curl -X POST https://roadpay.blackroad.io/api/checkout \
  -H "Content-Type: application/json" \
  -d '{"plan": "pro", "billing_cycle": "monthly"}'

# Check subscription
curl https://roadpay.blackroad.io/api/subscription \
  -H "Authorization: Bearer $TOKEN"
```

## Stack

- **Runtime**: Cloudflare Workers
- **Database**: D1 (SQLite at the edge)
- **Payments**: Stripe (card processing only)
- **Auth**: JWT via blackroad-auth

## Development

```bash
npm install
npm run dev     # Wrangler dev server
npm run deploy  # Deploy to Cloudflare
```

---

*Copyright (c) 2024-2026 BlackRoad OS, Inc. All rights reserved.*
