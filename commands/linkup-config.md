---
name: linkup-config
description: Check Linkup CLI configuration and status
---

# Linkup Configuration

You are checking the Linkup CLI configuration status.

## Instructions

1. Run the configuration check:

```bash
linkup config
```

2. This displays:
   - Current API key status (set or not)
   - Default settings
   - CLI version

3. If configuration issues are found, guide the user through `/linkup-setup`.

## Additional Checks

Check CLI version:
```bash
linkup --version
```

Verify CLI is in PATH:
```bash
which linkup
```

Test a simple search:
```bash
linkup search "hello world"
```

## Common Issues

| Issue | Solution |
|-------|----------|
| API key not set | Run `/linkup-setup` to configure |
| CLI not found | Install with `pip install linkup-cli` |
| Authentication failed | Verify API key at app.linkup.so |
