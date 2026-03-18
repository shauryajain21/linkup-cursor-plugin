# Linkup — Cursor Plugin

AI-powered web search, content extraction, and deep research powered by [linkup-cli](https://github.com/shauryajain21/linkup-cli).

## Features

| Capability | Skill | Command |
|------------|-------|---------|
| Web Search | linkup-search | `/linkup-search <query>` |
| Deep Research | linkup-search | `/linkup-deep <topic>` |
| Content Extraction | linkup-search | `/linkup-fetch <url>` |

Additional commands: `/linkup-setup`, `/linkup-config`

## Installation

1. Install the plugin in Cursor from the marketplace (or see [Local Development](#local-development) to test from source).
2. Run `/linkup-setup` to install linkup-cli and authenticate.

### Manual CLI Setup

```bash
pip install linkup-cli
export LINKUP_API_KEY="your-api-key"
```

Get your API key from [app.linkup.so](https://app.linkup.so).

## Quick Start

**Search the web:**
```
/linkup-search latest developments in AI agents
```

**Deep research (slower, more thorough):**
```
/linkup-deep comprehensive analysis of React Server Components in 2026
```

**Extract a webpage:**
```
/linkup-fetch https://example.com/article
```

## Local Development

To test the plugin locally without installing from the marketplace:

1. Clone this repo:
```bash
git clone https://github.com/linkup-api/linkup-cursor-plugin.git
```

2. Open the repo in Cursor:
```bash
cursor linkup-cursor-plugin
```

3. Skills and rules are auto-discovered from the standard directories. Type `/` in the chat to verify the linkup-* skills are listed.

4. Commands are not auto-discovered when testing locally. Symlink them into Cursor's project commands directory:
```bash
ln -s ../commands .cursor/commands
```

5. Type `/` again — the linkup-* commands should now appear alongside the skills.

6. Run `/linkup-setup` to confirm the CLI is installed and authenticated.

## Plugin Structure

```
.cursor-plugin/plugin.json   Plugin manifest
skills/                      1 skill (auto-discovered)
commands/                    5 slash commands
rules/                       Citation standards rule
```

## Commands Reference

| Command | Description |
|---------|-------------|
| `/linkup-search <query>` | Standard web search with AI synthesis |
| `/linkup-deep <topic>` | Deep research with iterative retrieval |
| `/linkup-fetch <url>` | Extract content from a specific URL |
| `/linkup-setup` | Install CLI and configure API key |
| `/linkup-config` | Check CLI configuration status |

## Search Depth Options

| Depth | Best For |
|-------|----------|
| Standard | Simple facts, quick lookups, single URL scraping |
| Deep | Multi-step research, scraping multiple URLs, complex queries |

## License

MIT — see [LICENSE](LICENSE).
