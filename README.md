# flyingkiwi tools for AI agents (hosted on Apify)

Three hosted MCP tools by **flyingkiwi**. They run on [Apify](https://apify.com) and you connect to them over a URL, so there's nothing to install. Your MCP client signs in to Apify with OAuth, or you can send your own Apify API token as `Authorization: Bearer <token>`. Runs are billed per event to your Apify account, and the price is shown on each tool's Apify page.

| Tool | What it does | MCP endpoint | Apify page |
| --- | --- | --- | --- |
| Document to Markdown | Converts PDF, Word (DOCX), PowerPoint (PPTX), Excel (XLSX), HTML and EPUB into clean Markdown for RAG, with OCR for scanned pages. Accepts URLs and Google Drive, Dropbox, OneDrive and SharePoint links | `https://mcp.apify.com/?tools=flyingkiwi/document-to-markdown` | [apify.com/flyingkiwi/document-to-markdown](https://apify.com/flyingkiwi/document-to-markdown) |
| ATS Jobs & Hiring Signals | Returns open jobs from Greenhouse, Lever, Ashby, Workable, SmartRecruiters, Recruitee and Personio career pages in one schema, with salaries where published. Monitor mode reports only new jobs | `https://mcp.apify.com/?tools=flyingkiwi/ats-jobs-hiring-signals` | [apify.com/flyingkiwi/ats-jobs-hiring-signals](https://apify.com/flyingkiwi/ats-jobs-hiring-signals) |
| App Store Trends & App Ideas | Gets Apple App Store top charts for any country and category, tracks rank changes, groups review complaints and praise, and can write an optional AI app-idea report | `https://mcp.apify.com/?tools=flyingkiwi/app-store-trends-app-ideas` | [apify.com/flyingkiwi/app-store-trends-app-ideas](https://apify.com/flyingkiwi/app-store-trends-app-ideas) |

## Connect

**Claude Code**

```bash
claude mcp add --transport http document-to-markdown "https://mcp.apify.com/?tools=flyingkiwi/document-to-markdown"
```

**`mcp.json`** (Cursor, VS Code and other clients that read this format)

```json
{
  "mcpServers": {
    "document-to-markdown": { "url": "https://mcp.apify.com/?tools=flyingkiwi/document-to-markdown" },
    "ats-jobs": { "url": "https://mcp.apify.com/?tools=flyingkiwi/ats-jobs-hiring-signals" },
    "app-store-trends": { "url": "https://mcp.apify.com/?tools=flyingkiwi/app-store-trends-app-ideas" }
  }
}
```

**Claude.ai / ChatGPT:** add the URL under Settings → Connectors.

## Registry metadata

Each folder holds the `server.json` published to the [official MCP Registry](https://registry.modelcontextprotocol.io) as `io.github.flyingkiwi-tools/<tool>`.

## About

These tools are made and maintained by flyingkiwi (New Zealand). They aren't official Apify products. Apify hosts them and handles sign-in and billing. To report an issue, open a GitHub issue here or use the Issues tab on the tool's Apify page.
