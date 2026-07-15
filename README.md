# Reich Tools MCP — Verification & Market Intelligence for AI Agents

Remote MCP server exposing two production tools, hosted on Apify's Streamable HTTP MCP infrastructure. No local install, no code — one URL. OAuth or API-token auth.

**House rule: tools that tell you the truth.** Both tools return honest failure states instead of fabricated data, and never charge for errors.

## Quick start

Add to any MCP client (Claude Desktop, Claude.ai, Cursor, VS Code, or any Streamable HTTP client):

```json
{
  "mcpServers": {
    "reich-tools": {
      "url": "https://mcp.apify.com?tools=shane_reich/name-clearance-verdict,shane_reich/stock-edge-signals"
    }
  }
}
```

On first connection you'll be prompted to sign in to Apify (OAuth). Alternatively, authenticate with a header: `"headers": { "Authorization": "Bearer <APIFY_TOKEN>" }`.

## Tools

### 🏅 Name Clearance Verdict — `shane_reich/name-clearance-verdict`
One call answers: **"Is this brand name safe to use?"**
- Trademark knockout across **USPTO + TMview (70+ IP offices)** with phonetic & fuzzy collision matching
- Nice-class inference from your product description
- RDAP domain availability + best-effort social handle checks
- Composite grade: `CLEAR / CAUTION / HIGH_RISK / UNKNOWN` — never `CLEAR` if a trademark source failed
- Alternative names that clear

→ [Store listing](https://apify.com/shane_reich/name-clearance-verdict) · $0.10 per verdict · failed lookups never charged

### 📈 Stock Edge — `shane_reich/stock-edge-signals`
BUY/SELL/HOLD technical signals for US stocks — **the only signal tool that grades its own homework.** Every signal is written to a permanent ledger, resolved against subsequent prices daily, and published (wins *and* losses) via a free `performance` mode.
- RSI, MA20/50 trend, momentum, volume confirmation, ATR-adjusted confidence
- Multi-provider failover (Finnhub, Twelve Data, Alpha Vantage)
- Batch up to 10 symbols; honest `INSUFFICIENT_DATA` states

→ [Store listing](https://apify.com/shane_reich/stock-edge-signals) · $0.015 per signal · free public track record · errors never charged

## Why agents use these

Both tools return one structured, deterministic JSON verdict per call — no prose parsing, no pagination, no session state. Designed for agent workflows: brand-name vetting inside product-launch pipelines, portfolio monitoring inside finance agents.

## Transport & compatibility

- **Transport:** Streamable HTTP (hosted at `mcp.apify.com`)
- **Auth:** OAuth or `Authorization: Bearer <APIFY_TOKEN>`
- **Clients tested:** Claude Desktop, Claude.ai, Cursor, VS Code
- Output schemas published (Actor output schema v1) so clients get structured results

---
Built and maintained by Shane Reich · [Apify profile](https://apify.com/shane_reich)
