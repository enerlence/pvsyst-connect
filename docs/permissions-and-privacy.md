# What the assistant can and cannot do

Suntropy Connect decides what an AI assistant (Claude, ChatGPT or any MCP
client) can do on your computer. The rules are enforced **on the computer
itself**, before each request runs. The assistant cannot change them.

## What you decide

In Suntropy Connect, under **Connection → Assistant permissions**:

| Setting | Effect |
|---|---|
| **Read only** | Browse projects, variants, results already computed and files in the authorised folders. No simulations, nothing created. |
| **Read and simulate** | Also run simulations, create sites and convert weather files. Each one spends a run of your PVsyst license. |
| **Read, simulate and create** | Also create and edit projects, variants and files in the Suntropy library on that computer. |
| **Daily limit** | Maximum license runs per day that assistants can launch. When reached, simulations stop until the next day; reading keeps working. |
| **Pause** | Nothing at all until you resume it. Also available from the tray icon. |

And under **Connection → Authorized folders**: the only folders the assistant
can see, besides the Suntropy library. Suntropy Connect can look for PVsyst
workspaces and PV*SOL folders on your disk, but it only **proposes** them; you
tick the ones to share. You can remove any folder at any time.

The same screen shows a log of the latest requests: what was asked, on which
project, and whether it was done, failed or was blocked.

## What it can never do, whatever the settings

- Change, move or delete anything in your own PVsyst or PV*SOL folders. It
  reads them, and simulations run on copies.
- See folders you have not authorised, or the rest of your disk.
- Run other programs or commands: only the PVsyst operations listed in the
  connector.

## Where your data goes

- **Projects and license stay on your computer.** Simulations run with your
  own PVsyst, through its command line, on your machine.
- The app keeps an **outgoing** connection to Suntropy; no port is opened on
  your computer.
- What the assistant asks for (a project summary, simulation results, a
  chart) travels from your computer through Suntropy to the assistant, only
  when it is asked for. Suntropy does not keep copies of your project files.
- Files such as PDF reports or hourly CSVs are handed to the assistant as a
  **download link that expires after 24 hours** and is served directly from
  your computer.
- The history of simulation jobs is stored on your computer.
- The assistant signs in with **your Suntropy account** through OAuth, and you
  approve each assistant on a consent page that lists these same permissions.
  What the assistant then does with the answers is governed by its provider
  (Anthropic, OpenAI…) and your settings there.

## Revoking access

- Remove the connector in the assistant's settings, or
- disconnect the computer from Suntropy (Connection → Disconnect this
  computer, or from your Suntropy account), or
- pause access from the tray icon.
