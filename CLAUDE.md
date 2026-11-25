# GARRISON (GRSN) — brand workspace

Store: grsnworld.com (Shopify). Owner: Josh (Josh Creationz).

This repo is the home base for GARRISON's background agents. Each agent writes
its output into `reports/` so there is a running history Josh can scroll back
through.

## Agents (`.claude/agents/`)

| Agent | Job | Writes to |
|---|---|---|
| `grsn-creative-director` | GARRISON's creative director: daily idea (`/grsn-today`), Yard Series, campaigns, captions, Corteiz blueprint. Reads `grsn/` every time | `grsn/content-log.md` |
| `grsn-promo-director` | Promotion creative direction: what to post, when, how it should look and read, and prepping the assets | `reports/promo/YYYY-MM-DD.md` |
| `grsn-shopify-marketing` | Shopify marketing admin: sales/traffic pulse, discounts, collections, product hygiene, campaign tracking | `reports/shopify/YYYY-MM-DD.md` |

Run one by hand with: "use the grsn-promo-director agent to plan this week".

## Ground rules for every agent

- **Nothing goes public without Josh's OK.** Agents draft, prepare and queue.
  Posting to Instagram/TikTok, publishing a theme, creating or activating a
  discount, changing prices, or emailing customers needs Josh's explicit yes in
  the conversation. Running in the background means *prepare and report*, not
  *publish*.
- **Spend:** don't run paid Higgsfield generations without a budget Josh set.
  Check `balance` / `estimate_*_cost` first and state the cost in the report.
- **Data over guesses:** numbers come from Shopify analytics or Windsor.ai
  reads, never from memory. If a read fails, say so in the report.
- **Use the GRSN skills** when they fit: `grsn-creative-director`,
  `grsn-pages`, `grsn-instagram`, `grsn-content`, `grsn-drop-planner`,
  `grsn-trend-scout`, `grsn-store`, `grsn-lookbook-flipbook`.
- Commit each new report to the working branch and push it.
