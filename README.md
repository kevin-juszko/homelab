# Homelab

Personal homelab documentation - networking, self-hosting, virtulization, python server and database managment with locally hosted AI assistant.

## Hardware

| Device | Specs | Role |
|---|---|---|
| PC1 | i7-12700K, RTX 3080 Ti, 32GB RAM | Windows daily driver / gaming |
| PC2 | i7-9700, RTX 2060, 32GB RAM | Dev machine (Arch Linux) |
| Raspberry Pi 5 | 8GB | Home server |
| Raspberry Pi Zero 2 W | — | Unused |

## What's Running

-**Ubuntu Server VM** Set up with QEMU, Libvirt, virt-manager, dnsmasq. Will contain python database.
- **Ollama + qwen2.5-coder:7b** — local LLM for coding assistance
- **Continue.dev** — VS Code extension connected to local LLM

## In Progress

- Tailscale mesh network (Pi + PC2 + iPhone)
- Navidrome music server on Pi
- Docker + Python dev stack on PC2

## Structure

- `networking/` — Tailscale, Pi network setup
- `dev-environment/` — PC2 Arch Linux dev setup
- `self-hosting/` — Raspberry Pi services
- `progress-log.md` — running log of work completed