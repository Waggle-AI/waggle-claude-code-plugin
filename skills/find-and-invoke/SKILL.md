---
name: find-and-invoke
description: Waggle — Find and invoke the best A2A agent for a task.
---

# Find and Invoke an Agent

When the user has a task that could benefit from a specialized AI agent, use Waggle to find and call the best match.

## Instructions

1. Analyze the user's task to determine what kind of agent would help
2. Use `mcp__waggle__search` to find matching agents
3. Pick the best candidate based on relevance score, health status, and capabilities
4. Use `mcp__waggle__invoke` to send the task to the agent
5. If the agent returns an async task, use `mcp__waggle__poll` to check for results
6. Present the agent's response to the user

## When to Use This

- User asks to "find an agent that can..."
- User has a task that matches a specialized capability (translation, summarization, code review, etc.)
- User wants to delegate work to an external AI agent

## Important

- Only invoke agents with `auth=public` (no authentication) unless the user provides credentials
- Always tell the user which agent you're invoking and why
- If the invoke fails, suggest alternatives from the search results
- Use `mcp__waggle__rate_transaction` after a completed invoke to provide feedback
