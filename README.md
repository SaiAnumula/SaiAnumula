<div align="center">

# Hi, I'm Sai Anumula 👋

### Network Engineering Technology + Cybersecurity @ Purdue University

**Infrastructure · Automation · Security · Local AI**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Sai%20Anumula-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/saianumula)
[![GitHub](https://img.shields.io/badge/GitHub-SaiAnumula-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/SaiAnumula)

</div>

---

## About me

I'm a junior at Purdue University dual-majoring in **Network Engineering Technology** and **Cybersecurity**, with an expected graduation date of **May 2028**.

I learn by building and maintaining systems I actually use: Linux machines, self-hosted services, monitoring, local AI tooling, and automation that runs my own internship search. Everything below is in production for me, not built for a screenshot.

## What I run

| Environment | Technologies | Purpose |
|---|---|---|
| **Primary server** | Ubuntu Server · Docker | Always-on Plex, Jellyfin, and Immich for the household |
| **Main desktop** | CachyOS · RX 9070 (16 GB) · 24 GB DDR4 | Daily Linux system, local AI inference, on-demand game hosting |
| **Game node** | Linux · Intel laptop | Runs smaller Minecraft and Palworld workloads when needed |
| **Remote administration** | Tailscale | Private access to approved systems without exposing management interfaces |
| **Observability** | Prometheus · Grafana · Loki (Grafana Alloy) | Metrics and logs for the machines I depend on |
| **Hardware projects** | Custom PCs · Raspberry Pi | Desktop, server, and NAS experimentation |

## Featured work

### 🏠 [Homelab](https://github.com/SaiAnumula/homelab)

My homelab is where I practice Linux administration, containerization, networking, storage planning, and troubleshooting. It includes:

- Docker-based Plex, Jellyfin, and Immich deployments, one Compose file per service
- Private remote administration through Tailscale; game servers use a single forwarded Playit port, nothing else
- CI that validates every Compose file and rejects unpinned image tags
- Backup documentation with a restore test that runs on a second machine

The architecture, sanitized configurations, and design decisions are documented in the [homelab repository](https://github.com/SaiAnumula/homelab).

### 📊 [Mission Control](https://github.com/SaiAnumula/homelab-mission-control)

A self-hosted monitoring dashboard, styled after btop, that shows the state of every machine on one page:

- A Python telemetry agent per host that uses only the standard library
- CPU, GPU, VRAM, memory, disk, temperature, Docker containers, and systemd services per device
- SMART drive health when `smartctl` is available, and UP/DOWN/DEGRADED/STALE status with stale readings labeled during outages
- React frontend with a standalone Python production server, reachable only over the LAN or tailnet

### 🤖 [Local AI assistant](https://github.com/SaiAnumula/local-ai-assistant)

Architecture notes, benchmark tooling, and sanitized results for the personal assistant I run with the Hermes agent and locally hosted open-weight models through Ollama:

- Re-tuned the whole stack when a RAM stick died and the machine dropped from 32 GB to 24 GB: moved the KV cache to q8_0, cut context from 128K to 64K, and verified the fit under the same systemd memory limits as production
- A benchmark suite for prefill speed, decode throughput, near-window recall, tool-call reliability, and calendar JSON correctness
- Memory telemetry on every run — RAM, swap, memory pressure, and VRAM — with a guard that aborts a benchmark before it starves the desktop
- CI runs the harnesses against a mock Ollama server, plus `shellcheck`, `ruff`, and a secret scan

### 🔒 Production systems (private)

Some of my current work stays private because it holds personal data or employer information. Descriptions only, no links:

- An automated multi-stage internship pipeline: discovers postings, scores them against my resume, drafts applications, and fills forms behind my own review — 780+ tests, a SQLite store, and a dashboard reachable only over Tailscale.
- A Tauri 2 + React 19 desktop tracker for the applications themselves: local-first, no cloud service, data stays on my machine.
- A fail-closed multi-provider AI quota workflow: routes work across providers and stops when quota is exhausted instead of silently overspending.

### 🎬 Raspberry Pi NAS proof of concept

For a class project, I built a working NAS with a **Raspberry Pi 5** and documented the process on video—including the problems I encountered and how I adapted the build.

▶️ **[Watch the Raspberry Pi NAS walkthrough](https://youtu.be/0SLmClxMjxE)**

## Tools and technologies

### Operating systems & infrastructure

<p>
  <img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black" alt="Linux" />
  <img src="https://img.shields.io/badge/CachyOS-1793D1?style=flat-square&logo=archlinux&logoColor=white" alt="CachyOS (Arch-based)" />
  <img src="https://img.shields.io/badge/Ubuntu-E95420?style=flat-square&logo=ubuntu&logoColor=white" alt="Ubuntu" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/Tailscale-242424?style=flat-square&logo=tailscale&logoColor=white" alt="Tailscale" />
</p>

### Observability

<p>
  <img src="https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white" alt="Prometheus" />
  <img src="https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white" alt="Grafana" />
  <img src="https://img.shields.io/badge/Loki-1F2937?style=flat-square&logo=grafana&logoColor=white" alt="Loki" />
</p>

### Languages & scripting

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white" alt="Bash" />
  <img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white" alt="Rust" />
  <img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white" alt="Java" />
</p>

### Apps, data & development tools

<p>
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" alt="React" />
  <img src="https://img.shields.io/badge/Tauri-FFC131?style=flat-square&logo=tauri&logoColor=black" alt="Tauri" />
  <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" alt="SQLite" />
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" alt="Git" />
  <img src="https://img.shields.io/badge/Microsoft%20Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white" alt="Microsoft Azure" />
</p>

## Current focus

- Run the Summer 2027 internship search on my automated pipeline and keep its test suite and dashboard healthy
- Repeat the local-AI reliability suite per case at 64K context so model choices rest on repeated runs, not one-shot results
- Extend the observability stack across the homelab with alerting, and keep backup restore tests regular
- Keep building networking and cybersecurity skills beyond coursework: trust boundaries, firewalling, and secret hygiene

---

<div align="center">

**Seeking networking, infrastructure, and cybersecurity internship opportunities for Summer 2027. [Connect with me on LinkedIn](https://www.linkedin.com/in/saianumula).**

</div>
