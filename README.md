# Humanizer PRO - MCP Server

AI text humanizer MCP server that transforms AI-generated content into natural, human-sounding text that bypasses GPTZero, Turnitin, Originality.ai, Copyleaks, ZeroGPT, and other AI detectors.

## Server Configuration

Add this to your MCP client configuration:

```json
{
  "mcpServers": {
    "humanizer-pro": {
      "url": "https://texthumanizer.pro/mcp"
    }
  }
}
```

## MCP Tools

### humanize_text

Rewrite AI-generated text to sound naturally human and bypass AI detectors like GPTZero, Turnitin, Originality.ai, Copyleaks, and ZeroGPT.

**Parameters:**
- `text` (string, required) - The text to rewrite and humanize
- `mode` (string, optional) - Rewriting mode: `stealth` (general-purpose, highest bypass rate), `academic` (Turnitin-optimized scholarly tone), `seo` (marketing content). Default: `stealth`
- `style` (string, optional) - Writing style for stealth mode: `creative`, `journalistic`, or `professional`

### scan_ai_detection

Analyze any text for AI-generated patterns. Returns AI probability score (0-100%), human-likeness percentage, verdict (AI-Generated, Mixed, Mostly Human, Human-Written), and recommendation. Capped at 250 words per scan.

**Parameters:**
- `text` (string, required) - The text to analyze

### check_word_balance

Check remaining word credits - shows subscription plan type, subscription words remaining, purchased credits, and total available balance.

### get_subscription_plans

Browse available plans: Free (500 words), Starter ($9.99/mo, 30K words), Creator ($14.99/mo, 100K words), Pro Annual ($119.88/yr, 100K words/mo). Shows the user's current plan.

## Authentication

This server uses **OAuth 2.0** authentication via Supabase Auth. Users authenticate with Google or email/password when connecting from any MCP client.

## Transport

| Transport | URL | Status |
|-----------|-----|--------|
| Streamable HTTP | `https://texthumanizer.pro/mcp` | Recommended |
| SSE (legacy) | `https://texthumanizer.pro/sse` | Supported |

## Registry Listings

- **Official MCP Registry**: [`io.github.khadinakbaronline/humanizer-pro`](https://registry.modelcontextprotocol.io)
- **Smithery**: [humanizer-pro](https://smithery.ai/servers/khadin-akbar/humanizer-pro)

## Server Discovery

Server card with full tool schemas is available at:
```
https://texthumanizer.pro/.well-known/mcp/server-card.json
```

## Compatible Clients

Works with ChatGPT, Claude, Cursor, Windsurf, and all MCP-compatible clients.

## Author

**Khadin Akbar**
- Twitter: [@khadinakbar](https://x.com/khadinakbar)
- LinkedIn: [khadinakbar](https://www.linkedin.com/in/khadinakbar)
- Website: [texthumanizer.pro](https://texthumanizer.pro)

## License

Proprietary. All rights reserved.

