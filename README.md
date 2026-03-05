# Humanizer PRO - MCP Server

<p align="center">
  <strong>AI text humanizer MCP server</strong><br>
  Transform AI-generated content into natural, human-sounding text that bypasses GPTZero, Turnitin, Originality.ai, Copyleaks, ZeroGPT, and other AI detectors.
</p>

<p align="center">
  <a href="https://texthumanizer.pro">Website</a> |
  <a href="https://smithery.ai/servers/khadin-akbar/humanizer-pro">Smithery</a> |
  <a href="https://registry.modelcontextprotocol.io">MCP Registry</a>
</p>

---

## Quick Setup

### ChatGPT

Humanizer PRO works natively with ChatGPT. Simply use the MCP endpoint:

```
https://texthumanizer.pro/mcp
```

### Claude Desktop

Add to your `claude_desktop_config.json`:

**macOS**: `~/Library/Application Support/Claude/claude_desktop_config.json`
**Windows**: `%APPDATA%\Claude\claude_desktop_config.json`

```json
{
  "mcpServers": {
    "humanizer-pro": {
      "url": "https://texthumanizer.pro/mcp"
    }
  }
}
```

### Claude Code (CLI)

```bash
claude mcp add humanizer-pro --transport http https://texthumanizer.pro/mcp
```

### Cursor

Add to your Cursor MCP settings (Settings > MCP Servers > Add):

```json
{
  "mcpServers": {
    "humanizer-pro": {
      "url": "https://texthumanizer.pro/mcp"
    }
  }
}
```

Or via Cursor Settings UI:
1. Open **Settings** (Cmd/Ctrl + ,)
2. Search for **MCP**
3. Click **Add MCP Server**
4. Name: `humanizer-pro`
5. Type: `sse`
6. URL: `https://texthumanizer.pro/sse`

### Windsurf

Add to your Windsurf MCP config at `~/.codeium/windsurf/mcp_config.json`:

```json
{
  "mcpServers": {
    "humanizer-pro": {
      "serverUrl": "https://texthumanizer.pro/mcp"
    }
  }
}
```

### VS Code (GitHub Copilot)

Add to your VS Code `settings.json` (Cmd/Ctrl + Shift + P > "Preferences: Open User Settings (JSON)"):

```json
{
  "mcp": {
    "servers": {
      "humanizer-pro": {
        "type": "http",
        "url": "https://texthumanizer.pro/mcp"
      }
    }
  }
}
```

### Cline

Add to your Cline MCP settings:

```json
{
  "mcpServers": {
    "humanizer-pro": {
      "url": "https://texthumanizer.pro/mcp",
      "transportType": "streamable-http"
    }
  }
}
```

### Continue

Add to your `~/.continue/config.json`:

```json
{
  "experimental": {
    "modelContextProtocolServers": [
      {
        "transport": {
          "type": "streamable-http",
          "url": "https://texthumanizer.pro/mcp"
        }
      }
    ]
  }
}
```

### Zed

Add to your Zed settings (`~/.config/zed/settings.json`):

```json
{
  "context_servers": {
    "humanizer-pro": {
      "settings": {
        "url": "https://texthumanizer.pro/mcp"
      }
    }
  }
}
```

### SSE Transport (Legacy)

For clients that only support SSE transport:

```json
{
  "mcpServers": {
    "humanizer-pro": {
      "url": "https://texthumanizer.pro/sse"
    }
  }
}
```

### Smithery (One-Click Install)

Install directly from Smithery:

[![Smithery Badge](https://smithery.ai/badge/khadin-akbar/humanizer-pro)](https://smithery.ai/servers/khadin-akbar/humanizer-pro)

```bash
npx @smithery/cli install @khadin-akbar/humanizer-pro
```

---

## MCP Tools

### humanize_text

Rewrite AI-generated text to sound naturally human and bypass AI detectors like GPTZero, Turnitin, Originality.ai, Copyleaks, and ZeroGPT.

**Parameters:**
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `text` | string | Yes | The text to rewrite and humanize |
| `mode` | string | No | `stealth` (highest bypass rate), `academic` (Turnitin-optimized), `seo` (marketing content). Default: `stealth` |
| `style` | string | No | `creative`, `journalistic`, or `professional` (stealth mode only) |

### scan_ai_detection

Analyze any text for AI-generated patterns. Returns AI probability score (0-100%), human-likeness percentage, verdict (AI-Generated, Mixed, Mostly Human, Human-Written), and recommendation. Capped at 250 words per scan.

**Parameters:**
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `text` | string | Yes | The text to analyze |

### check_word_balance

Check remaining word credits - shows subscription plan type, subscription words remaining, purchased credits, and total available balance.

*No parameters required.*

### get_subscription_plans

Browse available plans and see the user's current plan.

| Plan | Price | Words |
|------|-------|-------|
| Free | $0 | 500 words |
| Starter | $9.99/mo | 30,000 words/mo |
| Creator | $14.99/mo | 100,000 words/mo |
| Pro Annual | $119.88/yr | 100,000 words/mo |

*No parameters required.*

---

## Authentication

This server uses **OAuth 2.0** authentication via Supabase Auth. Users authenticate with Google or email/password when connecting from any MCP client. The OAuth flow is handled automatically by compatible clients.

## Transport

| Transport | URL | Recommended |
|-----------|-----|-------------|
| Streamable HTTP | `https://texthumanizer.pro/mcp` | Yes |
| SSE (legacy) | `https://texthumanizer.pro/sse` | For legacy clients |

## Server Discovery

Server card with full tool schemas:
```
https://texthumanizer.pro/.well-known/mcp/server-card.json
```

## Registry Listings

- **Official MCP Registry**: [`io.github.khadinakbaronline/humanizer-pro`](https://registry.modelcontextprotocol.io)
- **Smithery**: [humanizer-pro](https://smithery.ai/servers/khadin-akbar/humanizer-pro)

## Author

**Khadin Akbar**
- Twitter: [@khadinakbar](https://x.com/khadinakbar)
- LinkedIn: [khadinakbar](https://www.linkedin.com/in/khadinakbar)
- Website: [texthumanizer.pro](https://texthumanizer.pro)

## License

Proprietary. All rights reserved.

