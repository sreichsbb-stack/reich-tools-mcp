# SUBMISSIONS.md — MCP Registry Playbook (Shane's clicks, ~45 min total)

Everything below is paste-ready. Your logins, your clicks — I've done the words.

## Step 0 — Push the server-card repo (5 min, do this FIRST)
Several registries index public GitHub repos automatically; this repo is the anchor everything else points at.

```bash
cd reich-tools-mcp
git init && git add . && git commit -m "Reich Tools MCP server card"
# create a PUBLIC repo named reich-tools-mcp on github.com/sreichsbb-stack, then:
git remote add origin https://github.com/sreichsbb-stack/reich-tools-mcp.git
git branch -M main && git push -u origin main
```

## Paste-ready blurbs (used across all forms)

**Short (under 160 chars):**
> Brand-name trademark clearance + honest stock signals for AI agents. One URL, structured verdicts, never charged for errors. Hosted on Apify MCP.

**Medium:**
> Reich Tools MCP exposes two production tools for AI agents: Name Clearance Verdict (trademark knockout across USPTO + TMview's 70+ IP offices, domains, handles, composite risk grade) and Stock Edge Signals (BUY/SELL/HOLD technical signals with a public, self-graded accuracy ledger). Streamable HTTP, OAuth, structured JSON verdicts, honest failure states — errors are never charged.

**Server URL:** `https://mcp.apify.com?tools=shane_reich/name-clearance-verdict,shane_reich/stock-edge-signals`
**Repo:** `https://github.com/sreichsbb-stack/reich-tools-mcp`
**Tags:** trademark, brand, compliance, kyc, stocks, finance, signals, verification, apify

## Registry 1 — Glama (glama.ai) ~10 min
Glama primarily auto-indexes public GitHub MCP repos (their crawler picks up new repos within days).
1. Push the repo (Step 0) — that alone usually gets you indexed.
2. To accelerate: sign in at glama.ai (GitHub OAuth), look for "Add server" / claim flow, submit the repo URL.
3. If there's a Discord-based submission (they run one for directory feedback), post the repo link there.

## Registry 2 — mcp.so ~10 min
1. Go to mcp.so → "Submit" (top nav).
2. Sign in (GitHub), paste repo URL + Medium blurb + tags.
3. Category: pick "Business/Finance" or closest fit.

## Registry 3 — PulseMCP (pulsemcp.com) ~5 min
1. pulsemcp.com → "Submit a server" form.
2. Paste server URL, repo URL, Short blurb.

## Registry 4 — mcpservers.org ~10 min
This directory is backed by a GitHub repo (awesome-style list). Apify's own server is already listed there.
1. Find their GitHub repo (linked in site footer) → edit README/data file via GitHub web UI → add an entry with the Medium blurb → open the pull request from your account.
2. PR title: "Add Reich Tools MCP (trademark clearance + stock signals)"

## Registry 5 — Smithery (smithery.ai) ~5 min — OPTIONAL
Smithery is oriented toward deployable server packages; remote-hosted servers are second-class there. Submit the repo if the "Add server" flow accepts a remote URL; if it demands a smithery.yaml deployment, skip — not worth building a wrapper for aisle #5. Diminishing returns are real.

## While you're logged in to Apify (2 min, highest value of all)
- Stock Edge → Publication → **Publish on Store** (the button we left for you)
- Both actors → Publication → Display information → confirm categories include **AI** / **Agents** / **MCP servers** where available, and the SEO description mentions "MCP" and "AI agents" — that's how agents' discovery tools find you on Apify itself, which is still the biggest aisle of the lot.

## What NOT to do
- Don't pay any registry's "featured listing" upsell. Zero evidence it converts; capital stays at zero.
- Don't submit the same repo twice to one registry — duplicates get flagged and look spammy under your name.
