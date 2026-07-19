---
name: backup-restore
description: Restore a backup snapshot to an agent workspace from S3 by snapshot id. Use when the user asks to recover, roll back, or restore an agent.
version: 1.0.0
tags: ["backup", "restore", "recovery"]
license: Proprietary
metadata:
  vendor: Mitosis Labs
  homepage: https://mitosislabs.ai/backups
---

# Restore Backup

Restore a snapshot to an agent workspace from S3.

## When to use

- The user asks to recover, roll back, or restore an agent

## How

`POST /api/snapshots/restore` with JSON body `{ "snapshotId": "snap_..." }`.
