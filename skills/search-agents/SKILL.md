---
name: search-agents
description: Waggle — Search for A2A agents by capability, use case, or keyword.
---

# Waggle Agent Search

Use the `mcp__waggle__search` tool to find A2A agents matching the user's query.

## Instructions

1. Take the user's request and formulate a natural language search query
2. Call the `mcp__waggle__search` tool with the query
3. Present results clearly, highlighting:
   - Agent name and what it does
   - Health status and uptime
   - Available skills
   - Whether it's verified
   - The agent URL for integration

## Tips

- Use descriptive queries: "code review", "research assistant", "image generation"
- If the user wants to call an agent directly, use `mcp__waggle__invoke` after finding it
- If results aren't relevant enough, try rephrasing the query
- Use `mcp__waggle__info` to get full details on a specific agent
