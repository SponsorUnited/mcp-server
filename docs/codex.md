# SponsorUnited in Codex

These steps work for the Codex CLI. The Codex IDE extension and desktop app read
the same settings file, so they pick it up too.

## What you need

- A SponsorUnited account (the email and password you use on sponsorunited.com).
- [Codex](https://learn.chatgpt.com/docs/extend/mcp?surface=cli), installed and
  signed in.
- A web browser on the same computer. Sign-in opens a browser page.

## 1. Add the server

SponsorUnited only accepts sign-ins that come back on port `53282`, so set that
port before you sign in. Open your Codex settings file, `~/.codex/config.toml`
(create it if it does not exist), and add this:

```toml
[mcp_servers.sponsorunited]
url = "https://mcp.sponsorunited.ai/mcp"

[mcp_servers.sponsorunited.oauth]
client_id = "__PROD_CODEX_CLIENT_ID__"
callback_port = 53282
```

## 2. Sign in

```bash
codex mcp login sponsorunited
```

1. A browser page opens on `login.sponsorunited.ai`. Sign in with your
   SponsorUnited email and password.
2. When the page says you are signed in, go back to the terminal.

## 3. Try it

Run `codex mcp list` and check that `sponsorunited` is there. Then start
`codex` and ask something like:

> Using SponsorUnited, what tools do you have?

## Good to know

- **You stay signed in.** Sign-in lasts up to 30 days.
- **Changed your SponsorUnited password?** Access stops within 15 minutes. Run
  `codex mcp login sponsorunited` again and use the new password.
- **Sign out:** `codex mcp logout sponsorunited`.
- **Remove it:** `codex mcp remove sponsorunited`.

## If something goes wrong

| What you see | What to do |
| --- | --- |
| The sign-in page shows `redirect_mismatch` or an invalid redirect error | `callback_port = 53282` is missing or in the wrong section. Check step 1, then sign in again. |
| The browser can't reach `127.0.0.1:53282` | Another program is using port 53282. Close it, or restart your computer, then sign in again. |
| The sign-in page says your email or password is wrong | Use the same email and password you use on sponsorunited.com. |
| The sign-in page asks for a code | Check your email for a code from SponsorUnited and type it in. |

Still stuck? Contact your SponsorUnited account team.
