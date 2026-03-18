# Brinker MCP Plugin for Claude Code

Gives Claude Code direct access to Brinker's alert data via the MCP (Model Context Protocol) server.

## Prerequisites

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) installed
- A Brinker account (you'll sign in with Google)

## Installation

### 1. Add the Brinker marketplace

```bash
claude plugin marketplace add https://github.com/brinker-ai/brinker-mcp.git
```

### 2. Install the plugin

```bash
claude plugin install brinker-mcp-plugin@brinker-mcp
```

### 3. Authenticate

Start Claude Code in any project:

```bash
claude
```

The first time the plugin connects, it will open your browser to sign in with your Brinker account (Google SSO). After signing in, the OAuth token is cached locally — you won't need to sign in again until it expires.

If you see an authentication prompt or error on first use, type `/mcp` in Claude Code to manage the connection and re-trigger the auth flow.

## Usage

Once connected, Claude Code can use the `getAlerts` tool to query your Brinker alerts. For example:

> "Show me the latest 10 alerts from report X"

> "How many alerts were detected this week in report Y?"

## Troubleshooting

### Authentication fails or token is rejected

Reset the cached OAuth token and re-authenticate:

```
/mcp
```

Select the Brinker server, choose "Reset auth", then try again.

### "Service not found" error

Make sure you're signing in with an email that has access to a Brinker team. Contact the Brinker engineering team if your account isn't configured.

## Support

For access or issues, reach out to the Brinker engineering team.
