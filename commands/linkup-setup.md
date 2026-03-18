---
name: linkup-setup
description: Install and configure the Linkup CLI
---

# Linkup Setup

You are helping the user install and configure the Linkup CLI.

## Instructions

### Step 1: Check if Linkup CLI is installed

```bash
which linkup && linkup --version
```

### Step 2: Install if needed

If not installed, run:

```bash
pip install linkup-cli
```

Or with pipx for isolated installation:

```bash
pipx install linkup-cli
```

### Step 3: Configure API key

1. Get an API key from [app.linkup.so](https://app.linkup.so)
2. Set the environment variable:

```bash
export LINKUP_API_KEY="your-api-key"
```

To persist, add to shell profile (`~/.zshrc` or `~/.bashrc`):

```bash
echo 'export LINKUP_API_KEY="your-api-key"' >> ~/.zshrc
source ~/.zshrc
```

### Step 4: Verify setup

```bash
linkup config
```

This should display your current configuration.

### Step 5: Test with a search

```bash
linkup search "test query"
```

## Troubleshooting

- **Command not found**: Ensure pip/pipx bin directory is in PATH
- **Authentication error**: Verify API key is set correctly
- **Permission denied**: Try `pip install --user linkup-cli`
