# MakeItRun — MCP server

**Publish what you build in Claude or ChatGPT to a live URL — no developer required.**

MakeItRun is publishing infrastructure for AI-native tools, menus, reports, and
pages. When an assistant generates an HTML page — a menu, a dashboard, a
calculator, a one-pager — MakeItRun turns it into a real, permanent `https` URL
in one tool call, complete with a QR code and version history.

This repository holds the public MCP manifest ([`server.json`](./server.json))
for the **remote** MakeItRun MCP server. The server itself is hosted — there is
nothing to install.

## Connect

- **Server URL (OAuth 2.1):** `https://mcp.makeitrun.ai/mcp`
- **Anonymous (24-hour) fallback:** `https://mcp.makeitrun.ai/anon/mcp`

Add it as a custom connector in Claude (Settings → Connectors) or ChatGPT
(Settings → Connectors), then sign in once via OAuth (Google or email) and
publish with a single tool call.

## Tools

| Tool | What it does |
|------|--------------|
| `publish_html` | Publishes a self-contained HTML document to a permanent URL under your account, with an optional custom slug and search-engine indexing control. |
| `list_my_publishes` | Lists the pages you've published — id, slug, URL, title, last updated. |
| `delete_publish` | Permanently removes one of your pages by slug. |

Authentication is OAuth 2.1 with PKCE. Pages are served from a global CDN, last
indefinitely, and can be shared by link or QR code.

## Links

- Website: <https://makeitrun.ai>
- Docs: <https://makeitrun.ai/developers>
- Privacy & terms: <https://makeitrun.ai/legal>
- Support: `support@makeitrun.ai`

## License

[MIT](./LICENSE)
