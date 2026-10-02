# Link Order for macOS

Native menu bar network priority manager for **macOS 14+**, with Universal Apple Silicon and Intel installers. English interface.

## Download

[Download Link Order Community](https://github.com/drony/link-order-releases/releases/tag/v1.0.0)

Choose the **PKG** for direct installation, or the **DMG** containing the installer, notes and uninstaller. No Apple Developer account or Xcode is needed.

This repository contains public installation files and release notes. Source development is maintained separately.

## Install

1. Quit any previous Link Order version.
2. Open the PKG and approve macOS administrator access.
3. Open **Link Order** from Applications.

The Community edition uses local ad hoc signatures, without Apple Developer ID signing or notarization. If macOS blocks the installer, its **Privacy & Security → Open Anyway** flow may be required. Managed Macs may restrict installations. See [Apple's opening instructions](https://support.apple.com/en-us/102445).

## Included

- Menu bar panel and optional main window.
- Live drag reorder, service switches, Wired First / Wi-Fi First / Cellular Hotspot / Charge Only presets and saved profiles.
- Native macOS Network Locations.
- Muted disconnected adapters, green default-route indicators and measured traffic activity.
- Per-adapter RX/TX speeds, 60-second graphs and interface totals since boot.
- Optional 30-second health checks, wired dock automation, login launch and global Option+1/2/3/0 shortcuts.
- A narrow administrator helper for system network changes and persistent cellular blocking.
- App proxy mode for explicitly configured SOCKS5 applications, plus separate browser profiles for recognized Chrome, Brave, Edge, Chromium and Firefox bundles.

## App Routing limits

Community app proxy mode forwards **TCP only** through the selected available interface. Apps must use the shown SOCKS5 endpoint. The original browser session is unchanged. DNS uses macOS settings; UDP, WebRTC, existing connections and traffic bypassing the proxy are not covered. Counters describe endpoint traffic, not verified app identity. Some VPN policies or tunnel interfaces cannot support this path. It is not an app-wide kill switch.

General transparent routing for apps that do not support proxies requires the separately signed Network Extension edition. That extension is excluded from the Community installer. End users of a signed edition still do not need Xcode or an Apple Developer account.

## Release status

**Community beta.** Universal compilation, package creation and code-integrity checks completed. Clean-machine installation, physical adapter switching and live proxy/VPN traffic compatibility have not been validated on the developer's existing network. Report reproducible issues here; omit private IP/MAC addresses or credentials from screenshots/logs.

The installer pins the exact app build for helper access. Reinstall the new PKG for updates. Quitting the app stops its local proxies; persistent Charge Only continues if enabled. The DMG uninstaller removes the helper, retains personal profiles/browser data, and leaves disabled network services off.
