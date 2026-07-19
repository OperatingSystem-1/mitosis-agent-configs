---
name: backup-diff
description: Compare two backup snapshots by id and report which files changed. Use when investigating workspace drift between two points in time.
version: 1.0.0
tags: ["backup", "diff", "audit"]
license: Proprietary
metadata:
  vendor: Mitosis Labs
  homepage: https://mitosislabs.ai/backups
---

# Diff Backups

Compare two snapshots and report which files changed.

## When to use

- The user is investigating workspace drift between two points in time

## How

`GET /api/snapshots/diff?a=<id>&b=<id>`
