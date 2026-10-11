<p align="center">
  <img src="https://networktests.com/img/monitor/monitor-overview-2x.webp" alt="NetworkTests Monitor dashboard" width="760">
</p>

# NetworkTests

**Free network diagnostics — find out what's actually wrong with your connection, and prove it.**

Two tools, two kinds of problem:

| Something is wrong **right now** | The problem **comes and goes** |
|---|---|
| **[networktests.com](https://networktests.com)** — instant browser tests: packet loss, latency, jitter, download/upload, MTR & reverse path, DNS leak, TLS interception check, and more. Nothing to install. | **NetworkTests Monitor** — a desktop app for macOS, Windows and Linux that watches your connection every second and tells you in plain English where problems start: your Wi-Fi, your router, your ISP, your computer — or the app you're using. |

---

## NetworkTests Monitor — Download v0.4.3

**Free for personal use · No account · All data stays on your machine**

| Platform | File | SHA-256 |
|---|---|---|
| macOS 12+ (Universal, signed & notarized) | [NetworkTests-Monitor-0.4.3.pkg](https://github.com/networktests/networktests/releases/download/v0.4.3/NetworkTests-Monitor-0.4.3.pkg) | `b6a8b79e57a37c7a365435306c6951db684197876b510cbe9478c74857e5b4ad` |
| Windows 10/11 x64 (signed MSI) | [NetworkTests-Monitor-setup-0.4.3.msi](https://github.com/networktests/networktests/releases/download/v0.4.3/NetworkTests-Monitor-setup-0.4.3.msi) | `449270efbc17c70b02b4d26af4914c67c333424f7761a94bf8a13456b7b8cb5e` |
| Linux x86_64 | [networktests-monitor-0.4.3-linux-amd64.tar.gz](https://github.com/networktests/networktests/releases/download/v0.4.3/networktests-monitor-0.4.3-linux-amd64.tar.gz) | `079c7d3bcc1310a63c8148146eb9727f82c5ce8238b7f6bbcc473e8f75c00d32` |
| Linux arm64 | [networktests-monitor-0.4.3-linux-arm64.tar.gz](https://github.com/networktests/networktests/releases/download/v0.4.3/networktests-monitor-0.4.3-linux-arm64.tar.gz) | `ca3a2558224ba03a7d3d89f78b73b109e31e107197c236efd05a8d3d3e59eb70` |

Linux one-liner (installs dependencies, the app, and a menu entry):

```sh
curl -fsSL https://networktests.com/downloads/install.sh | sh
```

### What Monitor does

- **Per-second probes, three tiers** — your router, your ISP's first hop (auto-discovered), and five independent internet anchors (Google, Cloudflare, Quad9 DNS). Internet loss is packet-weighted across all five, so one server rate-limiting pings can't fake an outage.
- **Plain-English verdicts** — the elimination work (Wi-Fi vs router vs upstream vs machine) is done for you: *"Packets are being lost beyond your router — this is your ISP, not your home network."*
- **Application monitors** — one click for Zoom, Teams, Slack, Microsoft 365, Salesforce, Meet, GitHub, or any host (up to 30; HTTPS, TCP, or ping). HTTPS checks dissected into DNS → TCP → TLS → server wait → transfer, against a baseline learned from your own connection.
- **Aggregated alerts** — one slow app is that app's problem; several slowing together is your network. Only the latter notifies.
- **Hop-by-hop paths** — continuous MTR-style tracing to Google and Cloudflare plus up to three of your own destinations (ICMP/UDP), history from 5 minutes to 7 days.
- **Speed tests that catch bufferbloat** — on-demand and twice daily, measuring latency *under load*; ≥2× inflation + 200 ms flags it, with the SQM fix named.
- **PDF evidence report** — charts, app breakdowns, hop tables and the event timeline for any window up to 7 days. Built for ISP support tickets.
- **System correlation** — CPU/memory tracked alongside; a maxed-out machine gets blamed as the machine, not your ISP.

### Privacy

Monitoring history lives in a local database on your computer. No account, no sign-up, no central dashboard. Monitor generates only the network traffic required for its own measurements — verifiable with Little Snitch or Wireshark. Reports leave your machine only when you export and share one.

### Requirements & notes

- **macOS** 12+, Apple Silicon or Intel. Lives in the menu bar.
- **Windows** 10/11 64-bit. Runs in the system tray (check the `^` overflow — Windows hides new tray icons by default).
- **Linux** x86_64/arm64, WebKitGTK 4.1 + GTK 3 (the installer handles these on Ubuntu/Fedora). Needs a desktop session; Wi-Fi detail not read yet; GNOME tray needs the AppIndicator extension.
- Installers are signed by **HostAnywhere LLC** — the company behind networktests.com.

## Issues & feedback

NetworkTests Monitor is distributed as signed binaries (closed source). This repository hosts releases and documentation — bug reports and feature requests for the app **and** the website are very welcome in [Issues](https://github.com/networktests/networktests/issues).

## Learn more

- Product page: https://networktests.com/monitor
- Announcement: https://networktests.com/blog/networktests-monitor
- Bufferbloat testing guide: https://networktests.com/blog/bufferbloat-test-monitor
- Guides: proving packet loss to your ISP, reading MTR, fixing bufferbloat → https://networktests.com/blog
