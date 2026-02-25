# Hey, I'm Garrett 👋

**Mechanical engineer by degree, infrastructure builder by obsession.**

I design and build distributed systems for quantitative market analysis — a multi-node homelab running real-time data pipelines, time-series databases, and full-stack analytics dashboards. By day I'm a field engineer integrating avionics and mission computers for law enforcement and SAR aircraft. By night I'm deep in Docker Compose files and WebSocket streams.

---

### 🔧 What I'm Building

**QuantFlow** — A modular quantitative trading platform spread across dedicated hardware:

| Node | Role | Stack |
|------|------|-------|
| **NAS** (Proxmox) | Data warehouse + time-series DB | Ubuntu Server VM, OpenMediaVault, ZFS RAIDZ2, TimescaleDB, NFS |
| **NUC-Visualizer** | Analytics dashboard + research | FastAPI (BFF), React + TypeScript, Vite, Recharts, Lightweight Charts |
| **NUC-Trader** | Strategy execution engine | Python, event-driven architecture |
| **Jetson Xavier AGX** | ML inference + LLM serving | Ollama, FinBERT, CUDA, NVMe |
| **Pi 4B** | Network monitoring | Lightweight health polling |

The dashboard alone has 35+ macro endpoints, earnings scoring engines, real-time breadth analysis, Fed policy tracking, and multi-source sentiment aggregation — all backed by a 75-year FRED historical database.

> *"Despite their complexity, quant systems fundamentally aim to identify and exploit market inefficiencies just like traditional methods, but with greater precision and discipline"* — Rishi Narang, *Inside the Black Box*

<!-- 
SCREENSHOT PLACEHOLDER: Drop a screenshot of your dashboard here
![QuantFlow Dashboard](./assets/dashboard-preview.png)
-->

---

### 🏗️ Infrastructure

```
┌─────────────────────────────────────────────────────────────┐
│                    192.168.77.0/24 LAN                      │
│                   (10G + 1G Ethernet)                       │
│                                                             │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌───────────┐  │
│  │   NAS    │  │  NUC-VJ  │  │  NUC-TR  │  │  Jetson   │  │
│  │ Proxmox  │  │ Dashboard│  │ Executor │  │  Xavier   │  │
│  │          │  │          │  │          │  │           │  │
│  │ • OMV VM │  │ • FastAPI│  │ • Strats │  │ • Ollama  │  │
│  │ • ZFS 8x │  │ • React  │  │ • Orders │  │ • FinBERT │  │
│  │ • TSDB   │  │ • 8TB    │  │ • Risk   │  │ • 8TB     │  │
│  │ • NFS    │  │   NVMe   │  │ • 4TB    │  │   NVMe    │  │
│  └────┬─────┘  └────┬─────┘  └────┬─────┘  └─────┬─────┘  │
│       │   10G       │   1G        │   10G         │   1G   │
│       └─────────────┴─────────────┴───────────────┘        │
│                  Netgear GS110EMX Switch                    │
│                                                             │
│  ┌──────────┐         Private 10G Link:                     │
│  │  Pi 4B   │         NAS ↔ Jetson (10.10.20.0/24)         │
│  │ Monitor  │                                               │
│  └──────────┘                                               │
└─────────────────────────────────────────────────────────────┘
```

**Storage layer:** 8×SATA RAIDZ2 pool + 1TB L2ARC + 3TB NVMe hot storage for time-series data. NFS exports for read-only market data, read-write for backtest artifacts and ML models.

---

### 🛠️ Tech I Work With

**Infrastructure:** Proxmox, OpenMediaVault, ZFS, Docker/Compose, NFS, systemd, Tailscale

**Backend:** Python, FastAPI, TimescaleDB/PostgreSQL, SQLite, httpx, APScheduler, WebSockets

**Frontend:** React, TypeScript, Vite, Recharts, Lightweight Charts, Tailwind CSS, React Query

**Data:** Alpaca, FRED, FMP, Finnhub, FINRA, Yahoo Finance, CBOE, CFTC

**ML/AI:** Ollama, FinBERT, CUDA (Jetson Xavier AGX), DeepSeek

**Hardware:** Intel NUCs, NVIDIA Jetson Xavier AGX, Raspberry Pi, Netgear 10GbE switching

---

### 📌 Public Repos

Most of my work lives in private repos (4 interconnected services), but I share infrastructure patterns and templates publicly:

- 🏠 **[homelab-infrastructure](https://github.com/gman00910/homelab-infrastructure)** — Proxmox + ZFS + Docker Compose patterns from my build
- 📺 **[media-server-stack](https://github.com/gman00910/media-server-stack)** — Docker Compose media server with Plex/Sonarr/Radarr/etc.
<!-- Add more as you create them -->

---

### 📊 The Journey

I spent 4 years as a mechanical engineer designing hard drives at Seagate, then moved into avionics integration for airborne camera systems. Somewhere along the way I caught the trading bug, and that led me down the rabbit hole of building the infrastructure to do it right — which turned out to be a crash course in distributed systems, time-series databases, full-stack development, and ML pipelines.

---

### 📬 Get in Touch

- 💼 [LinkedIn](https://linkedin.com/in/garrettsmith33) 
- 📧 gm.smith1096@gmail.com 

---

<sub>*This profile was last updated February 2026. Infrastructure diagrams reflect current production topology.*</sub>
