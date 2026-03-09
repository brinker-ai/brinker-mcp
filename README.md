# brinker-mcp

A Claude Code plugin marketplace for the Brinker OSINT platform. Provides an MCP (Model Context Protocol) server that gives Claude Code direct access to Brinker's APIs and data.

## Installation

### 1. Add the marketplace

```bash
claude plugin marketplace add <your-internal-marketplace-url>
```

### 2. Install the plugin

```bash
claude plugin install brinker-mcp
```

### 3. Configure your API key

Add your Brinker API key to your project's `.mcp.json`:

```json
{
  "mcpServers": {
    "brinker": {
      "env": {
        "BRINKER_API_KEY": "your-api-key-here"
      }
    }
  }
}
```

> **Note:** Never commit `.mcp.json` with real API keys. Add it to `.gitignore`.

## Requirements

- Claude Code
- A valid Brinker API key

## Support

For access or issues, reach out to the Brinker engineering team.
