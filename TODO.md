# RoadPay — TODO

## [RC] Core Payment Engine
- [ ] Stripe Connect integration for marketplace payouts
- [ ] Multi-currency settlement accounts (USD, EUR, GBP, JPY)
- [ ] Idempotency key middleware for all charge endpoints
- [ ] Webhook signature verification library (Node, Python, Go, Ruby)
- [ ] Rate limiting per API key with sliding window

## [RC] Subscription Billing
- [ ] Metered usage billing engine with real-time aggregation
- [ ] Tiered + volume + graduated pricing model support
- [ ] Free trial → paid conversion flow with dunning
- [ ] Proration logic for mid-cycle plan changes
- [ ] Subscription pause/resume without cancellation
- [ ] Coupon and promotion code system

## [RC] Invoicing
- [ ] Auto-generate invoices from subscription charges
- [ ] Custom line items, discounts, tax overrides
- [ ] PDF generation with brand customization
- [ ] Hosted invoice page with embedded payment
- [ ] Late payment reminder sequence (3-touch)
- [ ] Partial and installment payment support

## [RC] Fraud Detection
- [ ] ML risk scoring pipeline (integrate Stripe Radar)
- [ ] Custom rule builder UI (country, velocity, amount, device)
- [ ] 3D Secure challenge flow handler
- [ ] Device fingerprinting integration
- [ ] Manual review queue with team assignment
- [ ] Chargeback auto-evidence submission

## [RC] SDK & Developer Experience
- [ ] @roadpay/sdk npm package (TypeScript)
- [ ] roadpay-python PyPI package
- [ ] roadpay-go module
- [ ] CLI tool: `npx roadpay init`, `listen`, `trigger`
- [ ] OpenAPI 3.1 spec generation from routes
- [ ] Sandbox mode with test card numbers

## [RC] Embedded Components
- [ ] React checkout component
- [ ] Vue checkout component
- [ ] Svelte checkout component
- [ ] Pricing table component (all frameworks)
- [ ] Customer portal component (manage subscriptions)
- [ ] WCAG 2.1 AA accessibility audit

## [RC] Analytics & Reporting
- [ ] Real-time MRR / ARR dashboard
- [ ] Churn analysis and cohort tracking
- [ ] LTV calculation per customer segment
- [ ] Revenue forecasting model
- [ ] CSV + JSON export endpoints
- [ ] Data warehouse connector (BigQuery, Snowflake, Redshift)

## [RC] Security & Compliance
- [ ] PCI DSS Level 1 compliance documentation
- [ ] SOC 2 Type II audit preparation
- [ ] Data residency selection (US, EU, APAC)
- [ ] Role-based access control with API key scoping
- [ ] Full audit log for all API access
- [ ] Bug bounty program setup

## [RC] Self-Hosted (Sovereign Mode)
- [ ] Docker Compose deployment package
- [ ] Kubernetes Helm chart
- [ ] PostgreSQL schema for local data storage
- [ ] Stripe webhook relay for self-hosted instances
- [ ] Configuration management (env vars + config file)
- [ ] Health check and monitoring endpoints

## [RC] Integrations
- [ ] WordPress / WooCommerce plugin
- [ ] Shopify app
- [ ] Zapier integration (triggers + actions)
- [ ] RoadCoin token acceptance (Q3 2026)
- [ ] QuickBooks / Xero accounting sync
- [ ] Slack notifications for payments + disputes
