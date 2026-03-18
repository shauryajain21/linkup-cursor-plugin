---
name: linkup-search
description: Search the web using Linkup (standard depth)
arguments:
  - name: query
    description: The search query
    required: true
---

# Linkup Web Search

You are performing a web search using the Linkup CLI.

## Instructions

1. Run the following command to search the web:

```bash
linkup search "$query"
```

2. If the search requires more context or the user wants raw results, you can modify:
   - Add `--depth deep` for more thorough research
   - Add `--output searchResults` for raw sources instead of synthesized answer

3. Present the results clearly to the user, citing sources when relevant.

## Error Handling

If the command fails:
- Check if Linkup CLI is installed: `which linkup`
- Check if API key is set: `linkup config`
- If not set up, suggest running `/linkup-setup`
