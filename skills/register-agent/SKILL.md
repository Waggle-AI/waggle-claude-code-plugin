---
name: register-agent
description: Register a new A2A agent with Waggle for indexing and discovery. Use when the user wants to submit their own agent or a discovered agent to the Waggle index.
---

# Register an Agent

Submit an A2A agent URL to Waggle for indexing and discovery.

## Instructions

1. Get the agent's base URL from the user (e.g., `https://my-agent.example.com`)
2. Use `mcp__waggle__register` to submit it
3. Report the registration result to the user
4. Explain that the agent will be probed and indexed, and will appear in search once validated

## Requirements

- The URL must serve an A2A agent card at `/.well-known/agent-card.json` or `/.well-known/agent.json`
- The agent must be publicly accessible
- Registration counts against the daily registration limit (10/day on free tier)
