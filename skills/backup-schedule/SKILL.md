---
name: backup-schedule
description: Create, read, or update an automated backup schedule with cron expression and retention policy. Use when the user asks to schedule or automate backups.
version: 1.0.0
tags: ["backup", "schedule", "cron"]
license: Proprietary
metadata:
  vendor: Mitosis Labs
  homepage: https://mitosislabs.ai/backups
---

# Manage Backup Schedules

Create, read, or update automated backup schedules.

## When to use

- The user asks to automate or schedule backups, set retention, or change cadence

## How

- `GET /api/snapshots/schedules` to list
- `PUT /api/snapshots/schedules` with `{ cron, retentionDays }` to upsert
