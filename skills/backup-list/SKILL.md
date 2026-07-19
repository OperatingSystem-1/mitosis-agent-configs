---
name: backup-list
description: List backup snapshots with optional filters for agent name, date range, and pagination. Use when the user asks to see, list, or query existing backups.
version: 1.0.0
tags: ["backup", "list", "query"]
license: Proprietary
metadata:
  vendor: Mitosis Labs
  homepage: https://mitosislabs.ai/backups
---

# List Backups

List backup snapshots for the authenticated user.

## When to use

- The user asks to see, list, or query existing backups
- Auditing what is currently stored

## How

`GET /api/snapshots` with optional query params:

- `agentName` — filter by agent
- `since`, `until` — ISO 8601 bounds
- `limit`, `offset` — pagination
