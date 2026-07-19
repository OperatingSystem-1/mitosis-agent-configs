---
name: backup-create
description: Create an encrypted snapshot of an AI agent workspace. Supports OpenClaw, Hermes, Claude Code, and Codex platforms. Use when the user asks to back up, snapshot, archive, or save agent state.
version: 1.0.0
tags: ["backup", "snapshot", "create"]
license: Proprietary
metadata:
  vendor: Mitosis Labs
  homepage: https://mitosislabs.ai/backups
---

# Create Backup

Create an encrypted snapshot of an AI agent workspace.

## When to use

- The user asks to back up, snapshot, archive, or save agent state
- A scheduled job needs to create a new snapshot
- Before risky operations like migrations or restores

## How

1. POST a multipart upload to `/api/snapshots/upload` with `Authorization: Bearer <api-key>`.
2. Required fields: `agentName`, `platform` (openclaw | hermes | claude-code | codex).
3. Optional: `description`.
4. The response includes a snapshot `id` and S3 location.

See [llms-full.txt](/llms-full.txt) for the full schema.
