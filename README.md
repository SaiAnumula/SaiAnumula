<div align="center">

# Hi, I'm Sai Anumula

### Network Engineering Technology + Cybersecurity @ Purdue University

Infrastructure · Automation · Security · Local AI

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Sai%20Anumula-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/saianumula)
[![GitHub](https://img.shields.io/badge/GitHub-SaiAnumula-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/SaiAnumula)

</div>

---

## About me

I'm a junior at Purdue University dual-majoring in Network Engineering Technology and Cybersecurity, graduating in May 2028.

I learn by running systems I use every day. Most of my time goes into Linux servers, self-hosted services, monitoring, local AI benchmarks, and small tools I build for myself and friends.

## What I run

| Environment | Technologies | Purpose |
|---|---|---|
| Primary server | Ubuntu Server, Docker | Always-on Plex, Jellyfin, and Immich for the household |
| Main desktop | CachyOS, RX 9070 (16 GB), 24 GB DDR4 | Daily Linux system, local AI testing, and on-demand game hosting |
| Laptop node | Ubuntu, Intel i3 | Runs smaller game servers and background jobs when needed |
| Remote access | Tailscale | Private admin access between approved devices without opening management ports |
| Monitoring | Prometheus, Grafana, Loki, Alloy | Host metrics, container telemetry, and log collection across machines |
| Hardware builds | Custom PCs, Raspberry Pi | Desktop, server, and NAS builds |

## Featured work

### [Homelab](https://github.com/SaiAnumula/homelab)

My homelab is where I practice Linux administration, Docker, networking, storage, and troubleshooting.

- Docker Compose setups for Plex, Jellyfin, and Immich, split into one file per service
- Tailscale for private administration, with a single Playit port forwarded for game servers
- GitHub Actions CI that validates Compose files and rejects unpinned image tags
- Backup and restore docs written for a second-machine restore test

The architecture, sanitized configs, and design notes are in the [homelab repository](https://github.com/SaiAnumula/homelab).

### [Mission Control](https://github.com/SaiAnumula/homelab-mission-control)

A self-hosted monitoring dashboard modeled after btop that puts all of my machines on one page.

- Lightweight Python telemetry agent per host built with the standard library only
- Tracks CPU, GPU, VRAM, memory, disk, temperatures, Docker containers, and systemd services
- Reports SMART drive health when `smartctl` is installed and marks stale readings when a host drops off
- React frontend served by a standalone Python server over LAN or Tailscale

### [Local AI assistant](https://github.com/SaiAnumula/local-ai-assistant)

Benchmarks, architecture notes, and sanitized telemetry from running the Hermes agent with local open-weight models. I retired standalone Ollama in November 2026 and benchmarked Inkling 2 Mini and Ornith 1.5 35B on PolyStrata. The local PolyStrata setup is paused, so daily Hermes runs on hosted inference.

- Re-tuned the stack after a failed RAM stick dropped the desktop from 32 GB to 24 GB by moving the KV cache to `q8_0`, cutting context from 128K to 64K, and testing under production systemd memory limits
- Harness covering prefill speed, decode throughput, long-context recall, tool-call reliability, and calendar JSON output
- Logs RAM, swap, memory pressure, and VRAM on every run and aborts before starving the desktop
- CI runs the test suite against a mock Ollama server alongside `shellcheck`, `ruff`, and a secret scan

### Private projects

A few tools I maintain stay private because they contain personal or account data.

- An automated internship application pipeline that discovers listings, scores them against a resume, drafts responses, and helps fill forms with human review. It has 780+ tests, a SQLite database, and a Tailscale-only web dashboard.
- A fail-closed quota workflow for T3 Code that reads provider usage caches and blocks runs when headroom is low or unknown.

### Raspberry Pi NAS proof of concept

For a class project, I built a working NAS on a Raspberry Pi 5 and recorded a walkthrough covering the problems I ran into and how I fixed them.

[Watch the Raspberry Pi NAS walkthrough](https://youtu.be/0SLmClxMjXE)

## Tools and technologies

### Operating systems & infrastructure

<p>
  <img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black" alt="Linux" />
  <img src="https://img.shields.io/badge/CachyOS-1793D1?style=flat-square&logo=archlinux&logoColor=white" alt="CachyOS (Arch-based)" />
  <img src="https://img.shields.io/badge/Ubuntu-E95420?style=flat-square&logo=ubuntu&logoColor=white" alt="Ubuntu" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/Tailscale-242424?style=flat-square&logo=tailscale&logoColor=white" alt="Tailscale" />
</p>

### Monitoring

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

### Apps, data & tools

<p>
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" alt="React" />
  <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" alt="SQLite" />
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" alt="Git" />
  <img src="https://img.shields.io/badge/Microsoft%20Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white" alt="Microsoft Azure" />
</p>

## Current focus

- Maintaining the internship pipeline and dashboard that my friends and I use
- Evaluating local models on PolyStrata and llama.cpp (Inkling 2 Mini, Ornith 1.5 35B, Qwen) on 24 GB RAM / 16 GB VRAM
- Expanding Prometheus, Grafana, and Loki coverage across my machines ([backup and restore runbook](https://github.com/SaiAnumula/homelab/blob/main/docs/backup-and-restore.md))
- Practicing network segmentation, host firewalls, and secret management outside of classwork

---

<div align="center">

**Seeking networking, infrastructure, and cybersecurity internship opportunities for Summer 2027. [Connect with me on LinkedIn](https://www.linkedin.com/in/saianumula).**

</div>
