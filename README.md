# Mitosis Agent Configs

Ready-to-use configuration for AI coding agents (Claude Code, Cursor, Copilot,
Codex, Windsurf) working with the [Mitosis](https://mitosislabs.ai) platform —
the agent-memory infrastructure by Mitosis Labs.

## What's here

- **`AGENTS.md`** — the canonical agent instructions: how to query Mitosis
  memory, call the public API, and connect over MCP
- **`.cursorrules`** — the same guidance packaged for Cursor
- **`claude/CLAUDE.md`** — drop-in project instructions for Claude Code
- **`mcp.json`** — MCP client configuration for the Mitosis servers

## Quick start

Connect any MCP client to the public server (no auth):

```json
{
  "mcpServers": {
    "mitosis": {
      "type": "streamable-http",
      "url": "https://mitosislabs.ai/api/mcp"
    }
  }
}
```

Or use the REST API directly: [`https://mitosislabs.ai/api/v1`](https://mitosislabs.ai/api/v1)
(OpenAPI spec at [/openapi.json](https://mitosislabs.ai/openapi.json)).

## Agent skills

[![skills.sh](https://skills.sh/b/operatingsystem-1/mitosis-agent-configs)](https://www.skills.sh/operatingsystem-1/mitosis-agent-configs)

The official Mitosis backup skills live in [`skills/`](skills/) and are
published on [skills.sh](https://www.skills.sh/operatingsystem-1/mitosis-agent-configs):

```bash
npx skills add OperatingSystem-1/mitosis-agent-configs
```

Skill manifests are also served (with content digests) from
https://mitosislabs.ai/.well-known/agent-skills/index.json.

## Machine surfaces

| Surface | URL |
|---|---|
| llms.txt | https://mitosislabs.ai/llms.txt |
| MCP server | https://mitosislabs.ai/api/mcp |
| REST API | https://mitosislabs.ai/api/v1 |
| Auth walkthrough | https://mitosislabs.ai/auth.md |
| Pricing | https://mitosislabs.ai/pricing.md |
| Agent skills | https://mitosislabs.ai/.well-known/agent-skills/index.json |

MIT licensed. Maintained by [Mitosis Labs](https://mitosislabs.ai/contact).
