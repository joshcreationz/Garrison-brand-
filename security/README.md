# GARRISON security: what has access, and how to shut it off

Plain English. Read top to bottom once.

## 1. What's switched on right now

| Access | What it can do | How it's locked | How to turn it OFF |
|---|---|---|---|
| **Shopify** connector | Read store data. Could also create discounts, edit products, publish themes | Every change needs your OK first (`.claude/settings.json`) | claude.ai → Settings → Connectors → Shopify → Disconnect. Also Shopify admin → Settings → Apps |
| **Windsor.ai (Instagram)** | Read @garrisonworldwide stats. Could also post, comment, delete | Every post/comment/delete needs your OK first | claude.ai → Settings → Connectors → Windsor → Disconnect. Also Instagram → Settings → Apps and websites → remove Windsor |
| **Higgsfield** | Make images/video (costs credits), publish to TikTok | Every generation and publish needs your OK first | claude.ai → Settings → Connectors → Higgsfield → Disconnect |
| **GitHub** repo `joshcreationz/Garrison-brand-` | Claude can read and write files in THIS repo only | Can't merge or delete without your OK | github.com → Settings → Applications → Claude |
| **2 scheduled tasks** (daily 7:17 and 7:43 AM) | Write reports into the repo. Read-only on the store and Instagram | They can't post or change the store | claude.ai → Code → Scheduled tasks → pause or delete |
| **Chrome** | Nothing. Not connected | Only if you install Claude in Chrome yourself | Remove the extension |

**Nobody else can use these.** They're tied to your Claude login. Protect that login and you protect all of it.

## 2. The rules the agents follow (and can't skip)
- `ask` list in `.claude/settings.json`: posting, commenting, deleting, discounts, product edits, theme publishing, spending Higgsfield credits, changing scheduled tasks. Claude must stop and get your yes **each time**.
- `deny` list: blocked completely. Reading password/key files, running internet scripts straight into your computer, deleting your whole drive, remote logins.
- These rules cover Claude Code in this folder, on your computer or in the cloud. They don't cover the normal claude.ai chat, so in a normal chat, still read before you hit Allow.

## 3. Before you click, download or reply to anything
Type `/grsn-check` and paste it in: the link, DM, email, file name, app name or command. You get ✅ / ⚠️ / 🛑 with plain steps.

## 4. Five things that stop 95% of hacks (do these this week)
1. **Two-factor on everything:** Instagram, Shopify, Gmail, GitHub, Claude, Higgsfield. Use an authenticator app (Google Authenticator / Authy), not texts if you can.
2. **Never give anyone a login code.** No real company DMs you for one. Ever.
3. **Don't click "verify / copyright / collab" links in DMs.** Open the app or type the website yourself.
4. **Password manager** (Apple Passwords, Bitwarden, 1Password). Different password for every account.
5. **Check who has access** once a month: Shopify admin → Settings → Users; Instagram → Settings → Apps and websites; Gmail → Security → Third-party access.

## 5. About downloading the repo
`git clone` of `joshcreationz/Garrison-brand-` only copies text files (instructions and notes). Nothing in it runs on its own. It's your repo, so only you and people you add can change it.
