# Quietwire changelog

## 0.4.0-beta.1
- **Check for updates** in the dock footer, plus a visible version number.
- **Automatic recovery** when a dock's Tailscale identity is revoked (deleted
  from the admin console) — the dock reopens the setup wizard instead of hanging.
- First bundled **PDF user guide** (Tailscale setup, install, usage, FAQ).

## 0.3.1-beta.1
- Upgrades always find the existing config (per-user install location); no more
  duplicate dock identities or re-run wizards on update.
- Working diagnostic log on Windows GUI builds.

## 0.3.0-beta.1
- **Dock-to-dock send**: push a file from one dock straight to another; bytes
  travel machine-to-machine over the tailnet.
- **Dock discovery**: each dock page lists the other docks on your network.
- **Tailnet HTTPS**: padlocked `https://<dock>.<tailnet>.ts.net/` when HTTPS
  certificates are enabled in the Tailscale admin console.

## 0.2.0-beta.1
- Tray / menu-bar app, silent background running, start-at-login.
- Windows `.exe` and macOS `.dmg` installers.
- Delete files, quick text notes, arrival notifications.

## 0.1.0
- Initial single-node drop dock: browser to machine, machine to browser.
