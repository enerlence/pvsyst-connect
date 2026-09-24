# Suntropy Connect for PVsyst and PV*SOL

Downloads and updates for the desktop app that connects the **licensed PVsyst
installed on your computer** (and your PV*SOL projects) with Suntropy and with
AI assistants such as Claude and ChatGPT.

**[Download for Windows](https://github.com/enerlence/pvsyst-connect/releases/latest)**

Requires Windows and PVsyst 8.x with an active license. You don't need to be an
administrator to install it. The app speaks English and Spanish (it follows
your system language; you can change it under Connection → Language or from
the tray icon).

*Versión en español: [README.es.md](README.es.md).*

## Guides

- [Connect Claude](docs/connect-claude.md): claude.ai, Claude Desktop and Claude Code.
- [Connect ChatGPT](docs/connect-chatgpt.md): developer mode on chatgpt.com.
- [What the assistant can and cannot do](docs/permissions-and-privacy.md): permissions, data and privacy.
- [Example prompts](docs/example-prompts.md): what to ask once it's connected.

## What the app does

Your PVsyst license and your projects **stay on your computer**. The app opens
an outgoing connection to Suntropy (no ports to open, no firewall changes) and
serves what is asked from there: reading projects, running simulations with
the PVsyst command line and returning results.

An AI assistant reaches it through Suntropy's MCP server:

| Program | MCP server address |
|---|---|
| PVsyst | `https://pvsyst-connect-gateway.suntropy.ai/pvsyst/mcp` |
| PV*SOL (read only) | `https://pvsyst-connect-gateway.suntropy.ai/pvsol/mcp` |

The assistant signs in with your Suntropy account (OAuth) and only sees the
folders you authorised in the app. You can pause it, limit it to reading, or
cap the license runs per day, and revoke it at any time.

## What's in this repository

Only the published binaries. **The source code is not in this repository**:
it lives in a private one, and only compiled versions and the metadata file
used by the app's auto-updater are published here.

| File | Purpose |
|---|---|
| `PVsystConnect-Setup-<version>.exe` | The installer. This is what you download |
| `latest.yml` | Read by the app itself to know whether there is a new version |
| `*.blockmap` | Lets an update download only what changed |

The app updates itself: it checks for a new version, downloads it in the
background and lets you know. It never restarts on its own while a simulation
is running.

## Windows warning when installing

The installer is not signed with a publisher certificate yet, so Windows
SmartScreen may warn that it doesn't recognise the publisher. That's expected
until there is a certificate: "More info" → "Run anyway".

## More

- Product page: <https://pvsyst-connect.suntropy.ai>
- Suntropy: <https://suntropy.ai>
- Support: reply to any Suntropy email or write from your Suntropy account.
