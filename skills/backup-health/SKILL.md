---
name: backup-health
description: Check current backup health: last snapshot, schedule status, and storage usage. Use when auditing whether backups are current.
version: 1.0.0
tags: ["backup", "audit", "health"]
license: Proprietary
metadata:
  vendor: Mitosis Labs
  homepage: https://mitosislabs.ai/backups
---

# Check Backup Health

Audit whether backups are current.

## When to use

- The user asks "are my backups working" or "when was my last backup"

## How

`GET /api/snapshots/health` returns last snapshot time, active schedules, and storage usage.
