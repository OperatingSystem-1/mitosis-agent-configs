---
name: backup-subscribe
description: Subscribe to Mitosis Backups via Stripe checkout (USD 2 per month or USD 12 per year). Use when the user wants to start paying for backups; no auth required, email-first flow.
version: 1.0.0
tags: ["backup", "subscribe", "checkout"]
license: Proprietary
metadata:
  vendor: Mitosis Labs
  homepage: https://mitosislabs.ai/backups
---

# Subscribe to Mitosis Backups

Start a paid Mitosis Backups subscription.

## When to use

- The user wants to start paying for backups (USD 2/month or USD 12/year)
- No authentication required — email-first checkout

## How

Navigate to `/backups/checkout?plan=annual` or `/backups/checkout?plan=monthly`. The Stripe checkout flow collects email and payment.
