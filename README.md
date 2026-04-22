# Eidos AGI — Claude Code Plugins

Plugin marketplace for Claude Code by [Eidos AGI](https://eidosagi.com).

## Install

```bash
claude plugin marketplace add eidos-agi/claude-plugins
```

## Available Plugins

### slack-cc

Two-way Slack channel for Claude Code. Bidirectional messaging with access control, pairing, and diagnostics.

```bash
# Install
claude plugin install slack-cc@eidos-agi

# Launch with channel bridge
claude --dangerously-load-development-channels plugin:slack-cc@eidos-agi

# Configure tokens (first time)
/slack-cc:configure <xoxb-bot-token> <xapp-app-token>
```

> **Important:** The `--dangerously-load-development-channels` flag is required. The shorter `--channels` flag only works for plugins on Anthropic's official allowlist. This applies to all private marketplace plugins. The flag name is a Claude Code security gate, not a safety warning about the plugin itself.

**What it does:**
- Inbound: Slack messages appear in your Claude session as `<channel>` tags
- Outbound: Claude replies via `reply`, `react`, `edit_message` tools
- Access control: DM pairing, per-channel allowlists, @mention auto-connect
- Diagnostics: 12-tool debug MCP for full-stack inspection

**Requirements:** A Slack app with Socket Mode enabled and a Bot User OAuth Token.

See [slack-cc](https://github.com/eidos-agi/slack-cc) for full docs.
