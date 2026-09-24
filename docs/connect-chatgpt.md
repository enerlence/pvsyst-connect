# Connect ChatGPT to PVsyst

ChatGPT can use Suntropy Connect as a custom connector through its
**developer mode**. Once connected it can read your PVsyst projects, run
simulations and prepare reports on your computer.

## Before you start

- **Suntropy Connect** installed on the Windows computer that has PVsyst, and
  connected: the **Connection** tab shows a green light.
- A paid **ChatGPT** plan (Plus, Pro, Business, Enterprise or Edu). Developer
  mode is available on the web, at chatgpt.com. On Business, Enterprise and
  Edu a workspace admin may need to allow it.

## Steps

1. On chatgpt.com, open **Settings → Apps & Connectors → Advanced settings**
   and turn on **Developer mode**. (Suntropy Connect can open this screen for
   you: **Connection → Connect an assistant → ChatGPT → Open ChatGPT
   connectors**.)
2. Back in **Apps & Connectors**, choose **Create** (new connector) and fill in:
   - **Name:** `PVsyst Connect`
   - **MCP server URL:** `https://pvsyst-connect-gateway.suntropy.ai/pvsyst/mcp`
   - **Authentication:** OAuth
3. Tick **I trust this application** and press **Create**.
4. ChatGPT opens Suntropy. Sign in with your Suntropy account. The consent page
   lists exactly what the assistant will and will not be able to do; if it was
   you who created the connector, press **Authorise**.

ChatGPT does not accept a pre-filled link, so the address has to be pasted by
hand. You don't need to paste any key: the sign-in is OAuth.

For PV*SOL, create a second connector named `PV*SOL Connect` with
`https://pvsyst-connect-gateway.suntropy.ai/pvsol/mcp` (read only).

## Use it in a conversation

In a new chat, open the **+** menu, choose **Developer mode** and enable
**PVsyst Connect**. Then ask, for example:

> Run the simulation of variant VC0 of my project "Warehouse" and show me the
> monthly production.

More ideas in [Example prompts](example-prompts.md).

In developer mode ChatGPT asks you to confirm every tool that writes
something. Simulations spend runs of your PVsyst license.

## Troubleshooting

- **The connector can't be created / "unsafe URL":** developer mode only
  accepts `https` addresses. Use the address above, not the local one
  (`http://127.0.0.1…`) that the app shows before the computer is connected.
- **The computer does not answer:** Suntropy Connect must be running and
  connected on the computer with PVsyst (tray icon).
- **"Assistant permissions" refusal:** change it in Suntropy Connect under
  **Connection → Assistant permissions**. The assistant cannot change it.
- **New tools don't show up after an update:** open the connector in
  **Apps & Connectors** and refresh it, or delete it and create it again.

## Disconnect

Delete the connector in **Settings → Apps & Connectors**. To cut access from
every assistant at once, disconnect the computer from Suntropy or pause access
from the tray icon.
