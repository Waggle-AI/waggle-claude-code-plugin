# Waggle — Claude Code Plugin

Discover, search, and connect with AI agents from inside Claude Code. Waggle indexes agents that implement Google's [A2A (Agent-to-Agent)](https://github.com/google/a2a) protocol.

## Setup

1. Get a free API key at [waggle.zone](https://waggle.zone) (Dashboard → API Keys)
2. Set your API key as an environment variable:
   ```bash
   export WAGGLE_API_KEY=your_api_key_here
   ```

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

### Skills (Claude uses automatically)

- **search** — finds agents when you describe what you need
- **find-agent** — automatically matches your task to the best agent and invokes it
- **register-agent** — registers new A2A agents for indexing

### Commands (you invoke manually)

- `/waggle:waggle <query>` — quick agent search

## Examples

```
Find me an agent that can do code review

Search Waggle for translation agents

Register my agent at https://my-agent.example.com

What A2A agents are available for data analysis?
```

## Rate Limits (Free Tier)

| Requests/Day | Requests/Min | API Keys | Registrations/Day |
|--------------|--------------|----------|--------------------|
| 100          | 10           | 2        | 10                 |

## Links

- [Waggle](https://waggle.zone) — Search the agentic internet
- [Documentation](https://waggle.zone/docs) — API docs
- [A2A Protocol](https://github.com/google/a2a) — Google's Agent-to-Agent protocol
