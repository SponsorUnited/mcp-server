# SponsorUnited for AI apps

Connect your AI app to SponsorUnited. You sign in with your SponsorUnited email
and password. Your app then sees the SponsorUnited data your account can see.

This page covers **Claude Code**. For other apps, use these guides:

- [claude.ai and Claude Desktop](docs/claude-ai-and-desktop.md)
- [Codex](docs/codex.md)
- [ChatGPT](docs/chatgpt.md)

## What you need

- A SponsorUnited account (the email and password you use on sponsorunited.com).
- [Claude Code](https://code.claude.com/docs/en/quickstart), installed and signed in.
- A web browser on the same computer. Sign-in opens a browser page.

## Set up Claude Code

### 1. Add this marketplace

Run this in your terminal:

```bash
claude plugin marketplace add SponsorUnited/mcp-server
```

You should see `✔ Successfully added marketplace: sponsorunited (declared in user settings)`.

### 2. Install the plugin

```bash
claude plugin install sponsorunited@sponsorunited
```

You should see `✔ Successfully installed plugin: sponsorunited@sponsorunited (scope: user)`.

You can also do steps 1 and 2 inside Claude Code: type
`/plugin marketplace add SponsorUnited/mcp-server`, then
`/plugin install sponsorunited@sponsorunited`.

### 3. Sign in

1. Start Claude Code: run `claude`.
2. Type `/mcp` and press Enter.
3. Pick the `sponsorunited` server, then pick **Authenticate**.
4. A browser page opens on `login.sponsorunited.ai`. Sign in with your
   SponsorUnited email and password.
5. When the page says you are signed in, go back to Claude Code.

`/mcp` now shows `sponsorunited` as connected.

### 4. Try it

Ask Claude Code something like:

> Using SponsorUnited, what tools do you have?

## Good to know

- **You stay signed in.** You only sign in again if you don't use it for 30 days.
- **Changed your SponsorUnited password?** Access stops within 15 minutes.
  Sign in again with the new password: `/mcp`, pick `sponsorunited`, then
  **Authenticate**.
- **Sign out:** `/mcp`, pick `sponsorunited`, then **Clear authentication**.
- **Get updates:** `claude plugin marketplace update sponsorunited`.
- **Remove it:** `claude plugin uninstall sponsorunited@sponsorunited`.

## If something goes wrong

| What you see | What to do |
| --- | --- |
| The browser shows an error about port `53281` or the page never loads | Another program is using port 53281. Close it, or restart your computer, then sign in again. |
| The sign-in page says your email or password is wrong | Use the same email and password you use on sponsorunited.com. If you can't sign in there either, reset your password on sponsorunited.com first. |
| The sign-in page asks for a code | Check your email for a code from SponsorUnited and type it in. |
| `/mcp` shows `sponsorunited` as failed | Pick it and choose **Authenticate** again. |

Still stuck? Contact your SponsorUnited account team.

## For developers

This repository is a [Claude Code plugin marketplace](https://code.claude.com/docs/en/plugin-marketplaces).

```text
.claude-plugin/marketplace.json            the marketplace: lists the plugins
plugins/sponsorunited/.claude-plugin/plugin.json
plugins/sponsorunited/.mcp.json            the MCP server and its sign-in settings
docs/                                      setup guides for other AI apps
```

The plugin holds no secrets. Each AI app has its own public OAuth client: an ID
with no secret. Sign-in uses OAuth with PKCE. Check your changes with:

```bash
claude plugin validate --strict . && claude plugin validate --strict ./plugins/sponsorunited
```
