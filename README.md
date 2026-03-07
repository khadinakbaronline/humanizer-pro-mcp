# Humanizer PRO - AI Text Humanizer MCP Server

<p align="center">
  <strong><a href="https://texthumanizer.pro">Humanizer PRO</a> - The Best AI Text Humanizer MCP Server</strong><br>
  Transform AI-generated content into natural, human-sounding text that bypasses GPTZero, Turnitin, Originality.ai, Copyleaks, ZeroGPT, and other AI detectors. Undetectable AI content rewriting with Stealth, Academic, and SEO modes.
</p>

<p align="center">
  <a href="https://texthumanizer.pro">Humanizer PRO Website</a> |
  <a href="https://texthumanizer.pro/mcp-docs">MCP Documentation</a> |
  <a href="https://smithery.ai/servers/khadin-akbar/humanizer-pro">Smithery</a> |
  <a href="https://registry.modelcontextprotocol.io">MCP Registry</a>
</p>

---

## What is Humanizer PRO?

[Humanizer PRO](https://texthumanizer.pro) is a powerful AI text humanizer that rewrites AI-generated content to make it undetectable by AI detection tools. The [Humanizer PRO MCP server](https://texthumanizer.pro/mcp-docs) brings this capability directly into your favorite AI coding assistants and chat clients through the Model Context Protocol (MCP).

**Key Features:**
- Bypass GPTZero, Turnitin, Originality.ai, Copyleaks, ZeroGPT and all major AI detectors
- Three humanization modes: Stealth (highest bypass rate), Academic (Turnitin-optimized), SEO (marketing-optimized)
- Built-in AI detection scanner with detailed scoring
- Word balance tracking and subscription management
- Works with ChatGPT, Claude, Cursor, VS Code, Windsurf, and all MCP-compatible clients

Learn more at [texthumanizer.pro](https://texthumanizer.pro) or read the full [MCP documentation](https://texthumanizer.pro/mcp-docs).

---

## Quick Setup - Connect Humanizer PRO to Your MCP Client

### ChatGPT - Humanizer PRO MCP Integration

[Humanizer PRO](https://texthumanizer.pro) works natively with ChatGPT. Simply use the MCP endpoint:

```
https://texthumanizer.pro/mcp
```

### Claude Desktop - Humanizer PRO MCP Setup

Add [Humanizer PRO](https://texthumanizer.pro) to your `claude_desktop_config.json`:

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

### Claude Code (CLI) - Humanizer PRO One-Line Setup

```bash
claude mcp add humanizer-pro --transport http https://texthumanizer.pro/mcp
```

### Cursor - Humanizer PRO AI Text Humanizer Setup

Add [Humanizer PRO](https://texthumanizer.pro) to your Cursor MCP settings (Settings > MCP Servers > Add):

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

### Windsurf - Humanizer PRO MCP Configuration

Add [Humanizer PRO](https://texthumanizer.pro) to your Windsurf MCP config at `~/.codeium/windsurf/mcp_config.json`:

```json
{
  "mcpServers": {
    "humanizer-pro": {
      "serverUrl": "https://texthumanizer.pro/mcp"
    }
  }
}
```

### VS Code (GitHub Copilot) - Humanizer PRO MCP Setup

Add [Humanizer PRO](https://texthumanizer.pro) to your VS Code `settings.json` (Cmd/Ctrl + Shift + P > "Preferences: Open User Settings (JSON)"):

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

### Cline - Humanizer PRO AI Humanizer MCP

Add [Humanizer PRO](https://texthumanizer.pro) to your Cline MCP settings:

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

### Continue - Humanizer PRO MCP Integration

Add [Humanizer PRO](https://texthumanizer.pro) to your `~/.continue/config.json`:

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

### Zed - Humanizer PRO AI Text Humanizer MCP

Add [Humanizer PRO](https://texthumanizer.pro) to your Zed settings (`~/.config/zed/settings.json`):

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

### SSE Transport (Legacy Clients)

For MCP clients that only support SSE transport, use [Humanizer PRO](https://texthumanizer.pro) SSE endpoint:

```json
{
  "mcpServers": {
    "humanizer-pro": {
      "url": "https://texthumanizer.pro/sse"
    }
  }
}
```

### Smithery - One-Click Humanizer PRO Install

Install [Humanizer PRO](https://texthumanizer.pro) directly from Smithery:

[![Smithery Badge](https://smithery.ai/badge/khadin-akbar/humanizer-pro)](https://smithery.ai/servers/khadin-akbar/humanizer-pro)

```bash
npx @smithery/cli install @khadin-akbar/humanizer-pro
```

---

## Humanizer PRO MCP Tools

Full documentation: [texthumanizer.pro/mcp-docs](https://texthumanizer.pro/mcp-docs)

### humanize_text - AI Text Humanizer Tool

Rewrite AI-generated text to sound naturally human and bypass AI detectors like GPTZero, Turnitin, Originality.ai, Copyleaks, and ZeroGPT. [Humanizer PRO](https://texthumanizer.pro) uses advanced NLP to make AI content undetectable while preserving the original meaning.

**Parameters:**
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `text` | string | Yes | The AI-generated text to rewrite and humanize |
| `mode` | string | No | `stealth` (highest bypass rate), `academic` (Turnitin-optimized scholarly tone), `seo` (marketing content). Default: `stealth` |
| `style` | string | No | `creative`, `journalistic`, or `professional` (stealth mode only) |

### scan_ai_detection - AI Content Detection Scanner

Analyze any text for AI-generated patterns using [Humanizer PRO](https://texthumanizer.pro) detection scanner. Returns AI probability score (0-100%), human-likeness percentage, verdict (AI-Generated, Mixed, Mostly Human, Human-Written), and recommendation. **Parameters:**
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `text` | string | Yes | The text to scan for AI detection |

### check_word_balance - Word Credits Tracker

Check your remaining [Humanizer PRO](https://texthumanizer.pro) word credits - shows subscription plan type, subscription words remaining, purchased credits, and total available balance.

*No parameters required.*

### get_subscription_plans - Humanizer PRO Pricing Plans

Browse available [Humanizer PRO](https://texthumanizer.pro) plans and see the user's current plan.

| Plan | Price | Words | Best For |
|------|-------|-------|----------|
| Free | $0 | 500 words | Try Humanizer PRO |
| Starter | $9.99/mo | 30,000 words/mo | Students and bloggers |
| Creator | $14.99/mo | 100,000 words/mo | Content creators and marketers |
| Pro Annual | $119.88/yr | 100,000 words/mo | Professionals (save 33%) |

*No parameters required.*

---

## Authentication

[Humanizer PRO](https://texthumanizer.pro) MCP server uses **OAuth 2.0** authentication via Supabase Auth. Users authenticate with Google or email/password when connecting from any MCP client. The OAuth flow is handled automatically by compatible clients.

## Transport Options

| Transport | URL | Recommended |
|-----------|-----|-------------|
| Streamable HTTP | `https://texthumanizer.pro/mcp` | Yes |
| SSE (legacy) | `https://texthumanizer.pro/sse` | For legacy clients |

## Server Discovery

[Humanizer PRO](https://texthumanizer.pro) server card with full tool schemas:
```
https://texthumanizer.pro/.well-known/mcp/server-card.json
```

## Registry Listings

- **Official MCP Registry**: [`io.github.khadinakbaronline/humanizer-pro`](https://registry.modelcontextprotocol.io)
- **Smithery**: [Humanizer PRO on Smithery](https://smithery.ai/servers/khadin-akbar/humanizer-pro)

## Links

- **Website**: [texthumanizer.pro](https://texthumanizer.pro)
- **MCP Documentation**: [texthumanizer.pro/mcp-docs](https://texthumanizer.pro/mcp-docs)
- **Server Card**: [texthumanizer.pro/.well-known/mcp/server-card.json](https://texthumanizer.pro/.well-known/mcp/server-card.json)

## Author

**Khadin Akbar** - Creator of [Humanizer PRO](https://texthumanizer.pro)
- Twitter: [@khadinakbar](https://x.com/khadinakbar)
- LinkedIn: [khadinakbar](https://www.linkedin.com/in/khadinakbar)
- Website: [texthumanizer.pro](https://texthumanizer.pro)

## License

Proprietary. All rights reserved. [Humanizer PRO](https://texthumanizer.pro) - The Best AI Text Humanizer.

