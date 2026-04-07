<br>
<p align="center">
  <a href="#_">
    <img src="https://raw.githubusercontent.com/lastparody/OPENGATE/main/.github/images/logo.svg" width="320" alt="OpenGate Logo">
  </a>
</p><br>

<p align="center">
  <a href="https://ozkantanrikulu.com" target="_blank" rel="noopener noreferrer"><img src="https://img.shields.io/badge/Powered%20by-Özkan%20Tanrıkulu-1e6eb5?style=plastic" alt="Powered by Özkan Tanrıkulu"></a>&nbsp;&nbsp;<a href="#"><img src="https://img.shields.io/badge/version-1.0.3-e94560?style=plastic" alt="Version"></a>&nbsp;&nbsp;<a href="#"><img src="https://img.shields.io/badge/macOS-14.0+-000000?style=plastic" alt="macOS"></a>&nbsp;&nbsp;<a href="#"><img src="https://img.shields.io/badge/Silicon%20%26%20Intel-compatible-cd7700?style=plastic" alt="Architecture"></a>&nbsp;&nbsp;<a href="#"><img src="https://img.shields.io/badge/license-Proprietary-9b59b6?style=plastic" alt="License"></a>&nbsp;&nbsp;<a href="https://virustotal.com/gui/file/623398d887cd857673805d68cb2dea91e0aca2859cb9e9b0783a94e95a117bc7" target="_blank" rel="noopener noreferrer"><img src="https://img.shields.io/badge/VirusTotal-Clean-brightgreen?style=plastic&logo=virustotal&logoColor=white" alt="VirusTotal"></a>


  
</p> <br>

<p align="center">
A native macOS app that bypasses ISP censorship and DPI filtering via SNI fragmentation, TCP segmentation, and DNS-over-HTTPS — one click to connect.
</p>

---

## What is OpenGate?

OpenGate is a native macOS application powered by a high-performance Go core. It defeats Deep Packet Inspection (DPI) through multi-layered evasion techniques, wrapped in a clean SwiftUI interface. No terminal. No configuration files. No technical knowledge required.

---

## Features

- **SNI Fragmentation** — Splits TLS Client Hello packets to prevent hostname-based filtering
- **TCP Segmentation** — Breaks TCP streams into small segments to confuse stateful DPI engines
- **DNS-over-HTTPS (DoH)** — Encrypts all DNS queries over HTTPS, eliminating DNS-based blocking and surveillance
- **Automatic System Proxy** — Instantly routes all macOS network traffic through the bypass core with a single click
- **Local Network Broadcasting** — Turns your Mac into a proxy server, extending DPI protection to every device on your local network
- **Launch at Login** — Automatically activates protection when you log in
- **Universal Binary** — Runs natively on both Apple Silicon and Intel Macs

---

## Performance

OpenGate is engineered for minimal system impact. Every component is optimized to run silently in the background without affecting your experience.

| Metric | Value |
|--------|-------|
| RAM Usage | ~30 MB (stable, background) |
| CPU Usage | <0,1% (idle) |
| Battery Impact | Negligible |
| Network Speed | No reduction |
| Initial Handshake Latency | +30–150 ms (first request only) |

> The 30–150 ms latency occurs only on the first connection handshake due to SNI fragmentation. All subsequent traffic flows at full speed with zero overhead.

---

## Installation

1. Download the latest `OpenGate.dmg` from [Releases](https://github.com/lastparody/opengate/releases)
2. Open the DMG and drag **OpenGate.app** to your Applications folder
3. On first launch, if macOS shows a security warning:
   - Close the dialog
   - Go to **System Settings → Privacy & Security**
   - Click **"Open Anyway"**

> OpenGate is not notarized by Apple. This is expected for open-distribution software. The security warning is a standard macOS Gatekeeper prompt.

---

## How to Use

1. Launch OpenGate from your Applications folder
2. Click the **shield button** to connect
3. The button turns green when protection is active
4. All network traffic is now routed through OpenGate

That's it.

---

## Settings

| Setting | Description |
|---------|-------------|
| Local Network Gateway | IP address for the bypass tunnel (default: 127.0.0.1) |
| DNS Address | DNS resolver address (default: 8.8.8.8) |
| Connection Port | Local port for the bypass core (default: 9090) |
| Secure DNS (DoH) | Encrypts DNS queries over HTTPS |
| IPv4 Priority | Forces DNS resolution to IPv4 for maximum stability |
| Network Scope | System-wide or application-based proxy mode |
| Proxy Broadcast | Share protection with other devices on your network |
| Launch at Startup | Auto-connect when you log in |

---


## FAQ

**❓ Does OpenGate slow down my internet?**
- No. Zero overhead on throughput. The only delay is a one-time **30–150 ms** on the first handshake due to SNI fragmentation — all subsequent traffic runs at full speed.

**❓ Does it drain my battery?**
- No. The Go core is event-driven and sleeps when idle. CPU usage stays below **0.1%** during normal operation.

**❓ How much RAM does it use?**
- Approximately **30 MB**, stable. Does not grow over time.

**❓ Do I need to keep the app open?**
- Yes. Enable **Launch at Startup** in settings to start it automatically on login.

**❓ Can I use it on other devices on the same network?**
- Yes. Enable **Proxy Broadcast Station** in settings, then configure the target device manually.

**❓ Is my traffic logged?**
- No. OpenGate runs entirely on your device. No data is sent to any external server.
  
---

## License

This software is proprietary. See [LICENSE](https://github.com/lastparody/opengate/blob/main/LICENSE) for full terms.

---

<p align="center">
2026 <a href="https://ozkantanrikulu.com">Özkan Tanrıkulu</a>  © OpenGate All Rights Reserved
    <br><a href="mailto:ozkantanrikulu98@gmail.com">ozkantanrikulu98@gmail.com</a>
</p>
