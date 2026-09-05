# Quietwire updates

Public version manifest and changelog for **Quietwire**, the in-house Dropbox for
Tailscale networks by ACAS Tools — one shared folder kept identical across every
machine you own, servers included, with a private web page for phones and other
devices. Files travel directly between your own machines; nothing goes through a cloud.

Quietwire reads `update-manifest.json` from this repository's `main` branch when —
and only when — a user chooses **Check for Updates** (dock page footer, tray menu, or
`--check-update`). The request carries no account, device, file, or usage information,
and Quietwire never downloads or runs an installer itself; it only reports whether a
newer version exists and links the release download page.

Version history: [CHANGELOG.md](CHANGELOG.md)

Contact: hello@acasintelligence.com · Copyright 2026 ACAS Tools.
