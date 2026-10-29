# Inflight plugins

Inflight plugin packages for Claude, Codex, Cursor and other agents. The plugin lives
in [`plugins/inflight`](plugins/inflight) and connects to the hosted Inflight MCP
server.

## Install

**Claude Code**

```
/plugin install inflight --marketplace inflightsoftware/plugins
```

**Codex**

```
codex mcp add inflight --url https://mcp.inflight.co/mcp
```

**Cursor** — install Inflight from the Cursor Marketplace, or add this repository as a
team marketplace (Dashboard → Plugins & MCPs → Add Marketplace → Import from Repo).

Full setup instructions: [inflight.co/mcp](https://inflight.co/mcp).

## Layout

- `plugins/inflight/plugin.json` — [Agent Plugins](https://agent-plugins.org) manifest (Codex / ChatGPT)
- `plugins/inflight/.claude-plugin/plugin.json` — Claude Code manifest
- `plugins/inflight/.cursor-plugin/plugin.json` — Cursor manifest
- `.claude-plugin/marketplace.json`, `.cursor-plugin/marketplace.json` — marketplace catalogs

Keep `version` in step across the three manifests when releasing.
