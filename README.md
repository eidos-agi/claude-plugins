# Eidos AGI — Claude Code Plugins

Plugin marketplace for Claude Code by [Eidos AGI](https://eidosagi.com).

## Install

```bash
claude plugin marketplace add eidos-agi/claude-plugins
```

## Available Plugins

### slack-eidos

Two-way Slack channel for Claude Code. Bidirectional messaging with access control, pairing, and diagnostics.

```bash
# Install
claude plugin install slack-eidos@eidos-agi

# Launch with channel
claude --channels plugin:slack-eidos@eidos-agi

# Configure (first time)
/slack-eidos:configure <xoxb-bot-token> <xapp-app-token>
```

**What it does:**
- Inbound: Slack messages appear in your Claude session as `<channel>` tags
- Outbound: Claude replies via `reply`, `react`, `edit_message` tools
- Access control: DM pairing, per-channel allowlists, @mention auto-connect
- Diagnostics: 12-tool debug MCP for full-stack inspection

**Requirements:** A Slack app with Socket Mode enabled and a Bot User OAuth Token.

See [slack-eidos-cc](https://github.com/eidos-agi/slack-eidos-cc) for full docs.
