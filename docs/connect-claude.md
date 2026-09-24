# Connect Claude to PVsyst

Once Suntropy Connect is installed and your computer is connected to Suntropy,
Claude can read your PVsyst projects, run simulations and prepare reports on
that computer. This guide takes about two minutes.

## Before you start

- **Suntropy Connect** installed on the Windows computer that has PVsyst, and
  connected: the **Connection** tab shows a green light. See the
  [README](../README.md) to download it.
- A **Claude** plan that allows custom connectors: Pro, Max, Team or
  Enterprise. On Team and Enterprise an organisation owner adds the connector
  first, under the organisation settings.

## Option 1: one click from the app

In Suntropy Connect, go to **Connection → Connect an assistant → Claude** and
press **Add to Claude**. Claude opens the "Add custom connector" dialog with
the name and address already filled in. Check them and confirm.

## Option 2: by hand

1. In Claude, open **Settings → Connectors** and choose **Add custom connector**.
2. Fill in:
   - **Name:** `PVsyst Connect`
   - **Remote MCP server URL:** `https://pvsyst-connect-gateway.suntropy.ai/pvsyst/mcp`
3. Press **Add**, then **Connect**.
4. Claude opens Suntropy. Sign in with your Suntropy account. A consent page
   lists exactly what the assistant will and will not be able to do; if it was
   you who added the connector, press **Authorise**.

For PV*SOL, repeat with the name `PV*SOL Connect` and the address
`https://pvsyst-connect-gateway.suntropy.ai/pvsol/mcp`. The PV*SOL connector
is read only: PV*SOL has no command line, so it reads the results already
saved in your projects.

## Use it in a conversation

In a new chat, open the **+** menu → **Connectors** and make sure
**PVsyst Connect** is on. Then just ask, for example:

> List my PVsyst projects and summarise the system of the most recent one.

More ideas in [Example prompts](example-prompts.md).

Claude asks for your confirmation before tools that change something (create
a project, edit a variant). Simulations spend runs of your PVsyst license:
check how many are left with *"How many PVsyst license runs do I have left?"*.

## Claude Code

One command, using the credential of the connected computer instead of OAuth:

```
claude mcp add --transport http pvsyst https://pvsyst-connect-gateway.suntropy.ai/pvsyst/mcp --header "x-api-key: YOUR_KEY"
```

Suntropy Connect shows the exact command with your key under
**Connection → Connect an assistant → Claude**, with a button to copy it.

## Troubleshooting

- **"No PVsyst worker registered" / the computer does not answer:** Suntropy
  Connect must be running and connected on the computer with PVsyst. Look for
  its icon in the Windows tray.
- **"Assistant permissions" refusal:** the assistant tried something you
  have not allowed on that computer (for example a simulation while access is
  set to *Read only*, or access is paused). Change it in Suntropy Connect under
  **Connection → Assistant permissions**. The assistant cannot change it.
- **A folder is missing:** the assistant only sees the Suntropy library and
  the folders you authorised. Add it under **Connection → Authorized folders**.
- **New tools don't show up after an update:** disconnect and reconnect the
  connector in Claude's settings to refresh the tool list.

## Disconnect

Remove the connector in Claude's **Settings → Connectors**. To cut access
from every assistant at once, disconnect the computer from Suntropy, or pause
access from the tray icon.
