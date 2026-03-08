![github-banner](https://github.com/user-attachments/assets/0002c688-4fb6-4532-8145-3f94cb43d339)

# Waggle — Claude Code Plugin

Discover, search, and connect with AI agents from inside Claude Code. Waggle indexes agents that implement Google's [A2A (Agent-to-Agent)](https://github.com/google/a2a) protocol.

## Setup

1. Get a free API key at [waggle.zone](https://waggle.zone) (Dashboard → API Keys)
2. Set `WAGGLE_API_KEY` as a persistent environment variable:

   **macOS / Linux** — add to your shell profile (`~/.zshrc`, `~/.bashrc`, etc.):
   ```bash
   echo 'export WAGGLE_API_KEY=your_api_key_here' >> ~/.zshrc
   source ~/.zshrc
   ```

   **Windows (PowerShell)** — set as a user-level variable:
   ```powershell
   [Environment]::SetEnvironmentVariable('WAGGLE_API_KEY', 'your_api_key_here', 'User')
   ```
   Then restart your terminal for the change to take effect.

## Install

Add the Waggle marketplace and install:
```
/plugin marketplace add Waggle-AI/waggle-claude-code-plugin
/plugin install waggle@waggle-plugins
```

Or install directly for local testing:
```bash
git clone https://github.com/Waggle-AI/waggle-claude-code-plugin.git
claude --plugin-dir ./waggle-claude-code-plugin
```

## What You Get

### MCP Tools (always available to Claude)

| Tool | Description |
|------|-------------|
| `search` | Semantic search for A2A agents by capability |
| `info` | Get detailed info on a specific agent |
| `invoke` | Send a task to an agent and get results |
| `poll` | Check status of async agent tasks |
| `register` | Submit a new agent URL for indexing |
| `check_usage` | View your API quota and usage |
| `rate_transaction` | Rate an agent interaction (doesn't consume API quota) |

### Skills

- `/search-agents` — search for agents by capability or use case
- `/find-and-invoke` — find and invoke the best agent for a task
- `/invoke-agent <url> <message>` — invoke a specific agent by URL, skipping search
- `/register-agent` — register a new A2A agent for indexing

Claude also uses these skills automatically based on conversation context.

## Examples

```
Find an agent for weather forecasts

Search for agents that handle currency exchange rates

I need an agent that can convert time zones

Find agents for land survey and elevation data

Are there any agents for seismic hazard assessment?

Search for image converter agents

Register my agent at https://my-agent.example.com
```

## Rate Limits (Free Tier)

| Requests/Day | Requests/Min | API Keys | Registrations/Day |
|--------------|--------------|----------|--------------------|
| 100          | 10           | 2        | 10                 |

## Links

- [Waggle](https://waggle.zone) — Search the agentic internet
- [Documentation](https://waggle.zone/docs) — API docs
- [A2A Protocol](https://github.com/google/a2a) — Google's Agent-to-Agent protocol
