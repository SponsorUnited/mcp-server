# SponsorUnited in claude.ai and Claude Desktop

Add SponsorUnited once on claude.ai. Claude Desktop and the Claude mobile apps
then use it too, because they share your Claude account's connectors.

## What you need

- A SponsorUnited account (the email and password you use on sponsorunited.com).
- A Claude account on a plan that allows custom connectors.
- On a Claude Team or Enterprise plan, only an owner can add a custom connector.
  If you are not an owner, ask one to do steps 1 to 5, then do "Connect" below.

## Values to copy

| Field | Value |
| --- | --- |
| Name | `SponsorUnited` |
| Remote MCP server URL | `https://mcp.sponsorunited.ai/mcp` |
| OAuth Client ID | `2qlhv32rigab3300b8b541p074` |
| OAuth Client Secret | leave empty |

## Add the connector

1. Open [claude.ai](https://claude.ai) and go to **Settings** > **Connectors**.
   On Team or Enterprise, owners go to **Organization settings** > **Connectors**.
2. Click **Add custom connector**.
3. Type the **Name** and the **Remote MCP server URL** from the table.
4. Click **Advanced settings**. Paste the **OAuth Client ID** from the table.
   Leave **OAuth Client Secret** empty.
5. Click **Add**.

## Connect

1. In **Settings** > **Connectors**, find **SponsorUnited** and click **Connect**.
2. A page opens on `login.sponsorunited.ai`. Sign in with your SponsorUnited
   email and password.
3. You return to claude.ai. SponsorUnited now shows as connected.

## Try it

Start a new chat. Open the tools menu in the message box and check that
SponsorUnited is on. Then ask something like:

> Using SponsorUnited, what tools do you have?

In Claude Desktop, the connector appears on its own. If it doesn't, quit and
reopen the app.

## Good to know

- **You stay signed in.** Sign-in lasts up to 30 days.
- **Changed your SponsorUnited password?** Access stops within 15 minutes. Go to
  **Settings** > **Connectors** > **SponsorUnited** and connect again.
- **Sign out:** **Settings** > **Connectors** > **SponsorUnited** > **Disconnect**.

## If something goes wrong

| What you see | What to do |
| --- | --- |
| After you save, the OAuth Client ID field is empty | Remove the connector and add it again. Paste the ID before you click **Add**. |
| The sign-in page says your email or password is wrong | Use the same email and password you use on sponsorunited.com. |
| The sign-in page asks for a code | Check your email for a code from SponsorUnited and type it in. |
| Claude says it can't reach SponsorUnited | Disconnect, then connect again. |

Still stuck? Contact your SponsorUnited account team.
