---
name: invoke-agent
description: Waggle — Invoke a specific A2A agent by URL, skipping search.
disable-model-invocation: true
argument-hint: <agent-url> <message>
---

# Invoke a Specific Agent

Send a task directly to an A2A agent without searching first.

## Instructions

1. Parse the arguments: the first argument is the agent URL, the rest is the message
2. Use `mcp__waggle__invoke` with the `agent_url` parameter and message
3. If the agent returns an async task, use `mcp__waggle__poll` to check for results
4. Present the agent's response to the user
5. Use `mcp__waggle__rate_transaction` after completion with the `url_hash` and `conversation_id` from the invoke response

## Example

```
/invoke-agent https://api.waggle.zone/agents/weather What's the weather in Tokyo?
```
