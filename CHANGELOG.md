# Quietwire changelog

## 0.8.1-beta.1
- Security: Host-header allowlist on every listener (DNS-rebinding defense); desktop-notification text is sanitized before display.

## 0.8.0-beta.1
- **Trash**: deleting a file or folder (from the page, or via sync from another dock) moves it to a trash kept for 30 days. Restore from the page; empty trash to purge.
- **Security**: cross-site request protection on every dock page; the local page and setup wizard are protected by a per-session token so other users or processes on the same machine cannot reach them; paths that cross a symlink are refused.

## 0.7.0-beta.1
- **Folders sync**: subfolders at any depth, empty folders, folder renames and deletes.
- Drag a whole folder onto the dock page to upload it with its structure.
- Hidden files, Thumbs.db/desktop.ini, Office lock files and symlinks are skipped on purpose.

## 0.6.2-beta.1
- Fix: renaming or quickly deleting a file in a shared folder could leave a stale copy on other docks (and get pushed back). Deletes now cover unsettled files, peers pull only settled files, and delete records are exchanged so everything converges.

## 0.6.1-beta.1
- Fix: Open Drop Folder on Windows opened Documents when the folder path used forward slashes.

## 0.6.0-beta.1
- **Shared folder mode** (on by default): every dock's folder converges to the
  same contents. Newest copy wins; deletes propagate; offline docks catch up.
- **Check for Updates** in the tray menu (Windows, macOS); `--check-update` on Linux.
- Dashboard: "shared folder" status line; per-file send hidden in shared mode.

## 0.5.1-beta.1
- **Local dock page**: the tray's Open Dock Page now opens a loopback address that
  works on the dock machine itself, even without the Tailscale client — files,
  other docks, check for updates and rename all available locally.

## 0.5.0-beta.1
- **Rename a dock in place** from the footer (and a `--rename` flag). Reuses the
  dock's Tailscale identity, so the device is renamed rather than recreated — no
  stale entries to clean up.

## 0.4.0-beta.1
- **Check for updates** in the dock footer, plus a visible version number.
- **Automatic recovery** when a dock's Tailscale identity is revoked (deleted
  from the admin console) â€” the dock reopens the setup wizard instead of hanging.
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
