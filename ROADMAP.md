# RoadPay — Roadmap

## Vision
RoadPay is the payment layer for BlackRoad OS. Built on Stripe, hardened for sovereignty. Accept payments in 135+ currencies, manage subscriptions, prevent fraud, and own your payment infrastructure.

---

## Q1 2026 — Foundation
- [RC] Core charge API with Stripe backend
- [RC] Customer and payment method management
- [RC] Basic subscription create/cancel/update
- [RC] Webhook relay with signature verification
- [RC] Node.js SDK (@roadpay/sdk) v1.0
- [RC] CLI tool for testing and event tailing
- [RC] Sandbox mode with test fixtures
- [RC] Landing page and documentation site

## Q2 2026 — Billing Engine
- [RC] Usage-based billing with metered aggregation
- [RC] Tiered, volume, graduated, and per-seat pricing
- [RC] Smart invoicing with auto-generation
- [RC] PDF invoices with brand customization
- [RC] Dunning management (retry logic + email sequences)
- [RC] Coupon and promotion code system
- [RC] Tax calculation for 40+ jurisdictions
- [RC] Python and Go SDKs

## Q3 2026 — Fraud & Components
- [RC] ML fraud scoring pipeline
- [RC] Custom fraud rule builder
- [RC] 3D Secure handling
- [RC] Device fingerprinting
- [RC] Embedded React checkout component
- [RC] Vue and Svelte checkout components
- [RC] Pricing table component
- [RC] Customer self-service portal
- [RC] RoadCoin token acceptance bridge

## Q4 2026 — Sovereign Mode
- [RC] Self-hosted Docker deployment
- [RC] Kubernetes Helm chart
- [RC] Local PostgreSQL data storage
- [RC] Data residency selection (US, EU, APAC)
- [RC] Revenue analytics dashboard (MRR, churn, LTV)
- [RC] Data warehouse export connectors
- [RC] SOC 2 Type II audit completion
- [RC] WordPress and Shopify plugins

## 2027 — Scale
- [RC] Multi-entity support (hold multiple Stripe accounts)
- [RC] White-label payment pages
- [RC] Advanced cohort and forecasting analytics
- [RC] Marketplace and platform payouts (Connect)
- [RC] On-premise installation for regulated industries
- [RC] PCI DSS Level 1 certification renewal
- [RC] Global payment method expansion (PIX, UPI, SEPA, iDEAL)

---

## Principles
1. **Stripe underneath** — we don't reinvent card processing, we make it better
2. **Bundle, don't nickel-and-dime** — fraud, invoicing, analytics included in every paid plan
3. **Sovereign option** — self-host when you need full data control
4. **Developer-first** — if it takes more than 5 minutes to integrate, we failed
5. **Transparent pricing** — no hidden fees, no surprise charges, no contracts

---

*BlackRoad OS, Inc. — Remember the Road. Pave Tomorrow.*
