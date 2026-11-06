# SponsorUnited in ChatGPT

ChatGPT adds SponsorUnited as a custom app (a connector). ChatGPT changes the
names of these menus often, so a label may differ a little from what you see.

## What you need

- A SponsorUnited account (the email and password you use on sponsorunited.com).
- A ChatGPT plan that allows custom apps with developer mode.
- On a ChatGPT Business or Enterprise workspace, an admin may have to turn on
  developer mode or add the app for you.

## Values to copy

| Field | Value |
| --- | --- |
| Name | `SponsorUnited` |
| MCP server URL | `https://mcp.sponsorunited.ai/mcp` |
| Authentication | OAuth |
| OAuth client ID | `__PROD_CHATGPT_CLIENT_ID__` |
| OAuth client secret | leave empty |

## 1. Turn on developer mode

1. In ChatGPT, open **Settings** > **Apps**.
2. Open **Advanced settings** and turn on **Developer mode**.

## 2. Create the app

1. In **Settings** > **Apps**, click **Create app**.
2. Type the **Name** and the **MCP server URL** from the table.
3. Set **Authentication** to **OAuth**.
4. Open the advanced OAuth settings. Choose a user-defined (pre-registered)
   OAuth client, not dynamic registration.
5. Paste the **OAuth client ID** from the table. Leave the client secret empty.
6. Accept the warning about custom apps, then click **Create**.

## 3. Sign in

1. ChatGPT opens a page on `login.sponsorunited.ai`. Sign in with your
   SponsorUnited email and password.
2. You return to ChatGPT. SponsorUnited now shows as connected.

## 4. Try it

Start a new chat. Click **+** in the message box, pick SponsorUnited, and ask
something like:

> Using SponsorUnited, what tools do you have?

## Good to know

- **You stay signed in.** You only sign in again if you don't use it for 30 days.
- **Changed your SponsorUnited password?** Access stops within 15 minutes.
  Open **Settings** > **Apps** > **SponsorUnited** and connect again.
- **Sign out:** **Settings** > **Apps** > **SponsorUnited** > **Disconnect**.

## If something goes wrong

| What you see | What to do |
| --- | --- |
| The sign-in page shows `redirect_mismatch` or an invalid redirect error | Contact your SponsorUnited account team. They need to allow ChatGPT's sign-in address. |
| You can't find **Create app** | Turn on developer mode first (step 1). On a work workspace, ask your ChatGPT admin. |
| The sign-in page says your email or password is wrong | Use the same email and password you use on sponsorunited.com. |
| The sign-in page asks for a code | Check your email for a code from SponsorUnited and type it in. |

Still stuck? Contact your SponsorUnited account team.
