# Hey, I'm Garrett 👋

I spent 4 years as a mechanical engineer designing hard drives at Seagate, then moved into avionics integration for airborne computer systems for mission aircrafts. Somewhere along the way I caught the trading bug, and that led me down the rabbit hole of building the infrastructure to do it right. 

This turned out to be a multi-year crash course in distributed systems, time-series databases, full-stack development, and ML pipelines. I've fully designed and built a multi-node, distributed system for quantitative market analysis, with stress on data reliability, and parity across live and "backtest" engines. 

---

### What I'm Building

**QuantFlow** — A modular quantitative trading platform:

| Node | Role | Stack |
|------|------|-------|
| **NAS** (Proxmox) | Data warehouse + time-series DB | Ubuntu Server VM, OpenMediaVault, ZFS RAIDZ2, TimescaleDB, NFS |
| **NUC-Visualizer** | Analytics dashboard + research | FastAPI (BFF), React + TypeScript, Vite, Recharts, Lightweight Charts |
| **NUC-Trader** | Strategy execution engine | Python, event-driven architecture |
| **Jetson** | ML inference + LLM serving | Ollama, FinBERT, CUDA |
| **Pi 4B** | Grafana | Network monitoring | Lightweight health polling |

The dashboard alone has 35+ macro endpoints, earnings scoring engines, real-time breadth analysis, Fed policy tracking, and multi-source sentiment aggregation. This is all used for varous strategies and a dynamic playbook for extracting alpha from the markets.

> *"Despite their complexity, quant systems fundamentally aim to identify and exploit market inefficiencies just like traditional methods, but with greater precision and discipline"* — Rishi Narang, *Inside the Black Box*

<!-- 
SCREENSHOT PLACEHOLDER: Drop a screenshot of your dashboard here
![QuantFlow Dashboard](./assets/dashboard-preview.png)
-->

---

### 📌 Public Repos

Most of my work lives in private repos (4 interconnected services), but I share infrastructure patterns and templates publicly:

- 🏠 **[homelab-infrastructure](https://github.com/gman00910/homelab-infrastructure)** — Proxmox + ZFS + Docker Compose patterns from my build
- 📺 **[media-server-stack](https://github.com/gman00910/media-server-stack)** — Docker Compose media server with Plex/Sonarr/Radarr/etc.
<!-- Add more as you create them -->

---

### 📬 Get in Touch

- 💼 [LinkedIn](https://linkedin.com/in/garrettsmith33) 
- 📧 gm.smith1096@gmail.com 

---

<sub>*This profile was last updated February 2026. Infrastructure diagrams reflect current production topology.*</sub>
