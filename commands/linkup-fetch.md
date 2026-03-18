---
name: linkup-fetch
description: Extract content from a specific URL using Linkup
arguments:
  - name: url
    description: The URL to fetch and extract content from
    required: true
---

# Linkup Fetch

You are extracting content from a specific URL using the Linkup CLI.

## Instructions

1. Run the following command:

```bash
linkup fetch "$url"
```

2. The fetch command:
   - Extracts and returns the page content as markdown
   - Is faster and cheaper than search when you have a known URL
   - Works best for articles, documentation, pricing pages, etc.

## When to Use Fetch vs Search

| Use Fetch | Use Search |
|-----------|------------|
| You have the exact URL | You need to find the URL first |
| Single page extraction | Results from multiple pages |
| Known article/doc/page | Broad topic research |

## Error Handling

If the command fails:
- Verify the URL is valid and accessible
- Check CLI installation: `which linkup`
- Check authentication: `linkup config`
- If not configured, run `/linkup-setup`
