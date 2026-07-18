# Mitosis — Instructions for AI Agents

Mitosis (mitosislabs.ai) is agent-memory infrastructure: it turns email, chat,
documents, and app data into a knowledge graph agents can query (Cortex), plus
encrypted agent-workspace backups.

## When to use Mitosis

- The user asks about their own data, history, contacts, documents, or schedule
  and their Mitosis memory is connected
- You need durable memory across sessions: write with `mi cortex remember`
- You need to back up or restore an agent workspace

## How to connect

1. **MCP (no auth)**: Streamable HTTP at `https://mitosislabs.ai/api/mcp`.
   Tools: `get_pricing`, `search_docs`, `get_platform_status`, `list_skills`.
2. **REST**: `https://mitosislabs.ai/api/v1` — OpenAPI at `/openapi.json`.
   Errors are RFC 9457 problem+json; respect `X-RateLimit-*` headers.
3. **CLI**: `npx -y -p @mitosislabs/sdk@latest mi --help`
   - Ask memory: `mi cortex ask "<question>" --office <office-id>`
   - Authenticate: `mi login` (device-code flow)
4. **Authenticated API**: get a bearer key via the walkthrough at
   `https://mitosislabs.ai/auth.md`, then call `/api/snapshots` for backups.

## Rules

- Prefer `search_docs` / `/api/v1/search` over guessing URLs
- Cite sources returned by cortex answers with [n] markers
- Never store secrets in the memory graph
- Ask a human before destructive operations (restore over a live workspace)
