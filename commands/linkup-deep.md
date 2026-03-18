---
name: linkup-deep
description: Deep research on a topic using Linkup (iterative multi-step retrieval)
arguments:
  - name: topic
    description: The topic to research deeply
    required: true
---

# Linkup Deep Research

You are performing deep research using the Linkup CLI. Deep mode executes up to 10 iterative retrieval passes, can scrape multiple URLs, and supports sequential instructions.

## Instructions

1. Run the following command:

```bash
linkup search "$topic" --depth deep
```

2. Deep mode is ideal for:
   - Finding URLs then scraping them
   - Multi-step research that builds on prior results
   - Extracting data from multiple pages
   - Complex queries requiring synthesis across sources

3. Present findings with clear citations and source URLs.

## When to Use Deep vs Standard

| Use Deep | Use Standard |
|----------|--------------|
| Need to scrape multiple URLs | Simple factual queries |
| Chain search → scrape | Data in search snippets |
| Complex multi-step research | Single URL extraction |
| Uncertain about data location | Speed is priority |

## Error Handling

If the command fails:
- Verify CLI installation: `which linkup`
- Check authentication: `linkup config`
- If not configured, run `/linkup-setup`
